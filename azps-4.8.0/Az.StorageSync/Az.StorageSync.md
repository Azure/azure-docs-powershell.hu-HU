---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180754"
---
# <span data-ttu-id="2f1be-101">Az. StorageSync modul</span><span class="sxs-lookup"><span data-stu-id="2f1be-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="2f1be-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f1be-102">Description</span></span>
<span data-ttu-id="2f1be-103">A tárterület-szinkronizálási modulban lévő parancsmagok segítségével kezelheti az Azure-fájlok szinkronizálásához használható műveleteket a PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="2f1be-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="2f1be-104">Az. StorageSync parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2f1be-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="2f1be-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f1be-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="2f1be-106">Ez a parancs felsorolja az összes Felhőbeli végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="2f1be-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="2f1be-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f1be-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="2f1be-108">Ez a parancs felsorolja az összes szinkronizálási csoportot egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="2f1be-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="2f1be-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="2f1be-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="2f1be-110">Ez a parancs felsorolja az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizálási szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="2f1be-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="2f1be-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f1be-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="2f1be-112">Ez a parancs felsorolja az összes kiszolgáló-végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="2f1be-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="2f1be-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2f1be-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="2f1be-114">Ez a parancs felsorolja az összes tárterület-szinkronizálási szolgáltatást az előfizetés/erőforrás csoport adott hatókörén belül.</span><span class="sxs-lookup"><span data-stu-id="2f1be-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="2f1be-115">Meghívó-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="2f1be-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="2f1be-116">Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="2f1be-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="2f1be-117">A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet.</span><span class="sxs-lookup"><span data-stu-id="2f1be-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="2f1be-118">A 10 000-es módosítások maximális száma észlelhető.</span><span class="sxs-lookup"><span data-stu-id="2f1be-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="2f1be-119">Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető, és egy 10 000-módosítási korláton belül.</span><span class="sxs-lookup"><span data-stu-id="2f1be-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="2f1be-120">Meghívó-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="2f1be-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="2f1be-121">Ellenőrzi, hogy milyen kompatibilitási problémákat tapasztal a rendszer és az Azure-fájlok szinkronizálása között.</span><span class="sxs-lookup"><span data-stu-id="2f1be-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="2f1be-122">Meghívó-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="2f1be-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="2f1be-123">Ez a parancs visszahívja az összes többszintű fájlt a helyi merevlemezre.</span><span class="sxs-lookup"><span data-stu-id="2f1be-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="2f1be-124">Új – AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f1be-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="2f1be-125">Ez a parancs Azure-szinkronizálási Felhőbeli végpontot hoz létre a szinkronizálási csoportban.</span><span class="sxs-lookup"><span data-stu-id="2f1be-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="2f1be-126">Új – AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f1be-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="2f1be-127">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="2f1be-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="2f1be-128">Új – AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f1be-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="2f1be-129">Ez a parancs létrehoz egy új kiszolgálói végpontot egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2f1be-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="2f1be-130">Ez a beállítás lehetővé teszi a kiszolgálón megadott elérési út szinkronizálását a fájlok más végpontokkal való szinkronizálásának megkezdéséhez a szinkronizálás csoportban.</span><span class="sxs-lookup"><span data-stu-id="2f1be-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="2f1be-131">Új – AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2f1be-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="2f1be-132">A parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="2f1be-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="2f1be-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2f1be-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="2f1be-134">Ez a parancs egy erőforrás-csoportban tárol egy tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="2f1be-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="2f1be-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="2f1be-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="2f1be-136">Ez a parancs a kiszolgálót egy olyan tárterület-szinkronizáló szolgáltatáshoz regisztrálja, amely bizalmi kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2f1be-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="2f1be-137">Ezt követően a PowerShell vagy az Azure portál segítségével konfigurálhatja a szinkronizálást a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2f1be-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="2f1be-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f1be-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="2f1be-139">Ez a parancs a megadott Felhőbeli végpontot fogja törölni egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="2f1be-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="2f1be-140">Ha nincs legalább egy felhő végpontja, a szinkronizálási csoportban nem lehet más kiszolgálói végpontokat szinkronizálni.</span><span class="sxs-lookup"><span data-stu-id="2f1be-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="2f1be-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2f1be-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="2f1be-142">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="2f1be-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="2f1be-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f1be-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="2f1be-144">Ez a parancs törli a megadott kiszolgálói végpontot.</span><span class="sxs-lookup"><span data-stu-id="2f1be-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="2f1be-145">A szinkronizálás erre a helyre beállítás azonnal megszűnik.</span><span class="sxs-lookup"><span data-stu-id="2f1be-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="2f1be-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2f1be-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="2f1be-147">Ezzel a paranccsal törlődik a megadott tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="2f1be-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="2f1be-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1be-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="2f1be-149">Csak hibaelhárítás esetén használható.</span><span class="sxs-lookup"><span data-stu-id="2f1be-149">Use for troubleshooting only.</span></span> <span data-ttu-id="2f1be-150">Ez a parancs a tárterület-szinkronizálási kiszolgáló tanúsítványát fogja használni a kiszolgáló identitásának a tárterület-szinkronizálási szolgáltatáshoz való leírásához.</span><span class="sxs-lookup"><span data-stu-id="2f1be-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="2f1be-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f1be-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="2f1be-152">Ez a parancs lehetővé teszi a kiszolgálói végpontok állítható paramétereinek módosítását.</span><span class="sxs-lookup"><span data-stu-id="2f1be-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="2f1be-153">Regisztráció törlése – AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="2f1be-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="2f1be-154">Figyelmeztetés: a kiszolgálók regisztrációjának megszüntetése a kiszolgálón futó összes kiszolgáló-végpontok lépcsőzetes törlését eredményezi.</span><span class="sxs-lookup"><span data-stu-id="2f1be-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="2f1be-155">Ez a parancs töröl egy kiszolgálót a tárterület-szinkronizálási szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="2f1be-155">This command will unregister a server from it's storage sync service.</span></span>

