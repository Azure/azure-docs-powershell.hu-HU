---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: 6b6c6c23fbabec663bb2e9863bb7090d5c869802
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013479"
---
# <span data-ttu-id="8682a-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8682a-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="8682a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8682a-102">SYNOPSIS</span></span>
<span data-ttu-id="8682a-103">SQL-adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="8682a-103">Restores a SQL database.</span></span>

## <span data-ttu-id="8682a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8682a-104">SYNTAX</span></span>

### <span data-ttu-id="8682a-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682a-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="8682a-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682a-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682a-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="8682a-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682a-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8682a-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="8682a-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682a-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8682a-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="8682a-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8682a-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="8682a-113">DESCRIPTION</span></span>
<span data-ttu-id="8682a-114">A **Restore-AzSqlDatabase** PARANCSMAG egy SQL-adatbázist egy geo-redundáns biztonsági másolatból, egy törölt adatbázis biztonsági másolatával, egy hosszú távú adatmegőrzési biztonsági másolatból vagy egy aktív adatbázis időpontjának időpontjából áll vissza.</span><span class="sxs-lookup"><span data-stu-id="8682a-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="8682a-115">A helyreállított adatbázis új adatbázisként jön létre.</span><span class="sxs-lookup"><span data-stu-id="8682a-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="8682a-116">Rugalmas SQL-adatbázist úgy hozhat létre, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="8682a-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="8682a-117">Példák</span><span class="sxs-lookup"><span data-stu-id="8682a-117">EXAMPLES</span></span>

### <span data-ttu-id="8682a-118">Példa 1: adatbázis visszaállítása időpontból</span><span class="sxs-lookup"><span data-stu-id="8682a-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="8682a-119">Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8682a-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="8682a-120">A második parancs visszaállítja az adatbázist $Database a megadott időpontos biztonsági másolatról a RestoredDatabase nevű adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="8682a-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="8682a-121">2. példa: adatbázis visszaállítása időpontból egy rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="8682a-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="8682a-122">Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8682a-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="8682a-123">A második parancs visszaállítja az adatbázis $Database a megadott időpontos biztonsági másolatból az RestoredDatabase nevű SQL-adatbázisba a elasticpool01 nevű rugalmas készletben.</span><span class="sxs-lookup"><span data-stu-id="8682a-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="8682a-124">3. példa: törölt adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="8682a-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="8682a-125">Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="8682a-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="8682a-126">A második parancs a visszaállítás [– AzSqlDatabase](./Restore-AzSqlDatabase.md) parancsmag használatával elindítja a törölt adatbázis biztonsági másolatának visszaállítását.</span><span class="sxs-lookup"><span data-stu-id="8682a-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="8682a-127">Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="8682a-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="8682a-128">Példa 4: törölt adatbázis visszaállítása rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="8682a-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="8682a-129">Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="8682a-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="8682a-130">A második parancs elindítja a visszaállítást a törölt adatbázis biztonsági másolatból a [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)használatával.</span><span class="sxs-lookup"><span data-stu-id="8682a-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="8682a-131">Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="8682a-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="8682a-132">Példa 5: adatbázis Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="8682a-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="8682a-133">Az első parancs megkapja a Database01 nevű adatbázis geo-redundáns biztonsági másolatát, majd a $GeoBackup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8682a-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="8682a-134">A második parancs visszaállítja a biztonsági mentést $GeoBackup a RestoredDatabase nevű SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="8682a-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="8682a-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8682a-135">PARAMETERS</span></span>

### <span data-ttu-id="8682a-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8682a-136">-AsJob</span></span>
<span data-ttu-id="8682a-137">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8682a-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8682a-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8682a-138">-ComputeGeneration</span></span>
<span data-ttu-id="8682a-139">A visszaállított adatbázishoz rendelt számítási generálás</span><span class="sxs-lookup"><span data-stu-id="8682a-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="8682a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8682a-140">-DefaultProfile</span></span>
<span data-ttu-id="8682a-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8682a-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8682a-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="8682a-142">-DeletionDate</span></span>
<span data-ttu-id="8682a-143">A törlési dátumot **datetime** típusú objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="8682a-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="8682a-144">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8682a-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="8682a-145">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="8682a-145">-Edition</span></span>
<span data-ttu-id="8682a-146">Az SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8682a-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="8682a-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8682a-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8682a-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="8682a-148">None</span></span>
- <span data-ttu-id="8682a-149">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="8682a-149">Basic</span></span>
- <span data-ttu-id="8682a-150">Standard</span><span class="sxs-lookup"><span data-stu-id="8682a-150">Standard</span></span>
- <span data-ttu-id="8682a-151">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="8682a-151">Premium</span></span>
- <span data-ttu-id="8682a-152">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="8682a-152">DataWarehouse</span></span>
- <span data-ttu-id="8682a-153">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="8682a-153">Free</span></span>
- <span data-ttu-id="8682a-154">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="8682a-154">Stretch</span></span>
- <span data-ttu-id="8682a-155">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="8682a-155">GeneralPurpose</span></span>
- <span data-ttu-id="8682a-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="8682a-156">BusinessCritical</span></span>

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

