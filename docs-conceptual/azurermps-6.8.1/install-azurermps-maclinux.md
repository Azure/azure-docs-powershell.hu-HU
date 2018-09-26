---
title: Az Azure PowerShell telepítése macOS vagy Linux rendszeren
description: Az Azure PowerShell telepítése macOS vagy Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 8347502df3c9cd6237a44293cfa3e5c051066940
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300663"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="1a8ee-103">Az Azure PowerShell telepítése macOS vagy Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="1a8ee-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="1a8ee-104">Nem Windows rendszerű platformokon az Azure PowerShell futtatható a PowerShell Core 6-os verziójában.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="1a8ee-105">A PowerShell e verziója bármely, .NET Core-t támogató platformon történő használatra készült.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="1a8ee-106">Az ilyen platformokon történő használathoz elérhető az Azure PowerShell egy speciális .NET Core-verziója.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="1a8ee-107">Jelenleg a PowerShell Core 6-os verziója és a .NET Core-hoz készült Azure PowerShell csak bétaverzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="1a8ee-108">A termékek korlátozott támogatással rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-108">Support for these products is limited.</span></span> <span data-ttu-id="1a8ee-109">Ha problémákba ütközik vagy hibát észlel, jelentse be a problémát a GitHubon.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="1a8ee-110">A PowerShell Core 6-os verziójának problémái</span><span class="sxs-lookup"><span data-stu-id="1a8ee-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="1a8ee-111">Az Azure PowerShell problémái</span><span class="sxs-lookup"><span data-stu-id="1a8ee-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="1a8ee-112">A PowerShell Core telepítése</span><span class="sxs-lookup"><span data-stu-id="1a8ee-112">Install PowerShell Core</span></span>

<span data-ttu-id="1a8ee-113">A PowerShell Core telepítési útmutatása eltér a macOS- és a Linux-disztribúciók esetében.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="1a8ee-114">Részletes útmutatásokat a következő cikkekben talál:</span><span class="sxs-lookup"><span data-stu-id="1a8ee-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="1a8ee-115">A PowerShell Core telepítése macOS rendszeren</span><span class="sxs-lookup"><span data-stu-id="1a8ee-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="1a8ee-116">A PowerShell Core telepítése Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="1a8ee-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="1a8ee-117">A .NET Core-hoz készült Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="1a8ee-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="1a8ee-118">A PowerShell Core tartalmazza az előre telepített PowerShellGet modult.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="1a8ee-119">Modulok a PowerShellben történő telepítéséhez megemelt jogosultsági szint szükséges, ezért a munkamenetet superuser felhasználóként kell elindítani:</span><span class="sxs-lookup"><span data-stu-id="1a8ee-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="1a8ee-120">Az Azure PowerShell telepítéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="1a8ee-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="1a8ee-121">A más cikkekben ismertetett `AzureRM` modul nem a .NET Core-hoz készült, és nem fog működni a PowerShell Core-ral.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="1a8ee-122">Az `AzureRM` és az `AzureRM.NetCore` is ugyanazokat a parancsmagneveket használja, csak az összesített modul neve tér el, valamint az, hogy a .NET melyik verzióján lettek létrehozva.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="1a8ee-123">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1a8ee-124">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="1a8ee-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="1a8ee-125">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="1a8ee-126">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="1a8ee-126">Sign in</span></span>

<span data-ttu-id="1a8ee-127">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM.Netcore` modult a PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="1a8ee-128">A modul importálásához __nincs__ szükség megemelt jogosultsági szintre.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="1a8ee-129">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1a8ee-130">Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="1a8ee-131">macOS és Linux rendszeren a `$Profile` környezeti változó segítségével használja a profilját.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="1a8ee-132">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="1a8ee-133">Elérhető parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1a8ee-133">Available cmdlets</span></span>

<span data-ttu-id="1a8ee-134">A .NET Core-hoz elérhető Azure PowerShell-modulok még fejlesztés alatt állnak.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="1a8ee-135">Ezek a modulok nem tartalmazzák a modulok Windows-verziójához elérhető teljes parancsmagkészletét.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-135">These modules don't provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="1a8ee-136">Az AzureRM.Netcore-modulokban az alábbi funkciók érhetők el:</span><span class="sxs-lookup"><span data-stu-id="1a8ee-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="1a8ee-137">Fiókkezelés</span><span class="sxs-lookup"><span data-stu-id="1a8ee-137">Account management</span></span>
  * <span data-ttu-id="1a8ee-138">Bejelentkezés Microsoft-fiókkal, vállalati fiókkal vagy szolgáltatásnévvel a Microsoft Azure Active Directoryn keresztül</span><span class="sxs-lookup"><span data-stu-id="1a8ee-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="1a8ee-139">Hitelesítő adatokat mentése lemezre a Save-AzureRmContext parancsmaggal és a mentett hitelesítő adatok betöltése az Import-AzureRmContext parancsmaggal</span><span class="sxs-lookup"><span data-stu-id="1a8ee-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="1a8ee-140">Környezet</span><span class="sxs-lookup"><span data-stu-id="1a8ee-140">Environment</span></span>
  * <span data-ttu-id="1a8ee-141">Különböző nem beépített Microsoft Azure-környezetek beszerzése</span><span class="sxs-lookup"><span data-stu-id="1a8ee-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="1a8ee-142">Testre szabott környezetek (például az Azure Stack- vagy a Windows Azure Pack-környezetek) hozzáadása/beállítása/eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1a8ee-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="1a8ee-143">Felügyeletisík-parancsmagok az Azure-szolgáltatásokhoz a Resource Manager és a klasszikus üzemi modell felületeinek használatával.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-143">Management plane cmdlets for Azure services using Resource Manager and classic deployment model interfaces.</span></span>
  * <span data-ttu-id="1a8ee-144">Virtuális gép</span><span class="sxs-lookup"><span data-stu-id="1a8ee-144">Virtual Machine</span></span>
  * <span data-ttu-id="1a8ee-145">App Service (webhelyek)</span><span class="sxs-lookup"><span data-stu-id="1a8ee-145">App Service (Websites)</span></span>
  * <span data-ttu-id="1a8ee-146">SQL Database</span><span class="sxs-lookup"><span data-stu-id="1a8ee-146">SQL Database</span></span>
  * <span data-ttu-id="1a8ee-147">Storage</span><span class="sxs-lookup"><span data-stu-id="1a8ee-147">Storage</span></span>
  * <span data-ttu-id="1a8ee-148">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="1a8ee-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="1a8ee-149">További lépések</span><span class="sxs-lookup"><span data-stu-id="1a8ee-149">Next Steps</span></span>

<span data-ttu-id="1a8ee-150">Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="1a8ee-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
