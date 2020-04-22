---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "81445696"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="4c799-103">Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="4c799-103">Install Azure PowerShell</span></span>

<span data-ttu-id="4c799-104">Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését ismerteti.</span><span class="sxs-lookup"><span data-stu-id="4c799-104">This article explains how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="4c799-105">Az útmutatás Windows, macOS és Linux platformon használható.</span><span class="sxs-lookup"><span data-stu-id="4c799-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="4c799-106">Az Azure PowerShell az Azure [Cloud Shellben](/azure/cloud-shell/overview) is elérhető, és mostantól a [Docker-rendszerképek](azureps-in-docker.md) előre telepítve tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="4c799-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c799-107">Követelmények</span><span class="sxs-lookup"><span data-stu-id="4c799-107">Requirements</span></span>

<span data-ttu-id="4c799-108">Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell Core 6.x vagy újabb verziójával működik.</span><span class="sxs-lookup"><span data-stu-id="4c799-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="4c799-109">Telepítenie kell a PowerShell Core-nak az operációs rendszerhez elérhető [legújabb verzióját](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="4c799-109">You should install the [latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) available for your operating system.</span></span> <span data-ttu-id="4c799-110">Az Azure PowerShell nem támaszt további követelményeket a PowerShell Core használata esetén.</span><span class="sxs-lookup"><span data-stu-id="4c799-110">Azure PowerShell has no additional requirements when run on PowerShell Core.</span></span>

