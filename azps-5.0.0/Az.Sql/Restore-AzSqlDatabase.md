---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185818"
---
# <span data-ttu-id="0f86e-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f86e-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="0f86e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f86e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f86e-103">SQL-adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="0f86e-103">Restores a SQL database.</span></span>

## <span data-ttu-id="0f86e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f86e-104">SYNTAX</span></span>

### <span data-ttu-id="0f86e-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f86e-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0f86e-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f86e-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f86e-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0f86e-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f86e-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f86e-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0f86e-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f86e-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f86e-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0f86e-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f86e-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f86e-113">DESCRIPTION</span></span>
<span data-ttu-id="0f86e-114">A **Restore-AzSqlDatabase** PARANCSMAG egy SQL-adatbázist egy geo-redundáns biztonsági másolatból, egy törölt adatbázis biztonsági másolatával, egy hosszú távú adatmegőrzési biztonsági másolatból vagy egy aktív adatbázis időpontjának időpontjából áll vissza.</span><span class="sxs-lookup"><span data-stu-id="0f86e-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="0f86e-115">A helyreállított adatbázis új adatbázisként jön létre.</span><span class="sxs-lookup"><span data-stu-id="0f86e-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="0f86e-116">Rugalmas SQL-adatbázist úgy hozhat létre, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="0f86e-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="0f86e-117">Példák</span><span class="sxs-lookup"><span data-stu-id="0f86e-117">EXAMPLES</span></span>

### <span data-ttu-id="0f86e-118">Példa 1: adatbázis visszaállítása időpontból</span><span class="sxs-lookup"><span data-stu-id="0f86e-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="0f86e-119">Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0f86e-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="0f86e-120">A második parancs visszaállítja az adatbázist $Database a megadott időpontos biztonsági másolatról a RestoredDatabase nevű adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="0f86e-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="0f86e-121">2. példa: adatbázis visszaállítása időpontból egy rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="0f86e-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="0f86e-122">Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0f86e-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="0f86e-123">A második parancs visszaállítja az adatbázis $Database a megadott időpontos biztonsági másolatból az RestoredDatabase nevű SQL-adatbázisba a elasticpool01 nevű rugalmas készletben.</span><span class="sxs-lookup"><span data-stu-id="0f86e-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="0f86e-124">3. példa: törölt adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="0f86e-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="0f86e-125">Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="0f86e-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="0f86e-126">A második parancs a visszaállítás [– AzSqlDatabase](./Restore-AzSqlDatabase.md) parancsmag használatával elindítja a törölt adatbázis biztonsági másolatának visszaállítását.</span><span class="sxs-lookup"><span data-stu-id="0f86e-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="0f86e-127">Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="0f86e-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="0f86e-128">Példa 4: törölt adatbázis visszaállítása rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="0f86e-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="0f86e-129">Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="0f86e-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="0f86e-130">A második parancs elindítja a visszaállítást a törölt adatbázis biztonsági másolatból a [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)használatával.</span><span class="sxs-lookup"><span data-stu-id="0f86e-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="0f86e-131">Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="0f86e-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="0f86e-132">Példa 5: adatbázis Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="0f86e-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="0f86e-133">Az első parancs megkapja a Database01 nevű adatbázis geo-redundáns biztonsági másolatát, majd a $GeoBackup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0f86e-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="0f86e-134">A második parancs visszaállítja a biztonsági mentést $GeoBackup a RestoredDatabase nevű SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="0f86e-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="0f86e-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f86e-135">PARAMETERS</span></span>

