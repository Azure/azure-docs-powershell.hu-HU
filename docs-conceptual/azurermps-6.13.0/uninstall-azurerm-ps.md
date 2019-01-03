---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 7456e45fe9a94d3c1e809dfd075a090448001607
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982825"
---
# <a name="uninstall-the-azure-powershell-module"></a>Az Azure PowerShell-modul eltávolítása

Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből. Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal.
Ha hibát tapasztal, kérjük, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues).


## <a name="uninstall-msi"></a>Eltávolítás – MSI

Ha az Azure PowerShellt az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.

| Platform | Utasítások |
|----------|--------------|
| Windows 10 | Start menü > Gépház > Alkalmazások |
| Windows 7 </br>Windows 8 | Start menü > Vezérlőpult > Programok > Program eltávolítása |

Itt a programok listájában megjelenik az Azure PowerShell, és innen eltávolíthatja a programot.

## <a name="uninstall-from-powershell"></a>Eltávolítás PowerShellből

Ha az Azure PowerShellt a PowerShellGet segítségével telepítette, használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot. Azonban az `Uninstall-Module` csak egy modult távolít el. Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat. Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.

Az Azure PowerShell aktuálisan telepített verzióinak megállapításához futtassa a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
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
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok nevét és verzióját. Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor használja a `-WhatIf` kapcsolót.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Futtassa ezt a parancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani. Az egyszerűség kedvéért az alábbi szkript az AzureRM összes verzióját eltávolítja, __kivéve__ a legfrissebbet.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
