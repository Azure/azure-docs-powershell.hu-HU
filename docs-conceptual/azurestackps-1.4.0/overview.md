# <a name="azure-stack-module-140"></a><span data-ttu-id="d56b0-101">Azure Stack modul 1.4.0</span><span class="sxs-lookup"><span data-stu-id="d56b0-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="d56b0-102">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="d56b0-102">Requirements:</span></span>
<span data-ttu-id="d56b0-103">A minimális támogatott Azure Stack-verzió a 1804-es.</span><span class="sxs-lookup"><span data-stu-id="d56b0-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="d56b0-104">Megjegyzés: korábbi verzió használata esetén az 1.2.11-es verziót telepítse</span><span class="sxs-lookup"><span data-stu-id="d56b0-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="d56b0-105">Ismert problémák:</span><span class="sxs-lookup"><span data-stu-id="d56b0-105">Known issues:</span></span>

- <span data-ttu-id="d56b0-106">A Riasztás bezárása művelethez az Azure Stack 1803-as verziója szükséges</span><span class="sxs-lookup"><span data-stu-id="d56b0-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="d56b0-107">A New-AzsOffer nem teszi lehetővé nyilvános állapotú ajánlatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="d56b0-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="d56b0-108">Utána meg kell hívni a Set-AzsOffer parancsmagot az állapot módosítására.</span><span class="sxs-lookup"><span data-stu-id="d56b0-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="d56b0-109">Az IP-készleteket nem lehet eltávolítani újratelepítés nélkül</span><span class="sxs-lookup"><span data-stu-id="d56b0-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="d56b0-110">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="d56b0-110">Breaking Changes</span></span>
<span data-ttu-id="d56b0-111">Nincsenek kompatibilitástörő változások az 1.3.0-s verzióhoz képest.</span><span class="sxs-lookup"><span data-stu-id="d56b0-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="d56b0-112">A 1.2.11-es verzióból migrált összes kompatibilitástörő változást itt találja: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="d56b0-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="d56b0-113">Telepítés</span><span class="sxs-lookup"><span data-stu-id="d56b0-113">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="d56b0-114">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="d56b0-114">Release Notes</span></span>
    * <span data-ttu-id="d56b0-115">Az Azurestack 1.4.0-s verzióban nincsenek kompatibilitástörő változások a korábbi, 1.3.0-s kiadáshoz képest.</span><span class="sxs-lookup"><span data-stu-id="d56b0-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="d56b0-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="d56b0-117">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="d56b0-119">A Set-AzsBackupShare parancsmagban a következő új paraméterek érhetőek el: BackupFrequencyInHours, IsBackupSchedulerEnabled és BackupRetentionPeriodInDays.</span><span class="sxs-lookup"><span data-stu-id="d56b0-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="d56b0-120">Az új New-EncyptionKeyBase64 parancsmag megkönnyíti titkosítási kulcsok készítését.</span><span class="sxs-lookup"><span data-stu-id="d56b0-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="d56b0-121">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="d56b0-123">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="d56b0-125">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="d56b0-126">Az új Add-AzsScaleUnitNode parancsmaggal az adminisztrátorok új skálázásiegység-csomópontokat adhatnak az azurestack bélyegzőhöz.</span><span class="sxs-lookup"><span data-stu-id="d56b0-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="d56b0-127">Az új parancsmag és a New-AzsScaleUnitNodeObject segítségével egyszerűbb létrehozni skálázásiegység-paraméter objektumokat.</span><span class="sxs-lookup"><span data-stu-id="d56b0-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="d56b0-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="d56b0-129">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="d56b0-131">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="d56b0-133">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="d56b0-135">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="d56b0-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="d56b0-137">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d56b0-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="d56b0-139">Az új Move-AzsSubscription parancsmaggal az előfizetések áthelyezhetőek a delegált szolgáltatói ajánlatok között.</span><span class="sxs-lookup"><span data-stu-id="d56b0-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="d56b0-140">Az új Test-AzsMoveSubscription parancsmaggal ellenőrizhető, hogy a felhasználói előfizetések áthelyezhetőek-e a delegált szolgáltatói ajánlatok között.</span><span class="sxs-lookup"><span data-stu-id="d56b0-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="d56b0-141">Ki lett javítva az a hiba, amely miatt többlapos eredmények esetén a rendszer csak egyetlen lapot jelenített meg eredményként.</span><span class="sxs-lookup"><span data-stu-id="d56b0-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="d56b0-142">Tartalom:</span><span class="sxs-lookup"><span data-stu-id="d56b0-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="d56b0-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="d56b0-143">Azure Bridge</span></span>
