---
title: Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 0d8019a7acaf2ba3baaa0772a76285ec497c991c
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091469"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="a433f-103">Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával</span><span class="sxs-lookup"><span data-stu-id="a433f-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="a433f-104">Ez a cikk az Azure PowerShell-modulok PowerShellGet segítségével való telepítésének lépéseit ismerteti Windows-környezetben.</span><span class="sxs-lookup"><span data-stu-id="a433f-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="a433f-105">A PowerShellGet használata és a modulok kezelése az Azure PowerShell előnyben részesített telepítési módja, de ha mégis inkább a Webplatform-telepítővel vagy az MSI-csomaggal szeretné telepíteni, tekintse meg az [egyéb telepítési módszerekkel kapcsolatos](other-install.md) szakaszt.</span><span class="sxs-lookup"><span data-stu-id="a433f-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="a433f-106">Az Azure PowerShell más platformokon való telepítéséhez tekintse meg [az Azure PowerShell macOS és Linux rendszeren való telepítését és konfigurálását](install-azurermps-maclinux.md) ismertető témakört.</span><span class="sxs-lookup"><span data-stu-id="a433f-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="a433f-107">Az Azure PowerShell ezen verziója nem támogatja a klasszikus Azure üzemi modellt.</span><span class="sxs-lookup"><span data-stu-id="a433f-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="a433f-108">A klasszikus üzemi modell támogatásához kövesse az [Azure PowerShell Service Management moduljának telepítésével](/powershell/azure/servicemanagement/install-azure-ps) kapcsolatos szakaszban található utasításokat.</span><span class="sxs-lookup"><span data-stu-id="a433f-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="a433f-109">Követelmények</span><span class="sxs-lookup"><span data-stu-id="a433f-109">Requirements</span></span>

<span data-ttu-id="a433f-110">A 6.0-s verziótól kezdve az Azure PowerShellhez a PowerShell 5.0-s vagy újabb verziójának kell futnia a Windows rendszeren.</span><span class="sxs-lookup"><span data-stu-id="a433f-110">Starting with version 6.0, Azure PowerShell requires version 5.0 or higher of PowerShell running on Windows.</span></span> <span data-ttu-id="a433f-111">Annak ellenőrzéséhez, hogy a PowerShell melyik verziója fut a számítógépén, futtassa a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="a433f-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell
$PSVersionTable.PSVersion
```

<span data-ttu-id="a433f-112">Ha elavult verzióval rendelkezik, tekintse meg a [meglévő Windows PowerShell frissítését](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) ismertető témakört.</span><span class="sxs-lookup"><span data-stu-id="a433f-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="a433f-113">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="a433f-113">Install the Azure PowerShell module</span></span>

<span data-ttu-id="a433f-114">Megemelt jogosultsági szint szükséges a modulok PowerShell-galériából való telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="a433f-114">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="a433f-115">Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben:</span><span class="sxs-lookup"><span data-stu-id="a433f-115">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="a433f-116">Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.</span><span class="sxs-lookup"><span data-stu-id="a433f-116">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="a433f-117">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="a433f-117">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="a433f-118">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="a433f-118">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="a433f-119">A telepítés folytatásához válassza az `Yes` vagy az `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="a433f-119">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="a433f-120">Az `AzureRM` modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="a433f-120">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a433f-121">A modul telepítése letölti az összes elérhető Azure Resource Manager-modult, és elérhetővé teszi a parancsmagjaikat használatra.</span><span class="sxs-lookup"><span data-stu-id="a433f-121">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="a433f-122">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="a433f-122">Sign in</span></span>

<span data-ttu-id="a433f-123">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="a433f-123">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="a433f-124">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="a433f-124">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a433f-125">Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="a433f-125">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="a433f-126">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="a433f-126">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="a433f-127">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="a433f-127">Update the Azure PowerShell module</span></span>

<span data-ttu-id="a433f-128">Frissítheti az Azure PowerShell-telepítést az [Update-Module](/powershell/module/powershellget/update-module) futtatásával.</span><span class="sxs-lookup"><span data-stu-id="a433f-128">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="a433f-129">Ez a parancs __nem__ távolítja el a korábbi verziókat.</span><span class="sxs-lookup"><span data-stu-id="a433f-129">This command does __not__ uninstall earlier versions.</span></span>

```powershell
Update-Module -Name AzureRM
```

<span data-ttu-id="a433f-130">Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="a433f-130">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="a433f-131">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="a433f-131">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="a433f-132">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="a433f-132">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="a433f-133">Előfordulhat, hogy több verzióra van szüksége, ha helyszíni Azure Stack-erőforrásokat használ, vagy a Windows egy régebbi verzióját használja, amely nem frissíthető a PowerShell 5.0-ra, vagy a klasszikus Azure üzemi modellt használja.</span><span class="sxs-lookup"><span data-stu-id="a433f-133">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="a433f-134">Régebbi verzió telepítéséhez a telepítéskor adja meg a `-RequiredVersion` argumentumot.</span><span class="sxs-lookup"><span data-stu-id="a433f-134">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="a433f-135">Az Azure PowerShell-modul betöltésekor alapértelmezés szerint a legújabb verzió lesz betöltve.</span><span class="sxs-lookup"><span data-stu-id="a433f-135">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="a433f-136">Másik verzió betöltéséhez adja meg a `-RequiredVersion` argumentumot.</span><span class="sxs-lookup"><span data-stu-id="a433f-136">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="a433f-137">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="a433f-137">Provide feedback</span></span>

<span data-ttu-id="a433f-138">Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="a433f-138">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="a433f-139">A parancssorból a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="a433f-139">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a433f-140">További lépések</span><span class="sxs-lookup"><span data-stu-id="a433f-140">Next Steps</span></span>

<span data-ttu-id="a433f-141">Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak szolgáltatásairól.</span><span class="sxs-lookup"><span data-stu-id="a433f-141">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>