---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ead6c48496c646b5184f88aeac64fbe650be17c4
ms.sourcegitcommit: 0356a4694f77eda40eec8c3759b9bb7f28979eb6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2019
ms.locfileid: "67193175"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="9d280-103">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="9d280-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="9d280-104">Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be.</span><span class="sxs-lookup"><span data-stu-id="9d280-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="9d280-105">Az útmutatás Windows, macOS és Linux platformon használható.</span><span class="sxs-lookup"><span data-stu-id="9d280-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="9d280-106">Az Az modulhoz jelenleg nem támogatottak más telepítési módszerek.</span><span class="sxs-lookup"><span data-stu-id="9d280-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d280-107">Követelmények</span><span class="sxs-lookup"><span data-stu-id="9d280-107">Requirements</span></span>

<span data-ttu-id="9d280-108">Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell Core 6.x vagy újabb verziójával működik.</span><span class="sxs-lookup"><span data-stu-id="9d280-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="9d280-109">Ha nem biztos abban, hogy rendelkezik-e PowerShell-lel, illetve macOS vagy Linux rendszert használ, [telepítse a PowerShell Core legújabb verzióját](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="9d280-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="9d280-110">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="9d280-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="9d280-111">Az Azure PowerShell futtatása PowerShell 5.1-ben Windows rendszeren:</span><span class="sxs-lookup"><span data-stu-id="9d280-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="9d280-112">Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="9d280-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="9d280-113">Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="9d280-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="9d280-114">Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="9d280-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="9d280-115">Nincsenek további követelmények az Azure PowerShellhez a PowerShell Core használata esetén.</span><span class="sxs-lookup"><span data-stu-id="9d280-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="9d280-116">Az Azure PowerShell-modul telepítése</span><span class="sxs-lookup"><span data-stu-id="9d280-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="9d280-117">Az AzureRM és az Az modul __nem__ lehet egyszerre telepítve a PowerShell 5.1-hez ugyanazon a Windows rendszeren.</span><span class="sxs-lookup"><span data-stu-id="9d280-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="9d280-118">Ha az AzureRM-nek továbbra is elérhetőnek kell maradnia a rendszeren, telepítse a PowerShell Core 6.x vagy újabb verziójához készült Az modult.</span><span class="sxs-lookup"><span data-stu-id="9d280-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="9d280-119">Ehhez [telepítse a PowerShell Core 6.x vagy újabb](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) verzióját, majd kövesse az itt ismertetett utasításokat a PowerShell Core-terminálban.</span><span class="sxs-lookup"><span data-stu-id="9d280-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="9d280-120">A modulok globális hatókörben való telepítéséhez megemelt jogosultsági szint szükséges a PowerShell-galériából való telepítés esetén.</span><span class="sxs-lookup"><span data-stu-id="9d280-120">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="9d280-121">Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben („Futtatás rendszergazdaként” a Windows, vagy felügyelői jogosultságok a macOS vagy a Linux alatt):</span><span class="sxs-lookup"><span data-stu-id="9d280-121">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="9d280-122">Ha nem rendelkezik rendszergazdai jogosultsággal, a `-Scope` argumentum hozzáadásával végezhet telepítést az aktuális felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="9d280-122">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="9d280-123">Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként.</span><span class="sxs-lookup"><span data-stu-id="9d280-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9d280-124">A PSGallery első használatakor a következő üzenet jelenik meg:</span><span class="sxs-lookup"><span data-stu-id="9d280-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="9d280-125">A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="9d280-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="9d280-126">Az Az modul az Azure PowerShell-parancsmagok összesített modulja.</span><span class="sxs-lookup"><span data-stu-id="9d280-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="9d280-127">A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.</span><span class="sxs-lookup"><span data-stu-id="9d280-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9d280-128">Hibaelhárítás</span><span class="sxs-lookup"><span data-stu-id="9d280-128">Troubleshooting</span></span>

