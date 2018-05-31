# <a name="azure-stack-module-130"></a><span data-ttu-id="3a6d0-101">Azure Stack modul 1.3.0</span><span class="sxs-lookup"><span data-stu-id="3a6d0-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="3a6d0-102">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-102">Requirements:</span></span>
<span data-ttu-id="3a6d0-103">A minimális támogatott Azure Stack-verzió a 1804-es.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="3a6d0-104">Megjegyzés: korábbi verzió használata esetén az 1.2.11-es verziót telepítse</span><span class="sxs-lookup"><span data-stu-id="3a6d0-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="3a6d0-105">Ismert problémák:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-105">Known issues:</span></span>

- <span data-ttu-id="3a6d0-106">A Riasztás bezárása művelethez az Azure Stack 1803-as verziója szükséges</span><span class="sxs-lookup"><span data-stu-id="3a6d0-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="3a6d0-107">Bizonyos Storage-parancsmagokhoz az Azure Stack 1804-es verziója szükséges</span><span class="sxs-lookup"><span data-stu-id="3a6d0-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="3a6d0-108">A New-AzsOffer nem teszi lehetővé nyilvános állapotú ajánlatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="3a6d0-109">Utána meg kell hívni a Set-AzsOffer parancsmagot az állapot módosítására.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="3a6d0-110">Az IP-készleteket nem lehet eltávolítani újratelepítés nélkül</span><span class="sxs-lookup"><span data-stu-id="3a6d0-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="3a6d0-111">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="3a6d0-111">Breaking Changes</span></span>
<span data-ttu-id="3a6d0-112">A 1.2.11-es verzióból migrált összes kompatibilitástörő változást itt találja: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="3a6d0-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="3a6d0-113">Telepítés</span><span class="sxs-lookup"><span data-stu-id="3a6d0-113">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="3a6d0-114">Tartalom:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="3a6d0-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="3a6d0-115">Azure Bridge</span></span>
<span data-ttu-id="3a6d0-116">Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="3a6d0-117">Backup</span><span class="sxs-lookup"><span data-stu-id="3a6d0-117">Backup</span></span>
<span data-ttu-id="3a6d0-118">A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="3a6d0-119">Konfigurálhatja a biztonsági másolatok tárolási helyét</span><span class="sxs-lookup"><span data-stu-id="3a6d0-119">Configure where backups are stored</span></span>
- <span data-ttu-id="3a6d0-120">Biztonsági mentéseket hajthat végre</span><span class="sxs-lookup"><span data-stu-id="3a6d0-120">Perform backups</span></span>
- <span data-ttu-id="3a6d0-121">Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat</span><span class="sxs-lookup"><span data-stu-id="3a6d0-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="3a6d0-122">Commerce</span><span class="sxs-lookup"><span data-stu-id="3a6d0-122">Commerce</span></span>
<span data-ttu-id="3a6d0-123">Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="3a6d0-124">Compute</span><span class="sxs-lookup"><span data-stu-id="3a6d0-124">Compute</span></span>
<span data-ttu-id="3a6d0-125">Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platform-rendszerképek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="3a6d0-126">Fabric</span><span class="sxs-lookup"><span data-stu-id="3a6d0-126">Fabric</span></span>
<span data-ttu-id="3a6d0-127">Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="3a6d0-128">Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="3a6d0-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="3a6d0-129">Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez</span><span class="sxs-lookup"><span data-stu-id="3a6d0-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="3a6d0-130">Skálázásiegység-csomópontok javítása</span><span class="sxs-lookup"><span data-stu-id="3a6d0-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="3a6d0-131">Infrastruktúra-szerepkör újraindítása</span><span class="sxs-lookup"><span data-stu-id="3a6d0-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="3a6d0-132">Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="3a6d0-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="3a6d0-133">Új IP-készletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="3a6d0-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="3a6d0-134">Katalógus</span><span class="sxs-lookup"><span data-stu-id="3a6d0-134">Gallery</span></span>
<span data-ttu-id="3a6d0-135">Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="3a6d0-136">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="3a6d0-136">Infrastructure Insights</span></span>
<span data-ttu-id="3a6d0-137">Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="3a6d0-138">Megtekintheti az Azure Stack bélyegző erőforrások állapotát</span><span class="sxs-lookup"><span data-stu-id="3a6d0-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="3a6d0-139">Megtekintheti és kezelheti a riasztásokat</span><span class="sxs-lookup"><span data-stu-id="3a6d0-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="3a6d0-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a6d0-140">KeyVault</span></span>
<span data-ttu-id="3a6d0-141">Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="3a6d0-142">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="3a6d0-142">Network</span></span>
<span data-ttu-id="3a6d0-143">A Network felügyeleti modul előzetes kiadása, amely:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="3a6d0-144">Lehetővé teszi a hálózati kvóták felügyeletét</span><span class="sxs-lookup"><span data-stu-id="3a6d0-144">Management of network quotas</span></span>
- <span data-ttu-id="3a6d0-145">Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését</span><span class="sxs-lookup"><span data-stu-id="3a6d0-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="3a6d0-146">Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="3a6d0-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="3a6d0-147">Storage</span><span class="sxs-lookup"><span data-stu-id="3a6d0-147">Storage</span></span>
<span data-ttu-id="3a6d0-148">Az Azure Stack Storage felügyeleti modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="3a6d0-149">Ebben a kiadásban a következő funkcionalitást biztosítjuk:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="3a6d0-150">Tárhelykvóták kezelése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-150">Manage storage quotas</span></span>
- <span data-ttu-id="3a6d0-151">Törölt tárolási erőforrások szemétgyűjtése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="3a6d0-152">Törölt tárfiókok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="3a6d0-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="3a6d0-153">Tárolók migrálása megosztások közt</span><span class="sxs-lookup"><span data-stu-id="3a6d0-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="3a6d0-154">Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-154">View information about the individual storage components</span></span>
- <span data-ttu-id="3a6d0-155">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="3a6d0-156">Subscription Admin</span><span class="sxs-lookup"><span data-stu-id="3a6d0-156">Subscription Admin</span></span>
<span data-ttu-id="3a6d0-157">Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="3a6d0-158">A modul a következő funkciókat biztosítja a rendszergazdák számára:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="3a6d0-159">Csomagok és ajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-159">Manage plans and offers</span></span>
- <span data-ttu-id="3a6d0-160">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-160">View usage and performance information</span></span>
- <span data-ttu-id="3a6d0-161">Az RBAC kezelése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="3a6d0-162">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="3a6d0-162">Subscription</span></span>
<span data-ttu-id="3a6d0-163">Az Azure Stack Subscription modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="3a6d0-164">A modul a következő funkciókat biztosítja a felhasználók számára:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="3a6d0-165">Előfizetések létrehozása, törlése és frissítése</span><span class="sxs-lookup"><span data-stu-id="3a6d0-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="3a6d0-166">Frissítés</span><span class="sxs-lookup"><span data-stu-id="3a6d0-166">Update</span></span>
<span data-ttu-id="3a6d0-167">Az Azure Stack Update adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="3a6d0-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="3a6d0-168">A modul használatával a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="3a6d0-168">In this module administrators can:</span></span>
- <span data-ttu-id="3a6d0-169">Listázhatja és telepítheti az elérhető frissítéseket</span><span class="sxs-lookup"><span data-stu-id="3a6d0-169">List and install available updates</span></span>
- <span data-ttu-id="3a6d0-170">Folytathatja a megszakított frissítéseket</span><span class="sxs-lookup"><span data-stu-id="3a6d0-170">Resume interrupted updates</span></span>
- <span data-ttu-id="3a6d0-171">Megtekintheti a telepített frissítéseket</span><span class="sxs-lookup"><span data-stu-id="3a6d0-171">View installed updates</span></span>
