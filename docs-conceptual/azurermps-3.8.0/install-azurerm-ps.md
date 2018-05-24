---
title: Az Azure PowerShell telepítése és konfigurálása | Microsoft Docs
description: Az Azure PowerShell telepítése és konfigurálása az első használathoz.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: e4f75bf0a42bffdb8e1b7cc1a3b0a19c56de4692
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="2aa5b-103">Az Azure PowerShell telepítése és konfigurálása</span><span class="sxs-lookup"><span data-stu-id="2aa5b-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="2aa5b-104">Az Azure PowerShell-t a PowerShell-galériából javasolt telepíteni.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-104">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="2aa5b-105">1. lépés: A PowerShellGet telepítése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="2aa5b-106">Ahhoz, hogy elemeket telepíthessen a PowerShell-galériából, szükség van a PowerShellGet modulra.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="2aa5b-107">Győződjön meg arról, hogy rendelkezik a PowerShellGet megfelelő verziójával, és az egyéb rendszerkövetelmények is teljesülnek.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="2aa5b-108">A következő parancs futtatásával ellenőrizze, hogy telepítve van-e a PowerShellGet a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="2aa5b-109">Az alábbihoz hasonló kimenetnek kell megjelennie:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-109">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="2aa5b-110">A PowerShellGet 1.1.2.0-s vagy újabb verziója szükséges.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-110">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="2aa5b-111">A PowerShellGet frissítéséhez használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-111">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="2aa5b-112">Ha a PowerShellGet nincs telepítve, akkor tekintse meg a jelen cikk [A PowerShellGet-modul beszerzése](#how-to-get-powershellget) című szakaszát.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-112">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="2aa5b-113">A PowerShellGet használatához olyan végrehajtási szabályzatra van szükség, amely lehetővé teszi a szkriptek futtatását.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-113">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="2aa5b-114">A PowerShell végrehajtási házirendjével kapcsolatos további információk: [A végrehajtási házirendek áttekintése](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="2aa5b-114">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="2aa5b-115">2. lépés: Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-115">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="2aa5b-116">Az Azure Powershell PowerShell-galériából történő telepítéséhez emelt szintű jogosultságok szükségesek.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-116">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="2aa5b-117">Futtassa a következő parancssort egy emelt szintű PowerShell-munkamenetből:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-117">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="2aa5b-118">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható tárházaként.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-118">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="2aa5b-119">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-119">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="2aa5b-120">A telepítés folytatásához válassza az „Igen” vagy az „Igen, mindet” lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-120">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="2aa5b-121">Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-121">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="2aa5b-122">Az AzureRM-modul az Azure Resource Manager-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-122">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="2aa5b-123">Az AzureRM modul telepítésekor a rendszer minden korábban nem telepített Azure PowerShell modult letölt a PowerShell-galériából.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-123">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="2aa5b-124">Ha az Azure PowerShell korábbi verziójával rendelkezik, hibaüzenetet kaphat.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-124">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="2aa5b-125">A probléma megoldásához tekintse meg a cikk [Frissítés az Azure PowerShell új verziójára ](#update-azps) című részét.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-125">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="2aa5b-126">3. lépés: Az AzureRM-modul betöltése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-126">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="2aa5b-127">A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-127">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="2aa5b-128">Ezt a lépést normál (nem emelt szintű) PowerShell-munkamenetben kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-128">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="2aa5b-129">A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-129">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="2aa5b-130">További lépések</span><span class="sxs-lookup"><span data-stu-id="2aa5b-130">Next Steps</span></span>

<span data-ttu-id="2aa5b-131">Az Azure PowerShell használatával kapcsolatos további információkat az alábbi cikkekben olvashat:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-131">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="2aa5b-132">Ismerkedés az Azure PowerShell szolgáltatással</span><span class="sxs-lookup"><span data-stu-id="2aa5b-132">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="2aa5b-133">Gyakori kérdések</span><span class="sxs-lookup"><span data-stu-id="2aa5b-133">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="2aa5b-134">A PowerShellGet beszerzése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-134">How to get PowerShellGet</span></span>