<span data-ttu-id="d56b0-144">Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="d56b0-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="d56b0-145">Backup</span><span class="sxs-lookup"><span data-stu-id="d56b0-145">Backup</span></span>
<span data-ttu-id="d56b0-146">A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="d56b0-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="d56b0-147">Konfigurálhatja a biztonsági másolatok tárolási helyét</span><span class="sxs-lookup"><span data-stu-id="d56b0-147">Configure where backups are stored</span></span>
- <span data-ttu-id="d56b0-148">Biztonsági mentéseket hajthat végre</span><span class="sxs-lookup"><span data-stu-id="d56b0-148">Perform backups</span></span>
- <span data-ttu-id="d56b0-149">Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat</span><span class="sxs-lookup"><span data-stu-id="d56b0-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="d56b0-150">Commerce</span><span class="sxs-lookup"><span data-stu-id="d56b0-150">Commerce</span></span>
<span data-ttu-id="d56b0-151">Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.</span><span class="sxs-lookup"><span data-stu-id="d56b0-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="d56b0-152">Compute</span><span class="sxs-lookup"><span data-stu-id="d56b0-152">Compute</span></span>
<span data-ttu-id="d56b0-153">Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platform-rendszerképek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="d56b0-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="d56b0-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="d56b0-154">Fabric</span></span>
<span data-ttu-id="d56b0-155">Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:</span><span class="sxs-lookup"><span data-stu-id="d56b0-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="d56b0-156">Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="d56b0-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="d56b0-157">Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez</span><span class="sxs-lookup"><span data-stu-id="d56b0-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="d56b0-158">Skálázásiegység-csomópontok javítása</span><span class="sxs-lookup"><span data-stu-id="d56b0-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="d56b0-159">Infrastruktúra-szerepkör újraindítása</span><span class="sxs-lookup"><span data-stu-id="d56b0-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="d56b0-160">Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="d56b0-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="d56b0-161">Új IP-készletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="d56b0-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="d56b0-162">Katalógus</span><span class="sxs-lookup"><span data-stu-id="d56b0-162">Gallery</span></span>
<span data-ttu-id="d56b0-163">Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="d56b0-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="d56b0-164">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="d56b0-164">Infrastructure Insights</span></span>
<span data-ttu-id="d56b0-165">Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="d56b0-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="d56b0-166">Megtekintheti az Azure Stack bélyegző erőforrások állapotát</span><span class="sxs-lookup"><span data-stu-id="d56b0-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="d56b0-167">Megtekintheti és kezelheti a riasztásokat</span><span class="sxs-lookup"><span data-stu-id="d56b0-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="d56b0-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d56b0-168">KeyVault</span></span>
<span data-ttu-id="d56b0-169">Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.</span><span class="sxs-lookup"><span data-stu-id="d56b0-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="d56b0-170">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="d56b0-170">Network</span></span>
<span data-ttu-id="d56b0-171">A Network felügyeleti modul előzetes kiadása, amely:</span><span class="sxs-lookup"><span data-stu-id="d56b0-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="d56b0-172">Lehetővé teszi a hálózati kvóták felügyeletét</span><span class="sxs-lookup"><span data-stu-id="d56b0-172">Management of network quotas</span></span>
- <span data-ttu-id="d56b0-173">Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését</span><span class="sxs-lookup"><span data-stu-id="d56b0-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="d56b0-174">Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="d56b0-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="d56b0-175">Storage</span><span class="sxs-lookup"><span data-stu-id="d56b0-175">Storage</span></span>
<span data-ttu-id="d56b0-176">Az Azure Stack Storage felügyeleti modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="d56b0-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="d56b0-177">Ebben a kiadásban a következő funkcionalitást biztosítjuk:</span><span class="sxs-lookup"><span data-stu-id="d56b0-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="d56b0-178">Tárhelykvóták kezelése</span><span class="sxs-lookup"><span data-stu-id="d56b0-178">Manage storage quotas</span></span>
- <span data-ttu-id="d56b0-179">Törölt tárolási erőforrások szemétgyűjtése</span><span class="sxs-lookup"><span data-stu-id="d56b0-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="d56b0-180">Törölt tárfiókok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="d56b0-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="d56b0-181">Tárolók migrálása megosztások közt</span><span class="sxs-lookup"><span data-stu-id="d56b0-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="d56b0-182">Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d56b0-182">View information about the individual storage components</span></span>
- <span data-ttu-id="d56b0-183">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="d56b0-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="d56b0-184">Subscription Admin</span><span class="sxs-lookup"><span data-stu-id="d56b0-184">Subscription Admin</span></span>
<span data-ttu-id="d56b0-185">Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="d56b0-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="d56b0-186">A modul a következő funkciókat biztosítja a rendszergazdák számára:</span><span class="sxs-lookup"><span data-stu-id="d56b0-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="d56b0-187">Csomagok és ajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="d56b0-187">Manage plans and offers</span></span>
- <span data-ttu-id="d56b0-188">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="d56b0-188">View usage and performance information</span></span>
- <span data-ttu-id="d56b0-189">Az RBAC kezelése</span><span class="sxs-lookup"><span data-stu-id="d56b0-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="d56b0-190">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="d56b0-190">Subscription</span></span>
<span data-ttu-id="d56b0-191">Az Azure Stack Subscription modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="d56b0-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="d56b0-192">A modul a következő funkciókat biztosítja a felhasználók számára:</span><span class="sxs-lookup"><span data-stu-id="d56b0-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="d56b0-193">Előfizetések létrehozása, törlése és frissítése</span><span class="sxs-lookup"><span data-stu-id="d56b0-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="d56b0-194">Frissítés</span><span class="sxs-lookup"><span data-stu-id="d56b0-194">Update</span></span>
<span data-ttu-id="d56b0-195">Az Azure Stack Update adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="d56b0-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="d56b0-196">A modul használatával a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="d56b0-196">In this module administrators can:</span></span>
- <span data-ttu-id="d56b0-197">Listázhatja és telepítheti az elérhető frissítéseket</span><span class="sxs-lookup"><span data-stu-id="d56b0-197">List and install available updates</span></span>
- <span data-ttu-id="d56b0-198">Folytathatja a megszakított frissítéseket</span><span class="sxs-lookup"><span data-stu-id="d56b0-198">Resume interrupted updates</span></span>
- <span data-ttu-id="d56b0-199">Megtekintheti a telepített frissítéseket</span><span class="sxs-lookup"><span data-stu-id="d56b0-199">View installed updates</span></span>
