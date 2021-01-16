---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 9b87539335752b07b6c03852f30959b13de4c06e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330221"
---
# <span data-ttu-id="b0d6a-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b0d6a-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="b0d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d6a-103">Visszaállít egy Azure SQL Felügyelt példány adatbázist.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="b0d6a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0d6a-104">SYNTAX</span></span>

### <span data-ttu-id="b0d6a-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0d6a-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b0d6a-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d6a-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-108">PointInTimeCrosssInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="b0d6a-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-109">PointInTimeCrosssInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b0d6a-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-110">PointInTimeCrosssInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d6a-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="b0d6a-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-112">PointInTimeDeletedDatabasesCrosssInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="b0d6a-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b0d6a-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b0d6a-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="b0d6a-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0d6a-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="b0d6a-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0d6a-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0d6a-117">DESCRIPTION</span></span>
<span data-ttu-id="b0d6a-118">A **Restore-AzSqlInstanceDatabase** parancsmag egy georedundáns biztonsági másolatból, egy élő adatbázis egy pontjából vagy egy hosszú távú adatmegőrzési biztonsági másolatból visszaállítja a példány-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="b0d6a-119">A visszaállított adatbázis új példányadatbázisként jön létre.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="b0d6a-120">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0d6a-120">EXAMPLES</span></span>

### <span data-ttu-id="b0d6a-121">1. példa: Példány-adatbázis visszaállítása egy időpontból</span><span class="sxs-lookup"><span data-stu-id="b0d6a-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="b0d6a-122">A parancs visszaállítja a Database01 példányadatbázist a megadott időpontban biztonsági másolatból a Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="b0d6a-123">2. példa: A példányadatbázis visszaállítása adott időpontból egy másik példányba egy másik erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="b0d6a-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="b0d6a-124">A parancs visszaállítja a Database01 példány-adatbázist az ResourceGroup01 erőforráscsoport Példányinstance1 példányán a megadott időpontban biztonsági másolatból az Database01_restored példány-kezelőInstance2 példány-adatbázisba az ResourceGroup02 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="b0d6a-125">3. példa: Geo-Restore példány-adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="b0d6a-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="b0d6a-126">Az első parancs lekérte a Database01 nevű adatbázis geodundáns biztonsági másolatát, majd a helyi $GeoBackup tárolja.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="b0d6a-127">A második parancs visszaállítja a biztonsági másolatot $GeoBackup a Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="b0d6a-128">4. példa: Törölt példány adatbázisának visszaállítása egy időpontból</span><span class="sxs-lookup"><span data-stu-id="b0d6a-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -FromPointInTimeBackup -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="b0d6a-129">Az első parancs a "managedInstance1" példányon az "DB1" nevű törölt példány-adatbázisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="b0d6a-130">A második parancs visszaállítja a lehívott adatbázist a megadott időben biztonsági másolatból a Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="b0d6a-131">5. példa: Törölt példány adatbázisának visszaállítása egy időpontból</span><span class="sxs-lookup"><span data-stu-id="b0d6a-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -FromPointInTimeBackup -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="b0d6a-132">Az első parancs a "managedInstance1" példányon az "DB1" nevű törölt példány-adatbázisokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="b0d6a-133">A második parancs visszaállítja a lehívott adatbázist a megadott időben biztonsági másolatból a bemeneti Database01_restored elnevezett példány-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="b0d6a-134">6. példa: Adatbázis visszaállítása az LTR biztonsági másolatából.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-134">Example 6: Restore a database from LTR backup.</span></span>
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

<span data-ttu-id="b0d6a-135">Visszaállítja az LTR-biztonsági mentést a megadott erőforrás-azonosítóval (amely a Get-AzSqlInstanceDatabaseLongTermRetentionBackup futtatásával található meg).</span><span class="sxs-lookup"><span data-stu-id="b0d6a-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="b0d6a-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0d6a-136">PARAMETERS</span></span>

### <span data-ttu-id="b0d6a-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0d6a-137">-AsJob</span></span>
<span data-ttu-id="b0d6a-138">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b0d6a-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0d6a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d6a-139">-DefaultProfile</span></span>
<span data-ttu-id="b0d6a-140">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b0d6a-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="b0d6a-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="b0d6a-141">-DeletionDate</span></span>
<span data-ttu-id="b0d6a-142">A törölt adatbázis törlési dátuma.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-142">The deletion date of deleted database.</span></span>

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

