---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 4b40a3aebab84176a48bcdb0ef818cfa05dea269
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/25/2020
ms.locfileid: "85363366"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="51eff-103">Az Azure PowerShell-modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51eff-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="51eff-104">Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből.</span><span class="sxs-lookup"><span data-stu-id="51eff-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="51eff-105">Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="51eff-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="51eff-106">Ha hibát tapasztal, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues), hogy kijavíthassuk.</span><span class="sxs-lookup"><span data-stu-id="51eff-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="51eff-107">Az Azure PowerShell eltávolítása az MSI-ből</span><span class="sxs-lookup"><span data-stu-id="51eff-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="51eff-108">Ha az Azure PowerShellt az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.</span><span class="sxs-lookup"><span data-stu-id="51eff-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="51eff-109">Platform</span><span class="sxs-lookup"><span data-stu-id="51eff-109">Platform</span></span>         |                      <span data-ttu-id="51eff-110">Utasítások</span><span class="sxs-lookup"><span data-stu-id="51eff-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="51eff-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="51eff-111">Windows 10</span></span>               | <span data-ttu-id="51eff-112">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="51eff-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="51eff-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51eff-113">Windows 7</span></span> </br><span data-ttu-id="51eff-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="51eff-114">Windows 8</span></span> | <span data-ttu-id="51eff-115">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51eff-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="51eff-116">Itt a programok listájában megjelenik az **Azure PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="51eff-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="51eff-117">Ezt az alkalmazást távolítsa el.</span><span class="sxs-lookup"><span data-stu-id="51eff-117">This is the app to uninstall.</span></span> <span data-ttu-id="51eff-118">Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.</span><span class="sxs-lookup"><span data-stu-id="51eff-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershellget"></a><span data-ttu-id="51eff-119">Az Azure PowerShell eltávolítása a PowerShellGet használatával</span><span class="sxs-lookup"><span data-stu-id="51eff-119">Uninstall Azure PowerShell from PowerShellGet</span></span>

<span data-ttu-id="51eff-120">Az Az modulok eltávolításához használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="51eff-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="51eff-121">Azonban az `Uninstall-Module` csak egy modult távolít el.</span><span class="sxs-lookup"><span data-stu-id="51eff-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="51eff-122">Az Azure PowerShell teljes eltávolításához egyesével kell eltávolítania a modulokat.</span><span class="sxs-lookup"><span data-stu-id="51eff-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="51eff-123">Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.</span><span class="sxs-lookup"><span data-stu-id="51eff-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="51eff-124">Az Azure PowerShell telepített verzióinak megállapításához futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="51eff-124">To check which versions of Azure PowerShell you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<a name="uninstall-script"/>

<span data-ttu-id="51eff-125">Az alábbi szkript lekérdezi a PowerShell-galériából a függő almodulok listáját.</span><span class="sxs-lookup"><span data-stu-id="51eff-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="51eff-126">Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját.</span><span class="sxs-lookup"><span data-stu-id="51eff-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="51eff-127">A szkript futtatásához rendszergazdai hozzáféréssel kell rendelkeznie egy olyan hatókörben, amely nem a **Folyamat** vagy az **AktuálisFelhasználó**.</span><span class="sxs-lookup"><span data-stu-id="51eff-127">You need to have administrator access to run this script in a scope other than **Process** or **CurrentUser**.</span></span>

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

