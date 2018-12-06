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
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826648"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="c0788-103">Azure Stack modul 1.4.0</span><span class="sxs-lookup"><span data-stu-id="c0788-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="c0788-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="c0788-104">Requirements:</span></span>
<span data-ttu-id="c0788-105">A minimális támogatott Azure Stack-verzió a 1804-es.</span><span class="sxs-lookup"><span data-stu-id="c0788-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="c0788-106">Megjegyzés: korábbi verzió használata esetén az 1.2.11-es verziót telepítse</span><span class="sxs-lookup"><span data-stu-id="c0788-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="c0788-107">Ismert problémák:</span><span class="sxs-lookup"><span data-stu-id="c0788-107">Known issues:</span></span>

- <span data-ttu-id="c0788-108">A Riasztás bezárása művelethez az Azure Stack 1803-as verziója szükséges</span><span class="sxs-lookup"><span data-stu-id="c0788-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="c0788-109">A New-AzsOffer nem teszi lehetővé nyilvános állapotú ajánlatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="c0788-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="c0788-110">Utána meg kell hívni a Set-AzsOffer parancsmagot az állapot módosítására.</span><span class="sxs-lookup"><span data-stu-id="c0788-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="c0788-111">Az IP-készleteket nem lehet eltávolítani újratelepítés nélkül</span><span class="sxs-lookup"><span data-stu-id="c0788-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="c0788-112">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="c0788-112">Breaking Changes</span></span>
<span data-ttu-id="c0788-113">Nincsenek kompatibilitástörő változások az 1.3.0-s verzióhoz képest.</span><span class="sxs-lookup"><span data-stu-id="c0788-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="c0788-114">A 1.2.11-es verzióból migrált összes kompatibilitástörő változást itt találja: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="c0788-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="c0788-115">Telepítés</span><span class="sxs-lookup"><span data-stu-id="c0788-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="c0788-116">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="c0788-116">Release Notes</span></span>
    * <span data-ttu-id="c0788-117">Az Azurestack 1.4.0-s verzióban nincsenek kompatibilitástörő változások a korábbi, 1.3.0-s kiadáshoz képest.</span><span class="sxs-lookup"><span data-stu-id="c0788-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="c0788-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="c0788-119">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="c0788-121">A Set-AzsBackupShare parancsmagban a következő új paraméterek érhetőek el: BackupFrequencyInHours, IsBackupSchedulerEnabled és BackupRetentionPeriodInDays.</span><span class="sxs-lookup"><span data-stu-id="c0788-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="c0788-122">Az új New-EncyptionKeyBase64 parancsmag megkönnyíti titkosítási kulcsok készítését.</span><span class="sxs-lookup"><span data-stu-id="c0788-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="c0788-123">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="c0788-125">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="c0788-127">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="c0788-128">Az új Add-AzsScaleUnitNode parancsmaggal az adminisztrátorok új skálázásiegység-csomópontokat adhatnak az azurestack bélyegzőhöz.</span><span class="sxs-lookup"><span data-stu-id="c0788-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="c0788-129">Az új parancsmag és a New-AzsScaleUnitNodeObject segítségével egyszerűbb létrehozni skálázásiegység-paraméter objektumokat.</span><span class="sxs-lookup"><span data-stu-id="c0788-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="c0788-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="c0788-131">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="c0788-133">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="c0788-135">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="c0788-137">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="c0788-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="c0788-139">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="c0788-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="c0788-141">Az új Move-AzsSubscription parancsmaggal az előfizetések áthelyezhetőek a delegált szolgáltatói ajánlatok között.</span><span class="sxs-lookup"><span data-stu-id="c0788-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="c0788-142">Az új Test-AzsMoveSubscription parancsmaggal ellenőrizhető, hogy a felhasználói előfizetések áthelyezhetőek-e a delegált szolgáltatói ajánlatok között.</span><span class="sxs-lookup"><span data-stu-id="c0788-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="c0788-143">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="c0788-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="c0788-144">Tartalom:</span><span class="sxs-lookup"><span data-stu-id="c0788-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="c0788-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="c0788-145">Azure Bridge</span></span>
