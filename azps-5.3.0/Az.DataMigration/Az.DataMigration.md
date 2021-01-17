---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465779"
---
# <span data-ttu-id="a4d89-101">Az.DataMigration modul</span><span class="sxs-lookup"><span data-stu-id="a4d89-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="a4d89-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4d89-102">Description</span></span>
<span data-ttu-id="a4d89-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="a4d89-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="a4d89-104">Az.DataMigration parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a4d89-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="a4d89-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="a4d89-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="a4d89-106">Beolvassa egy Azure-adatbázis-áttelepítési projekt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a4d89-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="a4d89-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a4d89-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="a4d89-108">Beolvassa az Azure Adatbázis-áttelepítési szolgáltatás egy példányához tartozó tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a4d89-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="a4d89-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a4d89-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="a4d89-110">Lekéri az Azure Adatbázis-áttelepítési szolgáltatás áttelepítési feladatával társított PSProjectTask objektumot.</span><span class="sxs-lookup"><span data-stu-id="a4d89-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="a4d89-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="a4d89-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="a4d89-112">Létrehoz egy új parancsot, amely egy meglévő DMS-feladaton hajtódik végre.</span><span class="sxs-lookup"><span data-stu-id="a4d89-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="a4d89-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="a4d89-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="a4d89-114">Létrehoz egy új Kapcsolat adatai objektumot, amely megadja a kapcsolat kiszolgálótípusát és nevét.</span><span class="sxs-lookup"><span data-stu-id="a4d89-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="a4d89-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="a4d89-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="a4d89-116">Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás DatabaseInfo objektumát, amely megadja az áttelepítés adatbázis-forrását.</span><span class="sxs-lookup"><span data-stu-id="a4d89-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="a4d89-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="a4d89-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="a4d89-118">Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás FileShare objektumát, amely megadja a helyi hálózati megosztást, amelybe a forrásadatbázis biztonsági másolatát át kell vinni.</span><span class="sxs-lookup"><span data-stu-id="a4d89-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="a4d89-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="a4d89-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="a4d89-120">Létrehoz egy új Azure Database Migration Service-projektet.</span><span class="sxs-lookup"><span data-stu-id="a4d89-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="a4d89-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="a4d89-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="a4d89-122">Létrehoz egy adatbázis-bemeneti objektumot, amely az áttelepítéshez szükséges forrás- és céladatbázisokkal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a4d89-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="a4d89-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a4d89-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="a4d89-124">Létrehozza az Azure Database Migration Service új példányát.</span><span class="sxs-lookup"><span data-stu-id="a4d89-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="a4d89-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="a4d89-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="a4d89-126">A szinkronizálási helyzetnek megfelelő adatbázis-információs objektumot hoz létre az áttelepítési feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="a4d89-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="a4d89-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a4d89-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="a4d89-128">Adatáttelepítési feladatot hoz létre és kezd el az Azure Adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="a4d89-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="a4d89-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="a4d89-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="a4d89-130">Eltávolít egy Azure Database Migration Service-projektet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="a4d89-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="a4d89-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a4d89-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="a4d89-132">Eltávolítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="a4d89-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="a4d89-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a4d89-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="a4d89-134">Eltávolít egy Azure Database Migration Service-feladatot az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="a4d89-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="a4d89-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a4d89-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="a4d89-136">Leállítva elindítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát.</span><span class="sxs-lookup"><span data-stu-id="a4d89-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="a4d89-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a4d89-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="a4d89-138">Leállítja az Azure Adatbázis-áttelepítési szolgáltatás futó állapotban található példányát.</span><span class="sxs-lookup"><span data-stu-id="a4d89-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="a4d89-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a4d89-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="a4d89-140">Leállít egy futó állapotban futó Azure Database Migration Service-feladatot.</span><span class="sxs-lookup"><span data-stu-id="a4d89-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

