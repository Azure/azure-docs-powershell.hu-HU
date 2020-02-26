---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 66d755384e532d434811f3e6122dcba97d5c48b5
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477848"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="fc15a-103">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="fc15a-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="fc15a-104">Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be.</span><span class="sxs-lookup"><span data-stu-id="fc15a-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="fc15a-105">Az útmutatás Windows, macOS és Linux platformon használható.</span><span class="sxs-lookup"><span data-stu-id="fc15a-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="fc15a-106">Az Az modulhoz jelenleg nem támogatottak más telepítési módszerek.</span><span class="sxs-lookup"><span data-stu-id="fc15a-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc15a-107">Követelmények</span><span class="sxs-lookup"><span data-stu-id="fc15a-107">Requirements</span></span>

<span data-ttu-id="fc15a-108">Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell Core 6.x vagy újabb verziójával működik.</span><span class="sxs-lookup"><span data-stu-id="fc15a-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="fc15a-109">Ha nem biztos abban, hogy rendelkezik-e PowerShell-lel, illetve macOS vagy Linux rendszert használ, [telepítse a PowerShell Core legújabb verzióját](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="fc15a-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="fc15a-110">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="fc15a-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="fc15a-111">Az Azure PowerShell futtatása PowerShell 5.1-ben Windows rendszeren:</span><span class="sxs-lookup"><span data-stu-id="fc15a-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="fc15a-112">Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="fc15a-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="fc15a-113">Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="fc15a-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="fc15a-114">Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="fc15a-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="fc15a-115">Nincsenek további követelmények az Azure PowerShellhez a PowerShell Core használata esetén.</span><span class="sxs-lookup"><span data-stu-id="fc15a-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="fc15a-116">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="fc15a-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="fc15a-117">Az AzureRM és az Az modul __nem__ lehet egyszerre telepítve a PowerShell 5.1-hez ugyanazon a Windows rendszeren.</span><span class="sxs-lookup"><span data-stu-id="fc15a-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="fc15a-118">Ha az AzureRM-nek továbbra is elérhetőnek kell maradnia a rendszeren, telepítse a PowerShell Core 6.x vagy újabb verziójához készült Az modult.</span><span class="sxs-lookup"><span data-stu-id="fc15a-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="fc15a-119">Ehhez [telepítse a PowerShell Core 6.x vagy újabb](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) verzióját, majd kövesse az itt ismertetett utasításokat a PowerShell Core-terminálban.</span><span class="sxs-lookup"><span data-stu-id="fc15a-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="fc15a-120">Ajánlott csak az aktív felhasználó számára telepíteni:</span><span class="sxs-lookup"><span data-stu-id="fc15a-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="fc15a-121">Ha a rendszer összes felhasználója számára szeretné telepíteni, akkor rendszergazdai jogosultságokra lesz szüksége.</span><span class="sxs-lookup"><span data-stu-id="fc15a-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="fc15a-122">Egy rendszergazdaként, illetve macOS vagy Linux rendszeren a `sudo` paranccsal indított, emelt szintű PowerShell-munkamenetben:</span><span class="sxs-lookup"><span data-stu-id="fc15a-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="fc15a-123">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="fc15a-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="fc15a-124">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="fc15a-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="fc15a-125">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="fc15a-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="fc15a-126">Az Az modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="fc15a-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="fc15a-127">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="fc15a-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="fc15a-128">Offline telepítés</span><span class="sxs-lookup"><span data-stu-id="fc15a-128">Install offline</span></span>

