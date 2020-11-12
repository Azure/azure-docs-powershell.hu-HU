---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 39b0a700c1568f7c241c1abff38665428f326825
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408424"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="13c0c-103">Az Azure PowerShell telepítése</span><span class="sxs-lookup"><span data-stu-id="13c0c-103">Install Azure PowerShell</span></span>

<span data-ttu-id="13c0c-104">Ez a cikk az Azure PowerShell-modulok a [PowerShellGet](/powershell/scripting/gallery/installing-psget) használatával való telepítését ismerteti.</span><span class="sxs-lookup"><span data-stu-id="13c0c-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="13c0c-105">Az útmutatás Windows, macOS és Linux platformon használható.</span><span class="sxs-lookup"><span data-stu-id="13c0c-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="13c0c-106">Az Azure PowerShell az Azure [Cloud Shellben](/azure/cloud-shell/overview) is elérhető.</span><span class="sxs-lookup"><span data-stu-id="13c0c-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview).</span></span>

## <a name="requirements"></a><span data-ttu-id="13c0c-107">Követelmények</span><span class="sxs-lookup"><span data-stu-id="13c0c-107">Requirements</span></span>

> [!NOTE]
> <span data-ttu-id="13c0c-108">A PowerShell az Azure PowerShell-lel történő használatához az összes platformon a PowerShell 7.x vagy újabb verziója javasolt.</span><span class="sxs-lookup"><span data-stu-id="13c0c-108">PowerShell 7.x and later is the recommended version of PowerShell for use with Azure PowerShell on all platforms.</span></span>