### <span data-ttu-id="8682a-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8682a-157">-ElasticPoolName</span></span>
<span data-ttu-id="8682a-158">Annak a rugalmas készletnek a nevét adja meg, amelybe az SQL-adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="8682a-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="8682a-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="8682a-160">Jelzi, hogy ez a parancsmag visszaállítja az adatbázist egy törölt SQL-adatbázis biztonsági másolatával.</span><span class="sxs-lookup"><span data-stu-id="8682a-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="8682a-161">A törölt SQL-adatbázisok biztonsági másolatának beszerzéséhez használhatja az Get-AzSqlDeletedDatabaseBackup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8682a-161">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="8682a-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-162">-FromGeoBackup</span></span>
<span data-ttu-id="8682a-163">Jelzi, hogy ez a parancsmag visszaállítja egy SQL-adatbázist egy geo-redundáns biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="8682a-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="8682a-164">Geo-redundáns biztonsági másolat készítéséhez használhatja az Get-AzSqlDatabaseGeoBackup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8682a-164">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="8682a-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="8682a-166">Azt jelzi, hogy ez a parancsmag hosszú távú adatmegőrzési biztonsági másolatból állítja vissza az SQL-adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="8682a-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="8682a-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="8682a-168">Azt jelzi, hogy ez a parancsmag visszaállítja az SQL-adatbázist egy időpontos biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="8682a-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="8682a-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8682a-169">-LicenseType</span></span>
<span data-ttu-id="8682a-170">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="8682a-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="8682a-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="8682a-171">-PointInTime</span></span>
<span data-ttu-id="8682a-172">Annak az időpontnak a időpontját adja meg **datetime** -objektumként, amelynek vissza szeretné ÁLLÍTANI az SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="8682a-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="8682a-173">Ha **datetime** típusú objektumot szeretne kapni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8682a-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="8682a-174">Használja ezt a paramétert a *FromPointInTimeBackup* paraméterrel együtt.</span><span class="sxs-lookup"><span data-stu-id="8682a-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="8682a-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8682a-175">-ResourceGroupName</span></span>
<span data-ttu-id="8682a-176">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli az SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="8682a-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="8682a-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8682a-177">-ResourceId</span></span>
<span data-ttu-id="8682a-178">A visszaállítandó erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8682a-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="8682a-179">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8682a-179">-ServerName</span></span>
<span data-ttu-id="8682a-180">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8682a-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="8682a-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="8682a-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="8682a-182">A szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8682a-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="8682a-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8682a-183">-TargetDatabaseName</span></span>
<span data-ttu-id="8682a-184">Itt adhatja meg annak az adatbázisnak a nevét, amelynek vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="8682a-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="8682a-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="8682a-185">-VCore</span></span>
<span data-ttu-id="8682a-186">A helyreállított Azure SQL-adatbázis vcore száma.</span><span class="sxs-lookup"><span data-stu-id="8682a-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="8682a-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8682a-187">CommonParameters</span></span>
<span data-ttu-id="8682a-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8682a-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8682a-189">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8682a-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8682a-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8682a-190">INPUTS</span></span>

### <span data-ttu-id="8682a-191">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="8682a-191">System.DateTime</span></span>

### <span data-ttu-id="8682a-192">System. String</span><span class="sxs-lookup"><span data-stu-id="8682a-192">System.String</span></span>

## <span data-ttu-id="8682a-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8682a-193">OUTPUTS</span></span>

### <span data-ttu-id="8682a-194">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8682a-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8682a-195">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8682a-195">NOTES</span></span>

## <span data-ttu-id="8682a-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8682a-196">RELATED LINKS</span></span>

[<span data-ttu-id="8682a-197">Azure SQL-adatbázis helyreállítása leállás esetén</span><span class="sxs-lookup"><span data-stu-id="8682a-197">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="8682a-198">Azure SQL-adatbázis helyreállítása felhasználói hibából</span><span class="sxs-lookup"><span data-stu-id="8682a-198">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="8682a-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8682a-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8682a-200">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-200">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="8682a-201">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="8682a-201">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="8682a-202">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8682a-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

