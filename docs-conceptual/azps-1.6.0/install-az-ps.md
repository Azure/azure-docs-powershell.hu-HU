---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475529"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="01fe9-103">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="01fe9-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="01fe9-104">Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be.</span><span class="sxs-lookup"><span data-stu-id="01fe9-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="01fe9-105">Az útmutatás Windows, macOS és Linux platformon használható.</span><span class="sxs-lookup"><span data-stu-id="01fe9-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="01fe9-106">Az Az modulhoz jelenleg nem támogatottak más telepítési módszerek.</span><span class="sxs-lookup"><span data-stu-id="01fe9-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fe9-107">Követelmények</span><span class="sxs-lookup"><span data-stu-id="01fe9-107">Requirements</span></span>

<span data-ttu-id="01fe9-108">Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell 6-os verziójával működik.</span><span class="sxs-lookup"><span data-stu-id="01fe9-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell 6 on any platform.</span></span>
<span data-ttu-id="01fe9-109">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="01fe9-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="01fe9-110">Ha elavult verzióval rendelkezik, vagy nincs telepítve a PowerShell, tekintse át [a PowerShell különféle verzióinak telepítését](/powershell/scripting/setup/installing-powershell) ismertető témakört.</span><span class="sxs-lookup"><span data-stu-id="01fe9-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="01fe9-111">A platformokra vonatkozó telepítési információk azon az oldalon keresztül érhetők el.</span><span class="sxs-lookup"><span data-stu-id="01fe9-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="01fe9-112">Ha Windows rendszeren futtatja a PowerShell 5-ös verzióját, akkor a .NET-keretrendszer 4.7.2-es verziójának is telepítve kell lennie.</span><span class="sxs-lookup"><span data-stu-id="01fe9-112">If you are using PowerShell 5 on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="01fe9-113">A .NET-keretrendszer új verziójának frissítésével vagy telepítésével kapcsolatos utasításokat a [.NET-keretrendszer telepítési útmutatójában](/dotnet/framework/install) találja.</span><span class="sxs-lookup"><span data-stu-id="01fe9-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="01fe9-114">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="01fe9-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="01fe9-115">Az AzureRM és az Az modul egyszerre is telepítve lehet ugyanazon a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="01fe9-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="01fe9-116">Ha mindkettő telepítve van, __ne engedélyezze az aliasokat__.</span><span class="sxs-lookup"><span data-stu-id="01fe9-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="01fe9-117">Az aliasok engedélyezése ütközéseket okozhat az AzureRM parancsmagok és az Az-parancsaliasok között, ami nem várt működéshez vezethet.</span><span class="sxs-lookup"><span data-stu-id="01fe9-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="01fe9-118">Az Az modul telepítése előtt ajánlott eltávolítani az AzureRM-et.</span><span class="sxs-lookup"><span data-stu-id="01fe9-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="01fe9-119">Az AzureRM-et bármikor eltávolíthatja, illetve bármikor engedélyezheti az aliasokat.</span><span class="sxs-lookup"><span data-stu-id="01fe9-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="01fe9-120">Az AzureRM-parancsaliasokról [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="01fe9-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="01fe9-121">Az eltávolításra vonatkozó útmutatásért lásd a következő cikket: [Az AzureRM modul eltávolítása](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="01fe9-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="01fe9-122">A modulok globális hatókörben való telepítéséhez megemelt jogosultsági szint szükséges a PowerShell-galériából való telepítés esetén.</span><span class="sxs-lookup"><span data-stu-id="01fe9-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="01fe9-123">Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben („Futtatás rendszergazdaként” a Windows, vagy felügyelői jogosultságok a macOS vagy a Linux alatt):</span><span class="sxs-lookup"><span data-stu-id="01fe9-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="01fe9-124">Ha nem rendelkezik rendszergazdai jogosultsággal, a `-Scope` argumentum hozzáadásával végezhet telepítést az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="01fe9-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="01fe9-125">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="01fe9-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="01fe9-126">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="01fe9-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="01fe9-127">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="01fe9-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="01fe9-128">Az Az modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="01fe9-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="01fe9-129">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="01fe9-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="01fe9-130">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="01fe9-130">Sign in</span></span>

<span data-ttu-id="01fe9-131">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="01fe9-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="01fe9-132">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="01fe9-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="01fe9-133">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="01fe9-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="01fe9-134">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="01fe9-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="01fe9-135">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="01fe9-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="01fe9-136">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="01fe9-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="01fe9-137">Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával.</span><span class="sxs-lookup"><span data-stu-id="01fe9-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="01fe9-138">Ez a parancs __nem__ távolítja el a régebbi verziókat.</span><span class="sxs-lookup"><span data-stu-id="01fe9-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="01fe9-139">Az Azure PowerShell régebbi verzióinak eltávolításáról [Az Azure PowerShell-modul eltávolítása](uninstall-az-ps.md) című szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="01fe9-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="01fe9-140">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="01fe9-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="01fe9-141">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="01fe9-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="01fe9-142">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="01fe9-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="01fe9-143">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="01fe9-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="01fe9-144">Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` argumentumot:</span><span class="sxs-lookup"><span data-stu-id="01fe9-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="01fe9-145">Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.</span><span class="sxs-lookup"><span data-stu-id="01fe9-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="01fe9-146">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="01fe9-146">Provide feedback</span></span>

<span data-ttu-id="01fe9-147">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="01fe9-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="01fe9-148">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="01fe9-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="01fe9-149">További lépések</span><span class="sxs-lookup"><span data-stu-id="01fe9-149">Next Steps</span></span>

<span data-ttu-id="01fe9-150">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="01fe9-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="01fe9-151">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="01fe9-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