|<span data-ttu-id="2aa5b-135">Operációs rendszer verziója</span><span class="sxs-lookup"><span data-stu-id="2aa5b-135">OS Version</span></span>|<span data-ttu-id="2aa5b-136">Telepítési utasítások</span><span class="sxs-lookup"><span data-stu-id="2aa5b-136">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="2aa5b-137">Windows 10 vagy Windows Server 2016 rendszert használok</span><span class="sxs-lookup"><span data-stu-id="2aa5b-137">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="2aa5b-138">Az operációs rendszer részét képező Windows Management Framework (WMF) 5.0 beépített eleme</span><span class="sxs-lookup"><span data-stu-id="2aa5b-138">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="2aa5b-139">Frissíteni szeretnék a PowerShell 5-ös verziójára</span><span class="sxs-lookup"><span data-stu-id="2aa5b-139">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="2aa5b-140">A WMF legújabb verziójának telepítése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-140">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="2aa5b-141">A PowerShell 3-as vagy 4-es verziójával rendelkező Windows-verziót használok</span><span class="sxs-lookup"><span data-stu-id="2aa5b-141">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="2aa5b-142">A PackageManagement-modulok beszerzése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-142">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="2aa5b-143">Az Azure PowerShell verziószámának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-143">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="2aa5b-144">Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-144">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="2aa5b-145">Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-145">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="2aa5b-146">Klasszikus telepítési módszerek támogatása</span><span class="sxs-lookup"><span data-stu-id="2aa5b-146">Support for classic deployment methods</span></span>

<span data-ttu-id="2aa5b-147">Ha van olyan üzemelő példánya, amely a klasszikus telepítési modellt használja, akkor az Azure PowerShell Service Management verzióját telepítheti.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-147">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="2aa5b-148">További információ: [Az Azure PowerShell Service Management moduljának telepítése](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="2aa5b-148">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="2aa5b-149">Az Azure és AzureRM-modulok ugyanazokat a függőségeket használják.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-149">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="2aa5b-150">Ha az Azure- és az AzureRM-modult egyaránt használja, minden csomagnak ugyanazt a verzióját kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-150">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="2aa5b-151">Frissítés az Azure PowerShell új verziójára</span><span class="sxs-lookup"><span data-stu-id="2aa5b-151">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="2aa5b-152">Ha az Azure PowerShell olyan korábbi verziója van telepítve, amely a Szolgáltatáskezelési modult tartalmazza, akkor a következő hibaüzenetet kaphatja:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-152">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="2aa5b-153">Ahogy a hibaüzenetben is olvasható, a modul telepítéséhez az -AllowClobber paramétert kell használnia.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-153">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="2aa5b-154">Használja az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-154">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="2aa5b-155">További információért tekintse meg az [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) súgótémakört.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-155">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="2aa5b-156">Modulverziók párhuzamos telepítése</span><span class="sxs-lookup"><span data-stu-id="2aa5b-156">Installing module versions side by side</span></span>

<span data-ttu-id="2aa5b-157">A PowerShellGet-metódus az egyetlen módszer, amely támogatja több verzió telepítését.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-157">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="2aa5b-158">Előfordulhat például, hogy rendelkezik az Azure PowerShell előző verziójával írt szkriptekkel, amelyek frissítésére nincs ideje vagy erőforrása.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-158">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="2aa5b-159">A következő parancsok bemutatják, hogy telepítheti az Azure PowerShell több verzióját:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-159">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="2aa5b-160">Egy PowerShell-munkamenetbe csak egyetlen modulverzió tölthető be.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-160">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="2aa5b-161">Meg kell nyitnia egy új PowerShell-ablakot, és az `Import-Module` parancs használatával importálnia kell az AzureRM-parancsmagok egy adott verzióját:</span><span class="sxs-lookup"><span data-stu-id="2aa5b-161">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="2aa5b-162">A 2.1.0-ás és az 1.2.6-os modulverziók az elsők, amelyeket párhuzamos telepítésre és használatra terveztek.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-162">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="2aa5b-163">Az Azure PowerShell korábbi verziónak betöltésekor az **AzureRM.Profile**-modul nem kompatibilis verziói töltődnek be.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-163">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="2aa5b-164">Ezért a parancsmagok minden parancsmag végrehajtásánál bejelentkezést fognak kérni.</span><span class="sxs-lookup"><span data-stu-id="2aa5b-164">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="2aa5b-165">Egyéb telepítési módszerek</span><span class="sxs-lookup"><span data-stu-id="2aa5b-165">Other installation methods</span></span>

<span data-ttu-id="2aa5b-166">A Webplatform-telepítő vagy az MSI-csomag használatával történő telepítéssel kapcsolatos további információkért lásd: [Egyéb telepítési módszerek](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="2aa5b-166">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
