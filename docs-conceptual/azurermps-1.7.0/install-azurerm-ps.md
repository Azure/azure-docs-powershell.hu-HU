---
title: Az Azure PowerShell telepítése és konfigurálása | Microsoft Docs
description: Az Azure PowerShell telepítése és konfigurálása az első használathoz.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/17/2017
ms.openlocfilehash: 98c6c7472203e8a0377c04a787d4e54b966a7bb7
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34822006"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="c03c7-103">Az Azure PowerShell telepítése és konfigurálása</span><span class="sxs-lookup"><span data-stu-id="c03c7-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="c03c7-104">Az Azure PowerShell-t a PowerShell-galériából javasolt telepíteni.</span><span class="sxs-lookup"><span data-stu-id="c03c7-104">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="c03c7-105">1. lépés: A PowerShellGet telepítése</span><span class="sxs-lookup"><span data-stu-id="c03c7-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="c03c7-106">Ahhoz, hogy elemeket telepíthessen a PowerShell-galériából, szükség van a PowerShellGet modulra.</span><span class="sxs-lookup"><span data-stu-id="c03c7-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="c03c7-107">Győződjön meg arról, hogy rendelkezik a PowerShellGet megfelelő verziójával, és az egyéb rendszerkövetelmények is teljesülnek.</span><span class="sxs-lookup"><span data-stu-id="c03c7-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="c03c7-108">A következő parancs futtatásával ellenőrizze, hogy telepítve van-e a PowerShellGet a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="c03c7-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="c03c7-109">Az alábbihoz hasonló kimenetnek kell megjelennie:</span><span class="sxs-lookup"><span data-stu-id="c03c7-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="c03c7-110">Ha a PowerShellGet nincs telepítve, akkor tekintse meg a jelen cikk [A PowerShellGet-modul beszerzése](#how-to-get-powershellget) című szakaszát.</span><span class="sxs-lookup"><span data-stu-id="c03c7-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="c03c7-111">A PowerShellGet használatához olyan végrehajtási szabályzatra van szükség, amely lehetővé teszi a szkriptek futtatását.</span><span class="sxs-lookup"><span data-stu-id="c03c7-111">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="c03c7-112">A PowerShell végrehajtási házirendjével kapcsolatos további információk: [A végrehajtási házirendek áttekintése](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="c03c7-112">For more information about PowerShell's Execution Policy, see [About Execution Policies](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="c03c7-113">2. lépés: Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="c03c7-113">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="c03c7-114">Az Azure Powershell PowerShell-galériából történő telepítéséhez emelt szintű jogosultságok szükségesek.</span><span class="sxs-lookup"><span data-stu-id="c03c7-114">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="c03c7-115">Futtassa a következő parancssort egy emelt szintű PowerShell-munkamenetből:</span><span class="sxs-lookup"><span data-stu-id="c03c7-115">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM
```

<span data-ttu-id="c03c7-116">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható tárházaként.</span><span class="sxs-lookup"><span data-stu-id="c03c7-116">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="c03c7-117">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="c03c7-117">The first time you use the PSGallery you see the following prompt:</span></span>

```
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="c03c7-118">A telepítés folytatásához válassza az „Igen” vagy az „Igen, mindet” lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c03c7-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="c03c7-119">Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.</span><span class="sxs-lookup"><span data-stu-id="c03c7-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="c03c7-120">Az AzureRM-modul az Azure Resource Manager-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="c03c7-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="c03c7-121">Az AzureRM modul telepítésekor a rendszer minden korábban nem telepített Azure PowerShell modult letölt a PowerShell-galériából.</span><span class="sxs-lookup"><span data-stu-id="c03c7-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="c03c7-122">Ha az Azure PowerShell korábbi verziójával rendelkezik, hibaüzenetet kaphat.</span><span class="sxs-lookup"><span data-stu-id="c03c7-122">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="c03c7-123">A probléma megoldásához tekintse meg a cikk [Frissítés az Azure PowerShell új verziójára ](#update-azps) című részét.</span><span class="sxs-lookup"><span data-stu-id="c03c7-123">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="c03c7-124">3. lépés: Az AzureRM-modul betöltése</span><span class="sxs-lookup"><span data-stu-id="c03c7-124">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="c03c7-125">A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="c03c7-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="c03c7-126">Ezt a lépést normál (nem emelt szintű) PowerShell-munkamenetben kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="c03c7-126">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="c03c7-127">A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:</span><span class="sxs-lookup"><span data-stu-id="c03c7-127">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="c03c7-128">További lépések</span><span class="sxs-lookup"><span data-stu-id="c03c7-128">Next Steps</span></span>

<span data-ttu-id="c03c7-129">Az Azure PowerShell használatával kapcsolatos további információkat az alábbi cikkekben olvashat:</span><span class="sxs-lookup"><span data-stu-id="c03c7-129">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="c03c7-130">Ismerkedés az Azure PowerShell szolgáltatással</span><span class="sxs-lookup"><span data-stu-id="c03c7-130">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="c03c7-131">Gyakori kérdések</span><span class="sxs-lookup"><span data-stu-id="c03c7-131">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="c03c7-132">A PowerShellGet beszerzése</span><span class="sxs-lookup"><span data-stu-id="c03c7-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="c03c7-133">Operációs rendszer verziója</span><span class="sxs-lookup"><span data-stu-id="c03c7-133">OS Version</span></span>|<span data-ttu-id="c03c7-134">Telepítési utasítások</span><span class="sxs-lookup"><span data-stu-id="c03c7-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="c03c7-135">Windows 10 vagy Windows Server 2016 rendszert használok</span><span class="sxs-lookup"><span data-stu-id="c03c7-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="c03c7-136">Az operációs rendszer részét képező Windows Management Framework (WMF) 5.0 beépített eleme</span><span class="sxs-lookup"><span data-stu-id="c03c7-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="c03c7-137">Frissíteni szeretnék a PowerShell 5-ös verziójára</span><span class="sxs-lookup"><span data-stu-id="c03c7-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="c03c7-138">A WMF legújabb verziójának telepítése</span><span class="sxs-lookup"><span data-stu-id="c03c7-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="c03c7-139">A PowerShell 3-as vagy 4-es verziójával rendelkező Windows-verziót használok</span><span class="sxs-lookup"><span data-stu-id="c03c7-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="c03c7-140">A PackageManagement-modulok beszerzése</span><span class="sxs-lookup"><span data-stu-id="c03c7-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="c03c7-141">Az Azure PowerShell verziószámának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="c03c7-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="c03c7-142">Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott.</span><span class="sxs-lookup"><span data-stu-id="c03c7-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="c03c7-143">Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="c03c7-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="c03c7-144">Klasszikus telepítési módszerek támogatása</span><span class="sxs-lookup"><span data-stu-id="c03c7-144">Support for classic deployment methods</span></span>

<span data-ttu-id="c03c7-145">Ha van olyan üzemelő példánya, amely a klasszikus telepítési modellt használja, akkor az Azure PowerShell Service Management verzióját telepítheti.</span><span class="sxs-lookup"><span data-stu-id="c03c7-145">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="c03c7-146">További információ: [Az Azure PowerShell Service Management moduljának telepítése](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="c03c7-146">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="c03c7-147">Az Azure és AzureRM-modulok ugyanazokat a függőségeket használják.</span><span class="sxs-lookup"><span data-stu-id="c03c7-147">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="c03c7-148">Ha az Azure- és az AzureRM-modult egyaránt használja, minden csomagnak ugyanazt a verzióját kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="c03c7-148">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="c03c7-149">Frissítés az Azure PowerShell új verziójára</span><span class="sxs-lookup"><span data-stu-id="c03c7-149">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="c03c7-150">Ha az Azure PowerShell olyan korábbi verziója van telepítve, amely a Szolgáltatáskezelési modult tartalmazza, akkor a következő hibaüzenetet kaphatja:</span><span class="sxs-lookup"><span data-stu-id="c03c7-150">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="c03c7-151">Ahogy a hibaüzenetben is olvasható, a modul telepítéséhez az -AllowClobber paramétert kell használnia.</span><span class="sxs-lookup"><span data-stu-id="c03c7-151">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="c03c7-152">Használja az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="c03c7-152">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="c03c7-153">További információért tekintse meg az [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) súgótémakört.</span><span class="sxs-lookup"><span data-stu-id="c03c7-153">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="c03c7-154">Modulverziók párhuzamos telepítése</span><span class="sxs-lookup"><span data-stu-id="c03c7-154">Installing module versions side by side</span></span>

<span data-ttu-id="c03c7-155">A PowerShellGet-metódus az egyetlen módszer, amely támogatja több verzió telepítését.</span><span class="sxs-lookup"><span data-stu-id="c03c7-155">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="c03c7-156">Előfordulhat például, hogy rendelkezik az Azure PowerShell előző verziójával írt szkriptekkel, amelyek frissítésére nincs ideje vagy erőforrása.</span><span class="sxs-lookup"><span data-stu-id="c03c7-156">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="c03c7-157">A következő parancsok bemutatják, hogy telepítheti az Azure PowerShell több verzióját:</span><span class="sxs-lookup"><span data-stu-id="c03c7-157">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="c03c7-158">Egy PowerShell-munkamenetbe csak egyetlen modulverzió tölthető be.</span><span class="sxs-lookup"><span data-stu-id="c03c7-158">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="c03c7-159">Meg kell nyitnia egy új PowerShell-ablakot, és az `Import-Module` parancs használatával importálnia kell az AzureRM-parancsmagok egy adott verzióját:</span><span class="sxs-lookup"><span data-stu-id="c03c7-159">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="c03c7-160">A 2.1.0-ás és az 1.2.6-os modulverziók az elsők, amelyeket párhuzamos telepítésre és használatra terveztek.</span><span class="sxs-lookup"><span data-stu-id="c03c7-160">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="c03c7-161">Az Azure PowerShell korábbi verziónak betöltésekor az **AzureRM.Profile**-modul nem kompatibilis verziói töltődnek be.</span><span class="sxs-lookup"><span data-stu-id="c03c7-161">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="c03c7-162">Ezért a parancsmagok minden parancsmag végrehajtásánál bejelentkezést fognak kérni.</span><span class="sxs-lookup"><span data-stu-id="c03c7-162">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="c03c7-163">Egyéb telepítési módszerek</span><span class="sxs-lookup"><span data-stu-id="c03c7-163">Other installation methods</span></span>

<span data-ttu-id="c03c7-164">A Webplatform-telepítő vagy az MSI-csomag használatával történő telepítéssel kapcsolatos további információkért lásd: [Egyéb telepítési módszerek](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="c03c7-164">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