<span data-ttu-id="fc15a-129">Néhány környezetben nem lehet csatlakozni a PowerShell-galériához.</span><span class="sxs-lookup"><span data-stu-id="fc15a-129">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="fc15a-130">Ezekben a helyzetekben offline telepítést végezhet az alábbi módszerek valamelyikével:</span><span class="sxs-lookup"><span data-stu-id="fc15a-130">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="fc15a-131">Töltse le a modulokat egy másik helyre, és azt a helyet használja a hálózat telepítési forrásaként.</span><span class="sxs-lookup"><span data-stu-id="fc15a-131">Download the modules to another location and use that as an installation source on your network.</span></span> <span data-ttu-id="fc15a-132">Ez bonyolult folyamat lehet, de lehetővé teszi, hogy a PowerShell-modulokat egyetlen kiszolgálón vagy fájlmegosztáson gyorsítótárazza, így a PowerShellGet használatával bármely leválasztott rendszeren üzembe helyezheti őket.</span><span class="sxs-lookup"><span data-stu-id="fc15a-132">This can be a complicated process, but will let you cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="fc15a-133">Megtudhatja, hogyan állíthat be helyi adattárat, és hogyan telepíthet leválasztott rendszerekre [helyi PowerShellGet-adattárakkal](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="fc15a-133">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="fc15a-134">[Letöltheti az Azure PowerShell MSI-t](install-az-ps-msi.md) a hálózathoz csatlakoztatott egyik gépre, majd a telepítőt olyan rendszerekre másolhatja, amelyek nem férnek hozzá a PowerShell-galériához.</span><span class="sxs-lookup"><span data-stu-id="fc15a-134">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="fc15a-135">Ne feledje, hogy az MSI-telepítő csak a PowerShell 5.1-hez, Windows rendszeren használható.</span><span class="sxs-lookup"><span data-stu-id="fc15a-135">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="fc15a-136">A modult a [Save-Module](/powershell/module/PowershellGet/Save-Module) paranccsal egy fájlmegosztásra mentheti, vagy egy másik forrásra mentheti, és más gépekre másolhatja:</span><span class="sxs-lookup"><span data-stu-id="fc15a-136">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="fc15a-137">Hibaelhárítás</span><span class="sxs-lookup"><span data-stu-id="fc15a-137">Troubleshooting</span></span>

<span data-ttu-id="fc15a-138">Az alábbiakban néhány, az Azure PowerShell modul telepítése során gyakran jelentkező problémáról olvashat.</span><span class="sxs-lookup"><span data-stu-id="fc15a-138">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="fc15a-139">Ha itt nem szereplő problémába ütközik, [jelentse be a problémát a GitHubon](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="fc15a-139">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="fc15a-140">Egy proxy blokkolja a kapcsolatot</span><span class="sxs-lookup"><span data-stu-id="fc15a-140">Proxy blocks connection</span></span>

<span data-ttu-id="fc15a-141">Ha `Install-Module`-hibaüzenet jelenik meg, amely jelzi, hogy a PowerShell-galéria nem érhető el, lehetséges, hogy egy proxy mögött van.</span><span class="sxs-lookup"><span data-stu-id="fc15a-141">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="fc15a-142">A különböző operációs rendszereknek eltérő követelményei vannak a rendszerszintű proxy konfigurálásához, amelynek részleteit itt most nem tárgyaljuk.</span><span class="sxs-lookup"><span data-stu-id="fc15a-142">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="fc15a-143">A proxybeállításokkal és az operációs rendszer beállításaival kapcsolatban vegye fel a kapcsolatot a rendszergazdával.</span><span class="sxs-lookup"><span data-stu-id="fc15a-143">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="fc15a-144">Lehetséges, hogy maga a PowerShell nem konfigurálható a proxy automatikus használatára.</span><span class="sxs-lookup"><span data-stu-id="fc15a-144">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="fc15a-145">PowerShell 5.1 vagy újabb változat esetén konfigurálja a proxyt PowerShell-munkamenet használatára az alábbi paranccsal:</span><span class="sxs-lookup"><span data-stu-id="fc15a-145">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="fc15a-146">Ha az operációs rendszer hitelesítő adatai megfelelően vannak konfigurálva, a PowerShell-kéréseket a proxyn keresztül irányítja át.</span><span class="sxs-lookup"><span data-stu-id="fc15a-146">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="fc15a-147">Ha azt szeretné, hogy ezt a beállítást a munkamenetek között is megőrizze a rendszer, adja hozzá ezt a parancsot egy [PowerShell-profilhoz](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="fc15a-147">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="fc15a-148">A csomag telepítéséhez a proxynak engedélyeznie kell az alábbi címekre irányuló HTTPS-kapcsolatokat:</span><span class="sxs-lookup"><span data-stu-id="fc15a-148">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="fc15a-149">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="fc15a-149">Sign in</span></span>

<span data-ttu-id="fc15a-150">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="fc15a-150">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="fc15a-151">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult az `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="fc15a-151">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="fc15a-152">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="fc15a-152">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="fc15a-153">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="fc15a-153">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="fc15a-154">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="fc15a-154">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="fc15a-155">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="fc15a-155">Update the Azure PowerShell module</span></span>

<span data-ttu-id="fc15a-156">Ha eredetileg az Install-Module parancsmagot használta, akkor használja az [Update-Module](/powershell/module/powershellget/update-module) parancsmagot a legújabb verzió beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="fc15a-156">If you originally used Install-Module, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="fc15a-157">Ha eredetileg az MSI-csomagot használta, akkor a frissítéshez töltse le és telepítse az új MSI-t.</span><span class="sxs-lookup"><span data-stu-id="fc15a-157">If you originally used the MSI package then you should download and install the new MSI in order to udpate.</span></span> <span data-ttu-id="fc15a-158">Ha bármilyen problémába ütközik a frissítés során a PowershellGet-csomag használata esetén, akkor nem elég __frissíteni__, de __újra is kell telepíteni__ a modult.</span><span class="sxs-lookup"><span data-stu-id="fc15a-158">If you have any issues with updating using the package from PowershellGet then you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="fc15a-159">Ez ugyanúgy történik, mint a telepítés, de előfordulhat, hogy hozzá kell adnia a `-Force` argumentumot:</span><span class="sxs-lookup"><span data-stu-id="fc15a-159">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="fc15a-160">Bár ez felülírhatja a telepített modulokat, még így is előfordulhat hogy maradnak régebbi verziók a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="fc15a-160">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="fc15a-161">Az Azure PowerShell régebbi verzióinak eltávolításáról [Az Azure PowerShell-modul eltávolítása](uninstall-az-ps.md) című szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="fc15a-161">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="fc15a-162">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="fc15a-162">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="fc15a-163">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="fc15a-163">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="fc15a-164">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="fc15a-164">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="fc15a-165">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="fc15a-165">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="fc15a-166">Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` argumentumot:</span><span class="sxs-lookup"><span data-stu-id="fc15a-166">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="fc15a-167">Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.</span><span class="sxs-lookup"><span data-stu-id="fc15a-167">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="fc15a-168">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="fc15a-168">Provide feedback</span></span>

<span data-ttu-id="fc15a-169">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="fc15a-169">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="fc15a-170">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="fc15a-170">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fc15a-171">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="fc15a-171">Next Steps</span></span>

<span data-ttu-id="fc15a-172">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="fc15a-172">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="fc15a-173">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="fc15a-173">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
