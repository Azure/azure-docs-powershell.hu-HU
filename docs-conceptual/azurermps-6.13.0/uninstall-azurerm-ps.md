---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: a0afae1ba51fdb34425c91049e08d7388f434d7d
ms.sourcegitcommit: 0b5b0434fba7a752b0199256e04fa34f06aaf33a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/21/2019
ms.locfileid: "56464978"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="d9d67-103">Az Azure PowerShell-modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d9d67-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="d9d67-104">Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből.</span><span class="sxs-lookup"><span data-stu-id="d9d67-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="d9d67-105">Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="d9d67-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="d9d67-106">Ha hibát tapasztal, kérjük, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="d9d67-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="d9d67-107">Az Azure PowerShell MSI eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d9d67-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="d9d67-108">Ha az Azure PowerShellt az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.</span><span class="sxs-lookup"><span data-stu-id="d9d67-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="d9d67-109">Platform</span><span class="sxs-lookup"><span data-stu-id="d9d67-109">Platform</span></span> | <span data-ttu-id="d9d67-110">Utasítások</span><span class="sxs-lookup"><span data-stu-id="d9d67-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="d9d67-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d9d67-111">Windows 10</span></span> | <span data-ttu-id="d9d67-112">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="d9d67-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="d9d67-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9d67-113">Windows 7</span></span> </br><span data-ttu-id="d9d67-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d9d67-114">Windows 8</span></span> | <span data-ttu-id="d9d67-115">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d9d67-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d9d67-116">Itt a programok listájában megjelenik az __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="d9d67-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="d9d67-117">Ezt az alkalmazást távolítsa el.</span><span class="sxs-lookup"><span data-stu-id="d9d67-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="d9d67-118">Eltávolítás PowerShellből</span><span class="sxs-lookup"><span data-stu-id="d9d67-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="d9d67-119">Ha az Azure PowerShellt a PowerShellGet segítségével telepítette, használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d9d67-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="d9d67-120">Azonban az `Uninstall-Module` csak egy modult távolít el.</span><span class="sxs-lookup"><span data-stu-id="d9d67-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="d9d67-121">Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat.</span><span class="sxs-lookup"><span data-stu-id="d9d67-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="d9d67-122">Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.</span><span class="sxs-lookup"><span data-stu-id="d9d67-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="d9d67-123">Az Azure PowerShell aktuálisan telepített verzióinak megállapításához futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="d9d67-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="d9d67-124">Az alábbi szkript lekérdezi a PowerShell-galériából a függő almodulok listáját.</span><span class="sxs-lookup"><span data-stu-id="d9d67-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="d9d67-125">Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját.</span><span class="sxs-lookup"><span data-stu-id="d9d67-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="d9d67-126">A szkript futtatásához rendszergazdai hozzáféréssel kell rendelkeznie egy olyan hatókörben, amely nem `Process` vagy `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="d9d67-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="d9d67-127">A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="d9d67-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="d9d67-128">A következő példa bemutatja, hogyan futtatható a függvény az Azure PowerShell egy régebbi verziójának eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="d9d67-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="d9d67-129">Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok nevét és verzióját.</span><span class="sxs-lookup"><span data-stu-id="d9d67-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="d9d67-130">Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor használja a `-WhatIf` kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="d9d67-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="d9d67-131">Futtassa ezt a parancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="d9d67-131">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="d9d67-132">Az egyszerűség kedvéért az alábbi szkript az AzureRM összes verzióját eltávolítja, __kivéve__ a legfrissebbet.</span><span class="sxs-lookup"><span data-stu-id="d9d67-132">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
