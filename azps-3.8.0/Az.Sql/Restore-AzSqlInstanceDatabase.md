---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 5b7208c52908e560d7b2eb0abc46befafdbaf41b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010874"
---
# <span data-ttu-id="507d1-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="507d1-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="507d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="507d1-102">SYNOPSIS</span></span>
<span data-ttu-id="507d1-103">Visszaállít egy Azure SQL Managed instance-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="507d1-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="507d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="507d1-104">SYNTAX</span></span>

### <span data-ttu-id="507d1-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="507d1-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507d1-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="507d1-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507d1-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="507d1-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="507d1-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="507d1-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507d1-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="507d1-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="507d1-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="507d1-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507d1-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="507d1-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="507d1-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="507d1-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507d1-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="507d1-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507d1-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="507d1-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="507d1-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="507d1-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="507d1-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="507d1-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="507d1-117">Leírás</span><span class="sxs-lookup"><span data-stu-id="507d1-117">DESCRIPTION</span></span>
<span data-ttu-id="507d1-118">A **Restore-AzSqlInstanceDatabase** parancsmag egy példány adatbázisát a Geo-redundáns biztonsági másolatból, az időpontból az aktív adatbázisból vagy hosszú távú adatmegőrzési biztonsági másolatból állítja vissza.</span><span class="sxs-lookup"><span data-stu-id="507d1-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="507d1-119">A helyreállított adatbázis új példány adatbázisként jön létre.</span><span class="sxs-lookup"><span data-stu-id="507d1-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="507d1-120">Példák</span><span class="sxs-lookup"><span data-stu-id="507d1-120">EXAMPLES</span></span>

### <span data-ttu-id="507d1-121">Példa 1: példány adatbázisának visszaállítása időpontból</span><span class="sxs-lookup"><span data-stu-id="507d1-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="507d1-122">A parancs visszaállítja a példány-adatbázis Database01 a megadott időpontos biztonsági másolatból az Database01_restored nevű adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="507d1-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="507d1-123">2. példa: példány adatbázisának visszaállítása egy másik példányra a különböző erőforráscsoport esetén</span><span class="sxs-lookup"><span data-stu-id="507d1-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="507d1-124">A parancs visszaállítja a példány-adatbázis Database01 a példány managedInstance1 az erőforráscsoport ResourceGroup01, a megadott időpontos biztonsági másolatról a példány-adatbázisra, amelyet az Database01_restored példánya nevű adatbázishoz (például managedInstance2 az erőforráscsoport ResourceGroup02).</span><span class="sxs-lookup"><span data-stu-id="507d1-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="507d1-125">Példa 3: példány-adatbázis Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="507d1-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="507d1-126">Az első parancs megkapja a Database01 nevű adatbázis geo-redundáns biztonsági másolatát, majd a $GeoBackup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="507d1-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="507d1-127">A második parancs visszaállítja a biztonsági mentést $GeoBackup a Database01_restored nevű példány-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="507d1-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="507d1-128">4. példa: a törölt példányok adatbázisának visszaállítása időpontból</span><span class="sxs-lookup"><span data-stu-id="507d1-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="507d1-129">Az első parancs a törölt példányok "D1" nevű adatbázisát (például "managedInstance1") kapja.</span><span class="sxs-lookup"><span data-stu-id="507d1-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="507d1-130">A második parancs visszaállítja a meghívott adatbázist a megadott időpontos biztonsági másolatról a Database01_restored nevű adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="507d1-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="507d1-131">Példa 5: a törölt példányok adatbázisának visszaállítása időpontból</span><span class="sxs-lookup"><span data-stu-id="507d1-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="507d1-132">Az első parancs a törölt példányok "D1" nevű adatbázisát (például "managedInstance1") kapja.</span><span class="sxs-lookup"><span data-stu-id="507d1-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="507d1-133">A második parancs visszaállítja a beolvasott adatbázist a megadott időpontos biztonsági másolatról a "beviteli objektum" Database01_restored nevű adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="507d1-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="507d1-134">6. példa: adatbázis visszaállítása a LTR biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="507d1-134">Example 6: Restore a database from LTR backup.</span></span> 
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="507d1-135">Visszaállítja a LTR biztonsági másolatát a megadott erőforrás-AZONOSÍTÓval (amely a Get-AzSqlInstanceDatabaseLongTermRetentionBackup futtatásával érhető el).</span><span class="sxs-lookup"><span data-stu-id="507d1-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="507d1-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="507d1-136">PARAMETERS</span></span>