### <span data-ttu-id="0f86e-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f86e-136">-AsJob</span></span>
<span data-ttu-id="0f86e-137">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f86e-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f86e-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="0f86e-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="0f86e-139">Az SQL-adatbázis biztonsági mentéseit tároló biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="0f86e-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="0f86e-140">A beállítások a következők: helyi, zóna és Geo.</span><span class="sxs-lookup"><span data-stu-id="0f86e-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0f86e-141">-ComputeGeneration</span></span>
<span data-ttu-id="0f86e-142">A visszaállított adatbázishoz rendelt számítási generálás</span><span class="sxs-lookup"><span data-stu-id="0f86e-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f86e-143">-DefaultProfile</span></span>
<span data-ttu-id="0f86e-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f86e-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f86e-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="0f86e-145">-DeletionDate</span></span>
<span data-ttu-id="0f86e-146">A törlési dátumot **datetime** típusú objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f86e-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="0f86e-147">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0f86e-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-148">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="0f86e-148">-Edition</span></span>
<span data-ttu-id="0f86e-149">Az SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f86e-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="0f86e-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0f86e-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0f86e-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="0f86e-151">None</span></span>
- <span data-ttu-id="0f86e-152">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="0f86e-152">Basic</span></span>
- <span data-ttu-id="0f86e-153">Standard</span><span class="sxs-lookup"><span data-stu-id="0f86e-153">Standard</span></span>
- <span data-ttu-id="0f86e-154">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="0f86e-154">Premium</span></span>
- <span data-ttu-id="0f86e-155">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="0f86e-155">DataWarehouse</span></span>
- <span data-ttu-id="0f86e-156">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="0f86e-156">Free</span></span>
- <span data-ttu-id="0f86e-157">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="0f86e-157">Stretch</span></span>
- <span data-ttu-id="0f86e-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0f86e-158">GeneralPurpose</span></span>
- <span data-ttu-id="0f86e-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0f86e-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0f86e-160">-ElasticPoolName</span></span>
<span data-ttu-id="0f86e-161">Annak a rugalmas készletnek a nevét adja meg, amelybe az SQL-adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="0f86e-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="0f86e-163">Jelzi, hogy ez a parancsmag visszaállítja az adatbázist egy törölt SQL-adatbázis biztonsági másolatával.</span><span class="sxs-lookup"><span data-stu-id="0f86e-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="0f86e-164">A törölt SQL-adatbázisok biztonsági másolatának beszerzéséhez használhatja az Get-AzSqlDeletedDatabaseBackup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0f86e-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-165">-FromGeoBackup</span></span>
<span data-ttu-id="0f86e-166">Jelzi, hogy ez a parancsmag visszaállítja egy SQL-adatbázist egy geo-redundáns biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="0f86e-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="0f86e-167">Geo-redundáns biztonsági másolat készítéséhez használhatja az Get-AzSqlDatabaseGeoBackup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0f86e-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="0f86e-169">Azt jelzi, hogy ez a parancsmag hosszú távú adatmegőrzési biztonsági másolatból állítja vissza az SQL-adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="0f86e-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="0f86e-171">Azt jelzi, hogy ez a parancsmag visszaállítja az SQL-adatbázist egy időpontos biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="0f86e-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0f86e-172">-LicenseType</span></span>
<span data-ttu-id="0f86e-173">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="0f86e-173">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="0f86e-174">-PointInTime</span></span>
<span data-ttu-id="0f86e-175">Annak az időpontnak a időpontját adja meg **datetime** -objektumként, amelynek vissza szeretné ÁLLÍTANI az SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="0f86e-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="0f86e-176">Ha **datetime** típusú objektumot szeretne kapni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0f86e-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0f86e-177">Használja ezt a paramétert a *FromPointInTimeBackup* paraméterrel együtt.</span><span class="sxs-lookup"><span data-stu-id="0f86e-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f86e-178">-ResourceGroupName</span></span>
<span data-ttu-id="0f86e-179">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli az SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="0f86e-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f86e-180">-ResourceId</span></span>
<span data-ttu-id="0f86e-181">A visszaállítandó erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f86e-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-182">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0f86e-182">-ServerName</span></span>
<span data-ttu-id="0f86e-183">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f86e-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0f86e-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="0f86e-185">A szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f86e-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f86e-186">-TargetDatabaseName</span></span>
<span data-ttu-id="0f86e-187">Itt adhatja meg annak az adatbázisnak a nevét, amelynek vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="0f86e-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="0f86e-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="0f86e-188">-VCore</span></span>
<span data-ttu-id="0f86e-189">A helyreállított Azure SQL-adatbázis vcore száma.</span><span class="sxs-lookup"><span data-stu-id="0f86e-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-190">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f86e-190">-Confirm</span></span>
<span data-ttu-id="0f86e-191">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f86e-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f86e-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f86e-192">-WhatIf</span></span>
<span data-ttu-id="0f86e-193">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f86e-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f86e-194">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f86e-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f86e-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f86e-195">CommonParameters</span></span>
<span data-ttu-id="0f86e-196">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f86e-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f86e-197">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0f86e-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f86e-198">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f86e-198">INPUTS</span></span>

### <span data-ttu-id="0f86e-199">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0f86e-199">System.DateTime</span></span>

### <span data-ttu-id="0f86e-200">System. String</span><span class="sxs-lookup"><span data-stu-id="0f86e-200">System.String</span></span>

## <span data-ttu-id="0f86e-201">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f86e-201">OUTPUTS</span></span>

### <span data-ttu-id="0f86e-202">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0f86e-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0f86e-203">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f86e-203">NOTES</span></span>

## <span data-ttu-id="0f86e-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f86e-204">RELATED LINKS</span></span>

[<span data-ttu-id="0f86e-205">Azure SQL-adatbázis helyreállítása leállás esetén</span><span class="sxs-lookup"><span data-stu-id="0f86e-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="0f86e-206">Azure SQL-adatbázis helyreállítása felhasználói hibából</span><span class="sxs-lookup"><span data-stu-id="0f86e-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="0f86e-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f86e-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0f86e-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="0f86e-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0f86e-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="0f86e-210">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0f86e-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