### <span data-ttu-id="b0d6a-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b0d6a-143">-FromGeoBackup</span></span>
<span data-ttu-id="b0d6a-144">Visszaállítás földrajzi biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="b0d6a-144">Restore from a geo backup.</span></span>

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

### <span data-ttu-id="b0d6a-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b0d6a-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="b0d6a-146">Visszaállítás hosszú távú adatmegőrzési biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-146">Restore from a Long Term Retention backup.</span></span>

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

### <span data-ttu-id="b0d6a-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="b0d6a-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="b0d6a-148">Visszaállítás egy időben biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-148">Restore from a point-in-time backup.</span></span>

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

### <span data-ttu-id="b0d6a-149">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="b0d6a-149">-GeoBackupObject</span></span>
<span data-ttu-id="b0d6a-150">Visszaállítható példány adatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="b0d6a-150">The recoverable instance database object to restore</span></span>

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

### <span data-ttu-id="b0d6a-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0d6a-151">-InputObject</span></span>
<span data-ttu-id="b0d6a-152">A visszaállítható Példányadatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="b0d6a-152">The Instance Database object to restore</span></span>

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

### <span data-ttu-id="b0d6a-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b0d6a-153">-InstanceName</span></span>
<span data-ttu-id="b0d6a-154">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-154">The instance name.</span></span>

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

### <span data-ttu-id="b0d6a-155">-Name</span><span class="sxs-lookup"><span data-stu-id="b0d6a-155">-Name</span></span>
<span data-ttu-id="b0d6a-156">A visszaállítható példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-156">The instance database name to restore.</span></span>

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

### <span data-ttu-id="b0d6a-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="b0d6a-157">-PointInTime</span></span>
<span data-ttu-id="b0d6a-158">Az adatbázis visszaállításának ideje.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-158">The point in time to restore the database to.</span></span>

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

### <span data-ttu-id="b0d6a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d6a-159">-ResourceGroupName</span></span>
<span data-ttu-id="b0d6a-160">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="b0d6a-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d6a-161">-ResourceId</span></span>
<span data-ttu-id="b0d6a-162">A visszaállítani szükséges Példányadatbázis-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b0d6a-162">The resource id of Instance Database object to restore</span></span>

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

### <span data-ttu-id="b0d6a-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0d6a-163">-SubscriptionId</span></span>
<span data-ttu-id="b0d6a-164">Forrás-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-164">Source subscription id.</span></span>

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

### <span data-ttu-id="b0d6a-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0d6a-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="b0d6a-166">Annak a célpéldány-adatbázisnak a neve, amelybe vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-166">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="b0d6a-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="b0d6a-167">-TargetInstanceName</span></span>
<span data-ttu-id="b0d6a-168">Annak a célpéldánynak a neve, amelybe vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="b0d6a-169">Ha nincs megadva, a célpéldány megegyezik a forráspéldánysal.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-169">If not specified, the target instance is the same as the source instance.</span></span>

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

### <span data-ttu-id="b0d6a-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d6a-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="b0d6a-171">Annak a célerőforrás-csoportnak a neve, amelybe vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="b0d6a-172">Ha nincs megadva, a célerőforrás-csoport megegyezik a forráserőforrás-csoporttal.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-172">If not specified, the target resource group is the same as the source resource group.</span></span>

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

### <span data-ttu-id="b0d6a-173">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0d6a-173">-Confirm</span></span>
<span data-ttu-id="b0d6a-174">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0d6a-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0d6a-175">-WhatIf</span></span>
<span data-ttu-id="b0d6a-176">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0d6a-177">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0d6a-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d6a-178">CommonParameters</span></span>
<span data-ttu-id="b0d6a-179">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d6a-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d6a-180">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0d6a-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d6a-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0d6a-181">INPUTS</span></span>

### <span data-ttu-id="b0d6a-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b0d6a-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="b0d6a-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b0d6a-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="b0d6a-184">System.String</span><span class="sxs-lookup"><span data-stu-id="b0d6a-184">System.String</span></span>

## <span data-ttu-id="b0d6a-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0d6a-185">OUTPUTS</span></span>

### <span data-ttu-id="b0d6a-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b0d6a-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b0d6a-187">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0d6a-187">NOTES</span></span>

## <span data-ttu-id="b0d6a-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0d6a-188">RELATED LINKS</span></span>
