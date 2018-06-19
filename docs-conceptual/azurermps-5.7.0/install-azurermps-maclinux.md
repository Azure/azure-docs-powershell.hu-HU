---
title: Az Azure PowerShell telepítése macOS vagy Linux rendszeren
description: Az Azure PowerShell telepítése macOS vagy Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323254"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="a9d62-103">Az Azure PowerShell telepítése macOS vagy Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="a9d62-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="a9d62-104">Nem Windows rendszerű platformokon az Azure PowerShell futtatható a PowerShell Core 6-os verzióján.</span><span class="sxs-lookup"><span data-stu-id="a9d62-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="a9d62-105">A Windowshoz készült .NET-keretrendszerre épülő standard Azure PowerShelltől eltérően ez a termék a .NET Core-ra épül, és bármely, a .Net Core futtatókörnyezetet támogató platformon futtatható.</span><span class="sxs-lookup"><span data-stu-id="a9d62-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="a9d62-106">Jelenleg a PowerShell Core 6-os verziója és a .NET Core-hoz készült Azure PowerShell csak bétaverzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="a9d62-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="a9d62-107">A termékek korlátozott támogatással rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="a9d62-107">Support for these products is limited.</span></span> <span data-ttu-id="a9d62-108">Ha problémákba ütközik vagy hibát észlel, jelentse be a problémát a GitHubon.</span><span class="sxs-lookup"><span data-stu-id="a9d62-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="a9d62-109">A PowerShell Core 6-os verziójának problémái</span><span class="sxs-lookup"><span data-stu-id="a9d62-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="a9d62-110">Az Azure PowerShell problémái</span><span class="sxs-lookup"><span data-stu-id="a9d62-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="a9d62-111">A PowerShell Core 6-os verziójának telepítése</span><span class="sxs-lookup"><span data-stu-id="a9d62-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="a9d62-112">A PowerShell Core 6-os verziójának telepítése Linux vagy macOS rendszeren a Linux-disztribúciótól és az operációs rendszer verziójától függően változik.</span><span class="sxs-lookup"><span data-stu-id="a9d62-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="a9d62-113">Részletes útmutatásokat a következő cikkekben talál:</span><span class="sxs-lookup"><span data-stu-id="a9d62-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="a9d62-114">A PowerShell Core telepítése macOS rendszeren</span><span class="sxs-lookup"><span data-stu-id="a9d62-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="a9d62-115">A PowerShell Core telepítése Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="a9d62-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="a9d62-116">A .NET Core-hoz készült Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="a9d62-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="a9d62-117">A PowerShell Core 6-os verziója tartalmazza az előre telepített PowerShellGet modult.</span><span class="sxs-lookup"><span data-stu-id="a9d62-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="a9d62-118">Ez megkönnyíti a PowerShell-galériában közzétett modulok telepítését.</span><span class="sxs-lookup"><span data-stu-id="a9d62-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="a9d62-119">Az Azure PowerShell telepítéséhez nyisson meg egy új PowerShell-munkamenetet, majd futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="a9d62-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="a9d62-120">Az AzureRM.Netcore-modul betöltése</span><span class="sxs-lookup"><span data-stu-id="a9d62-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="a9d62-121">A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe.</span><span class="sxs-lookup"><span data-stu-id="a9d62-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="a9d62-122">A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:</span><span class="sxs-lookup"><span data-stu-id="a9d62-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="a9d62-123">Amikor az importálás befejeződött, tesztelheti az újonnan telepített modult. Ehhez próbáljon meg bejelentkezni az Azure-ba az alábbi paranccsal:</span><span class="sxs-lookup"><span data-stu-id="a9d62-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="a9d62-124">A fenti parancsnak fel kell kérnie, hogy lépjen a `https://aka.ms/devicelogin` oldalra, és adja meg a megadott kódot.</span><span class="sxs-lookup"><span data-stu-id="a9d62-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="a9d62-125">Elérhető parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a9d62-125">Available cmdlets</span></span>

<span data-ttu-id="a9d62-126">A .NET Standardhoz elérhető Azure PowerShell-modulok még fejlesztés alatt állnak.</span><span class="sxs-lookup"><span data-stu-id="a9d62-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="a9d62-127">Ezek a modulok nem tartalmazzák a modulok Windows verziójához elérhető teljes parancsmagkészletét.</span><span class="sxs-lookup"><span data-stu-id="a9d62-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="a9d62-128">Az AzureRM.Netcore-modulokban az alábbi funkciók érhetők el:</span><span class="sxs-lookup"><span data-stu-id="a9d62-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="a9d62-129">Fiókkezelés</span><span class="sxs-lookup"><span data-stu-id="a9d62-129">Account management</span></span>
  - <span data-ttu-id="a9d62-130">Bejelentkezés Microsoft-fiókkal, szervezeti fiókkal vagy egyszerű szolgáltatásnévvel a Microsoft Azure Active Directoryn keresztül</span><span class="sxs-lookup"><span data-stu-id="a9d62-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="a9d62-131">Hitelesítő adatokat mentése lemezre a Save-AzureRmContext parancsmaggal és a mentett hitelesítő adatok betöltése az Import-AzureRmContext parancsmaggal</span><span class="sxs-lookup"><span data-stu-id="a9d62-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="a9d62-132">Környezet</span><span class="sxs-lookup"><span data-stu-id="a9d62-132">Environment</span></span>
  - <span data-ttu-id="a9d62-133">Különböző nem beépített Microsoft Azure-környezetek beszerzése</span><span class="sxs-lookup"><span data-stu-id="a9d62-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="a9d62-134">Testre szabott környezetek (például az Azure Stack- vagy a Windows Azure Pack-környezetek) hozzáadása/beállítása/eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a9d62-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="a9d62-135">Felügyeletisík-parancsmagok az Azure-szolgáltatásokhoz a Resource Manager és a Service Manager felületeinek használatával.</span><span class="sxs-lookup"><span data-stu-id="a9d62-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="a9d62-136">Virtuális gép</span><span class="sxs-lookup"><span data-stu-id="a9d62-136">Virtual Machine</span></span>
  - <span data-ttu-id="a9d62-137">App Service (webhelyek)</span><span class="sxs-lookup"><span data-stu-id="a9d62-137">App Service (Websites)</span></span>
  - <span data-ttu-id="a9d62-138">SQL Database</span><span class="sxs-lookup"><span data-stu-id="a9d62-138">SQL Database</span></span>
  - <span data-ttu-id="a9d62-139">Storage</span><span class="sxs-lookup"><span data-stu-id="a9d62-139">Storage</span></span>
  - <span data-ttu-id="a9d62-140">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="a9d62-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="a9d62-141">További lépések</span><span class="sxs-lookup"><span data-stu-id="a9d62-141">Next Steps</span></span>

<span data-ttu-id="a9d62-142">Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="a9d62-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
