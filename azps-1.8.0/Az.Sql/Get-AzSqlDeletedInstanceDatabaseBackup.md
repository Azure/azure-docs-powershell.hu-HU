---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: ce68b8c8a03fbfe99adbb6070df072dd8ebb0cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668995"
---
# <span data-ttu-id="45a2a-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="45a2a-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="45a2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="45a2a-103">Visszaállíthatja a törölt adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="45a2a-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="45a2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45a2a-104">SYNTAX</span></span>

### <span data-ttu-id="45a2a-105">DeletedDatabaseList (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45a2a-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45a2a-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="45a2a-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45a2a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="45a2a-107">DESCRIPTION</span></span>
<span data-ttu-id="45a2a-108">A **Get-AzSqlDeletedInstanceDatabaseBackup** parancsmag egy megadott, törölt SQL-példány-adatbázis biztonsági másolatát kapja, amelyet visszaállíthat, vagy minden törölt biztonsági másolatot visszaadhat.</span><span class="sxs-lookup"><span data-stu-id="45a2a-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="45a2a-109">Ezt a parancsmagot az Azure SQL instance Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="45a2a-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="45a2a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="45a2a-110">EXAMPLES</span></span>

### <span data-ttu-id="45a2a-111">Példa 1: az összes törölt adatbázis biztonsági másolatának beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="45a2a-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="45a2a-112">Ez a parancs minden törölt adatbázis biztonsági másolatát beolvassa a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="45a2a-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="45a2a-113">2. példa: meghatározott törölt adatbázis biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="45a2a-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="45a2a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45a2a-114">PARAMETERS</span></span>

### <span data-ttu-id="45a2a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45a2a-115">-DatabaseName</span></span>
<span data-ttu-id="45a2a-116">Az Azure SQL-példány adatbázisának neve a biztonsági másolatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="45a2a-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a2a-117">-DefaultProfile</span></span>
<span data-ttu-id="45a2a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45a2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a2a-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="45a2a-119">-DeletionDate</span></span>
<span data-ttu-id="45a2a-120">Az Azure SQL-példány adatbázisának törlési dátuma a biztonsági másolatok (például 2016-02-23T00:22.847 Z) beolvasásához</span><span class="sxs-lookup"><span data-stu-id="45a2a-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a2a-121">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="45a2a-121">-InstanceName</span></span>
<span data-ttu-id="45a2a-122">Az adatbázisnak az Azure SQL-alapú felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="45a2a-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="45a2a-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="45a2a-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a2a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a2a-125">CommonParameters</span></span>
<span data-ttu-id="45a2a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45a2a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a2a-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45a2a-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a2a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45a2a-128">INPUTS</span></span>

### <span data-ttu-id="45a2a-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="45a2a-129">None</span></span>

## <span data-ttu-id="45a2a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45a2a-130">OUTPUTS</span></span>

### <span data-ttu-id="45a2a-131">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="45a2a-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="45a2a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45a2a-132">NOTES</span></span>

## <span data-ttu-id="45a2a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45a2a-133">RELATED LINKS</span></span>