<span data-ttu-id="c0788-146">Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="c0788-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="c0788-147">Backup</span><span class="sxs-lookup"><span data-stu-id="c0788-147">Backup</span></span>
<span data-ttu-id="c0788-148">A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="c0788-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="c0788-149">Konfigurálhatja a biztonsági másolatok tárolási helyét</span><span class="sxs-lookup"><span data-stu-id="c0788-149">Configure where backups are stored</span></span>
- <span data-ttu-id="c0788-150">Biztonsági mentéseket hajthat végre</span><span class="sxs-lookup"><span data-stu-id="c0788-150">Perform backups</span></span>
- <span data-ttu-id="c0788-151">Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat</span><span class="sxs-lookup"><span data-stu-id="c0788-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="c0788-152">Commerce</span><span class="sxs-lookup"><span data-stu-id="c0788-152">Commerce</span></span>
<span data-ttu-id="c0788-153">Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.</span><span class="sxs-lookup"><span data-stu-id="c0788-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="c0788-154">Compute</span><span class="sxs-lookup"><span data-stu-id="c0788-154">Compute</span></span>
<span data-ttu-id="c0788-155">Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platform-rendszerképek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="c0788-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="c0788-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="c0788-156">Fabric</span></span>
<span data-ttu-id="c0788-157">Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:</span><span class="sxs-lookup"><span data-stu-id="c0788-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="c0788-158">Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="c0788-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="c0788-159">Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez</span><span class="sxs-lookup"><span data-stu-id="c0788-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="c0788-160">Skálázásiegység-csomópontok javítása</span><span class="sxs-lookup"><span data-stu-id="c0788-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="c0788-161">Infrastruktúra-szerepkör újraindítása</span><span class="sxs-lookup"><span data-stu-id="c0788-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="c0788-162">Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="c0788-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="c0788-163">Új IP-készletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0788-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="c0788-164">Katalógus</span><span class="sxs-lookup"><span data-stu-id="c0788-164">Gallery</span></span>
<span data-ttu-id="c0788-165">Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="c0788-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="c0788-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="c0788-166">Infrastructure Insights</span></span>
<span data-ttu-id="c0788-167">Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="c0788-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="c0788-168">Megtekintheti az Azure Stack bélyegző erőforrások állapotát</span><span class="sxs-lookup"><span data-stu-id="c0788-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="c0788-169">Megtekintheti és kezelheti a riasztásokat</span><span class="sxs-lookup"><span data-stu-id="c0788-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="c0788-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c0788-170">KeyVault</span></span>
<span data-ttu-id="c0788-171">Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.</span><span class="sxs-lookup"><span data-stu-id="c0788-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="c0788-172">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="c0788-172">Network</span></span>
<span data-ttu-id="c0788-173">A Network felügyeleti modul előzetes kiadása, amely:</span><span class="sxs-lookup"><span data-stu-id="c0788-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="c0788-174">Lehetővé teszi a hálózati kvóták felügyeletét</span><span class="sxs-lookup"><span data-stu-id="c0788-174">Management of network quotas</span></span>
- <span data-ttu-id="c0788-175">Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését</span><span class="sxs-lookup"><span data-stu-id="c0788-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="c0788-176">Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="c0788-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="c0788-177">Storage</span><span class="sxs-lookup"><span data-stu-id="c0788-177">Storage</span></span>
<span data-ttu-id="c0788-178">Az Azure Stack Storage felügyeleti modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="c0788-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="c0788-179">Ebben a kiadásban a következő funkcionalitást biztosítjuk:</span><span class="sxs-lookup"><span data-stu-id="c0788-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="c0788-180">Tárhelykvóták kezelése</span><span class="sxs-lookup"><span data-stu-id="c0788-180">Manage storage quotas</span></span>
- <span data-ttu-id="c0788-181">Törölt tárolási erőforrások szemétgyűjtése</span><span class="sxs-lookup"><span data-stu-id="c0788-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="c0788-182">Törölt tárfiókok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="c0788-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="c0788-183">Tárolók migrálása megosztások közt</span><span class="sxs-lookup"><span data-stu-id="c0788-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="c0788-184">Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése</span><span class="sxs-lookup"><span data-stu-id="c0788-184">View information about the individual storage components</span></span>
- <span data-ttu-id="c0788-185">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="c0788-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="c0788-186">Subscription Admin</span><span class="sxs-lookup"><span data-stu-id="c0788-186">Subscription Admin</span></span>
<span data-ttu-id="c0788-187">Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="c0788-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="c0788-188">A modul a következő funkciókat biztosítja a rendszergazdák számára:</span><span class="sxs-lookup"><span data-stu-id="c0788-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="c0788-189">Csomagok és ajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="c0788-189">Manage plans and offers</span></span>
- <span data-ttu-id="c0788-190">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="c0788-190">View usage and performance information</span></span>
- <span data-ttu-id="c0788-191">Az RBAC kezelése</span><span class="sxs-lookup"><span data-stu-id="c0788-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="c0788-192">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0788-192">Subscription</span></span>
<span data-ttu-id="c0788-193">Az Azure Stack Subscription modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="c0788-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="c0788-194">A modul a következő funkciókat biztosítja a felhasználók számára:</span><span class="sxs-lookup"><span data-stu-id="c0788-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="c0788-195">Előfizetések létrehozása, törlése és frissítése</span><span class="sxs-lookup"><span data-stu-id="c0788-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="c0788-196">Frissítés</span><span class="sxs-lookup"><span data-stu-id="c0788-196">Update</span></span>
<span data-ttu-id="c0788-197">Az Azure Stack Update adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="c0788-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="c0788-198">A modul használatával a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="c0788-198">In this module administrators can:</span></span>
- <span data-ttu-id="c0788-199">Listázhatja és telepítheti az elérhető frissítéseket</span><span class="sxs-lookup"><span data-stu-id="c0788-199">List and install available updates</span></span>
- <span data-ttu-id="c0788-200">Folytathatja a megszakított frissítéseket</span><span class="sxs-lookup"><span data-stu-id="c0788-200">Resume interrupted updates</span></span>
- <span data-ttu-id="c0788-201">Megtekintheti a telepített frissítéseket</span><span class="sxs-lookup"><span data-stu-id="c0788-201">View installed updates</span></span>
