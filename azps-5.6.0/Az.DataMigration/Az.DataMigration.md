---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: c73e82285a848c9ff6abf197eb3352cf708a2f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921993"
---
# <span data-ttu-id="cec6b-101">Az.DataMigration modul</span><span class="sxs-lookup"><span data-stu-id="cec6b-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="cec6b-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="cec6b-102">Description</span></span>
<span data-ttu-id="cec6b-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="cec6b-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="cec6b-104">Az.DataMigration parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cec6b-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="cec6b-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="cec6b-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="cec6b-106">Beolvassa egy Azure-adatbázis-áttelepítési projekt tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="cec6b-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="cec6b-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cec6b-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="cec6b-108">Beolvassa az Azure Adatbázis-áttelepítési szolgáltatás egy példányához tartozó tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="cec6b-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="cec6b-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="cec6b-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="cec6b-110">Lekéri az Azure Adatbázis-áttelepítési szolgáltatás áttelepítési feladatával társított PSProjectTask objektumot.</span><span class="sxs-lookup"><span data-stu-id="cec6b-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="cec6b-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="cec6b-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="cec6b-112">Létrehoz egy új parancsot, amely egy meglévő DMS-feladaton hajtódik végre.</span><span class="sxs-lookup"><span data-stu-id="cec6b-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="cec6b-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="cec6b-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="cec6b-114">Létrehoz egy új Kapcsolat adatai objektumot, amely megadja a kapcsolat kiszolgálótípusát és nevét.</span><span class="sxs-lookup"><span data-stu-id="cec6b-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="cec6b-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="cec6b-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="cec6b-116">Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás DatabaseInfo objektumát, amely megadja az áttelepítés adatbázis-forrását.</span><span class="sxs-lookup"><span data-stu-id="cec6b-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="cec6b-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="cec6b-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="cec6b-118">Létrehozza az Azure Adatbázis-áttelepítési szolgáltatás FileShare objektumát, amely megadja a helyi hálózati megosztást, amelybe a forrásadatbázis biztonsági másolatát át kell vinni.</span><span class="sxs-lookup"><span data-stu-id="cec6b-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="cec6b-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="cec6b-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="cec6b-120">Létrehoz egy új Azure Database Migration Service-projektet.</span><span class="sxs-lookup"><span data-stu-id="cec6b-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="cec6b-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="cec6b-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="cec6b-122">Létrehoz egy adatbázis-bemeneti objektumot, amely az áttelepítéshez szükséges forrás- és céladatbázisokkal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cec6b-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="cec6b-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cec6b-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="cec6b-124">Létrehozza az Azure Database Migration Service új példányát.</span><span class="sxs-lookup"><span data-stu-id="cec6b-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="cec6b-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="cec6b-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="cec6b-126">A szinkronizálási helyzetnek megfelelő adatbázis-információs objektumot hoz létre az áttelepítési feladathoz.</span><span class="sxs-lookup"><span data-stu-id="cec6b-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="cec6b-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="cec6b-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="cec6b-128">Adatáttelepítési feladatot hoz létre és kezd el az Azure Adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="cec6b-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="cec6b-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="cec6b-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="cec6b-130">Eltávolít egy Azure Database Migration Service-projektet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="cec6b-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="cec6b-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cec6b-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="cec6b-132">Eltávolítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="cec6b-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="cec6b-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="cec6b-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="cec6b-134">Eltávolít egy Azure Database Migration Service-feladatot az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="cec6b-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="cec6b-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cec6b-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="cec6b-136">Leállítva elindítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát.</span><span class="sxs-lookup"><span data-stu-id="cec6b-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="cec6b-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cec6b-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="cec6b-138">Leállítja az Azure Adatbázis-áttelepítési szolgáltatás futó állapotban található példányát.</span><span class="sxs-lookup"><span data-stu-id="cec6b-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="cec6b-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="cec6b-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="cec6b-140">Leállít egy futó állapotban futó Azure Database Migration Service-feladatot.</span><span class="sxs-lookup"><span data-stu-id="cec6b-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

