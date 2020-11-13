---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ff9135839b01ad9a1bf10e5969cd3226fe492145
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410145"
---
# <a name="uninstall-the-azure-powershell-module"></a>Az Azure PowerShell-modul eltávolítása

Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből. Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal. Ha hibát tapasztal, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues), hogy kijavíthassuk.

## <a name="uninstall-the-az-powershell-module-from-msi"></a>Az Az PowerShell-modul eltávolítása az MSI használatával

Ha az Az PowerShell-modult az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.

|         Platform         |                      Utasítások                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start menü > Gépház > Alkalmazások                                |
| Windows 7 </br>Windows 8 | Start menü > Vezérlőpult > Programok > Program eltávolítása |

Itt a programok listájában megjelenik az **Azure PowerShell**. Ezt az alkalmazást távolítsa el. Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a>Az Az PowerShell-modul eltávolítása a PowerShellGet használatával

Az Az modulok eltávolításához használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot. Azonban az `Uninstall-Module` csak egy modult távolít el. Az Az PowerShell-modul teljes eltávolításához egyesével kell eltávolítania a modulokat. Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.

Az Az PowerShell-modul telepített verzióinak megállapításához futtassa a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

Az alábbi szkript lekérdezi a PowerShell-galériából a függő almodulok listáját. Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját. A szkript futtatásához rendszergazdai hozzáféréssel kell rendelkeznie egy olyan hatókörben, amely nem a **Folyamat** vagy az **Aktuális felhasználó**.

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe. A következő példa bemutatja, hogyan futtatható a függvény az Az PowerShell-modul és almoduljai régebbi verziójának eltávolításához.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok **nevét** , **verzióját** és **állapotát**. Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor adja meg a `-WhatIf` paramétert.

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> Ha ez a szkript nem talál egy pontosan ugyanolyan verziójú függőséget az eltávolításhoz, akkor a függőségnek _egyik_ verzióját sem fogja eltávolítani. Ennek oka, hogy a célmodulnak más verziói is megtalálhatók lehetnek a rendszeren, amelyek használhatják az adott függőségeket.

Futtassa az alábbi példaparancsot az Az PowerShell-modul minden olyan verziója esetében, amelyet el szeretne távolítani.
Az egyszerűség kedvéért az alábbi szkript az Az összes verzióját eltávolítja, **kivéve** a legfrissebbet.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>Az AzureRM modul eltávolítása

Ha a rendszeren telepítve van az Az modul, és el szeretné távolítani az AzureRM-et, két módszert használhat. A követendő módszer az AzureRM modul telepítési módjától függ. Ha nem biztos benne, hogy mi volt az eredeti telepítési módszer, először kövesse az MSI eltávolításának lépéseit.

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a>Az AzureRM PowerShell-modul eltávolítása az MSI használatával

Ha az AzureRM PowerShell-modult az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.

|         Platform         |                      Utasítások                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start menü > Gépház > Alkalmazások                                |
| Windows 7 </br>Windows 8 | Start menü > Vezérlőpult > Programok > Program eltávolítása |

Ezen a képernyőn a programok listájában megjelenik az **Azure PowerShell** vagy a **Microsoft Azure PowerShell – év, hónap**. Ezt az alkalmazást távolítsa el. Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a>Az AzureRM PowerShell-modul eltávolítása a PowerShellGet használatával

Ha az AzureRM-et a PowerShellGet segítségével telepítette, akkor az `Az.Accounts` modul részeként elérhető [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) parancsmaggal távolíthatja el a modulokat. Az alábbi példa eltávolítja az _összes_ AzureRM-modult a gépéről. Ehhez rendszergazdai jogosultságok szükségesek.

```powershell-interactive
Uninstall-AzureRm
```
