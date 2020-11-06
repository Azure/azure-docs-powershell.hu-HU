---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494614"
---
# <span data-ttu-id="81a08-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81a08-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="81a08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81a08-102">SYNOPSIS</span></span>
<span data-ttu-id="81a08-103">SQL-adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="81a08-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81a08-104">SYNTAX</span></span>

### <span data-ttu-id="81a08-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81a08-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81a08-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81a08-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81a08-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="81a08-109">DESCRIPTION</span></span>
<span data-ttu-id="81a08-110">A **Restore-AzureRmSqlDatabase** PARANCSMAG egy SQL-adatbázist egy geo-redundáns biztonsági másolatból, egy törölt adatbázis biztonsági másolatával, egy hosszú távú adatmegőrzési biztonsági másolatból vagy egy aktív adatbázis időpontjának időpontjából áll vissza.</span><span class="sxs-lookup"><span data-stu-id="81a08-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="81a08-111">A helyreállított adatbázis új adatbázisként jön létre.</span><span class="sxs-lookup"><span data-stu-id="81a08-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="81a08-112">Rugalmas SQL-adatbázist úgy hozhat létre, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="81a08-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="81a08-113">Példák</span><span class="sxs-lookup"><span data-stu-id="81a08-113">EXAMPLES</span></span>

### <span data-ttu-id="81a08-114">Példa 1: adatbázis visszaállítása időpontból</span><span class="sxs-lookup"><span data-stu-id="81a08-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="81a08-115">Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="81a08-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="81a08-116">A második parancs visszaállítja az adatbázist $Database a megadott időpontos biztonsági másolatról a RestoredDatabase nevű adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="81a08-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="81a08-117">2. példa: adatbázis visszaállítása időpontból egy rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="81a08-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="81a08-118">Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="81a08-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="81a08-119">A második parancs visszaállítja az adatbázis $Database a megadott időpontos biztonsági másolatból az RestoredDatabase nevű SQL-adatbázisba a elasticpool01 nevű rugalmas készletben.</span><span class="sxs-lookup"><span data-stu-id="81a08-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="81a08-120">3. példa: törölt adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="81a08-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="81a08-121">Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="81a08-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="81a08-122">A második parancs a visszaállítás [– AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) parancsmag használatával elindítja a törölt adatbázis biztonsági másolatának visszaállítását.</span><span class="sxs-lookup"><span data-stu-id="81a08-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="81a08-123">Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="81a08-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="81a08-124">Példa 4: törölt adatbázis visszaállítása rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="81a08-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="81a08-125">Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="81a08-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="81a08-126">A második parancs elindítja a visszaállítást a törölt adatbázis biztonsági másolatból a [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)használatával.</span><span class="sxs-lookup"><span data-stu-id="81a08-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="81a08-127">Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.</span><span class="sxs-lookup"><span data-stu-id="81a08-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="81a08-128">Példa 5: adatbázis Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="81a08-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="81a08-129">Az első parancs megkapja a Database01 nevű adatbázis geo-redundáns biztonsági másolatát, majd a $GeoBackup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="81a08-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="81a08-130">A második parancs visszaállítja a biztonsági mentést $GeoBackup a RestoredDatabase nevű SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="81a08-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="81a08-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81a08-131">PARAMETERS</span></span>

