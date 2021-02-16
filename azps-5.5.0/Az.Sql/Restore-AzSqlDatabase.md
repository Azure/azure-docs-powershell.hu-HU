---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168651"
---
# <span data-ttu-id="d6512-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6512-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="d6512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6512-102">SYNOPSIS</span></span>
<span data-ttu-id="d6512-103">Sql-adatbázis visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="d6512-103">Restores a SQL database.</span></span>

## <span data-ttu-id="d6512-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6512-104">SYNTAX</span></span>

### <span data-ttu-id="d6512-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6512-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="d6512-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6512-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6512-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="d6512-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6512-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6512-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="d6512-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6512-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6512-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="d6512-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6512-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6512-113">DESCRIPTION</span></span>
<span data-ttu-id="d6512-114">A **Restore-AzSqlDatabase** parancsmag egy SQL-adatbázist visszaállít georedundáns biztonsági másolatból, törölt adatbázis biztonsági másolatából, hosszú távú adatmegőrzési biztonsági másolatból vagy egy élő adatbázis egy pontjából.</span><span class="sxs-lookup"><span data-stu-id="d6512-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="d6512-115">A visszaállított adatbázis új adatbázisként jön létre.</span><span class="sxs-lookup"><span data-stu-id="d6512-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="d6512-116">Rugalmas SQL-adatbázist úgy hozhat létre, hogy a *RugalmasságPoolName* paramétert egy meglévő rugalmas készletre használhatja.</span><span class="sxs-lookup"><span data-stu-id="d6512-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="d6512-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6512-117">EXAMPLES</span></span>

### <span data-ttu-id="d6512-118">1. példa: Adatbázis visszaállítása egy időpontból</span><span class="sxs-lookup"><span data-stu-id="d6512-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="d6512-119">Az első parancs lekérte az Adatbázis01 nevű SQL-adatbázist, majd a $Database tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6512-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="d6512-120">A második parancs visszaállítja az adatbázist $Database a megadott időpontban biztonsági másolatból a RestoredDatabase nevű adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="d6512-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="d6512-121">2. példa: Adatbázis visszaállítása egy időpontból egy rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="d6512-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d6512-122">Az első parancs lekérte az Adatbázis01 nevű SQL-adatbázist, majd a $Database tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6512-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="d6512-123">A második parancs visszaállítja az adatbázist $Database a megadott időpontban biztonsági másolatból a RestoredDatabase nevű SQL-adatbázisba a rugalmasságipool01 nevű rugalmas készletben.</span><span class="sxs-lookup"><span data-stu-id="d6512-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="d6512-124">3. példa: Törölt adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="d6512-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="d6512-125">Az első parancs a [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)paranccsal visszaállítandó törölt adatbázis biztonsági másolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="d6512-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="d6512-126">A második parancs elindítja a visszaállítást a törölt adatbázis biztonsági másolatából a [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d6512-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="d6512-127">Ha a -PointInTime paraméter nincs megadva, a rendszer visszaállítja az adatbázist a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="d6512-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="d6512-128">4. példa: Törölt adatbázis visszaállítása rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="d6512-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="d6512-129">Az első parancs a [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)paranccsal visszaállítandó törölt adatbázis biztonsági másolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="d6512-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="d6512-130">A második parancs elindítja a visszaállítást a törölt adatbázis biztonsági másolatából [a Restore-AzSqlDatabase segítségével.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="d6512-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="d6512-131">Ha a -PointInTime paraméter nincs megadva, a rendszer visszaállítja az adatbázist a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="d6512-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="d6512-132">5. példa: Geo-Restore adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="d6512-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="d6512-133">Az első parancs lekérte a Database01 nevű adatbázis georedundáns biztonsági másolatát, majd a helyi $GeoBackup tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6512-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="d6512-134">A második parancs visszaállítja a biztonsági másolatot $GeoBackup adatbázisból a RestoredDatabase nevű SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="d6512-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="d6512-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6512-135">PARAMETERS</span></span>

### <span data-ttu-id="d6512-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6512-136">-AsJob</span></span>
<span data-ttu-id="d6512-137">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d6512-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6512-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d6512-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="d6512-139">Az SQL-adatbázis biztonsági másolatai tárolásához használt biztonsági mentési tárterület-redundancia.</span><span class="sxs-lookup"><span data-stu-id="d6512-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="d6512-140">A beállítások a helyi, a zóna és a földrajzi hely.</span><span class="sxs-lookup"><span data-stu-id="d6512-140">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="d6512-141">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="d6512-141">-ComputeGeneration</span></span>
<span data-ttu-id="d6512-142">A visszaállított adatbázishoz hozzárendelni megfelelő számítási generáció</span><span class="sxs-lookup"><span data-stu-id="d6512-142">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="d6512-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6512-143">-DefaultProfile</span></span>
<span data-ttu-id="d6512-144">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d6512-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6512-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="d6512-145">-DeletionDate</span></span>
<span data-ttu-id="d6512-146">A törlési dátumot **DateTime-objektumként** adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6512-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="d6512-147">**DateTime-objektum** betöltéshez használja a Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d6512-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d6512-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="d6512-148">-Edition</span></span>
<span data-ttu-id="d6512-149">Az SQL-adatbázis kiadását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d6512-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="d6512-150">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="d6512-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6512-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="d6512-151">None</span></span>
- <span data-ttu-id="d6512-152">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="d6512-152">Basic</span></span>
- <span data-ttu-id="d6512-153">Normál</span><span class="sxs-lookup"><span data-stu-id="d6512-153">Standard</span></span>
- <span data-ttu-id="d6512-154">Prémium</span><span class="sxs-lookup"><span data-stu-id="d6512-154">Premium</span></span>
- <span data-ttu-id="d6512-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="d6512-155">DataWarehouse</span></span>
- <span data-ttu-id="d6512-156">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="d6512-156">Free</span></span>
- <span data-ttu-id="d6512-157">Nyújtás</span><span class="sxs-lookup"><span data-stu-id="d6512-157">Stretch</span></span>
- <span data-ttu-id="d6512-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="d6512-158">GeneralPurpose</span></span>
- <span data-ttu-id="d6512-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="d6512-159">BusinessCritical</span></span>

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

