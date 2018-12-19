---
title: Az Azure Stack Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216619"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="ddb05-103">Azure Stack 1.5.0-s modul</span><span class="sxs-lookup"><span data-stu-id="ddb05-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb05-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="ddb05-104">Requirements:</span></span>
<span data-ttu-id="ddb05-105">A minimális támogatott Azure Stack-verzió az 1808-as.</span><span class="sxs-lookup"><span data-stu-id="ddb05-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="ddb05-106">Megjegyzés: Ha korábbi verziót használ, telepítse az 1.4.0-s verziót</span><span class="sxs-lookup"><span data-stu-id="ddb05-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="ddb05-107">Ismert problémák:</span><span class="sxs-lookup"><span data-stu-id="ddb05-107">Known issues:</span></span>

- <span data-ttu-id="ddb05-108">A New-AzsOffer nem teszi lehetővé nyilvános állapotú ajánlatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="ddb05-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="ddb05-109">Utána meg kell hívni a Set-AzsOffer parancsmagot az állapot módosítására.</span><span class="sxs-lookup"><span data-stu-id="ddb05-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="ddb05-110">Az IP-készleteket nem lehet eltávolítani újratelepítés nélkül</span><span class="sxs-lookup"><span data-stu-id="ddb05-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="ddb05-111">Telepítés</span><span class="sxs-lookup"><span data-stu-id="ddb05-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a><span data-ttu-id="ddb05-112">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="ddb05-112">Release Notes</span></span>
* <span data-ttu-id="ddb05-113">Minden Azure Stack Admin-modul függősége nagyobb vagy egyenlő lett az AzureRM.Profile-modulhoz viszonyítva</span><span class="sxs-lookup"><span data-stu-id="ddb05-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="ddb05-114">Beágyazotterőforrás-nevek támogatása minden modulban</span><span class="sxs-lookup"><span data-stu-id="ddb05-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="ddb05-115">Hibajavítás minden olyan modulban, amelyben az ErrorActionPreference felül lett bírálva Stopként</span><span class="sxs-lookup"><span data-stu-id="ddb05-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="ddb05-116">Azs.Compute.Admin modul</span><span class="sxs-lookup"><span data-stu-id="ddb05-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="ddb05-117">Új kvótatulajdonságok hozzáadva a felügyelt lemez támogatásához</span><span class="sxs-lookup"><span data-stu-id="ddb05-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="ddb05-118">Lemezmigráláshoz kapcsolódó parancsmagok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ddb05-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="ddb05-119">További tulajdonságok a platformrendszerkép- és a VM-bővítmény-objektumokban</span><span class="sxs-lookup"><span data-stu-id="ddb05-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="ddb05-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="ddb05-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="ddb05-121">Új parancsmag skálázásiegység-csomópontok hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="ddb05-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="ddb05-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="ddb05-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="ddb05-123">A Set-AzsBackupShare most már egy alias a Set-AzsBackupConfiguration parancsmagra</span><span class="sxs-lookup"><span data-stu-id="ddb05-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ddb05-124">A Get-AzsBackupLocation most már egy alias a Get-AzsBackupConfiguration parancsmagra</span><span class="sxs-lookup"><span data-stu-id="ddb05-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ddb05-125">A Set-AzsBackupConfiguration, a BackupShare paraméter most már egy alias a paraméter-útvonalra</span><span class="sxs-lookup"><span data-stu-id="ddb05-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="ddb05-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="ddb05-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="ddb05-127">A Get-AzsDelegatedProviderOffer, az OfferName paraméter most már egy alias az Offerre</span><span class="sxs-lookup"><span data-stu-id="ddb05-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="ddb05-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="ddb05-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="ddb05-129">A Get-AzsDelegatedProviderOffer, az OfferName paraméter most már egy alias az Offerre</span><span class="sxs-lookup"><span data-stu-id="ddb05-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="ddb05-130">Tartalom:</span><span class="sxs-lookup"><span data-stu-id="ddb05-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ddb05-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="ddb05-131">Azure Bridge</span></span>
<span data-ttu-id="ddb05-132">Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="ddb05-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ddb05-133">Backup</span><span class="sxs-lookup"><span data-stu-id="ddb05-133">Backup</span></span>
<span data-ttu-id="ddb05-134">A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="ddb05-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ddb05-135">Konfigurálhatja a biztonsági másolatok tárolási helyét</span><span class="sxs-lookup"><span data-stu-id="ddb05-135">Configure where backups are stored</span></span>
- <span data-ttu-id="ddb05-136">Biztonsági mentéseket hajthat végre</span><span class="sxs-lookup"><span data-stu-id="ddb05-136">Perform backups</span></span>
- <span data-ttu-id="ddb05-137">Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat</span><span class="sxs-lookup"><span data-stu-id="ddb05-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ddb05-138">Commerce</span><span class="sxs-lookup"><span data-stu-id="ddb05-138">Commerce</span></span>
<span data-ttu-id="ddb05-139">Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.</span><span class="sxs-lookup"><span data-stu-id="ddb05-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ddb05-140">Compute</span><span class="sxs-lookup"><span data-stu-id="ddb05-140">Compute</span></span>
<span data-ttu-id="ddb05-141">Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platformrendszerképek, felügyelt lemezek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="ddb05-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ddb05-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="ddb05-142">Fabric</span></span>
<span data-ttu-id="ddb05-143">Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:</span><span class="sxs-lookup"><span data-stu-id="ddb05-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ddb05-144">Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="ddb05-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ddb05-145">Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez</span><span class="sxs-lookup"><span data-stu-id="ddb05-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ddb05-146">Skálázásiegység-csomópontok javítása</span><span class="sxs-lookup"><span data-stu-id="ddb05-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ddb05-147">Infrastruktúra-szerepkör újraindítása</span><span class="sxs-lookup"><span data-stu-id="ddb05-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ddb05-148">Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="ddb05-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ddb05-149">Új IP-készletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="ddb05-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ddb05-150">Katalógus</span><span class="sxs-lookup"><span data-stu-id="ddb05-150">Gallery</span></span>
<span data-ttu-id="ddb05-151">Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="ddb05-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ddb05-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="ddb05-152">Infrastructure Insights</span></span>
<span data-ttu-id="ddb05-153">Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="ddb05-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ddb05-154">Megtekintheti az Azure Stack bélyegző erőforrások állapotát</span><span class="sxs-lookup"><span data-stu-id="ddb05-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ddb05-155">Megtekintheti és kezelheti a riasztásokat</span><span class="sxs-lookup"><span data-stu-id="ddb05-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ddb05-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ddb05-156">KeyVault</span></span>
<span data-ttu-id="ddb05-157">Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.</span><span class="sxs-lookup"><span data-stu-id="ddb05-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ddb05-158">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="ddb05-158">Network</span></span>
<span data-ttu-id="ddb05-159">A Network felügyeleti modul előzetes kiadása, amely:</span><span class="sxs-lookup"><span data-stu-id="ddb05-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ddb05-160">Lehetővé teszi a hálózati kvóták felügyeletét</span><span class="sxs-lookup"><span data-stu-id="ddb05-160">Management of network quotas</span></span>
- <span data-ttu-id="ddb05-161">Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését</span><span class="sxs-lookup"><span data-stu-id="ddb05-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ddb05-162">Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="ddb05-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ddb05-163">Storage</span><span class="sxs-lookup"><span data-stu-id="ddb05-163">Storage</span></span>
<span data-ttu-id="ddb05-164">Az Azure Stack Storage felügyeleti modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="ddb05-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ddb05-165">Ebben a kiadásban a következő funkcionalitást biztosítjuk:</span><span class="sxs-lookup"><span data-stu-id="ddb05-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ddb05-166">Tárhelykvóták kezelése</span><span class="sxs-lookup"><span data-stu-id="ddb05-166">Manage storage quotas</span></span>
- <span data-ttu-id="ddb05-167">Törölt tárolási erőforrások szemétgyűjtése</span><span class="sxs-lookup"><span data-stu-id="ddb05-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ddb05-168">Törölt tárfiókok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ddb05-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ddb05-169">Tárolók migrálása megosztások közt</span><span class="sxs-lookup"><span data-stu-id="ddb05-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ddb05-170">Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése</span><span class="sxs-lookup"><span data-stu-id="ddb05-170">View information about the individual storage components</span></span>
- <span data-ttu-id="ddb05-171">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="ddb05-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ddb05-172">Subscription Admin</span><span class="sxs-lookup"><span data-stu-id="ddb05-172">Subscription Admin</span></span>
<span data-ttu-id="ddb05-173">Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="ddb05-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ddb05-174">A modul a következő funkciókat biztosítja a rendszergazdák számára:</span><span class="sxs-lookup"><span data-stu-id="ddb05-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ddb05-175">Csomagok és ajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="ddb05-175">Manage plans and offers</span></span>
- <span data-ttu-id="ddb05-176">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="ddb05-176">View usage and performance information</span></span>
- <span data-ttu-id="ddb05-177">Az RBAC kezelése</span><span class="sxs-lookup"><span data-stu-id="ddb05-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ddb05-178">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="ddb05-178">Subscription</span></span>
<span data-ttu-id="ddb05-179">Az Azure Stack Subscription modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="ddb05-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ddb05-180">A modul a következő funkciókat biztosítja a felhasználók számára:</span><span class="sxs-lookup"><span data-stu-id="ddb05-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ddb05-181">Előfizetések létrehozása, törlése és frissítése</span><span class="sxs-lookup"><span data-stu-id="ddb05-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ddb05-182">Frissítés</span><span class="sxs-lookup"><span data-stu-id="ddb05-182">Update</span></span>
<span data-ttu-id="ddb05-183">Az Azure Stack Update adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="ddb05-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ddb05-184">A modul használatával a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="ddb05-184">In this module administrators can:</span></span>
- <span data-ttu-id="ddb05-185">Listázhatja és telepítheti az elérhető frissítéseket</span><span class="sxs-lookup"><span data-stu-id="ddb05-185">List and install available updates</span></span>
- <span data-ttu-id="ddb05-186">Folytathatja a megszakított frissítéseket</span><span class="sxs-lookup"><span data-stu-id="ddb05-186">Resume interrupted updates</span></span>
- <span data-ttu-id="ddb05-187">Megtekintheti a telepített frissítéseket</span><span class="sxs-lookup"><span data-stu-id="ddb05-187">View installed updates</span></span>