<span data-ttu-id="4c799-111">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="4c799-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="4c799-112">Az Azure PowerShell használata PowerShell 5.1-ben Windows rendszeren:</span><span class="sxs-lookup"><span data-stu-id="4c799-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="4c799-113">Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="4c799-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="4c799-114">Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="4c799-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="4c799-115">Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="4c799-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="4c799-116">Győződjön meg arról, hogy a PowerShellGet legújabb verziójával rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="4c799-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="4c799-117">Futtassa az `Update-Module PowerShellGet -Force` parancsot.</span><span class="sxs-lookup"><span data-stu-id="4c799-117">Run `Update-Module PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="4c799-118">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="4c799-118">Install the Azure PowerShell module</span></span>

<span data-ttu-id="4c799-119">Az előnyben részesített telepítési módszer a PowerShellGet-parancsmagok használata.</span><span class="sxs-lookup"><span data-stu-id="4c799-119">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="4c799-120">Ez a módszer Windows, macOS és Linux platformon ugyanúgy működik.</span><span class="sxs-lookup"><span data-stu-id="4c799-120">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="4c799-121">Futtassa az alábbi parancsot egy PowerShell-munkamenetből:</span><span class="sxs-lookup"><span data-stu-id="4c799-121">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="4c799-122">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="4c799-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="4c799-123">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="4c799-123">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="4c799-124">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="4c799-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="4c799-125">Az Az modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="4c799-125">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="4c799-126">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="4c799-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

> [!WARNING]
> <span data-ttu-id="4c799-127">Az AzureRM és az Az modul nem lehet egyszerre telepítve a PowerShell 5.1-hez ugyanazon a Windows rendszeren.</span><span class="sxs-lookup"><span data-stu-id="4c799-127">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="4c799-128">Ha az AzureRM-nek továbbra is elérhetőnek kell maradnia a rendszeren, telepítse a PowerShell Core 6.x vagy újabb verziójához készült Az modult.</span><span class="sxs-lookup"><span data-stu-id="4c799-128">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span>

<span data-ttu-id="4c799-129">Először [telepítse a PowerShell Core 6.x vagy újabb verzióját](/powershell/scripting/install/installing-powershell-core-on-windows).</span><span class="sxs-lookup"><span data-stu-id="4c799-129">First, [install PowerShell Core 6.x or later](/powershell/scripting/install/installing-powershell-core-on-windows)</span></span>

<span data-ttu-id="4c799-130">Ezután telepítse az Az modult csak az aktuális felhasználó számára egy PowerShell Core-munkamenetből.</span><span class="sxs-lookup"><span data-stu-id="4c799-130">Then, from a PowerShell Core session, install the Az module for the current user only.</span></span> <span data-ttu-id="4c799-131">Ez az ajánlott telepítési hatókör.</span><span class="sxs-lookup"><span data-stu-id="4c799-131">This is the recommended installation scope.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="4c799-132">A modulnak a rendszer összes felhasználója számára történő telepítéséhez emelt szintű jogosultságokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="4c799-132">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="4c799-133">A PowerShell-munkamenetet a **Futtatás rendszergazdaként** paranccsal indítsa el Windows, illetve a `sudo` paranccsal macOS vagy Linux rendszeren:</span><span class="sxs-lookup"><span data-stu-id="4c799-133">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a><span data-ttu-id="4c799-134">Offline telepítés</span><span class="sxs-lookup"><span data-stu-id="4c799-134">Install offline</span></span>

<span data-ttu-id="4c799-135">Néhány környezetben nem lehet csatlakozni a PowerShell-galériához.</span><span class="sxs-lookup"><span data-stu-id="4c799-135">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="4c799-136">Ezekben a helyzetekben offline telepítést végezhet az alábbi módszerek valamelyikével:</span><span class="sxs-lookup"><span data-stu-id="4c799-136">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="4c799-137">Töltse le a modulokat a hálózat egy másik helyére, és azt a helyet használja a telepítési forrásként.</span><span class="sxs-lookup"><span data-stu-id="4c799-137">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="4c799-138">Ez lehetővé teszi, hogy a PowerShell-modulokat egyetlen kiszolgálón vagy fájlmegosztáson gyorsítótárazza, így a PowerShellGet használatával bármely leválasztott rendszeren üzembe helyezheti őket.</span><span class="sxs-lookup"><span data-stu-id="4c799-138">This allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="4c799-139">Megtudhatja, hogyan állíthat be helyi adattárat, és hogyan telepíthet leválasztott rendszerekre [helyi PowerShellGet-adattárakkal](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="4c799-139">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="4c799-140">[Letöltheti az Azure PowerShell MSI-t](install-az-ps-msi.md) a hálózathoz csatlakoztatott egyik gépre, majd a telepítőt olyan rendszerekre másolhatja, amelyek nem férnek hozzá a PowerShell-galériához.</span><span class="sxs-lookup"><span data-stu-id="4c799-140">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="4c799-141">Ne feledje, hogy az MSI-telepítő csak a PowerShell 5.1-hez, Windows rendszeren használható.</span><span class="sxs-lookup"><span data-stu-id="4c799-141">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="4c799-142">A modult a [Save-Module](/powershell/module/PowershellGet/Save-Module) paranccsal egy fájlmegosztásra mentheti, vagy egy másik forrásra mentheti, és más gépekre másolhatja:</span><span class="sxs-lookup"><span data-stu-id="4c799-142">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="4c799-143">Hibaelhárítás</span><span class="sxs-lookup"><span data-stu-id="4c799-143">Troubleshooting</span></span>

<span data-ttu-id="4c799-144">Az alábbiakban néhány, az Azure PowerShell modul telepítése során gyakran jelentkező problémáról olvashat.</span><span class="sxs-lookup"><span data-stu-id="4c799-144">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="4c799-145">Ha itt nem szereplő problémába ütközik, [jelentse be a problémát a GitHubon](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="4c799-145">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="4c799-146">Egy proxy blokkolja a kapcsolatot</span><span class="sxs-lookup"><span data-stu-id="4c799-146">Proxy blocks connection</span></span>

<span data-ttu-id="4c799-147">Ha `Install-Module`-hibaüzenet jelenik meg, amely jelzi, hogy a PowerShell-galéria nem érhető el, lehetséges, hogy egy proxy mögött van.</span><span class="sxs-lookup"><span data-stu-id="4c799-147">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="4c799-148">A különböző operációs rendszerek és hálózati környezetek eltérő követelményeket támasztanak a rendszerszintű proxy konfigurálására vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="4c799-148">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="4c799-149">A proxybeállításokkal és a környezet számára történő konfigurálásukkal kapcsolatban vegye fel a kapcsolatot a rendszergazdával.</span><span class="sxs-lookup"><span data-stu-id="4c799-149">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="4c799-150">Lehetséges, hogy maga a PowerShell nem konfigurálható a proxy automatikus használatára.</span><span class="sxs-lookup"><span data-stu-id="4c799-150">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="4c799-151">A PowerShell 5.1-es vagy újabb verziója esetén konfigurálja a PowerShell-munkamenetet egy proxy használatára az alábbi parancsokkal:</span><span class="sxs-lookup"><span data-stu-id="4c799-151">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="4c799-152">Ha az operációs rendszer hitelesítő adatai megfelelően vannak konfigurálva, ez a konfiguráció a proxyn keresztül irányítja át PowerShell-kéréseket.</span><span class="sxs-lookup"><span data-stu-id="4c799-152">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="4c799-153">Ha azt szeretné, hogy ezt a beállítást a munkamenetek között is megőrizze a rendszer, adja hozzá a parancsokat a [PowerShell-profilhoz](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="4c799-153">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="4c799-154">A csomag telepítéséhez a proxynak engedélyeznie kell az alábbi címekre irányuló HTTPS-kapcsolatokat:</span><span class="sxs-lookup"><span data-stu-id="4c799-154">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="4c799-155">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="4c799-155">Sign in</span></span>

<span data-ttu-id="4c799-156">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="4c799-156">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="4c799-157">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult az `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="4c799-157">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="4c799-158">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="4c799-158">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="4c799-159">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="4c799-159">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="4c799-160">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="4c799-160">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="4c799-161">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="4c799-161">Update the Azure PowerShell module</span></span>

