---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: e71b4d0d662b29a32610fecb36351532040428e4
ms.sourcegitcommit: a261efc84dedfd829c0613cf62f8fcf3aa62adb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2019
ms.locfileid: "68807443"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="4465c-103">Az Azure PowerShell-modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4465c-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="4465c-104">Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből.</span><span class="sxs-lookup"><span data-stu-id="4465c-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="4465c-105">Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="4465c-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="4465c-106">Ha hibát tapasztal, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues), hogy kijavíthassuk.</span><span class="sxs-lookup"><span data-stu-id="4465c-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="4465c-107">Az Az modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4465c-107">Uninstall the Az module</span></span>

<span data-ttu-id="4465c-108">Az Az modulok eltávolításához használja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4465c-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="4465c-109">Azonban az `Uninstall-Module` csak egy modult távolít el.</span><span class="sxs-lookup"><span data-stu-id="4465c-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="4465c-110">Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat.</span><span class="sxs-lookup"><span data-stu-id="4465c-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="4465c-111">Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.</span><span class="sxs-lookup"><span data-stu-id="4465c-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="4465c-112">Az Azure PowerShell aktuálisan telepített verzióinak megállapításához futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="4465c-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="4465c-113">Az alábbi szkript lekérdezi a PowerShell-galériából a függő almodulok listáját.</span><span class="sxs-lookup"><span data-stu-id="4465c-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="4465c-114">Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját.</span><span class="sxs-lookup"><span data-stu-id="4465c-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="4465c-115">A szkript futtatásához rendszergazdai hozzáféréssel kell rendelkeznie egy olyan hatókörben, amely nem `Process` vagy `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="4465c-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="4465c-116">A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="4465c-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="4465c-117">A következő példa bemutatja, hogyan futtatható a függvény az Azure PowerShell egy régebbi verziójának eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="4465c-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="4465c-118">Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok nevét és verzióját.</span><span class="sxs-lookup"><span data-stu-id="4465c-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="4465c-119">Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor használja a `-WhatIf` kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="4465c-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="4465c-120">Ha ez a szkript nem talál egy pontosan ugyanolyan verziójú függőséget az eltávolításhoz, akkor a függőségnek _egyik_ verzióját sem fogja eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="4465c-120">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="4465c-121">Ennek oka, hogy a célmodulnak más verziói is megtalálhatók lehetnek a rendszeren, amelyek használhatják az adott függőségeket.</span><span class="sxs-lookup"><span data-stu-id="4465c-121">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="4465c-122">Ebben az esetben az adott függőség elérhető verziói lesznek felsorolva.</span><span class="sxs-lookup"><span data-stu-id="4465c-122">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="4465c-123">Ezután manuálisan eltávolíthatja a régi verziókat az `Uninstall-Module` paranccsal.</span><span class="sxs-lookup"><span data-stu-id="4465c-123">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="4465c-124">Futtassa ezt a parancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="4465c-124">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="4465c-125">Az egyszerűség kedvéért az alábbi szkript az Az összes verzióját eltávolítja, __kivéve__ a legfrissebbet.</span><span class="sxs-lookup"><span data-stu-id="4465c-125">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="4465c-126">Az AzureRM modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4465c-126">Uninstall the AzureRM module</span></span>

<span data-ttu-id="4465c-127">Ha a rendszeren telepítve van az Az modul, és el szeretné távolítani az AzureRM-et, két módszert használhat, amelyekhez nem kell futtatnia a fenti `Uninstall-AllModules` szkriptet.</span><span class="sxs-lookup"><span data-stu-id="4465c-127">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="4465c-128">A követendő módszer az AzureRM modul telepítési módjától függ.</span><span class="sxs-lookup"><span data-stu-id="4465c-128">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="4465c-129">Ha nem biztos benne, hogy mi volt az eredeti telepítési módszer, először kövesse az MSI eltávolításának lépéseit.</span><span class="sxs-lookup"><span data-stu-id="4465c-129">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="4465c-130">Az Azure PowerShell MSI eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4465c-130">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="4465c-131">Ha az Azure PowerShell AzureRM modulokat az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.</span><span class="sxs-lookup"><span data-stu-id="4465c-131">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="4465c-132">Platform</span><span class="sxs-lookup"><span data-stu-id="4465c-132">Platform</span></span> | <span data-ttu-id="4465c-133">Utasítások</span><span class="sxs-lookup"><span data-stu-id="4465c-133">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="4465c-134">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4465c-134">Windows 10</span></span> | <span data-ttu-id="4465c-135">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="4465c-135">Start > Settings > Apps</span></span> |
| <span data-ttu-id="4465c-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4465c-136">Windows 7</span></span> </br><span data-ttu-id="4465c-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4465c-137">Windows 8</span></span> | <span data-ttu-id="4465c-138">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4465c-138">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="4465c-139">Itt a programok listájában megjelenik az __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="4465c-139">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="4465c-140">Ezt az alkalmazást távolítsa el.</span><span class="sxs-lookup"><span data-stu-id="4465c-140">This is the app to uninstall.</span></span> <span data-ttu-id="4465c-141">Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.</span><span class="sxs-lookup"><span data-stu-id="4465c-141">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="4465c-142">Eltávolítás PowerShellből</span><span class="sxs-lookup"><span data-stu-id="4465c-142">Uninstall from PowerShell</span></span>

<span data-ttu-id="4465c-143">Ha az AzureRM-et a PowerShellGet segítségével telepítette, akkor az `Az.Accounts` modul részeként elérhető [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) paranccsal távolíthatja el a modulokat.</span><span class="sxs-lookup"><span data-stu-id="4465c-143">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="4465c-144">Ez eltávolítja az _összes_ AzureRM modult a gépéről, de rendszergazdai jogosultság szükséges hozzá.</span><span class="sxs-lookup"><span data-stu-id="4465c-144">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="4465c-145">Ha nem tudja sikeresen futtatni az `Uninstall-AzureRM` parancsot, használja helyette a cikkben szereplő [`Uninstall-AllModules` szkriptet](#uninstall-script) a következő hívással:</span><span class="sxs-lookup"><span data-stu-id="4465c-145">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```