<span data-ttu-id="13c0c-109">Az Azure PowerShell kompatibilis a PowerShell 6.2.4-es vagy újabb verziójával az összes platformon.</span><span class="sxs-lookup"><span data-stu-id="13c0c-109">Azure PowerShell works with PowerShell 6.2.4 and later on all platforms.</span></span> <span data-ttu-id="13c0c-110">Windows rendszeren a PowerShell 5.1-es verziójával is támogatott.</span><span class="sxs-lookup"><span data-stu-id="13c0c-110">It is also supported with PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="13c0c-111">Telepítse az operációs rendszeréhez elérhető [legújabb PowerShell-verziót](/powershell/scripting/install/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="13c0c-111">Install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="13c0c-112">Az Azure PowerShell nem támaszt további követelményeket a PowerShell 6.2.4-es vagy újabb verziója használata esetén.</span><span class="sxs-lookup"><span data-stu-id="13c0c-112">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="13c0c-113">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="13c0c-113">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="13c0c-114">Az Azure PowerShell használata PowerShell 5.1-ben Windows rendszeren:</span><span class="sxs-lookup"><span data-stu-id="13c0c-114">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="13c0c-115">Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="13c0c-115">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="13c0c-116">Ha a Windows 10 1607-es vagy újabb verzióját használja, már telepítve van a PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="13c0c-116">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="13c0c-117">Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="13c0c-117">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="13c0c-118">Győződjön meg arról, hogy a PowerShellGet legújabb verziójával rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="13c0c-118">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="13c0c-119">Futtassa az `Install-Module -Name PowerShellGet -Force` parancsot.</span><span class="sxs-lookup"><span data-stu-id="13c0c-119">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="13c0c-120">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="13c0c-120">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="13c0c-121">Az AzureRM és az Az modul nem lehet egyszerre telepítve a PowerShell 5.1-hez ugyanazon a Windows rendszeren.</span><span class="sxs-lookup"><span data-stu-id="13c0c-121">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="13c0c-122">Ha az AzureRM-nek továbbra is elérhetőnek kell maradnia a rendszeren, telepítse a PowerShell Core 6.x vagy újabb verziójához készült Az modult.</span><span class="sxs-lookup"><span data-stu-id="13c0c-122">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span>

<span data-ttu-id="13c0c-123">Az előnyben részesített telepítési módszer a PowerShellGet-parancsmagok használata.</span><span class="sxs-lookup"><span data-stu-id="13c0c-123">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="13c0c-124">Csak az aktuális felhasználó számára telepítse az Az modult.</span><span class="sxs-lookup"><span data-stu-id="13c0c-124">Install the Az module for the current user only.</span></span> <span data-ttu-id="13c0c-125">Ez az ajánlott telepítési hatókör.</span><span class="sxs-lookup"><span data-stu-id="13c0c-125">This is the recommended installation scope.</span></span> <span data-ttu-id="13c0c-126">Ez a módszer Windows, macOS és Linux platformon ugyanúgy működik.</span><span class="sxs-lookup"><span data-stu-id="13c0c-126">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="13c0c-127">Futtassa az alábbi parancsot egy PowerShell-munkamenetből:</span><span class="sxs-lookup"><span data-stu-id="13c0c-127">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="13c0c-128">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="13c0c-128">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="13c0c-129">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="13c0c-129">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="13c0c-130">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="13c0c-130">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="13c0c-131">A modulnak a rendszer összes felhasználója számára történő telepítéséhez emelt szintű jogosultságokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="13c0c-131">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="13c0c-132">A PowerShell-munkamenetet a **Futtatás rendszergazdaként** paranccsal indítsa el Windows, illetve a `sudo` paranccsal macOS vagy Linux rendszeren:</span><span class="sxs-lookup"><span data-stu-id="13c0c-132">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="13c0c-133">Az Az modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="13c0c-133">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="13c0c-134">A modul telepítésével letölti az összes általánosan elérhető Az PowerShell-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="13c0c-134">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="13c0c-135">Offline telepítés</span><span class="sxs-lookup"><span data-stu-id="13c0c-135">Install offline</span></span>

<span data-ttu-id="13c0c-136">Néhány környezetben nem lehet csatlakozni a PowerShell-galériához.</span><span class="sxs-lookup"><span data-stu-id="13c0c-136">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="13c0c-137">Ezekben a helyzetekben offline telepítést végezhet az alábbi módszerek valamelyikével:</span><span class="sxs-lookup"><span data-stu-id="13c0c-137">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="13c0c-138">Töltse le a modulokat a hálózat egy másik helyére, és azt a helyet használja a telepítési forrásként.</span><span class="sxs-lookup"><span data-stu-id="13c0c-138">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="13c0c-139">Ez a módszer lehetővé teszi, hogy a PowerShell-modulokat egyetlen kiszolgálón vagy fájlmegosztáson gyorsítótárazza, így a PowerShellGet használatával bármely leválasztott rendszeren üzembe helyezheti őket.</span><span class="sxs-lookup"><span data-stu-id="13c0c-139">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="13c0c-140">Megtudhatja, hogyan állíthat be helyi adattárat, és hogyan telepíthet leválasztott rendszerekre [helyi PowerShellGet-adattárakkal](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="13c0c-140">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="13c0c-141">[Letöltheti az Azure PowerShell MSI-t](install-az-ps-msi.md) a hálózathoz csatlakoztatott egyik gépre, majd a telepítőt olyan rendszerekre másolhatja, amelyek nem férnek hozzá a PowerShell-galériához.</span><span class="sxs-lookup"><span data-stu-id="13c0c-141">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="13c0c-142">Ne feledje, hogy az MSI-telepítő csak a PowerShell 5.1-hez, Windows rendszeren használható.</span><span class="sxs-lookup"><span data-stu-id="13c0c-142">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="13c0c-143">A modult a [Save-Module](/powershell/module/PowershellGet/Save-Module) paranccsal egy fájlmegosztásra mentheti, vagy egy másik forrásra mentheti, és más gépekre másolhatja:</span><span class="sxs-lookup"><span data-stu-id="13c0c-143">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="13c0c-144">Hibaelhárítás</span><span class="sxs-lookup"><span data-stu-id="13c0c-144">Troubleshooting</span></span>

<span data-ttu-id="13c0c-145">Az alábbiakban néhány, az Azure PowerShell modul telepítése során gyakran jelentkező problémáról olvashat.</span><span class="sxs-lookup"><span data-stu-id="13c0c-145">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="13c0c-146">Ha itt nem szereplő problémába ütközik, [jelentse be a problémát a GitHubon](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="13c0c-146">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="13c0c-147">Egy proxy blokkolja a kapcsolatot</span><span class="sxs-lookup"><span data-stu-id="13c0c-147">Proxy blocks connection</span></span>

<span data-ttu-id="13c0c-148">Ha `Install-Module`-hibaüzenet jelenik meg, amely jelzi, hogy a PowerShell-galéria nem érhető el, lehetséges, hogy egy proxy mögött van.</span><span class="sxs-lookup"><span data-stu-id="13c0c-148">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="13c0c-149">A különböző operációs rendszerek és hálózati környezetek eltérő követelményeket támasztanak a rendszerszintű proxy konfigurálására vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="13c0c-149">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="13c0c-150">A proxybeállításokkal és a környezet számára történő konfigurálásukkal kapcsolatban vegye fel a kapcsolatot a rendszergazdával.</span><span class="sxs-lookup"><span data-stu-id="13c0c-150">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="13c0c-151">Lehetséges, hogy maga a PowerShell nem konfigurálható a proxy automatikus használatára.</span><span class="sxs-lookup"><span data-stu-id="13c0c-151">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="13c0c-152">A PowerShell 5.1-es vagy újabb verziója esetén konfigurálja a PowerShell-munkamenetet egy proxy használatára az alábbi parancsokkal:</span><span class="sxs-lookup"><span data-stu-id="13c0c-152">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="13c0c-153">Ha az operációs rendszer hitelesítő adatai megfelelően vannak konfigurálva, ez a konfiguráció a proxyn keresztül irányítja át PowerShell-kéréseket.</span><span class="sxs-lookup"><span data-stu-id="13c0c-153">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="13c0c-154">Ha azt szeretné, hogy ezt a beállítást a munkamenetek között is megőrizze a rendszer, adja hozzá a parancsokat a [PowerShell-profilhoz](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="13c0c-154">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="13c0c-155">A csomag telepítéséhez a proxynak engedélyeznie kell az alábbi címekre irányuló HTTPS-kapcsolatokat:</span><span class="sxs-lookup"><span data-stu-id="13c0c-155">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="13c0c-156">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="13c0c-156">Sign in</span></span>

<span data-ttu-id="13c0c-157">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="13c0c-157">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="13c0c-158">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult az `Import-Module -Name Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="13c0c-158">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="13c0c-159">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="13c0c-159">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="13c0c-160">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="13c0c-160">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="13c0c-161">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="13c0c-161">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="13c0c-162">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="13c0c-162">Update the Azure PowerShell module</span></span>

<span data-ttu-id="13c0c-163">PowerShell-modulok frissítéséhez ugyanazt a módszert használja, mint a modul telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="13c0c-163">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="13c0c-164">Ha eredetileg például az `Install-Module` parancsmagot használta, akkor használja az [Update-Module](/powershell/module/powershellget/update-module) parancsmagot a legújabb verzió beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="13c0c-164">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="13c0c-165">Ha eredetileg az MSI-csomagot használta, akkor töltse le és telepítse az új MSI-csomagot.</span><span class="sxs-lookup"><span data-stu-id="13c0c-165">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="13c0c-166">A PowerShellGet-parancsmagok nem tudnak MSI-csomagból telepített modulokat frissíteni.</span><span class="sxs-lookup"><span data-stu-id="13c0c-166">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="13c0c-167">Az MSI-csomagok nem frissítenek a PowerShellGettel telepített modulokat.</span><span class="sxs-lookup"><span data-stu-id="13c0c-167">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="13c0c-168">Ha bármilyen problémába ütközik a PowerShellGettel történő frissítés közben, akkor a **frissítés** helyett **újra kell telepítenie** a modult.</span><span class="sxs-lookup"><span data-stu-id="13c0c-168">If you have any issues updating using PowershellGet, then you should **reinstall** , rather than **update**.</span></span> <span data-ttu-id="13c0c-169">Az újratelepítés ugyanúgy történik, mint a telepítés, de hozzá kell adnia a `-Force` paramétert:</span><span class="sxs-lookup"><span data-stu-id="13c0c-169">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="13c0c-170">Az MSI-alapú telepítésektől eltérően a PowerShellGettel történő telepítés vagy frissítés nem távolítja el a rendszeren esetlegesen megtalálható régebbi verziókat.</span><span class="sxs-lookup"><span data-stu-id="13c0c-170">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="13c0c-171">Az Azure PowerShell régebbi verzióinak eltávolításáról [az Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="13c0c-171">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="13c0c-172">Az MSI-alapú telepítésekkel kapcsolatban [az Azure PowerShell MSI-vel történő telepítését](install-az-ps-msi.md) ismertető témakörben tekinthet meg további információt.</span><span class="sxs-lookup"><span data-stu-id="13c0c-172">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="13c0c-173">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="13c0c-173">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="13c0c-174">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="13c0c-174">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="13c0c-175">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="13c0c-175">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="13c0c-176">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="13c0c-176">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="13c0c-177">Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.</span><span class="sxs-lookup"><span data-stu-id="13c0c-177">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="13c0c-178">Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` paramétert:</span><span class="sxs-lookup"><span data-stu-id="13c0c-178">You can install or load a specific version of the `Az` module using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 1.8.0
Install-Module -Name Az -RequiredVersion 1.8.0
# Load Az version 1.8.0
Import-Module -Name Az -RequiredVersion 1.8.0
```

## <a name="provide-feedback"></a><span data-ttu-id="13c0c-179">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="13c0c-179">Provide feedback</span></span>

<span data-ttu-id="13c0c-180">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="13c0c-180">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="13c0c-181">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="13c0c-181">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="13c0c-182">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="13c0c-182">Next Steps</span></span>

<span data-ttu-id="13c0c-183">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="13c0c-183">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="13c0c-184">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="13c0c-184">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
