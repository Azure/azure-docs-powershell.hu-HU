---
title: Az Azure PowerShell telepítése és konfigurálása | Microsoft Docs
description: Az Azure PowerShell telepítése és konfigurálása az első használathoz.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 5092440515f8c8fae8baefa6e3c5c856e48bb62c
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575008"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="1ba83-103">Az Azure PowerShell telepítése és konfigurálása</span><span class="sxs-lookup"><span data-stu-id="1ba83-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="1ba83-104">Ez a cikk az Azure PowerShell-modulok Windows-környezetben való telepítésének lépéseit ismerteti.</span><span class="sxs-lookup"><span data-stu-id="1ba83-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="1ba83-105">Ha a macOS vagy Linux rendszeren szeretné használni az Azure PowerShellt, tekintse meg a következő cikket: [Az Azure PowerShell telepítése és konfigurálása macOS és Linux rendszeren](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="1ba83-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="1ba83-106">Az Azure PowerShell-t a PowerShell-galériából javasolt telepíteni.</span><span class="sxs-lookup"><span data-stu-id="1ba83-106">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="1ba83-107">1. lépés: A PowerShellGet telepítése</span><span class="sxs-lookup"><span data-stu-id="1ba83-107">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="1ba83-108">Ahhoz, hogy elemeket telepíthessen a PowerShell-galériából, szükség van a PowerShellGet modulra.</span><span class="sxs-lookup"><span data-stu-id="1ba83-108">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="1ba83-109">Győződjön meg arról, hogy rendelkezik a PowerShellGet megfelelő verziójával, és az egyéb rendszerkövetelmények is teljesülnek.</span><span class="sxs-lookup"><span data-stu-id="1ba83-109">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="1ba83-110">A következő parancs futtatásával ellenőrizze, hogy telepítve van-e a PowerShellGet a rendszerben.</span><span class="sxs-lookup"><span data-stu-id="1ba83-110">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="1ba83-111">Az alábbihoz hasonló kimenetnek kell megjelennie:</span><span class="sxs-lookup"><span data-stu-id="1ba83-111">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="1ba83-112">A PowerShellGet 1.1.2.0-s vagy újabb verziója szükséges.</span><span class="sxs-lookup"><span data-stu-id="1ba83-112">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="1ba83-113">A PowerShellGet frissítéséhez használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="1ba83-113">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="1ba83-114">Ha a PowerShellGet nincs telepítve, akkor tekintse meg a jelen cikk [A PowerShellGet-modul beszerzése](#how-to-get-powershellget) című szakaszát.</span><span class="sxs-lookup"><span data-stu-id="1ba83-114">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="1ba83-115">A PowerShellGet használatához olyan végrehajtási szabályzatra van szükség, amely lehetővé teszi a szkriptek futtatását.</span><span class="sxs-lookup"><span data-stu-id="1ba83-115">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="1ba83-116">A PowerShell végrehajtási házirendjével kapcsolatos további információk: [A végrehajtási házirendek áttekintése](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="1ba83-116">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="1ba83-117">Az ebben a dokumentumban bemutatott AzureRM modul .NET-keretrendszert használ.</span><span class="sxs-lookup"><span data-stu-id="1ba83-117">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="1ba83-118">Ennek következtében nem kompatibilis a PowerShell 6.0-s verziójával, amely a .NET Core-t használja.</span><span class="sxs-lookup"><span data-stu-id="1ba83-118">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="1ba83-119">Ha 6.0-s PowerShell verziót használ, kövesse a [macOS és Linux rendszerekre vonatkozó telepítési utasításokat](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="1ba83-119">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="1ba83-120">2. lépés: Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="1ba83-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="1ba83-121">Az Azure Powershell PowerShell-galériából történő telepítéséhez emelt szintű jogosultságok szükségesek.</span><span class="sxs-lookup"><span data-stu-id="1ba83-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="1ba83-122">Futtassa a következő parancssort egy emelt szintű PowerShell-munkamenetből:</span><span class="sxs-lookup"><span data-stu-id="1ba83-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="1ba83-123">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható tárházaként.</span><span class="sxs-lookup"><span data-stu-id="1ba83-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1ba83-124">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="1ba83-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="1ba83-125">A telepítés folytatásához válassza az „Igen” vagy az „Igen, mindet” lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1ba83-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="1ba83-126">Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.</span><span class="sxs-lookup"><span data-stu-id="1ba83-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="1ba83-127">Az AzureRM-modul az Azure Resource Manager-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="1ba83-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="1ba83-128">Az AzureRM modul telepítésekor a rendszer minden korábban nem telepített Azure PowerShell modult letölt a PowerShell-galériából.</span><span class="sxs-lookup"><span data-stu-id="1ba83-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="1ba83-129">Ha az Azure PowerShell korábbi verziójával rendelkezik, hibaüzenetet kaphat.</span><span class="sxs-lookup"><span data-stu-id="1ba83-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="1ba83-130">A probléma megoldásához tekintse meg a cikk [Frissítés az Azure PowerShell új verziójára ](#update-azps) című részét.</span><span class="sxs-lookup"><span data-stu-id="1ba83-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="1ba83-131">3. lépés: Az AzureRM-modul betöltése</span><span class="sxs-lookup"><span data-stu-id="1ba83-131">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="1ba83-132">A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="1ba83-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="1ba83-133">Ezt a lépést normál (nem emelt szintű) PowerShell-munkamenetben kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="1ba83-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="1ba83-134">A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:</span><span class="sxs-lookup"><span data-stu-id="1ba83-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="1ba83-135">További lépések</span><span class="sxs-lookup"><span data-stu-id="1ba83-135">Next Steps</span></span>

<span data-ttu-id="1ba83-136">Az Azure PowerShell használatával kapcsolatos további információkat az alábbi cikkekben olvashat:</span><span class="sxs-lookup"><span data-stu-id="1ba83-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="1ba83-137">Ismerkedés az Azure PowerShell szolgáltatással</span><span class="sxs-lookup"><span data-stu-id="1ba83-137">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="1ba83-138">Hibák jelentése és visszajelzés</span><span class="sxs-lookup"><span data-stu-id="1ba83-138">Reporting issues and feedback</span></span>

<span data-ttu-id="1ba83-139">Ha az eszköz használata során bármilyen hibát tapasztal, jelentse be a problémát a GitHub-adattár [Hibák](https://github.com/Azure/azure-powershell/issues) szakaszában.</span><span class="sxs-lookup"><span data-stu-id="1ba83-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="1ba83-140">A parancssorból a `Send-Feedback` parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="1ba83-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1ba83-141">Gyakori kérdések</span><span class="sxs-lookup"><span data-stu-id="1ba83-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="1ba83-142">A PowerShellGet beszerzése</span><span class="sxs-lookup"><span data-stu-id="1ba83-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="1ba83-143">Operációs rendszer verziója</span><span class="sxs-lookup"><span data-stu-id="1ba83-143">OS Version</span></span>|<span data-ttu-id="1ba83-144">Telepítési utasítások</span><span class="sxs-lookup"><span data-stu-id="1ba83-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="1ba83-145">Windows 10 vagy Windows Server 2016 rendszert használok</span><span class="sxs-lookup"><span data-stu-id="1ba83-145">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="1ba83-146">Az operációs rendszer részét képező Windows Management Framework (WMF) 5.0 beépített eleme</span><span class="sxs-lookup"><span data-stu-id="1ba83-146">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="1ba83-147">Frissíteni szeretnék a PowerShell 5-ös verziójára</span><span class="sxs-lookup"><span data-stu-id="1ba83-147">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="1ba83-148">A WMF legújabb verziójának telepítése</span><span class="sxs-lookup"><span data-stu-id="1ba83-148">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="1ba83-149">A PowerShell 3-as vagy 4-es verziójával rendelkező Windows-verziót használok</span><span class="sxs-lookup"><span data-stu-id="1ba83-149">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="1ba83-150">A PackageManagement-modulok beszerzése</span><span class="sxs-lookup"><span data-stu-id="1ba83-150">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="1ba83-151">Az Azure PowerShell verziószámának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="1ba83-151">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="1ba83-152">Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott.</span><span class="sxs-lookup"><span data-stu-id="1ba83-152">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="1ba83-153">Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="1ba83-153">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell-interactive
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="1ba83-154">Klasszikus telepítési módszerek támogatása</span><span class="sxs-lookup"><span data-stu-id="1ba83-154">Support for classic deployment methods</span></span>

<span data-ttu-id="1ba83-155">Ha van olyan üzemelő példánya, amely a klasszikus telepítési modellt használja, akkor az Azure PowerShell Service Management verzióját telepítheti.</span><span class="sxs-lookup"><span data-stu-id="1ba83-155">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="1ba83-156">További információ: [Az Azure PowerShell Service Management modul áttekintése](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="1ba83-156">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="1ba83-157">Az Azure és AzureRM-modulok ugyanazokat a függőségeket használják.</span><span class="sxs-lookup"><span data-stu-id="1ba83-157">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="1ba83-158">Ha az Azure- és az AzureRM-modult egyaránt használja, minden csomagnak ugyanazt a verzióját kell telepítenie.</span><span class="sxs-lookup"><span data-stu-id="1ba83-158">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="1ba83-159">Frissítés az Azure PowerShell egy új verziójára</span><span class="sxs-lookup"><span data-stu-id="1ba83-159">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="1ba83-160">Ha az Azure PowerShell olyan korábbi verziója van telepítve, amely a Szolgáltatáskezelési modult tartalmazza, akkor a következő hibaüzenetet kaphatja:</span><span class="sxs-lookup"><span data-stu-id="1ba83-160">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="1ba83-161">Ahogy a hibaüzenetben is olvasható, a modul telepítéséhez az -AllowClobber paramétert kell használnia.</span><span class="sxs-lookup"><span data-stu-id="1ba83-161">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="1ba83-162">Használja az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="1ba83-162">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="1ba83-163">További információért tekintse meg az [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) súgótémakört.</span><span class="sxs-lookup"><span data-stu-id="1ba83-163">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="1ba83-164">Modulverziók párhuzamos telepítése</span><span class="sxs-lookup"><span data-stu-id="1ba83-164">Installing module versions side by side</span></span>

<span data-ttu-id="1ba83-165">A PowerShellGet-metódus az egyetlen módszer, amely támogatja több verzió telepítését.</span><span class="sxs-lookup"><span data-stu-id="1ba83-165">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="1ba83-166">Előfordulhat például, hogy rendelkezik az Azure PowerShell előző verziójával írt szkriptekkel, amelyek frissítésére nincs ideje vagy erőforrása.</span><span class="sxs-lookup"><span data-stu-id="1ba83-166">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="1ba83-167">A következő parancsok bemutatják, hogy telepítheti az Azure PowerShell több verzióját:</span><span class="sxs-lookup"><span data-stu-id="1ba83-167">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="1ba83-168">Egy PowerShell-munkamenetbe csak egyetlen modulverzió tölthető be.</span><span class="sxs-lookup"><span data-stu-id="1ba83-168">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="1ba83-169">Meg kell nyitnia egy új PowerShell-ablakot, és az `Import-Module` parancs használatával importálnia kell az AzureRM-parancsmagok egy adott verzióját:</span><span class="sxs-lookup"><span data-stu-id="1ba83-169">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="1ba83-170">A 2.1.0-ás és az 1.2.6-os modulverziók az elsők, amelyeket párhuzamos telepítésre és használatra terveztek.</span><span class="sxs-lookup"><span data-stu-id="1ba83-170">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="1ba83-171">Az Azure PowerShell korábbi verziónak betöltésekor az **AzureRM.Profile**-modul nem kompatibilis verziói töltődnek be.</span><span class="sxs-lookup"><span data-stu-id="1ba83-171">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="1ba83-172">Ezért a parancsmagok minden parancsmag végrehajtásánál bejelentkezést fognak kérni.</span><span class="sxs-lookup"><span data-stu-id="1ba83-172">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="1ba83-173">Egyéb telepítési módszerek</span><span class="sxs-lookup"><span data-stu-id="1ba83-173">Other installation methods</span></span>

<span data-ttu-id="1ba83-174">A Webplatform-telepítő vagy az MSI-csomag használatával történő telepítéssel kapcsolatos további információkért lásd: [Egyéb telepítési módszerek](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="1ba83-174">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
