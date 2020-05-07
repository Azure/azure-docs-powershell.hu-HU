---
title: Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 5de386bde1b8be5a4455b85d4f5fcdf38e4fcea2
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "65535021"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="e5d14-103">Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával</span><span class="sxs-lookup"><span data-stu-id="e5d14-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="e5d14-104">Ez a cikk a PowerShell 5.x verziójához készült Azure PowerShell-modulok telepítésének lépéseit ismerteti Windows-környezetben a PowerShellGet használatával.</span><span class="sxs-lookup"><span data-stu-id="e5d14-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="e5d14-105">A PowerShellGet használata és a modulok kezelése az Azure PowerShell előnyben részesített telepítési módja, de ha mégis inkább a Webplatform-telepítővel vagy az MSI-csomaggal szeretné telepíteni, tekintse meg az [egyéb telepítési módszerekkel kapcsolatos](other-install.md) szakaszt.</span><span class="sxs-lookup"><span data-stu-id="e5d14-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="e5d14-106">Az Azure PowerShell e verziója nem támogatja a klasszikus Azure üzemi modellt.</span><span class="sxs-lookup"><span data-stu-id="e5d14-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="e5d14-107">A klasszikus üzemi modell támogatásához kövesse az [Azure PowerShell Service Management moduljának telepítésével](/powershell/azure/servicemanagement/install-azure-ps) kapcsolatos szakaszban található utasításokat.</span><span class="sxs-lookup"><span data-stu-id="e5d14-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5d14-108">Az AzureRM modul a macOS és a Linux esetében nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="e5d14-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="e5d14-109">Az Azure PowerShell-parancsmagok ezeken a platformokon való használatával kapcsolatban lásd: [Az Az modul telepítése](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="e5d14-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d14-110">Követelmények</span><span class="sxs-lookup"><span data-stu-id="e5d14-110">Requirements</span></span>

<span data-ttu-id="e5d14-111">A 6.0-s verziótól kezdve az Azure PowerShellhez a PowerShell 5.0-s vagy újabb verziója szükséges.</span><span class="sxs-lookup"><span data-stu-id="e5d14-111">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="e5d14-112">Annak ellenőrzéséhez, hogy a PowerShell melyik verziója fut a számítógépén, futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="e5d14-112">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="e5d14-113">Ha elavult verzióval rendelkezik, tekintse meg a [meglévő Windows PowerShell frissítését](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) ismertető témakört.</span><span class="sxs-lookup"><span data-stu-id="e5d14-113">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5d14-114">Az ebben a dokumentumban bemutatott AzureRM modul .NET-keretrendszert használ.</span><span class="sxs-lookup"><span data-stu-id="e5d14-114">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="e5d14-115">Ennek következtében nem kompatibilis a PowerShell 6.0-s verziójával, amely a .NET Core-t használja.</span><span class="sxs-lookup"><span data-stu-id="e5d14-115">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="e5d14-116">Ha 6.0-s PowerShell verziót használ, kövesse a [macOS és Linux rendszerekre vonatkozó telepítési utasításokat](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="e5d14-116">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="e5d14-117">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="e5d14-117">Install the Azure PowerShell module</span></span>

<span data-ttu-id="e5d14-118">Megemelt jogosultsági szint szükséges a modulok PowerShell-galériából való telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e5d14-118">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="e5d14-119">Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben:</span><span class="sxs-lookup"><span data-stu-id="e5d14-119">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="e5d14-120">Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.</span><span class="sxs-lookup"><span data-stu-id="e5d14-120">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="e5d14-121">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="e5d14-121">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="e5d14-122">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="e5d14-122">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="e5d14-123">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="e5d14-123">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="e5d14-124">Az `AzureRM` modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="e5d14-124">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e5d14-125">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="e5d14-125">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="e5d14-126">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="e5d14-126">Sign in</span></span>

<span data-ttu-id="e5d14-127">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="e5d14-127">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="e5d14-128">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module AzureRM` segítségével.</span><span class="sxs-lookup"><span data-stu-id="e5d14-128">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="e5d14-129">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="e5d14-129">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="e5d14-130">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="e5d14-130">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="e5d14-131">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="e5d14-131">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="e5d14-132">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="e5d14-132">Update the Azure PowerShell module</span></span>

<span data-ttu-id="e5d14-133">Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával.</span><span class="sxs-lookup"><span data-stu-id="e5d14-133">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="e5d14-134">Ez a parancs __nem__ távolítja el a korábbi verziókat.</span><span class="sxs-lookup"><span data-stu-id="e5d14-134">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="e5d14-135">Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="e5d14-135">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="e5d14-136">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="e5d14-136">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="e5d14-137">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="e5d14-137">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="e5d14-138">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="e5d14-138">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

<span data-ttu-id="e5d14-139">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="e5d14-139">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="e5d14-140">Előfordulhat, hogy több verzióra van szüksége, ha helyszíni Azure Stack-erőforrásokat használ, illetve ha a Windows egy régebbi verzióját vagy a klasszikus Azure üzemi modellt használja.</span><span class="sxs-lookup"><span data-stu-id="e5d14-140">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="e5d14-141">Régebbi verzió telepítéséhez a telepítéskor adja meg a `-RequiredVersion` argumentumot.</span><span class="sxs-lookup"><span data-stu-id="e5d14-141">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="e5d14-142">Az Azure PowerShell-modul betöltésekor alapértelmezés szerint a legújabb verzió lesz betöltve.</span><span class="sxs-lookup"><span data-stu-id="e5d14-142">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="e5d14-143">Másik verzió betöltéséhez adja meg a `-RequiredVersion` argumentumot.</span><span class="sxs-lookup"><span data-stu-id="e5d14-143">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="e5d14-144">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="e5d14-144">Provide feedback</span></span>

<span data-ttu-id="e5d14-145">Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="e5d14-145">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="e5d14-146">A parancssorból a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="e5d14-146">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e5d14-147">További lépések</span><span class="sxs-lookup"><span data-stu-id="e5d14-147">Next Steps</span></span>

<span data-ttu-id="e5d14-148">Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak funkcióiról.</span><span class="sxs-lookup"><span data-stu-id="e5d14-148">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
