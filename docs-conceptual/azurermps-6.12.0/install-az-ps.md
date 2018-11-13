---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276040"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="fcc62-103">Az Azure PowerShell telepítése a PowerShellGet segítségével</span><span class="sxs-lookup"><span data-stu-id="fcc62-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="fcc62-104">Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be.</span><span class="sxs-lookup"><span data-stu-id="fcc62-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="fcc62-105">Az Az előzetes kiadásában más telepítési módszerek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="fcc62-105">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="fcc62-106">Követelmények</span><span class="sxs-lookup"><span data-stu-id="fcc62-106">Requirements</span></span>

<span data-ttu-id="fcc62-107">Az Azure PowerShell a Windows alatt a PowerShell 5.x, más platformon a PowerShell 6.x verziójával működik.</span><span class="sxs-lookup"><span data-stu-id="fcc62-107">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="fcc62-108">Annak ellenőrzéséhez, hogy a PowerShell melyik verziója fut a számítógépén, futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="fcc62-108">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="fcc62-109">Ha elavult verzióval rendelkezik, vagy nincs telepítve a PowerShell, tekintse át [a PowerShell különféle verzióinak telepítését](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6) ismertető témakört.</span><span class="sxs-lookup"><span data-stu-id="fcc62-109">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="fcc62-110">A platformokra vonatkozó telepítési információk azon az oldalon keresztül érhetők el.</span><span class="sxs-lookup"><span data-stu-id="fcc62-110">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="fcc62-111">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="fcc62-111">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="fcc62-112">Az `AzureRM` és az `Az` modul nem lehet egyszerre telepítve ugyanazon a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="fcc62-112">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="fcc62-113">Az `Az` modul telepítéséhez az `AzureRM` modult el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="fcc62-113">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="fcc62-114">Az erre vonatkozó utasításokért lásd: [Az Azure PowerShell-modul (AzureRM) eltávolítása](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="fcc62-114">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="fcc62-115">A modulok globális hatókörben való telepítéséhez megemelt jogosultsági szint szükséges a PowerShell-galériából való telepítés esetén.</span><span class="sxs-lookup"><span data-stu-id="fcc62-115">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="fcc62-116">Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben („Futtatás rendszergazdaként” a Windows, vagy felügyelői jogosultságok a macOS vagy a Linux alatt):</span><span class="sxs-lookup"><span data-stu-id="fcc62-116">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="fcc62-117">Ha nem rendelkezik rendszergazdai jogosultsággal, a `-Scope` argumentum hozzáadásával végezhet telepítést az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="fcc62-117">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="fcc62-118">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="fcc62-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="fcc62-119">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="fcc62-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="fcc62-120">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="fcc62-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="fcc62-121">Az `Az` modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="fcc62-121">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="fcc62-122">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="fcc62-122">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="fcc62-123">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="fcc62-123">Sign in</span></span>

<span data-ttu-id="fcc62-124">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `Az` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="fcc62-124">To start working with Azure PowerShell, you need to load `Az` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

<span data-ttu-id="fcc62-125">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="fcc62-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="fcc62-126">Az `Az` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="fcc62-126">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="fcc62-127">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="fcc62-127">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="fcc62-128">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="fcc62-128">Update the Azure PowerShell module</span></span>

<span data-ttu-id="fcc62-129">Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával.</span><span class="sxs-lookup"><span data-stu-id="fcc62-129">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="fcc62-130">Ez a parancs __nem__ távolítja el a korábbi verziókat.</span><span class="sxs-lookup"><span data-stu-id="fcc62-130">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="fcc62-131">Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="fcc62-131">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="fcc62-132">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="fcc62-132">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="fcc62-133">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="fcc62-133">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="fcc62-134">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="fcc62-134">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="fcc62-135">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="fcc62-135">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="fcc62-136">Az `Az` modul adott verziójának betöltéséhez használja a `-RequiredVersion` argumentumot az `Install-Module` vagy az `Import-Module` parancsban:</span><span class="sxs-lookup"><span data-stu-id="fcc62-136">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` or `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="fcc62-137">Ha a modul több verziója is telepítve van, az importáláskor alapértelmezés szerint a legújabb verzió töltődik be.</span><span class="sxs-lookup"><span data-stu-id="fcc62-137">If you have more than one version of the module installed, the latest version is loaded by default when importing.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="fcc62-138">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="fcc62-138">Provide feedback</span></span>

<span data-ttu-id="fcc62-139">Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="fcc62-139">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="fcc62-140">A parancssorból a [Send-Feedback](/powershell/module/az.profile/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="fcc62-140">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fcc62-141">További lépések</span><span class="sxs-lookup"><span data-stu-id="fcc62-141">Next Steps</span></span>

<span data-ttu-id="fcc62-142">Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="fcc62-142">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>