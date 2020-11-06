---
Module Name: AzureRM.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/AzureRM.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/AzureRM.DataMigration.md
ms.openlocfilehash: 1842bf625623e66d35adf32490a1d71315413c84
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490227"
---
# <span data-ttu-id="54c55-101">AzureRM. DataMigration modul</span><span class="sxs-lookup"><span data-stu-id="54c55-101">AzureRM.DataMigration Module</span></span>
## <span data-ttu-id="54c55-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="54c55-102">Description</span></span>
<span data-ttu-id="54c55-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="54c55-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="54c55-104">AzureRM. DataMigration parancsmagok</span><span class="sxs-lookup"><span data-stu-id="54c55-104">AzureRM.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="54c55-105">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="54c55-105">Get-AzureRmDataMigrationProject</span></span>](Get-AzureRmDataMigrationProject.md)
<span data-ttu-id="54c55-106">Beolvassa az Azure adatbázis-áttelepítési projektek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="54c55-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="54c55-107">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="54c55-107">Get-AzureRmDataMigrationService</span></span>](Get-AzureRmDataMigrationService.md)
<span data-ttu-id="54c55-108">Beolvassa az Azure adatbázis áttelepítési szolgáltatásának példányaival társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="54c55-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="54c55-109">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="54c55-109">Get-AzureRmDataMigrationTask</span></span>](Get-AzureRmDataMigrationTask.md)
<span data-ttu-id="54c55-110">Beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított PSProjectTask-objektumot.</span><span class="sxs-lookup"><span data-stu-id="54c55-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### <span data-ttu-id="54c55-111">[New-AzureRmDataMigrationCommand (Get-AzureRmDataMigrationCommand.md)</span><span class="sxs-lookup"><span data-stu-id="54c55-111">[New-AzureRmDataMigrationCommand(Get-AzureRmDataMigrationCommand.md)</span></span>
<span data-ttu-id="54c55-112">Új parancsot hoz létre, amelyet egy meglévő Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatán kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="54c55-112">Creates a new command to be executed on an existing Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="54c55-113">Új – AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="54c55-113">New-AzureRmDataMigrationConnectionInfo</span></span>](New-AzureRmDataMigrationConnectionInfo.md)
<span data-ttu-id="54c55-114">Új kapcsolati adatobjektumot hoz létre a kiszolgáló típusa és a kapcsolat neve mezőben.</span><span class="sxs-lookup"><span data-stu-id="54c55-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="54c55-115">Új – AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="54c55-115">New-AzureRmDataMigrationDatabaseInfo</span></span>](New-AzureRmDataMigrationDatabaseInfo.md)
<span data-ttu-id="54c55-116">Létrehozza az Azure Database áttelepítési szolgáltatás DatabaseInfo objektumát, amely az áttelepítéshez szükséges adatbázis-forrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="54c55-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="54c55-117">Új – AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="54c55-117">New-AzureRmDataMigrationFileShare</span></span>](New-AzureRmDataMigrationFileShare.md)
<span data-ttu-id="54c55-118">Létrehozza az Azure adatbázis-áttelepítési szolgáltatás fájlmegosztásról objektumát, amely a helyi hálózati megosztást adja meg a forrás adatbázis biztonsági másolatának elkészítéséhez.</span><span class="sxs-lookup"><span data-stu-id="54c55-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="54c55-119">Új – AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="54c55-119">New-AzureRmDataMigrationProject</span></span>](New-AzureRmDataMigrationProject.md)
<span data-ttu-id="54c55-120">Új Azure adatbázis-áttelepítési szolgáltatás projekt létrehozása</span><span class="sxs-lookup"><span data-stu-id="54c55-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="54c55-121">Új – AzureRmDataMigrationSelectedDB</span><span class="sxs-lookup"><span data-stu-id="54c55-121">New-AzureRmDataMigrationSelectedDB</span></span>](New-AzureRmDataMigrationSelectedDB.md)
<span data-ttu-id="54c55-122">Létrehoz egy adatbázis-beviteli objektumot, amely információt tartalmaz az áttelepítéshez szükséges forrás-és céladatbázis-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="54c55-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="54c55-123">Új – AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="54c55-123">New-AzureRmDataMigrationService</span></span>](New-AzureRmDataMigrationService.md)
<span data-ttu-id="54c55-124">Az Azure-adatbázis áttelepítési szolgáltatásának új példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="54c55-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="54c55-125">Új – AzureRmDataMigrationSyncSelectedDB</span><span class="sxs-lookup"><span data-stu-id="54c55-125">New-AzureRmDataMigrationSyncSelectedDB</span></span>](New-AzureRmDataMigrationSyncSelectedDB.md)
<span data-ttu-id="54c55-126">Adatbázis-beviteli objektum létrehozása olyan szinkronizálási esetekhez, amelyek információkat tartalmaznak a forrás-és a célként megadott adatbázis áttelepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="54c55-126">Creates a database input object for sync scenarios that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="54c55-127">Új – AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="54c55-127">New-AzureRmDataMigrationTask</span></span>](New-AzureRmDataMigrationTask.md)
<span data-ttu-id="54c55-128">Áttelepítési feladatot hoz létre és indít el az Azure adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="54c55-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="54c55-129">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="54c55-129">Remove-AzureRmDataMigrationProject</span></span>](Remove-AzureRmDataMigrationProject.md)
<span data-ttu-id="54c55-130">Az Azure adatbázis-áttelepítési szolgáltatás projekt eltávolítása az Azure-ról</span><span class="sxs-lookup"><span data-stu-id="54c55-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="54c55-131">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="54c55-131">Remove-AzureRmDataMigrationService</span></span>](Remove-AzureRmDataMigrationService.md)
<span data-ttu-id="54c55-132">Eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="54c55-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="54c55-133">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="54c55-133">Remove-AzureRmDataMigrationTask</span></span>](Remove-AzureRmDataMigrationTask.md)
<span data-ttu-id="54c55-134">Az Azure adatbázis-áttelepítési szolgáltatás tevékenységének eltávolítása az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="54c55-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="54c55-135">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="54c55-135">Start-AzureRmDataMigrationService</span></span>](Start-AzureRmDataMigrationService.md)
<span data-ttu-id="54c55-136">Elindítja az Azure adatbázis áttelepítési szolgáltatásának példányát egy leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="54c55-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="54c55-137">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="54c55-137">Stop-AzureRmDataMigrationService</span></span>](Stop-AzureRmDataMigrationService.md)
<span data-ttu-id="54c55-138">Leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotban lévő példányát.</span><span class="sxs-lookup"><span data-stu-id="54c55-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="54c55-139">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="54c55-139">Stop-AzureRmDataMigrationTask</span></span>](Stop-AzureRmDataMigrationTask.md)
<span data-ttu-id="54c55-140">Egy futó államban futó Azure adatbázis-áttelepítési szolgáltatási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="54c55-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

