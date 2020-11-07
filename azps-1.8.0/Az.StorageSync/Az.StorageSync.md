---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 1ab1690d3c5fccca2994abc4958f3cf7e6a4e52d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657820"
---
# <span data-ttu-id="91a54-101">Az. StorageSync modul</span><span class="sxs-lookup"><span data-stu-id="91a54-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="91a54-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="91a54-102">Description</span></span>
<span data-ttu-id="91a54-103">A tárterület-szinkronizálási modulban lévő parancsmagok segítségével kezelheti az Azure-fájlok szinkronizálásához használható műveleteket a PowerShellben.</span><span class="sxs-lookup"><span data-stu-id="91a54-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="91a54-104">Az. StorageSync parancsmagok</span><span class="sxs-lookup"><span data-stu-id="91a54-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="91a54-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="91a54-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="91a54-106">Ez a parancs felsorolja az összes Felhőbeli végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="91a54-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="91a54-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91a54-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="91a54-108">Ez a parancs felsorolja az összes szinkronizálási csoportot egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="91a54-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="91a54-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="91a54-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="91a54-110">Ez a parancs felsorolja az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizálási szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="91a54-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="91a54-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91a54-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="91a54-112">Ez a parancs felsorolja az összes kiszolgáló-végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="91a54-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="91a54-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="91a54-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="91a54-114">Ez a parancs felsorolja az összes tárterület-szinkronizálási szolgáltatást az előfizetés/erőforrás csoport adott hatókörén belül.</span><span class="sxs-lookup"><span data-stu-id="91a54-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="91a54-115">Meghívó-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="91a54-115">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="91a54-116">Ellenőrzi, hogy milyen kompatibilitási problémákat tapasztal a rendszer és az Azure-fájlok szinkronizálása között.</span><span class="sxs-lookup"><span data-stu-id="91a54-116">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="91a54-117">Meghívó-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="91a54-117">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="91a54-118">Ez a parancs visszahívja az összes többszintű fájlt a helyi merevlemezre.</span><span class="sxs-lookup"><span data-stu-id="91a54-118">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="91a54-119">Új – AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="91a54-119">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="91a54-120">Ez a parancs Azure-szinkronizálási Felhőbeli végpontot hoz létre a szinkronizálási csoportban.</span><span class="sxs-lookup"><span data-stu-id="91a54-120">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="91a54-121">Új – AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91a54-121">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="91a54-122">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="91a54-122">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="91a54-123">Új – AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91a54-123">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="91a54-124">Ez a parancs létrehoz egy új kiszolgálói végpontot egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="91a54-124">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="91a54-125">Ez a beállítás lehetővé teszi a kiszolgálón megadott elérési út szinkronizálását a fájlok más végpontokkal való szinkronizálásának megkezdéséhez a szinkronizálás csoportban.</span><span class="sxs-lookup"><span data-stu-id="91a54-125">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="91a54-126">Új – AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="91a54-126">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="91a54-127">A parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="91a54-127">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="91a54-128">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="91a54-128">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="91a54-129">Ez a parancs a kiszolgálót egy olyan tárterület-szinkronizáló szolgáltatáshoz regisztrálja, amely bizalmi kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="91a54-129">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="91a54-130">Ezt követően a PowerShell vagy az Azure portál segítségével konfigurálhatja a szinkronizálást a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="91a54-130">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="91a54-131">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="91a54-131">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="91a54-132">Ez a parancs a megadott Felhőbeli végpontot fogja törölni egy szinkronizálási csoportból.</span><span class="sxs-lookup"><span data-stu-id="91a54-132">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="91a54-133">Ha nincs legalább egy felhő végpontja, a szinkronizálási csoportban nem lehet más kiszolgálói végpontokat szinkronizálni.</span><span class="sxs-lookup"><span data-stu-id="91a54-133">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="91a54-134">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91a54-134">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="91a54-135">Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.</span><span class="sxs-lookup"><span data-stu-id="91a54-135">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="91a54-136">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91a54-136">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="91a54-137">Ez a parancs törli a megadott kiszolgálói végpontot.</span><span class="sxs-lookup"><span data-stu-id="91a54-137">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="91a54-138">A szinkronizálás erre a helyre beállítás azonnal megszűnik.</span><span class="sxs-lookup"><span data-stu-id="91a54-138">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="91a54-139">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="91a54-139">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="91a54-140">Ezzel a paranccsal törlődik a megadott tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="91a54-140">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="91a54-141">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="91a54-141">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="91a54-142">Csak hibaelhárítás esetén használható.</span><span class="sxs-lookup"><span data-stu-id="91a54-142">Use for troubleshooting only.</span></span> <span data-ttu-id="91a54-143">Ez a parancs a tárterület-szinkronizálási kiszolgáló tanúsítványát fogja használni a kiszolgáló identitásának a tárterület-szinkronizálási szolgáltatáshoz való leírásához.</span><span class="sxs-lookup"><span data-stu-id="91a54-143">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="91a54-144">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91a54-144">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="91a54-145">Ez a parancs lehetővé teszi a kiszolgálói végpontok állítható paramétereinek módosítását.</span><span class="sxs-lookup"><span data-stu-id="91a54-145">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="91a54-146">Regisztráció törlése – AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="91a54-146">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="91a54-147">Figyelmeztetés: a kiszolgálók regisztrációjának megszüntetése a kiszolgálón futó összes kiszolgáló-végpontok lépcsőzetes törlését eredményezi.</span><span class="sxs-lookup"><span data-stu-id="91a54-147">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="91a54-148">Ez a parancs töröl egy kiszolgálót a tárterület-szinkronizálási szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="91a54-148">This command will unregister a server from it's storage sync service.</span></span>