### <span data-ttu-id="d6512-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d6512-160">-ElasticPoolName</span></span>
<span data-ttu-id="d6512-161">Annak a rugalmas készletnek a neve, amelybe az SQL-adatbázist be kell tenni.</span><span class="sxs-lookup"><span data-stu-id="d6512-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="d6512-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="d6512-163">Azt jelzi, hogy ez a parancsmag visszaállít egy adatbázist egy törölt SQL-adatbázis biztonsági másolatából.</span><span class="sxs-lookup"><span data-stu-id="d6512-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="d6512-164">A Get-AzSqlDeletedDatabaseBackup parancsmag használatával lekértheti a törölt SQL-adatbázis biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="d6512-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="d6512-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-165">-FromGeoBackup</span></span>
<span data-ttu-id="d6512-166">Azt jelzi, hogy ez a parancsmag földrajzi redundáns biztonsági másolatból visszaállít egy SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d6512-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="d6512-167">A Get-AzSqlDatabaseGeoBackup parancsmag használatával georedundáns biztonsági másolatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="d6512-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="d6512-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="d6512-169">Azt jelzi, hogy ez a parancsmag visszaállít egy SQL-adatbázist egy hosszú távú adatmegőrzési biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="d6512-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="d6512-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="d6512-171">Azt jelzi, hogy ez a parancsmag visszaállít egy SQL-adatbázist egy időben biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="d6512-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="d6512-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d6512-172">-LicenseType</span></span>
<span data-ttu-id="d6512-173">Az Azure Sql-adatbázis licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="d6512-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="d6512-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="d6512-174">-PointInTime</span></span>
<span data-ttu-id="d6512-175">Azt az időpontot adja meg  DateTime-objektumként, amelybe vissza szeretné állítani az SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d6512-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="d6512-176">**DateTime-objektum** betöltéshez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d6512-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="d6512-177">Használja ezt a paramétert a *FromPointInTimeBackup paraméterrel* együtt.</span><span class="sxs-lookup"><span data-stu-id="d6512-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="d6512-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6512-178">-ResourceGroupName</span></span>
<span data-ttu-id="d6512-179">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a parancsmag hozzárendeli az SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d6512-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="d6512-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6512-180">-ResourceId</span></span>
<span data-ttu-id="d6512-181">A visszaállítani szükséges erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6512-181">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="d6512-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6512-182">-ServerName</span></span>
<span data-ttu-id="d6512-183">Az SQL-adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6512-183">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="d6512-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d6512-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="d6512-185">A szolgáltatás-célként megadott célként megadott név.</span><span class="sxs-lookup"><span data-stu-id="d6512-185">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="d6512-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6512-186">-TargetDatabaseName</span></span>
<span data-ttu-id="d6512-187">Annak az adatbázisnak a nevét adja meg, amelybe vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="d6512-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="d6512-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="d6512-188">-VCore</span></span>
<span data-ttu-id="d6512-189">A visszaállított Azure Sql-adatbázis Vcore-számai.</span><span class="sxs-lookup"><span data-stu-id="d6512-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="d6512-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6512-190">-Confirm</span></span>
<span data-ttu-id="d6512-191">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d6512-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6512-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6512-192">-WhatIf</span></span>
<span data-ttu-id="d6512-193">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d6512-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6512-194">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6512-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6512-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6512-195">CommonParameters</span></span>
<span data-ttu-id="d6512-196">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6512-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6512-197">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6512-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6512-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6512-198">INPUTS</span></span>

### <span data-ttu-id="d6512-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d6512-199">System.DateTime</span></span>

### <span data-ttu-id="d6512-200">System.String</span><span class="sxs-lookup"><span data-stu-id="d6512-200">System.String</span></span>

## <span data-ttu-id="d6512-201">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6512-201">OUTPUTS</span></span>

### <span data-ttu-id="d6512-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d6512-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d6512-203">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6512-203">NOTES</span></span>

## <span data-ttu-id="d6512-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6512-204">RELATED LINKS</span></span>

[<span data-ttu-id="d6512-205">Azure SQL-adatbázis helyreállítása kimaradásból</span><span class="sxs-lookup"><span data-stu-id="d6512-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="d6512-206">Azure SQL-adatbázis helyreállítása felhasználói hibából</span><span class="sxs-lookup"><span data-stu-id="d6512-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="d6512-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d6512-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="d6512-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="d6512-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d6512-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="d6512-210">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d6512-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