### <span data-ttu-id="507d1-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="507d1-137">-AsJob</span></span>
<span data-ttu-id="507d1-138">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="507d1-138">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507d1-139">-DefaultProfile</span></span>
<span data-ttu-id="507d1-140">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="507d1-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="507d1-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="507d1-141">-DeletionDate</span></span>
<span data-ttu-id="507d1-142">A törölt adatbázis törlési dátuma.</span><span class="sxs-lookup"><span data-stu-id="507d1-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="507d1-143">-FromGeoBackup</span></span>
<span data-ttu-id="507d1-144">Visszaállítás a Geo biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="507d1-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="507d1-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="507d1-146">Visszaállítás hosszú távú adatmegőrzési biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="507d1-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="507d1-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="507d1-148">Visszaállítás egy időpontos biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="507d1-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-149">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="507d1-149">-GeoBackupObject</span></span>
<span data-ttu-id="507d1-150">A helyreállítható példány adatbázis-objektum visszaállítása</span><span class="sxs-lookup"><span data-stu-id="507d1-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="507d1-151">-InputObject</span></span>
<span data-ttu-id="507d1-152">A példány adatbázis-objektum visszaállítása</span><span class="sxs-lookup"><span data-stu-id="507d1-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-153">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="507d1-153">-InstanceName</span></span>
<span data-ttu-id="507d1-154">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="507d1-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-155">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="507d1-155">-Name</span></span>
<span data-ttu-id="507d1-156">A példány adatbázisának neve a visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="507d1-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="507d1-157">-PointInTime</span></span>
<span data-ttu-id="507d1-158">A pontos idő az adatbázis visszaállításához.</span><span class="sxs-lookup"><span data-stu-id="507d1-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507d1-159">-ResourceGroupName</span></span>
<span data-ttu-id="507d1-160">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="507d1-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="507d1-161">-ResourceId</span></span>
<span data-ttu-id="507d1-162">A Restore példány adatbázis-objektumának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="507d1-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="507d1-163">-SubscriptionId</span></span>
<span data-ttu-id="507d1-164">Forrás-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="507d1-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="507d1-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="507d1-166">Annak a célnak az adatbázisnak a neve, amelyet vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="507d1-166">The name of the target instance database to restore to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="507d1-167">-TargetInstanceName</span></span>
<span data-ttu-id="507d1-168">Annak a TARGET-példánynak a neve, amelybe vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="507d1-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="507d1-169">Ha nincs megadva, a cél példány megegyezik a forrás példánytal.</span><span class="sxs-lookup"><span data-stu-id="507d1-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507d1-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="507d1-171">Annak a cél erőforrás-csoportnak a neve, amelybe vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="507d1-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="507d1-172">Ha nem adja meg, a cél erőforráscsoport megegyezik a forrás erőforrás csoporttal.</span><span class="sxs-lookup"><span data-stu-id="507d1-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-173">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="507d1-173">-Confirm</span></span>
<span data-ttu-id="507d1-174">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="507d1-174">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="507d1-175">-WhatIf</span></span>
<span data-ttu-id="507d1-176">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="507d1-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="507d1-177">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="507d1-177">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507d1-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507d1-178">CommonParameters</span></span>
<span data-ttu-id="507d1-179">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="507d1-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507d1-180">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="507d1-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507d1-181">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="507d1-181">INPUTS</span></span>

### <span data-ttu-id="507d1-182">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="507d1-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="507d1-183">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="507d1-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="507d1-184">System. String</span><span class="sxs-lookup"><span data-stu-id="507d1-184">System.String</span></span>

## <span data-ttu-id="507d1-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="507d1-185">OUTPUTS</span></span>

### <span data-ttu-id="507d1-186">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="507d1-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="507d1-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="507d1-187">NOTES</span></span>

## <span data-ttu-id="507d1-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="507d1-188">RELATED LINKS</span></span>
