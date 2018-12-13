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
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217235"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="c2e9c-103">Az Azure PowerShell-modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c2e9c-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="c2e9c-104">Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="c2e9c-105">Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="c2e9c-106">Ha hibát tapasztal, kérjük, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="c2e9c-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="c2e9c-107">Eltávolítás – MSI vagy Webplatform-telepítő</span><span class="sxs-lookup"><span data-stu-id="c2e9c-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="c2e9c-108">Ha az Azure PowerShellt az MSI-csomaggal vagy a Webplatform-telepítővel telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShellel.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="c2e9c-109">Platform</span><span class="sxs-lookup"><span data-stu-id="c2e9c-109">Platform</span></span> | <span data-ttu-id="c2e9c-110">Utasítások</span><span class="sxs-lookup"><span data-stu-id="c2e9c-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="c2e9c-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c2e9c-111">Windows 10</span></span> | <span data-ttu-id="c2e9c-112">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="c2e9c-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="c2e9c-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2e9c-113">Windows 7</span></span> </br><span data-ttu-id="c2e9c-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c2e9c-114">Windows 8</span></span> | <span data-ttu-id="c2e9c-115">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c2e9c-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="c2e9c-116">Itt a programok listájában megjelenik az Azure PowerShell, és innen eltávolíthatja a programot.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="c2e9c-117">Eltávolítás PowerShellből</span><span class="sxs-lookup"><span data-stu-id="c2e9c-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="c2e9c-118">Ha az Azure PowerShellt a PowerShellGet segítségével telepítette, használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="c2e9c-119">Azonban az `Uninstall-Module` csak egy modult távolít el.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="c2e9c-120">Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="c2e9c-121">Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="c2e9c-122">Az alábbi szkripttel az Azure PowerShell egyetlen verziója távolítható el teljesen.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="c2e9c-123">A szkript lekérdezi a PowerShell-galériából a függő almodulok listáját.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="c2e9c-124">Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="c2e9c-125">A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="c2e9c-126">A következő példa bemutatja, hogyan futtatható a függvény az Azure PowerShell egy régebbi verziójának eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="c2e9c-127">Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok nevét és verzióját.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="c2e9c-128">Futtassa ezt a parancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="c2e9c-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>