### <span data-ttu-id="81a08-132">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="81a08-132">-DeletionDate</span></span>
<span data-ttu-id="81a08-133">A törlési dátumot **datetime** típusú objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="81a08-133">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="81a08-134">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="81a08-134">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-135">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="81a08-135">-Edition</span></span>
<span data-ttu-id="81a08-136">Az SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="81a08-136">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="81a08-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="81a08-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81a08-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="81a08-138">None</span></span>
- <span data-ttu-id="81a08-139">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="81a08-139">Premium</span></span>
- <span data-ttu-id="81a08-140">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="81a08-140">Basic</span></span>
- <span data-ttu-id="81a08-141">Standard</span><span class="sxs-lookup"><span data-stu-id="81a08-141">Standard</span></span>
- <span data-ttu-id="81a08-142">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="81a08-142">DataWarehouse</span></span>
- <span data-ttu-id="81a08-143">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="81a08-143">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-144">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="81a08-144">-ElasticPoolName</span></span>
<span data-ttu-id="81a08-145">Annak a rugalmas készletnek a nevét adja meg, amelybe az SQL-adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="81a08-145">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-146">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-146">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="81a08-147">Jelzi, hogy ez a parancsmag visszaállítja az adatbázist egy törölt SQL-adatbázis biztonsági másolatával.</span><span class="sxs-lookup"><span data-stu-id="81a08-147">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="81a08-148">A törölt SQL-adatbázisok biztonsági másolatának beszerzéséhez használhatja az Get-AzureRMSqlDeletedDatabaseBackup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="81a08-148">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-149">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-149">-FromGeoBackup</span></span>
<span data-ttu-id="81a08-150">Jelzi, hogy ez a parancsmag visszaállítja egy SQL-adatbázist egy geo-redundáns biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="81a08-150">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="81a08-151">Geo-redundáns biztonsági másolat készítéséhez használhatja az Get-AzureRMSqlDatabaseGeoBackup parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="81a08-151">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-152">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-152">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="81a08-153">Azt jelzi, hogy ez a parancsmag hosszú távú adatmegőrzési biztonsági másolatból állítja vissza az SQL-adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="81a08-153">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-154">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-154">-FromPointInTimeBackup</span></span>
<span data-ttu-id="81a08-155">Azt jelzi, hogy ez a parancsmag visszaállítja az SQL-adatbázist egy időpontos biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="81a08-155">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-156">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="81a08-156">-PointInTime</span></span>
<span data-ttu-id="81a08-157">Annak az időpontnak a időpontját adja meg **datetime** -objektumként, amelynek vissza szeretné ÁLLÍTANI az SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="81a08-157">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="81a08-158">Ha **datetime** típusú objektumot szeretne kapni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="81a08-158">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="81a08-159">Használja ezt a paramétert a *FromPointInTimeBackup* paraméterrel együtt.</span><span class="sxs-lookup"><span data-stu-id="81a08-159">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a08-160">-ResourceGroupName</span></span>
<span data-ttu-id="81a08-161">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli az SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="81a08-161">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="81a08-162">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81a08-162">-ResourceId</span></span>
<span data-ttu-id="81a08-163">A visszaállítandó erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="81a08-163">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="81a08-164">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="81a08-164">-ServerName</span></span>
<span data-ttu-id="81a08-165">Az SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81a08-165">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="81a08-166">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="81a08-166">-ServiceObjectiveName</span></span>
<span data-ttu-id="81a08-167">A szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81a08-167">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-168">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="81a08-168">-TargetDatabaseName</span></span>
<span data-ttu-id="81a08-169">Itt adhatja meg annak az adatbázisnak a nevét, amelynek vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="81a08-169">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="81a08-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a08-170">-DefaultProfile</span></span>
<span data-ttu-id="81a08-171">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81a08-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a08-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a08-172">CommonParameters</span></span>
<span data-ttu-id="81a08-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81a08-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a08-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a08-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a08-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81a08-175">INPUTS</span></span>

## <span data-ttu-id="81a08-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81a08-176">OUTPUTS</span></span>

### <span data-ttu-id="81a08-177">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="81a08-177">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="81a08-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81a08-178">NOTES</span></span>

## <span data-ttu-id="81a08-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81a08-179">RELATED LINKS</span></span>

[<span data-ttu-id="81a08-180">Azure SQL-adatbázis helyreállítása leállás esetén</span><span class="sxs-lookup"><span data-stu-id="81a08-180">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="81a08-181">Azure SQL-adatbázis helyreállítása felhasználói hibából</span><span class="sxs-lookup"><span data-stu-id="81a08-181">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="81a08-182">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81a08-182">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="81a08-183">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-183">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="81a08-184">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="81a08-184">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="81a08-185">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="81a08-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

