---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6a34ac1821c3cec359d0d64664d3f1689621b304
ms.sourcegitcommit: e736293cbc7b813b6b133781c88c7978fb22122a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/20/2019
ms.locfileid: "58215270"
---
# <a name="uninstall-the-azure-powershell-module"></a>Az Azure PowerShell-modul eltávolítása

Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből. Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal.
Ha hibát tapasztal, kérjük, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-the-az-module"></a>Az Az modul eltávolítása

Az Az modulok eltávolításához használja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot. Azonban az `Uninstall-Module` csak egy modult távolít el. Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat. Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.

Az Azure PowerShell aktuálisan telepített verzióinak megállapításához futtassa a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

Az alábbi szkript lekérdezi a PowerShell-galériából a függő almodulok listáját. Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját. A szkript futtatásához rendszergazdai hozzáféréssel kell rendelkeznie egy olyan hatókörben, amely nem `Process` vagy `CurrentUser`.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe. A következő példa bemutatja, hogyan futtatható a függvény az Azure PowerShell egy régebbi verziójának eltávolításához.

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok nevét és verzióját. Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor használja a `-WhatIf` kapcsolót.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

Futtassa ezt a parancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani. Az egyszerűség kedvéért az alábbi szkript az Az összes verzióját eltávolítja, __kivéve__ a legfrissebbet.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Az AzureRM modul eltávolítása

Ha a rendszeren telepítve van az Az modul, és el szeretné távolítani az AzureRM-et, két módszert használhat, amelyekhez nem kell futtatnia a fenti `Uninstall-AllModules` szkriptet. A követendő módszer az AzureRM modul telepítési módjától függ.
Ha nem biztos benne, először kövesse az MSI eltávolításának lépéseit.

### <a name="uninstall-azure-powershell-msi"></a>Az Azure PowerShell MSI eltávolítása

Ha az Azure PowerShell AzureRM modulokat az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.

| Platform | Utasítások |
|----------|--------------|
| Windows 10 | Start menü > Gépház > Alkalmazások |
| Windows 7 </br>Windows 8 | Start menü > Vezérlőpult > Programok > Program eltávolítása |

Itt a programok listájában megjelenik az __Azure PowerShell__. Ezt az alkalmazást távolítsa el. Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.

### <a name="uninstall-from-powershell"></a>Eltávolítás PowerShellből

Ha az AzureRM-et a PowerShellGet segítségével telepítette, akkor az `Az.Accounts` modul részeként elérhető [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) paranccsal távolíthatja el a modulokat. Ez eltávolítja az _összes_ AzureRM modult a gépéről, de rendszergazdai jogosultság szükséges hozzá.

```powershell-interactive
Uninstall-AzureRm
```

Ha nem tudja sikeresen futtatni az `Uninstall-AzureRM` parancsot, használja helyette a cikkben szereplő `Uninstall-AllModules` szkriptet.