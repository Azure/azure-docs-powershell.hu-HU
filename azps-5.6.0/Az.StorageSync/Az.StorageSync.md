---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929202"
---
# <span data-ttu-id="b988c-101">Az.StorageSync modul</span><span class="sxs-lookup"><span data-stu-id="b988c-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="b988c-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="b988c-102">Description</span></span>
<span data-ttu-id="b988c-103">A Tárterület-szinkronizálás modul parancsmagja lehetővé teszi az Azure File Syncre vonatkozó műveletek kezelését a PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="b988c-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="b988c-104">Az.StorageSync-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b988c-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="b988c-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b988c-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="b988c-106">Ez a parancs felsorolja egy adott szinkronizálási csoport összes felhőbeli végpontját.</span><span class="sxs-lookup"><span data-stu-id="b988c-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="b988c-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b988c-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="b988c-108">Ez a parancs felsorolja az adott tár szinkronizálási szolgáltatásában található összes szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="b988c-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="b988c-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b988c-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="b988c-110">Ez a parancs felsorolja az adott tárhelyszinkronizálási szolgáltatáshoz regisztrált összes kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="b988c-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="b988c-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b988c-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b988c-112">Ez a parancs felsorolja egy adott szinkronizálási csoport összes kiszolgálói végpontját.</span><span class="sxs-lookup"><span data-stu-id="b988c-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="b988c-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b988c-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="b988c-114">Ez a parancs felsorolja az adott előfizetési/erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b988c-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="b988c-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="b988c-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="b988c-116">Ezzel a paranccsal manuálisan elindíthatja a névterek változásainak észlelését.</span><span class="sxs-lookup"><span data-stu-id="b988c-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="b988c-117">Meg lehet célzottan a teljes megosztásra, almappára vagy fájlkészletre.</span><span class="sxs-lookup"><span data-stu-id="b988c-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="b988c-118">Legfeljebb 10 000 módosítás észlelhető.</span><span class="sxs-lookup"><span data-stu-id="b988c-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="b988c-119">Ha ön ismeri a módosítások hatókörét, a parancs végrehajtását a névtér bizonyos részeire korlátozhatja, így a változások észlelése gyorsan befejeződhet, és a 10 000 módosítási korláton belülre eshet.</span><span class="sxs-lookup"><span data-stu-id="b988c-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="b988c-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="b988c-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="b988c-121">A rendszer és az Azure File Sync közötti esetleges kompatibilitási problémákat ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="b988c-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="b988c-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="b988c-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="b988c-123">Ez a parancs visszahívja az összes réteges fájlt a helyi lemezre.</span><span class="sxs-lookup"><span data-stu-id="b988c-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="b988c-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b988c-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="b988c-125">Ez a parancs egy Azure File Sync felhőbeli végpontot hoz létre egy szinkronizálási csoportban.</span><span class="sxs-lookup"><span data-stu-id="b988c-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="b988c-126">New-AzstorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b988c-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="b988c-127">Ez a parancs egy új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="b988c-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="b988c-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b988c-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b988c-129">Ez a parancs új kiszolgáló végpontot hoz létre egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="b988c-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="b988c-130">Ez lehetővé teszi, hogy a kiszolgálón megadott elérési út elindítsa a fájlok szinkronizálását a szinkronizálási csoport más végpontjaival.</span><span class="sxs-lookup"><span data-stu-id="b988c-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="b988c-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b988c-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="b988c-132">Ez a parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="b988c-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="b988c-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b988c-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="b988c-134">Ez a parancs egy tárterület-szinkronizálási szolgáltatást állít be egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="b988c-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="b988c-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b988c-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="b988c-136">Ez a parancs regisztrál egy kiszolgálót egy tárterület-szinkronizálási szolgáltatásban, amely megbízhatósági kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b988c-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="b988c-137">Ezután a PowerShell vagy az Azure Portal segítségével konfigurálhatja a szinkronizálást ezen a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="b988c-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="b988c-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b988c-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="b988c-139">Ez a parancs törli a megadott felhőbeli végpontot egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="b988c-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="b988c-140">Legalább egy felhőbeli végpont nélkül a szinkronizálási csoport egyetlen másik kiszolgálói végpontja sem tud szinkronizálni.</span><span class="sxs-lookup"><span data-stu-id="b988c-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="b988c-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b988c-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="b988c-142">Ez a parancs törli a megadott szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="b988c-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="b988c-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b988c-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b988c-144">Ez a parancs törli a megadott kiszolgálói végpontot.</span><span class="sxs-lookup"><span data-stu-id="b988c-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="b988c-145">Az erre a helyre való szinkronizálás azonnal leáll.</span><span class="sxs-lookup"><span data-stu-id="b988c-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="b988c-146">Remove-AzstorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b988c-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="b988c-147">Ez a parancs törli a megadott tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b988c-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="b988c-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="b988c-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="b988c-149">Csak hibaelhárításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="b988c-149">Use for troubleshooting only.</span></span> <span data-ttu-id="b988c-150">Ez a parancs roll the storage sync server certificate used to describe the server identity to the storage sync service.</span><span class="sxs-lookup"><span data-stu-id="b988c-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="b988c-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b988c-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b988c-152">Ez a parancs lehetővé teszi a kiszolgáló végpontjának módosítható paramétereinek módosításait.</span><span class="sxs-lookup"><span data-stu-id="b988c-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="b988c-153">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b988c-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="b988c-154">Figyelmeztetés: A kiszolgáló regisztrációjának törlése kaszkádolt törlést eredményez a kiszolgáló összes kiszolgálói végpontjának.</span><span class="sxs-lookup"><span data-stu-id="b988c-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="b988c-155">Ez a parancs a kiszolgáló tárhelyszinkronizálási szolgáltatásában való regisztrációját is visszaveszi.</span><span class="sxs-lookup"><span data-stu-id="b988c-155">This command will unregister a server from it's storage sync service.</span></span>

