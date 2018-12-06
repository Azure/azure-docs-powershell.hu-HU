---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 3828a6f9d60a68c2837cc201a50d8707324f4f0a
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828569"
---
# <a name="uninstall-the-azure-powershell-module"></a>Az Azure PowerShell-modul eltávolítása

Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből. Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal.
Ha hibát tapasztal, kérjük, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-msi-or-web-platform-installer"></a>Eltávolítás – MSI vagy Webplatform-telepítő

Ha az Azure PowerShellt az MSI-csomaggal vagy a Webplatform-telepítővel telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShellel.

| Platform | Utasítások |
|----------|--------------|
| Windows 10 | Start menü > Gépház > Alkalmazások |
| Windows 7 </br>Windows 8 | Start menü > Vezérlőpult > Programok > Program eltávolítása |

Itt a programok listájában megjelenik az Azure PowerShell, és innen eltávolíthatja a programot.

## <a name="uninstall-from-powershell"></a>Eltávolítás PowerShellből

Ha az Azure PowerShellt a PowerShellGet segítségével telepítette, használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot. Azonban az `Uninstall-Module` csak egy modult távolít el. Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat. Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.

Az alábbi szkripttel az Azure PowerShell egyetlen verziója távolítható el teljesen. A szkript lekérdezi a PowerShell-galériából a függő almodulok listáját. Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
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

Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok nevét és verzióját.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Futtassa ezt a parancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani.