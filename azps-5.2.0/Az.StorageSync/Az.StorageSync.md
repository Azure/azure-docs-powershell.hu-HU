---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325481"
---
# <span data-ttu-id="e2e2a-101">Az.StorageSync modul</span><span class="sxs-lookup"><span data-stu-id="e2e2a-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="e2e2a-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2e2a-102">Description</span></span>
<span data-ttu-id="e2e2a-103">A Tárterület-szinkronizálás modul parancsmagja lehetővé teszi az Azure File Syncre vonatkozó műveletek kezelését a PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="e2e2a-104">Az.StorageSync-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e2e2a-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="e2e2a-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2e2a-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="e2e2a-106">Ez a parancs felsorolja egy adott szinkronizálási csoport összes felhőbeli végpontját.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="e2e2a-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e2e2a-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="e2e2a-108">Ez a parancs felsorolja az adott tár szinkronizálási szolgáltatásában található összes szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="e2e2a-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e2e2a-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="e2e2a-110">Ez a parancs felsorolja az adott tárhelyszinkronizálási szolgáltatáshoz regisztrált összes kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="e2e2a-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2e2a-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="e2e2a-112">Ez a parancs felsorolja egy adott szinkronizálási csoport összes kiszolgálói végpontját.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="e2e2a-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e2e2a-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="e2e2a-114">Ez a parancs felsorolja az adott előfizetési/erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="e2e2a-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="e2e2a-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="e2e2a-116">Ezzel a paranccsal manuálisan elindítható a névterek változásainak észlelése.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="e2e2a-117">Meg lehet célzottan a teljes megosztásra, almappára vagy fájlkészletre.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="e2e2a-118">Legfeljebb 10 000 módosítás észlelhető.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="e2e2a-119">Ha ön ismeri a módosítások hatókörét, a parancs végrehajtását a névtér bizonyos részeire korlátozhatja, így a változások észlelése gyorsan befejeződhet, és a 10 000 módosítási korláton belülre eshet.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="e2e2a-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="e2e2a-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="e2e2a-121">A rendszer és az Azure File Sync közötti esetleges kompatibilitási problémákat ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="e2e2a-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="e2e2a-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="e2e2a-123">Ez a parancs visszahívja az összes réteges fájlt a helyi lemezre.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="e2e2a-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2e2a-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="e2e2a-125">Ez a parancs egy Azure File Sync felhőbeli végpontot hoz létre egy szinkronizálási csoportban.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="e2e2a-126">New-AzstorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e2e2a-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="e2e2a-127">Ez a parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="e2e2a-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2e2a-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="e2e2a-129">Ez a parancs új kiszolgáló végpontot hoz létre egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="e2e2a-130">Ez lehetővé teszi, hogy a kiszolgálón megadott elérési út elindítsa a fájlok szinkronizálását a szinkronizálási csoport más végpontjaival.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="e2e2a-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e2e2a-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="e2e2a-132">Ez a parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="e2e2a-133">Set-AzstorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e2e2a-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="e2e2a-134">Ez a parancs egy tárterület-szinkronizálási szolgáltatást állít be egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="e2e2a-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e2e2a-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="e2e2a-136">Ez a parancs regisztrál egy kiszolgálót egy tárterület-szinkronizálási szolgáltatásban, amely megbízhatósági kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="e2e2a-137">Ezután a PowerShell vagy az Azure Portal segítségével konfigurálhatja a szinkronizálást ezen a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="e2e2a-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2e2a-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="e2e2a-139">Ez a parancs törli a megadott felhőbeli végpontot egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="e2e2a-140">Legalább egy felhőbeli végpont nélkül a szinkronizálási csoport egyetlen másik kiszolgálói végpontja sem tud szinkronizálni.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="e2e2a-141">Remove-AzstorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e2e2a-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="e2e2a-142">Ez a parancs törli a megadott szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="e2e2a-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2e2a-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="e2e2a-144">Ez a parancs törli a megadott kiszolgálóvégpontot.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="e2e2a-145">Az erre a helyre való szinkronizálás azonnal leáll.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="e2e2a-146">Remove-AzstorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e2e2a-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="e2e2a-147">Ez a parancs törli a megadott tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="e2e2a-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="e2e2a-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="e2e2a-149">Csak hibaelhárításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-149">Use for troubleshooting only.</span></span> <span data-ttu-id="e2e2a-150">Ez a parancs roll the storage sync server certificate used to describe the server identity to the storage sync service.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="e2e2a-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e2e2a-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="e2e2a-152">Ez a parancs lehetővé teszi a kiszolgáló végpontjának módosítható paramétereinek módosításait.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="e2e2a-153">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e2e2a-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="e2e2a-154">Figyelmeztetés: A kiszolgáló regisztrációjának törlése kaszkádolt törlést eredményez a kiszolgáló összes kiszolgálói végpontjának.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="e2e2a-155">Ez a parancs a kiszolgáló tárhelyszinkronizálási szolgáltatásában való regisztrációját is visszaveszi.</span><span class="sxs-lookup"><span data-stu-id="e2e2a-155">This command will unregister a server from it's storage sync service.</span></span>

