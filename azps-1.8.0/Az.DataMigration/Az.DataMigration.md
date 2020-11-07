---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657805"
---
# <span data-ttu-id="9540f-101">Az. DataMigration modul</span><span class="sxs-lookup"><span data-stu-id="9540f-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="9540f-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="9540f-102">Description</span></span>
<span data-ttu-id="9540f-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="9540f-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="9540f-104">Az. DataMigration parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9540f-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="9540f-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="9540f-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="9540f-106">Beolvassa az Azure adatbázis-áttelepítési projektek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="9540f-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="9540f-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9540f-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="9540f-108">Beolvassa az Azure adatbázis áttelepítési szolgáltatásának példányaival társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9540f-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="9540f-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9540f-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="9540f-110">Beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított PSProjectTask-objektumot.</span><span class="sxs-lookup"><span data-stu-id="9540f-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="9540f-111">Meghívó-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="9540f-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="9540f-112">Új parancsot hoz létre, amelyet egy meglévő DMS-feladaton kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="9540f-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="9540f-113">Új – AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="9540f-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="9540f-114">Új kapcsolati adatobjektumot hoz létre a kiszolgáló típusa és a kapcsolat neve mezőben.</span><span class="sxs-lookup"><span data-stu-id="9540f-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="9540f-115">Új – AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="9540f-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="9540f-116">Létrehozza az Azure Database áttelepítési szolgáltatás DatabaseInfo objektumát, amely az áttelepítéshez szükséges adatbázis-forrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="9540f-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="9540f-117">Új – AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="9540f-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="9540f-118">Létrehozza az Azure adatbázis-áttelepítési szolgáltatás fájlmegosztásról objektumát, amely a helyi hálózati megosztást adja meg a forrás adatbázis biztonsági másolatának elkészítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9540f-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="9540f-119">Új – AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="9540f-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="9540f-120">Új Azure adatbázis-áttelepítési szolgáltatás projekt létrehozása</span><span class="sxs-lookup"><span data-stu-id="9540f-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="9540f-121">Új – AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="9540f-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="9540f-122">Létrehoz egy adatbázis-beviteli objektumot, amely információt tartalmaz az áttelepítéshez szükséges forrás-és céladatbázis-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="9540f-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="9540f-123">Új – AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9540f-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="9540f-124">Az Azure-adatbázis áttelepítési szolgáltatásának új példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9540f-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="9540f-125">Új – AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="9540f-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="9540f-126">Adatbázis-információ objektum létrehozása az áttelepítési feladathoz használt szinkronizálási forgatókönyvhez</span><span class="sxs-lookup"><span data-stu-id="9540f-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="9540f-127">Új – AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9540f-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="9540f-128">Áttelepítési feladatot hoz létre és indít el az Azure adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9540f-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="9540f-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="9540f-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="9540f-130">Az Azure adatbázis-áttelepítési szolgáltatás projekt eltávolítása az Azure-ról</span><span class="sxs-lookup"><span data-stu-id="9540f-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="9540f-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9540f-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="9540f-132">Eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="9540f-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="9540f-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9540f-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="9540f-134">Az Azure adatbázis-áttelepítési szolgáltatás tevékenységének eltávolítása az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="9540f-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="9540f-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9540f-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="9540f-136">Elindítja az Azure adatbázis áttelepítési szolgáltatásának példányát egy leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="9540f-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="9540f-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9540f-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="9540f-138">Leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotban lévő példányát.</span><span class="sxs-lookup"><span data-stu-id="9540f-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="9540f-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9540f-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="9540f-140">Egy futó államban futó Azure adatbázis-áttelepítési szolgáltatási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="9540f-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

