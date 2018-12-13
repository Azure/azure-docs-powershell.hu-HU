---
title: Az Azure PowerShell Az telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével Windows, macOS és Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216997"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="268d4-103">Az Azure PowerShell Az modul telepítése</span><span class="sxs-lookup"><span data-stu-id="268d4-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="268d4-104">Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be.</span><span class="sxs-lookup"><span data-stu-id="268d4-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="268d4-105">Az útmutatás Windows, macOS és Linux platformon használható.</span><span class="sxs-lookup"><span data-stu-id="268d4-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="268d4-106">Az Az előzetes kiadásában más telepítési módszerek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="268d4-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="268d4-107">Követelmények</span><span class="sxs-lookup"><span data-stu-id="268d4-107">Requirements</span></span>

<span data-ttu-id="268d4-108">Az Azure PowerShell a Windows alatt a PowerShell 5.x, más platformon a PowerShell 6.x verziójával működik.</span><span class="sxs-lookup"><span data-stu-id="268d4-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="268d4-109">Annak ellenőrzéséhez, hogy a PowerShell melyik verziója fut a számítógépén, futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="268d4-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="268d4-110">Ha elavult verzióval rendelkezik, vagy nincs telepítve a PowerShell, tekintse át [a PowerShell különféle verzióinak telepítését](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6) ismertető témakört.</span><span class="sxs-lookup"><span data-stu-id="268d4-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="268d4-111">A platformokra vonatkozó telepítési információk azon az oldalon keresztül érhetők el.</span><span class="sxs-lookup"><span data-stu-id="268d4-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="268d4-112">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="268d4-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="268d4-113">Az `AzureRM` és az `Az` modul egyszerre is telepítve lehet ugyanazon a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="268d4-113">You can have both the `AzureRM` and `Az` modules installed at the same time.</span></span> <span data-ttu-id="268d4-114">Ha mindkettő telepítve van, __ne engedélyezze az aliasokat__.</span><span class="sxs-lookup"><span data-stu-id="268d4-114">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="268d4-115">Az aliasok engedélyezése ütközéseket okozhat az `AzureRM` parancsmagok és az `Az` aliasok között, ami nem várt működéshez vezethet.</span><span class="sxs-lookup"><span data-stu-id="268d4-115">Enabling aliases will cause conflicts between `AzureRM` cmdlets and `Az` command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="268d4-116">Az `Az` modul telepítése előtt ajánlott eltávolítani az `AzureRM`-et.</span><span class="sxs-lookup"><span data-stu-id="268d4-116">It's recommended that before installing the `Az` module, you uninstall `AzureRM`.</span></span> <span data-ttu-id="268d4-117">Az `AzureRM`-et bármikor eltávolíthatja, illetve bármikor engedélyezheti az aliasokat.</span><span class="sxs-lookup"><span data-stu-id="268d4-117">You can always uninstall `AzureRM` or enable aliases at any time.</span></span> <span data-ttu-id="268d4-118">Az eltávolításra vonatkozó útmutatásért lásd a következő cikket: [Az Azure PowerShell module (AzureRM) eltávolítása](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="268d4-118">For uninstall instructions, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span> 

<span data-ttu-id="268d4-119">A modulok globális hatókörben való telepítéséhez megemelt jogosultsági szint szükséges a PowerShell-galériából való telepítés esetén.</span><span class="sxs-lookup"><span data-stu-id="268d4-119">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="268d4-120">Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben („Futtatás rendszergazdaként” a Windows, vagy felügyelői jogosultságok a macOS vagy a Linux alatt):</span><span class="sxs-lookup"><span data-stu-id="268d4-120">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="268d4-121">Ha nem rendelkezik rendszergazdai jogosultsággal, a `-Scope` argumentum hozzáadásával végezhet telepítést az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="268d4-121">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="268d4-122">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="268d4-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="268d4-123">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="268d4-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="268d4-124">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="268d4-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="268d4-125">Az `Az` modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="268d4-125">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="268d4-126">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="268d4-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="268d4-127">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="268d4-127">Sign in</span></span>

<span data-ttu-id="268d4-128">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="268d4-128">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="268d4-129">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="268d4-129">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="268d4-130">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="268d4-130">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="268d4-131">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="268d4-131">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="268d4-132">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="268d4-132">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="268d4-133">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="268d4-133">Update the Azure PowerShell module</span></span>

<span data-ttu-id="268d4-134">Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával.</span><span class="sxs-lookup"><span data-stu-id="268d4-134">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="268d4-135">Ez a parancs __nem__ távolítja el a korábbi verziókat.</span><span class="sxs-lookup"><span data-stu-id="268d4-135">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="268d4-136">Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="268d4-136">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="268d4-137">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="268d4-137">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="268d4-138">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="268d4-138">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="268d4-139">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="268d4-139">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="268d4-140">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="268d4-140">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="268d4-141">Az `Az` modul adott verziójának betöltéséhez használja a `-RequiredVersion` argumentumot az `Install-Module` vagy az `Import-Module` parancsban:</span><span class="sxs-lookup"><span data-stu-id="268d4-141">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="268d4-142">Ha a modul több verziója is telepítve van, alapértelmezés szerint a legújabb verzió töltődik be.</span><span class="sxs-lookup"><span data-stu-id="268d4-142">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="268d4-143">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="268d4-143">Provide feedback</span></span>

<span data-ttu-id="268d4-144">Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="268d4-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="268d4-145">A parancssorból a [Send-Feedback](/powershell/module/az.profile/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="268d4-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="268d4-146">További lépések</span><span class="sxs-lookup"><span data-stu-id="268d4-146">Next Steps</span></span>

<span data-ttu-id="268d4-147">Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="268d4-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