<span data-ttu-id="4c799-162">PowerShell-modulok frissítéséhez ugyanazt a módszert használja, mint a modul telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="4c799-162">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="4c799-163">Ha eredetileg például az `Install-Module` parancsmagot használta, akkor használja az [Update-Module](/powershell/module/powershellget/update-module) parancsmagot a legújabb verzió beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="4c799-163">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="4c799-164">Ha eredetileg az MSI-csomagot használta, akkor töltse le és telepítse az új MSI-csomagot.</span><span class="sxs-lookup"><span data-stu-id="4c799-164">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="4c799-165">A PowerShellGet-parancsmagok nem tudnak MSI-csomagból telepített modulokat frissíteni.</span><span class="sxs-lookup"><span data-stu-id="4c799-165">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="4c799-166">Az MSI-csomagok nem frissítenek a PowerShellGettel telepített modulokat.</span><span class="sxs-lookup"><span data-stu-id="4c799-166">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="4c799-167">Ha bármilyen problémába ütközik a PowerShellGettel történő frissítés esetén, akkor a **frissítés** helyett **újra kell telepítenie** a modult.</span><span class="sxs-lookup"><span data-stu-id="4c799-167">If you have any issues updating using PowershellGet then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="4c799-168">Az újratelepítés ugyanúgy történik, mint a telepítés, de hozzá kell adnia a `-Force` paramétert:</span><span class="sxs-lookup"><span data-stu-id="4c799-168">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="4c799-169">Az MSI-alapú telepítésektől eltérően a PowerShellGettel történő telepítés vagy frissítés nem távolítja el a rendszeren esetlegesen megtalálható régebbi verziókat.</span><span class="sxs-lookup"><span data-stu-id="4c799-169">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="4c799-170">Az Azure PowerShell régebbi verzióinak eltávolításáról [az Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="4c799-170">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="4c799-171">Az MSI-alapú telepítésekkel kapcsolatban [az Azure PowerShell MSI-vel történő telepítését](install-az-ps-msi.md) ismertető témakörben tekinthet meg további információt.</span><span class="sxs-lookup"><span data-stu-id="4c799-171">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="4c799-172">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="4c799-172">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="4c799-173">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="4c799-173">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="4c799-174">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="4c799-174">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="4c799-175">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="4c799-175">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="4c799-176">Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.</span><span class="sxs-lookup"><span data-stu-id="4c799-176">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="4c799-177">Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` paramétert:</span><span class="sxs-lookup"><span data-stu-id="4c799-177">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="4c799-178">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="4c799-178">Provide feedback</span></span>

<span data-ttu-id="4c799-179">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="4c799-179">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="4c799-180">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="4c799-180">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4c799-181">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="4c799-181">Next Steps</span></span>

<span data-ttu-id="4c799-182">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="4c799-182">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="4c799-183">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="4c799-183">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