<span data-ttu-id="9d280-129">Az alábbiakban néhány, az Azure PowerShell modul telepítése során gyakran jelentkező problémáról olvashat.</span><span class="sxs-lookup"><span data-stu-id="9d280-129">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="9d280-130">Ha itt nem szereplő problémába ütközik, [jelentse be a problémát a GitHubon](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="9d280-130">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="9d280-131">Egy proxy blokkolja a kapcsolatot</span><span class="sxs-lookup"><span data-stu-id="9d280-131">Proxy blocks connection</span></span>

<span data-ttu-id="9d280-132">Ha `Install-Module`-hibaüzenet jelenik meg, amely jelzi, hogy a PowerShell-galéria nem érhető el, lehetséges, hogy egy proxy mögött van.</span><span class="sxs-lookup"><span data-stu-id="9d280-132">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="9d280-133">A különböző operációs rendszereknek eltérő követelményei vannak a rendszerszintű proxy konfigurálásához, amelynek részleteit itt most nem tárgyaljuk.</span><span class="sxs-lookup"><span data-stu-id="9d280-133">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="9d280-134">A proxybeállításokkal és az operációs rendszer beállításaival kapcsolatban vegye fel a kapcsolatot a rendszergazdával.</span><span class="sxs-lookup"><span data-stu-id="9d280-134">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="9d280-135">Lehetséges, hogy maga a PowerShell nem konfigurálható a proxy automatikus használatára.</span><span class="sxs-lookup"><span data-stu-id="9d280-135">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="9d280-136">PowerShell 5.1 vagy újabb változat esetén konfigurálja a proxyt PowerShell-munkamenet használatára az alábbi paranccsal:</span><span class="sxs-lookup"><span data-stu-id="9d280-136">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="9d280-137">Ha az operációs rendszer hitelesítő adatai megfelelően vannak konfigurálva, a PowerShell-kéréseket a proxyn keresztül irányítja át.</span><span class="sxs-lookup"><span data-stu-id="9d280-137">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="9d280-138">Ha azt szeretné, hogy ezt a beállítást a munkamenetek között is megőrizze a rendszer, adja hozzá ezt a parancsot egy [PowerShell-profilhoz](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="9d280-138">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="9d280-139">A csomag telepítéséhez a proxynak engedélyeznie kell az alábbi címekre irányuló HTTPS-kapcsolatokat:</span><span class="sxs-lookup"><span data-stu-id="9d280-139">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="9d280-140">Bejelentkezés</span><span class="sxs-lookup"><span data-stu-id="9d280-140">Sign in</span></span>

<span data-ttu-id="9d280-141">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="9d280-141">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="9d280-142">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="9d280-142">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="9d280-143">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="9d280-143">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="9d280-144">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="9d280-144">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="9d280-145">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="9d280-145">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="9d280-146">Az Azure PowerShell-modul frissítése</span><span class="sxs-lookup"><span data-stu-id="9d280-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="9d280-147">Az Az modul csomagolásának módja miatt az [Update-Module](/powershell/module/powershellget/update-module) parancs nem fogja megfelelően frissíteni a telepítést.</span><span class="sxs-lookup"><span data-stu-id="9d280-147">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="9d280-148">Az Az gyakorlatilag egy metamodul, amely magában foglalja az Azure-szolgáltatásokkal való kommunikációt szolgáló parancsmagokat tartalmazó összes almodult.</span><span class="sxs-lookup"><span data-stu-id="9d280-148">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="9d280-149">Ez azt jelenti, hogy az Azure PowerShell-modul frissítéséhez nem elég __frissíteni__ azt, hanem __újra kell telepítenie__.</span><span class="sxs-lookup"><span data-stu-id="9d280-149">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="9d280-150">Ez ugyanúgy történik, mint a telepítés, de előfordulhat, hogy hozzá kell adnia a `-Force` argumentumot:</span><span class="sxs-lookup"><span data-stu-id="9d280-150">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="9d280-151">Bár ez felülírhatja a telepített modulokat, még így is előfordulhat hogy maradnak régebbi verziók a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="9d280-151">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="9d280-152">Az Azure PowerShell régebbi verzióinak eltávolításáról [Az Azure PowerShell-modul eltávolítása](uninstall-az-ps.md) című szakaszban olvashat.</span><span class="sxs-lookup"><span data-stu-id="9d280-152">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="9d280-153">Az Azure PowerShell több verziójának használata</span><span class="sxs-lookup"><span data-stu-id="9d280-153">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="9d280-154">Lehetőség van az Azure PowerShell több verziójának telepítésére.</span><span class="sxs-lookup"><span data-stu-id="9d280-154">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="9d280-155">Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:</span><span class="sxs-lookup"><span data-stu-id="9d280-155">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="9d280-156">Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="9d280-156">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="9d280-157">Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` argumentumot:</span><span class="sxs-lookup"><span data-stu-id="9d280-157">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="9d280-158">Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.</span><span class="sxs-lookup"><span data-stu-id="9d280-158">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="9d280-159">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="9d280-159">Provide feedback</span></span>

<span data-ttu-id="9d280-160">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="9d280-160">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="9d280-161">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="9d280-161">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9d280-162">További lépések</span><span class="sxs-lookup"><span data-stu-id="9d280-162">Next Steps</span></span>

<span data-ttu-id="9d280-163">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="9d280-163">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="9d280-164">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="9d280-164">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
