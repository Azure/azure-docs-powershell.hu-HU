---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365749"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="b0e4c-103">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="b0e4c-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="b0e4c-104">Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="b0e4c-105">Az útmutatás Windows, macOS és Linux platformon használható.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="b0e4c-106">Az Az modulhoz jelenleg nem támogatottak más telepítési módszerek.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e4c-107">Követelmények</span><span class="sxs-lookup"><span data-stu-id="b0e4c-107">Requirements</span></span>

<span data-ttu-id="b0e4c-108">Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell Core 6.x vagy újabb verziójával működik.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="b0e4c-109">Ha nem biztos abban, hogy rendelkezik-e PowerShell-lel, illetve macOS vagy Linux rendszert használ, [telepítse a PowerShell Core legújabb verzióját](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="b0e4c-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="b0e4c-110">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="b0e4c-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="b0e4c-111">Az Azure PowerShell futtatása PowerShell 5.1-ben Windows rendszeren:</span><span class="sxs-lookup"><span data-stu-id="b0e4c-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="b0e4c-112">Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="b0e4c-113">Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="b0e4c-114">Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="b0e4c-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="b0e4c-115">Nincsenek további követelmények az Azure PowerShellhez a PowerShell Core használata esetén.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="b0e4c-116">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="b0e4c-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="b0e4c-117">Az AzureRM és az Az modul egyszerre is telepítve lehet ugyanazon a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="b0e4c-118">Ha mindkettő telepítve van, __ne engedélyezze az aliasokat__.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="b0e4c-119">Az aliasok engedélyezése ütközéseket okozhat az AzureRM parancsmagok és az Az-parancsaliasok között, ami nem várt működéshez vezethet.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="b0e4c-120">Az Az modul telepítése előtt ajánlott eltávolítani az AzureRM-et.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="b0e4c-121">Az AzureRM-et bármikor eltávolíthatja, illetve bármikor engedélyezheti az aliasokat.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="b0e4c-122">Az AzureRM-parancsaliasokról [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="b0e4c-123">Az eltávolításra vonatkozó útmutatásért lásd a következő cikket: [Az AzureRM modul eltávolítása](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="b0e4c-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="b0e4c-124">A modulok globális hatókörben való telepítéséhez megemelt jogosultsági szint szükséges a PowerShell-galériából való telepítés esetén.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="b0e4c-125">Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben („Futtatás rendszergazdaként” a Windows, vagy felügyelői jogosultságok a macOS vagy a Linux alatt):</span><span class="sxs-lookup"><span data-stu-id="b0e4c-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="b0e4c-126">Ha nem rendelkezik rendszergazdai jogosultsággal, a `-Scope` argumentum hozzáadásával végezhet telepítést az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="b0e4c-127">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="b0e4c-128">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="b0e4c-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="b0e4c-129">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="b0e4c-130">Az Az modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b0e4c-131">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="b0e4c-132">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="b0e4c-132">Sign in</span></span>

<span data-ttu-id="b0e4c-133">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="b0e4c-134">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="b0e4c-135">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="b0e4c-136">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="b0e4c-137">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="b0e4c-138">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="b0e4c-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="b0e4c-139">Az Az modul csomagolásának módja miatt az [Update-Module](/powershell/module/powershellget/update-module) parancs nem fogja megfelelően frissíteni a telepítést.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="b0e4c-140">Az Az gyakorlatilag egy metamodul, amely magában foglalja az Azure-szolgáltatásokkal való kommunikációt szolgáló parancsmagokat tartalmazó összes almodult.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="b0e4c-141">Ez azt jelenti, hogy az Azure PowerShell-modul frissítéséhez nem elég __frissíteni__ azt, hanem __újra kell telepítenie__.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="b0e4c-142">Ez ugyanúgy történik, mint a telepítés, de előfordulhat, hogy hozzá kell adnia a `-Force` argumentumot:</span><span class="sxs-lookup"><span data-stu-id="b0e4c-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="b0e4c-143">Bár ez felülírhatja a telepített modulokat, még így is előfordulhat hogy maradnak régebbi verziók a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="b0e4c-144">Az Azure PowerShell régebbi verzióinak eltávolításáról [Az Azure PowerShell-modul eltávolítása](uninstall-az-ps.md) című szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="b0e4c-145">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="b0e4c-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="b0e4c-146">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="b0e4c-147">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="b0e4c-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="b0e4c-148">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="b0e4c-149">Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` argumentumot:</span><span class="sxs-lookup"><span data-stu-id="b0e4c-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="b0e4c-150">Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="b0e4c-151">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="b0e4c-151">Provide feedback</span></span>

<span data-ttu-id="b0e4c-152">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="b0e4c-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="b0e4c-153">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b0e4c-154">További lépések</span><span class="sxs-lookup"><span data-stu-id="b0e4c-154">Next Steps</span></span>

<span data-ttu-id="b0e4c-155">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="b0e4c-156">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
