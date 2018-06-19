---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323101"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="3c51d-103">Az Azure PowerShell telepítése a PowerShellGet segítségével</span><span class="sxs-lookup"><span data-stu-id="3c51d-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="3c51d-104">Ez a cikk az Azure PowerShell-modulok PowerShellGet segítségével való telepítésének lépéseit ismerteti Windows-környezetben.</span><span class="sxs-lookup"><span data-stu-id="3c51d-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="3c51d-105">Ez az Azure PowerShell előnyben részesített telepítési módja, de ha mégis inkább a Webplatform-telepítővel vagy az MSI-csomaggal szeretné telepíteni, tekintse meg az [egyéb telepítési módszerekkel kapcsolatos](other-install.md) szakaszt.</span><span class="sxs-lookup"><span data-stu-id="3c51d-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="3c51d-106">Ha a macOS vagy Linux rendszeren szeretné használni az Azure PowerShellt, tekintse meg a következő cikket: [Az Azure PowerShell telepítése és konfigurálása macOS és Linux rendszeren](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="3c51d-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="3c51d-107">Rendszerkövetelmények</span><span class="sxs-lookup"><span data-stu-id="3c51d-107">System requirements</span></span>

<span data-ttu-id="3c51d-108">Az Azure PowerShell 6.1.0-s verziójához szükség van a PowerShell 5.0-s (vagy újabb) verziójára.</span><span class="sxs-lookup"><span data-stu-id="3c51d-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="3c51d-109">A PowerShell 5.0-s verziójára történő frissítéssel kapcsolatos információkért lásd a [meglévő Windows PowerShell frissítésével](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) kapcsolatos szakaszt.</span><span class="sxs-lookup"><span data-stu-id="3c51d-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="3c51d-110">A PowerShellGet automatikusan települ a PowerShell 5.0 részeként.</span><span class="sxs-lookup"><span data-stu-id="3c51d-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="3c51d-111">Az Azure PowerShell-modul telepítése vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="3c51d-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="3c51d-112">Az Azure Powershell PowerShell-galériából történő telepítéséhez emelt szintű jogosultságok szükségesek.</span><span class="sxs-lookup"><span data-stu-id="3c51d-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="3c51d-113">Futtassa a következő parancssort egy emelt szintű PowerShell-munkamenetből:</span><span class="sxs-lookup"><span data-stu-id="3c51d-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="3c51d-114">Ez a parancs frissíti a meglévő Azure PowerShell-telepítéseket.</span><span class="sxs-lookup"><span data-stu-id="3c51d-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="3c51d-115">Ha több verziót kell telepítenie, tekintse meg a gyakori kérdések között a [Telepíthetek több Azure PowerShell-verziót?](#multiple-versions) kérdésre adott választ.</span><span class="sxs-lookup"><span data-stu-id="3c51d-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="3c51d-116">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="3c51d-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="3c51d-117">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="3c51d-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="3c51d-118">A telepítés folytatásához válassza az „Igen” vagy az „Igen, mindet” lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3c51d-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="3c51d-119">Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.</span><span class="sxs-lookup"><span data-stu-id="3c51d-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="3c51d-120">Az AzureRM-modul az Azure Resource Manager-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="3c51d-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="3c51d-121">Az AzureRM-modul telepítésekor a rendszer minden korábban nem telepített Azure PowerShell-modult letölt a PowerShell-galériából.</span><span class="sxs-lookup"><span data-stu-id="3c51d-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="3c51d-122">Az Azure PowerShell-modul betöltése</span><span class="sxs-lookup"><span data-stu-id="3c51d-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="3c51d-123">A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="3c51d-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="3c51d-124">Ezt a lépést normál (nem emelt szintű) PowerShell-munkamenetben kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="3c51d-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="3c51d-125">A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:</span><span class="sxs-lookup"><span data-stu-id="3c51d-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="3c51d-126">Hibák jelentése és visszajelzés</span><span class="sxs-lookup"><span data-stu-id="3c51d-126">Reporting issues and feedback</span></span>

<span data-ttu-id="3c51d-127">Ha az eszköz használata során bármilyen hibát tapasztal, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="3c51d-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="3c51d-128">A parancssorból a `Send-Feedback` parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="3c51d-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3c51d-129">További lépések</span><span class="sxs-lookup"><span data-stu-id="3c51d-129">Next Steps</span></span>

<span data-ttu-id="3c51d-130">Az Azure PowerShell használatával kapcsolatos további információkat az alábbi cikkekben olvashat:</span><span class="sxs-lookup"><span data-stu-id="3c51d-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="3c51d-131">Ismerkedés az Azure PowerShell szolgáltatással</span><span class="sxs-lookup"><span data-stu-id="3c51d-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="3c51d-132">Gyakori kérdések</span><span class="sxs-lookup"><span data-stu-id="3c51d-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="3c51d-133">Hogyan ellenőrizhetem az Azure PowerShell verziószámát?</span><span class="sxs-lookup"><span data-stu-id="3c51d-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="3c51d-134">Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott.</span><span class="sxs-lookup"><span data-stu-id="3c51d-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="3c51d-135">Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="3c51d-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="3c51d-136">Használhatom az Azure PowerShellt klasszikus Azure üzemi modell esetében?</span><span class="sxs-lookup"><span data-stu-id="3c51d-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="3c51d-137">Ha van olyan üzemelő példánya, amely a klasszikus telepítési modellt használja, akkor az Azure PowerShell Service Management verzióját telepítheti.</span><span class="sxs-lookup"><span data-stu-id="3c51d-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="3c51d-138">További információ: [Az Azure PowerShell Service Management moduljának telepítése](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="3c51d-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="3c51d-139">Az Azure és AzureRM-modulok ugyanazokat a függőségeket használják.</span><span class="sxs-lookup"><span data-stu-id="3c51d-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="3c51d-140">Ha az Azure- és az AzureRM-modult egyaránt használja, minden csomagnak ugyanazt a verzióját kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="3c51d-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="3c51d-141"><a name="multiple-versions"/>Telepíthetek több Azure PowerShell-verziót?</span><span class="sxs-lookup"><span data-stu-id="3c51d-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="3c51d-142">A PowerShellGet az egyetlen telepítési módszer, amely támogatja több verzió telepítését.</span><span class="sxs-lookup"><span data-stu-id="3c51d-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="3c51d-143">Több verzió telepítéséhez hozzáadhatja a `-RequiredVersion` paramétert az `Install-Module` parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="3c51d-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="3c51d-144">Például a 6.1.0-s és az 1.2.9-es verzió telepítése:</span><span class="sxs-lookup"><span data-stu-id="3c51d-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="3c51d-145">Egy PowerShell-munkamenetbe csak egyetlen modulverzió tölthető be.</span><span class="sxs-lookup"><span data-stu-id="3c51d-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="3c51d-146">Nyisson meg egy új PowerShell-ablakot, és az `Import-Module` paranccsal importálja az Azure PowerShell-modul egy adott verzióját.</span><span class="sxs-lookup"><span data-stu-id="3c51d-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="3c51d-147">A 2.1.0-ás és az 1.2.6-os modulverziók az elsők, amelyeket párhuzamos telepítésre és használatra terveztek.</span><span class="sxs-lookup"><span data-stu-id="3c51d-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="3c51d-148">Az Azure PowerShell korábbi verziónak betöltésekor az **AzureRM.Profile**-modul nem kompatibilis verziói töltődnek be.</span><span class="sxs-lookup"><span data-stu-id="3c51d-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="3c51d-149">Ezért a parancsmagok minden parancsmag végrehajtásánál bejelentkezést fognak kérni.</span><span class="sxs-lookup"><span data-stu-id="3c51d-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
