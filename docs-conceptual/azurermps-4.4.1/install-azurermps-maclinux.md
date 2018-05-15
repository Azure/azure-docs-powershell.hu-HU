---
title: Az Azure PowerShell telepítése és konfigurálása macOS és Linux rendszeren | Microsoft Docs
description: Az Azure PowerShell telepítése és konfigurálása az első használathoz macOS és Linux rendszeren.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="fdb47-103">Az Azure PowerShell telepítése és konfigurálása macOS és Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="fdb47-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="fdb47-104">A PowerShell Core 6-os verziója és az Azure PowerShell most már nem Windows rendszerű platformokra is telepíthető.</span><span class="sxs-lookup"><span data-stu-id="fdb47-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="fdb47-105">Az Azure PowerShell macOS és Linux rendszeren való telepítése nem sokban tér el a Windows rendszeren való telepítéstől, először azonban telepítenie kell a PowerShell Core 6-os verzióját is.</span><span class="sxs-lookup"><span data-stu-id="fdb47-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="fdb47-106">Jelenleg a PowerShell Core 6-os verziója és a .NET Core-hoz készült Azure PowerShell csak bétaverzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="fdb47-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="fdb47-107">A termékek korlátozott támogatással rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="fdb47-107">Support for these products is limited.</span></span> <span data-ttu-id="fdb47-108">Ha problémákba ütközik vagy hibákat észlel, kérjük, a GitHubon keresztül jelentse.</span><span class="sxs-lookup"><span data-stu-id="fdb47-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="fdb47-109">A PowerShell Core 6-os verziójának problémái</span><span class="sxs-lookup"><span data-stu-id="fdb47-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="fdb47-110">Az Azure PowerShell problémái</span><span class="sxs-lookup"><span data-stu-id="fdb47-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="fdb47-111">1. lépés: A PowerShell Core 6-os verziójának telepítése</span><span class="sxs-lookup"><span data-stu-id="fdb47-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="fdb47-112">A PowerShell Core 6-os verziójának telepítési folyamata attól függően változik, hogy milyen operációs rendszerre telepíti.</span><span class="sxs-lookup"><span data-stu-id="fdb47-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="fdb47-113">Bár a PowerShell Core 6-os verziója a Windows rendszeren is telepíthető, ez a cikk a macOS és a Linux rendszerre összpontosít.</span><span class="sxs-lookup"><span data-stu-id="fdb47-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="fdb47-114">Ha Windows rendszeren szeretné használni az Azure PowerShellt, tekintse meg a Windowsra vonatkozó [telepítési](./install-azurerm-ps.md) cikket.</span><span class="sxs-lookup"><span data-stu-id="fdb47-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="fdb47-115">A **PowerShell Core 6-os verziójának** telepítése Linux vagy macOS rendszeren a Linux-disztribúciótól és az operációs rendszer verziójától függően változik.</span><span class="sxs-lookup"><span data-stu-id="fdb47-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="fdb47-116">Részletes útmutatásokat a következő cikkben talál:</span><span class="sxs-lookup"><span data-stu-id="fdb47-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="fdb47-117">A PowerShell Core telepítése macOS és Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="fdb47-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="fdb47-118">2. lépés: A .NET Core-hoz készült Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="fdb47-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="fdb47-119">A PowerShell Core 6-os verziója tartalmazza az előre telepített PowerShellGet modult.</span><span class="sxs-lookup"><span data-stu-id="fdb47-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="fdb47-120">Ez megkönnyíti a PowerShell-galériában közzétett modulok telepítését.</span><span class="sxs-lookup"><span data-stu-id="fdb47-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="fdb47-121">Az Azure PowerShell telepítéséhez nyisson meg egy új PowerShell-munkamenetet, majd futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="fdb47-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="fdb47-122">3. lépés: Az AzureRM.Netcore modul betöltése</span><span class="sxs-lookup"><span data-stu-id="fdb47-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="fdb47-123">A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="fdb47-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="fdb47-124">A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:</span><span class="sxs-lookup"><span data-stu-id="fdb47-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="fdb47-125">Amikor az importálás befejeződött, tesztelheti az újonnan telepített modult. Ehhez próbáljon meg bejelentkezni az Azure-ba az alábbi paranccsal:</span><span class="sxs-lookup"><span data-stu-id="fdb47-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="fdb47-126">A fenti parancsnak fel kell kérnie, hogy lépjen a `https://aka.ms/devicelogin` oldalra, és adja meg a megadott kódot.</span><span class="sxs-lookup"><span data-stu-id="fdb47-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="fdb47-127">Elérhető parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fdb47-127">Available cmdlets</span></span>

<span data-ttu-id="fdb47-128">A .NET Standardhoz elérhető Azure PowerShell-modulok még fejlesztés alatt állnak.</span><span class="sxs-lookup"><span data-stu-id="fdb47-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="fdb47-129">Ezek a modulok nem tartalmazzák a modulok Windows verziójához elérhető teljes parancsmagkészletét.</span><span class="sxs-lookup"><span data-stu-id="fdb47-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="fdb47-130">Az AzureRM.Netcore-modulokban az alábbi funkciók érhetők el:</span><span class="sxs-lookup"><span data-stu-id="fdb47-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="fdb47-131">Fiókkezelés</span><span class="sxs-lookup"><span data-stu-id="fdb47-131">Account management</span></span>
  - <span data-ttu-id="fdb47-132">Bejelentkezés Microsoft-fiókkal, szervezeti fiókkal vagy egyszerű szolgáltatásnévvel a Microsoft Azure Active Directoryn keresztül</span><span class="sxs-lookup"><span data-stu-id="fdb47-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="fdb47-133">Hitelesítő adatokat mentése lemezre a Save-AzureRmContext parancsmaggal és a mentett hitelesítő adatok betöltése az Import-AzureRmContext parancsmaggal</span><span class="sxs-lookup"><span data-stu-id="fdb47-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="fdb47-134">Környezet</span><span class="sxs-lookup"><span data-stu-id="fdb47-134">Environment</span></span>
  - <span data-ttu-id="fdb47-135">Különböző nem beépített Microsoft Azure-környezetek beszerzése</span><span class="sxs-lookup"><span data-stu-id="fdb47-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="fdb47-136">Testre szabott környezetek (például az Azure Stack- vagy a Windows Azure Pack-környezetek) hozzáadása/beállítása/eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fdb47-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="fdb47-137">Felügyeletisík-parancsmagok az Azure-szolgáltatásokhoz a Resource Manager és a Service Manager felületeinek használatával.</span><span class="sxs-lookup"><span data-stu-id="fdb47-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="fdb47-138">Virtuális gép</span><span class="sxs-lookup"><span data-stu-id="fdb47-138">Virtual Machine</span></span>
  - <span data-ttu-id="fdb47-139">App Service (webhelyek)</span><span class="sxs-lookup"><span data-stu-id="fdb47-139">App Service (Websites)</span></span>
  - <span data-ttu-id="fdb47-140">SQL Database</span><span class="sxs-lookup"><span data-stu-id="fdb47-140">SQL Database</span></span>
  - <span data-ttu-id="fdb47-141">Storage</span><span class="sxs-lookup"><span data-stu-id="fdb47-141">Storage</span></span>
  - <span data-ttu-id="fdb47-142">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="fdb47-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="fdb47-143">További lépések</span><span class="sxs-lookup"><span data-stu-id="fdb47-143">Next Steps</span></span>

<span data-ttu-id="fdb47-144">Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="fdb47-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