<span data-ttu-id="51eff-128">A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="51eff-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="51eff-129">A következő példa bemutatja, hogyan futtatható a függvény az Azure PowerShell egy régebbi verziójának eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="51eff-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="51eff-130">Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok **nevét**, **verzióját** és **állapotát**.</span><span class="sxs-lookup"><span data-stu-id="51eff-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="51eff-131">Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor adja meg a `-WhatIf` paramétert.</span><span class="sxs-lookup"><span data-stu-id="51eff-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="51eff-132">Ha ez a szkript nem talál egy pontosan ugyanolyan verziójú függőséget az eltávolításhoz, akkor a függőségnek _egyik_ verzióját sem fogja eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="51eff-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="51eff-133">Ennek oka, hogy a célmodulnak más verziói is megtalálhatók lehetnek a rendszeren, amelyek használhatják az adott függőségeket.</span><span class="sxs-lookup"><span data-stu-id="51eff-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="51eff-134">Futtassa az alábbi példaparancsot minden olyan Azure PowerShell-verzió esetében, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="51eff-134">Run the following example for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="51eff-135">Az egyszerűség kedvéért az alábbi szkript az Az összes verzióját eltávolítja, **kivéve** a legfrissebbet.</span><span class="sxs-lookup"><span data-stu-id="51eff-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions | 
    Sort-Object -Property Version -Descending | 
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="51eff-136">Az AzureRM modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51eff-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="51eff-137">Ha a rendszeren telepítve van az Az modul, és el szeretné távolítani az AzureRM-et, két módszert használhat, amelyekhez nem kell futtatnia a fenti `Uninstall-AzModule` szkriptet.</span><span class="sxs-lookup"><span data-stu-id="51eff-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AzModule` script above.</span></span> <span data-ttu-id="51eff-138">A követendő módszer az AzureRM modul telepítési módjától függ.</span><span class="sxs-lookup"><span data-stu-id="51eff-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="51eff-139">Ha nem biztos benne, hogy mi volt az eredeti telepítési módszer, először kövesse az MSI eltávolításának lépéseit.</span><span class="sxs-lookup"><span data-stu-id="51eff-139">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="51eff-140">Az Azure PowerShell MSI eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51eff-140">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="51eff-141">Ha az Azure PowerShell AzureRM modulokat az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.</span><span class="sxs-lookup"><span data-stu-id="51eff-141">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="51eff-142">Platform</span><span class="sxs-lookup"><span data-stu-id="51eff-142">Platform</span></span>         |                      <span data-ttu-id="51eff-143">Utasítások</span><span class="sxs-lookup"><span data-stu-id="51eff-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="51eff-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="51eff-144">Windows 10</span></span>               | <span data-ttu-id="51eff-145">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="51eff-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="51eff-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51eff-146">Windows 7</span></span> </br><span data-ttu-id="51eff-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="51eff-147">Windows 8</span></span> | <span data-ttu-id="51eff-148">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="51eff-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="51eff-149">Ezen a képernyőn a programok listájában megjelenik az **Azure PowerShell** vagy a **Microsoft Azure PowerShell – év, hónap**.</span><span class="sxs-lookup"><span data-stu-id="51eff-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="51eff-150">Ezt az alkalmazást távolítsa el.</span><span class="sxs-lookup"><span data-stu-id="51eff-150">This is the app to uninstall.</span></span> <span data-ttu-id="51eff-151">Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.</span><span class="sxs-lookup"><span data-stu-id="51eff-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="51eff-152">Eltávolítás PowerShellből</span><span class="sxs-lookup"><span data-stu-id="51eff-152">Uninstall from PowerShell</span></span>

<span data-ttu-id="51eff-153">Ha az AzureRM-et a PowerShellGet segítségével telepítette, akkor az `Az.Accounts` modul részeként elérhető [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) parancsmaggal távolíthatja el a modulokat.</span><span class="sxs-lookup"><span data-stu-id="51eff-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="51eff-154">Az alábbi példa eltávolítja az _összes_ AzureRM modult a gépéről, de rendszergazdai jogosultság szükséges hozzá.</span><span class="sxs-lookup"><span data-stu-id="51eff-154">The following example removes _all_ AzureRM modules from your machine but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="51eff-155">Ha nem tudja sikeresen futtatni az `Uninstall-AzureRM` parancsot, használja helyette a cikkben szereplő [`Uninstall-AzModule` szkriptet](#uninstall-script) a következő hívással:</span><span class="sxs-lookup"><span data-stu-id="51eff-155">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AzModule` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name AzureRM -AllVersions
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```
