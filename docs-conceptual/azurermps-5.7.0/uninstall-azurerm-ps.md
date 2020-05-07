---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cc0b6a4369116e92b8200ffbc0838d6ee2991263
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037692"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="0ac7c-103">Az Azure PowerShell-modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0ac7c-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="0ac7c-104">Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="0ac7c-105">Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="0ac7c-106">Ha hibát tapasztal, kérjük, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="0ac7c-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="0ac7c-107">Eltávolítás – MSI vagy Webplatform-telepítő</span><span class="sxs-lookup"><span data-stu-id="0ac7c-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="0ac7c-108">Ha az Azure PowerShellt az MSI-csomaggal vagy a Webplatform-telepítővel telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShellel.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="0ac7c-109">Platform</span><span class="sxs-lookup"><span data-stu-id="0ac7c-109">Platform</span></span> | <span data-ttu-id="0ac7c-110">Utasítások</span><span class="sxs-lookup"><span data-stu-id="0ac7c-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="0ac7c-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="0ac7c-111">Windows 10</span></span> | <span data-ttu-id="0ac7c-112">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="0ac7c-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="0ac7c-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0ac7c-113">Windows 7</span></span> </br><span data-ttu-id="0ac7c-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0ac7c-114">Windows 8</span></span> | <span data-ttu-id="0ac7c-115">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0ac7c-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="0ac7c-116">Itt a programok listájában megjelenik az Azure PowerShell, és innen eltávolíthatja a programot.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="0ac7c-117">Eltávolítás PowerShellből</span><span class="sxs-lookup"><span data-stu-id="0ac7c-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="0ac7c-118">Ha az Azure PowerShellt a PowerShellGet segítségével telepítette, használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="0ac7c-119">Azonban az `Uninstall-Module` csak egy modult távolít el.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="0ac7c-120">Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="0ac7c-121">Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="0ac7c-122">Az alábbi szkripttel az Azure PowerShell egyetlen verziója távolítható el teljesen.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="0ac7c-123">A szkript lekérdezi a PowerShell-galériából a függő almodulok listáját.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="0ac7c-124">Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

<span data-ttu-id="0ac7c-125">A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="0ac7c-126">A következő példa bemutatja, hogyan futtatható a függvény az Azure PowerShell egy régebbi verziójának eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="0ac7c-127">Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok nevét és verzióját.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="0ac7c-128">Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor használja a `-WhatIf` kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="0ac7c-129">Ha ez a szkript nem talál egy pontosan ugyanolyan verziójú függőséget az eltávolításhoz, akkor a függőségnek _egyik_ verzióját sem fogja eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="0ac7c-130">Ennek oka, hogy a célmodulnak más verziói is megtalálhatók lehetnek a rendszeren, amelyek használhatják az adott függőségeket.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="0ac7c-131">Ebben az esetben az adott függőség elérhető verziói lesznek felsorolva.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="0ac7c-132">Ezután manuálisan eltávolíthatja a régi verziókat az `Uninstall-Module` paranccsal.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="0ac7c-133">Futtassa ezt a parancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="0ac7c-134">Az egyszerűség kedvéért az alábbi szkript az AzureRM összes verzióját eltávolítja, __kivéve__ a legfrissebbet.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
