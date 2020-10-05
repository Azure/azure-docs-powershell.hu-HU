---
title: Az Azure PowerShell eltávolítása
description: Az Azure PowerShell teljes eltávolítása
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7f831bdf6d6144640e036d72900958847283acf1
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/26/2020
ms.locfileid: "91381496"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="2b191-103">Azure PowerShell-modulok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b191-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="2b191-104">Ez a cikk bemutatja, hogyan távolítható el az Azure PowerShell egy régebbi verziója, illetve hogyan távolítható el az Azure PowerShell teljesen a rendszerből.</span><span class="sxs-lookup"><span data-stu-id="2b191-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="2b191-105">Ha úgy döntött, hogy teljesen eltávolítja az Azure PowerShellt, ossza meg velünk visszajelzését a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="2b191-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="2b191-106">Ha hibát tapasztal, [jelentse be a GitHubon](https://github.com/azure/azure-powershell/issues), hogy kijavíthassuk.</span><span class="sxs-lookup"><span data-stu-id="2b191-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="2b191-107">Az Az modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b191-107">Uninstall the Az module</span></span>

<span data-ttu-id="2b191-108">Ha a rendszeren telepítve van az Az modul, és el szeretné távolítani, két módszert használhat.</span><span class="sxs-lookup"><span data-stu-id="2b191-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="2b191-109">A követendő módszer az Az modul telepítési módjától függ.</span><span class="sxs-lookup"><span data-stu-id="2b191-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="2b191-110">Ha nem biztos benne, hogy mi volt az eredeti telepítési módszer, először kövesse az MSI eltávolítási lépéseit.</span><span class="sxs-lookup"><span data-stu-id="2b191-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="2b191-111">1\. módszer: Az Az PowerShell-modul eltávolítása az MSI használatával</span><span class="sxs-lookup"><span data-stu-id="2b191-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="2b191-112">Ha az Az PowerShell-modult az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.</span><span class="sxs-lookup"><span data-stu-id="2b191-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="2b191-113">Platform</span><span class="sxs-lookup"><span data-stu-id="2b191-113">Platform</span></span>         |                      <span data-ttu-id="2b191-114">Utasítások</span><span class="sxs-lookup"><span data-stu-id="2b191-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="2b191-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2b191-115">Windows 10</span></span>               | <span data-ttu-id="2b191-116">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="2b191-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="2b191-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b191-117">Windows 7</span></span> </br><span data-ttu-id="2b191-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2b191-118">Windows 8</span></span> | <span data-ttu-id="2b191-119">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b191-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2b191-120">Itt a programok listájában megjelenik az **Azure PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="2b191-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="2b191-121">Ezt az alkalmazást távolítsa el.</span><span class="sxs-lookup"><span data-stu-id="2b191-121">This is the app to uninstall.</span></span> <span data-ttu-id="2b191-122">Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.</span><span class="sxs-lookup"><span data-stu-id="2b191-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="2b191-123">2\. lehetőség: Az Az PowerShell-modul eltávolítása a PowerShellGet használatával</span><span class="sxs-lookup"><span data-stu-id="2b191-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="2b191-124">Az Az modulok eltávolításához használhatja az [Uninstall-Module](/powershell/module/powershellget/uninstall-module) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2b191-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="2b191-125">Azonban az `Uninstall-Module` csak egy modult távolít el.</span><span class="sxs-lookup"><span data-stu-id="2b191-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="2b191-126">Az Az PowerShell-modul teljes eltávolításához egyesével kell eltávolítania a modulokat.</span><span class="sxs-lookup"><span data-stu-id="2b191-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="2b191-127">Az eltávolítás bonyolult lehet, ha több Azure PowerShell-verzió is telepítve van.</span><span class="sxs-lookup"><span data-stu-id="2b191-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="2b191-128">Az Az PowerShell-modul telepített verzióinak megállapításához futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="2b191-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="2b191-129">Az alábbi szkript lekérdezi a PowerShell-galériából a függő almodulok listáját.</span><span class="sxs-lookup"><span data-stu-id="2b191-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="2b191-130">Ezután a szkript eltávolítja az egyes almodulok megfelelő verzióját.</span><span class="sxs-lookup"><span data-stu-id="2b191-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="2b191-131">A szkript futtatásához rendszergazdai hozzáféréssel kell rendelkeznie egy olyan hatókörben, amely nem a **Folyamat** vagy az **Aktuális felhasználó**.</span><span class="sxs-lookup"><span data-stu-id="2b191-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

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

<span data-ttu-id="2b191-132">A függvény használatához másolja és illessze be a kódot a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="2b191-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="2b191-133">A következő példa bemutatja, hogyan futtatható a függvény az Az PowerShell-modul és almoduljai régebbi verziójának eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="2b191-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="2b191-134">Miközben a szkript fut, megjeleníti az eltávolítás alatt álló egyes almodulok **nevét**, **verzióját** és **állapotát**.</span><span class="sxs-lookup"><span data-stu-id="2b191-134">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="2b191-135">Ha úgy szeretné futtatni a szkriptet, hogy az eltávolításuk nélkül tekinthesse meg a törlésre kijelölt elemeket, akkor adja meg a `-WhatIf` paramétert.</span><span class="sxs-lookup"><span data-stu-id="2b191-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="2b191-136">Ha ez a szkript nem talál egy pontosan ugyanolyan verziójú függőséget az eltávolításhoz, akkor a függőségnek _egyik_ verzióját sem fogja eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="2b191-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="2b191-137">Ennek oka, hogy a célmodulnak más verziói is megtalálhatók lehetnek a rendszeren, amelyek használhatják az adott függőségeket.</span><span class="sxs-lookup"><span data-stu-id="2b191-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="2b191-138">Futtassa az alábbi példaparancsot az Az PowerShell-modul minden olyan verziója esetében, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="2b191-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="2b191-139">Az egyszerűség kedvéért az alábbi szkript az Az összes verzióját eltávolítja, **kivéve** a legfrissebbet.</span><span class="sxs-lookup"><span data-stu-id="2b191-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="2b191-140">Az AzureRM modul eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b191-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="2b191-141">Ha a rendszeren telepítve van az Az modul, és el szeretné távolítani az AzureRM-et, két módszert használhat.</span><span class="sxs-lookup"><span data-stu-id="2b191-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="2b191-142">A követendő módszer az AzureRM modul telepítési módjától függ.</span><span class="sxs-lookup"><span data-stu-id="2b191-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="2b191-143">Ha nem biztos benne, hogy mi volt az eredeti telepítési módszer, először kövesse az MSI eltávolítási lépéseit.</span><span class="sxs-lookup"><span data-stu-id="2b191-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="2b191-144">1\. módszer: Az AzureRM PowerShell-modul eltávolítása az MSI használatával</span><span class="sxs-lookup"><span data-stu-id="2b191-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="2b191-145">Ha az AzureRM PowerShell-modult az MSI-csomaggal telepítette, akkor a Windows rendszer segítségével kell eltávolítania, nem a PowerShell-lel.</span><span class="sxs-lookup"><span data-stu-id="2b191-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="2b191-146">Platform</span><span class="sxs-lookup"><span data-stu-id="2b191-146">Platform</span></span>         |                      <span data-ttu-id="2b191-147">Utasítások</span><span class="sxs-lookup"><span data-stu-id="2b191-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="2b191-148">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2b191-148">Windows 10</span></span>               | <span data-ttu-id="2b191-149">Start menü > Gépház > Alkalmazások</span><span class="sxs-lookup"><span data-stu-id="2b191-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="2b191-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b191-150">Windows 7</span></span> </br><span data-ttu-id="2b191-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2b191-151">Windows 8</span></span> | <span data-ttu-id="2b191-152">Start menü > Vezérlőpult > Programok > Program eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b191-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2b191-153">Ezen a képernyőn a programok listájában megjelenik az **Azure PowerShell** vagy a **Microsoft Azure PowerShell – év, hónap**.</span><span class="sxs-lookup"><span data-stu-id="2b191-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="2b191-154">Ezt az alkalmazást távolítsa el.</span><span class="sxs-lookup"><span data-stu-id="2b191-154">This is the app to uninstall.</span></span> <span data-ttu-id="2b191-155">Ha nem látja ezt a programot a listában, akkor a telepítést a PowerShellGet segítségével végezte, és a következő utasításokat kell követnie.</span><span class="sxs-lookup"><span data-stu-id="2b191-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="2b191-156">2\. lehetőség: Az AzureRM PowerShell-modul eltávolítása a PowerShellGet használatával</span><span class="sxs-lookup"><span data-stu-id="2b191-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="2b191-157">Ha az AzureRM-et a PowerShellGet segítségével telepítette, akkor az `Az.Accounts` modul részeként elérhető [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) parancsmaggal távolíthatja el a modulokat.</span><span class="sxs-lookup"><span data-stu-id="2b191-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="2b191-158">Az `Az.Accounts` modul használatához telepíteni kell az Az modult.</span><span class="sxs-lookup"><span data-stu-id="2b191-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="2b191-159">Az Az modul az AzureRM mellett való telepítése nem támogatott, azonban az AzureRM azonnal eltávolítható az Az modullal.</span><span class="sxs-lookup"><span data-stu-id="2b191-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="2b191-160">Ha még nincs telepítve az Az modul, az AzureRM modul figyelmeztetését a következő paranccsal lehet megkerülni az Az telepítése során:</span><span class="sxs-lookup"><span data-stu-id="2b191-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="2b191-161">Az Az modul telepítése után az alábbi paranccsal eltávolítható az _összes_ AzureRM-modul a gépéről.</span><span class="sxs-lookup"><span data-stu-id="2b191-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="2b191-162">Ehhez rendszergazdai jogosultságok szükségesek.</span><span class="sxs-lookup"><span data-stu-id="2b191-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
