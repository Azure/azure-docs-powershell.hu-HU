---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: e7110511840542b8efed22b1267b76074434b94a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672343"
---
# Restore-AzureRmSqlDatabase

## Áttekintés
SQL-adatbázis visszaállítása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### FromPointInTimeBackup
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedDatabaseBackup
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromGeoBackup
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### FromLongTermRetentionBackup
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Restore-AzureRmSqlDatabase** PARANCSMAG egy SQL-adatbázist egy geo-redundáns biztonsági másolatból, egy törölt adatbázis biztonsági másolatával, egy hosszú távú adatmegőrzési biztonsági másolatból vagy egy aktív adatbázis időpontjának időpontjából áll vissza.
A helyreállított adatbázis új adatbázisként jön létre.

Rugalmas SQL-adatbázist úgy hozhat létre, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.

## Példák

### Példa 1: adatbázis visszaállítása időpontból
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.

A második parancs visszaállítja az adatbázist $Database a megadott időpontos biztonsági másolatról a RestoredDatabase nevű adatbázisra.

### 2. példa: adatbázis visszaállítása időpontból egy rugalmas készletbe
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

Az első parancs a Database01 nevű SQL-adatbázist kapja, majd a $Database változóban tárolja.

A második parancs visszaállítja az adatbázis $Database a megadott időpontos biztonsági másolatból az RestoredDatabase nevű SQL-adatbázisba a elasticpool01 nevű rugalmas készletben.

### 3. példa: törölt adatbázis visszaállítása
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.
A második parancs a visszaállítás [– AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) parancsmag használatával elindítja a törölt adatbázis biztonsági másolatának visszaállítását. Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.

### Példa 4: törölt adatbázis visszaállítása rugalmas készletbe
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

Az első parancs beolvassa a törölt adatbázis biztonsági másolatát, amelyet a [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)segítségével vissza szeretne állítani.
A második parancs elindítja a visszaállítást a törölt adatbázis biztonsági másolatból a [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)használatával. Ha a-PointInTime paraméter nincs megadva, az adatbázis visszakerül a törlési időpontra.

### Példa 5: adatbázis Geo-Restore
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

Az első parancs megkapja a Database01 nevű adatbázis geo-redundáns biztonsági másolatát, majd a $GeoBackup változóban tárolja.

A második parancs visszaállítja a biztonsági mentést $GeoBackup a RestoredDatabase nevű SQL-adatbázisba.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeletionDate
A törlési dátumot **datetime** típusú objektumként adja meg.
A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Kiadás
Az SQL-adatbázis kiadását adja meg.
A paraméter elfogadható értékei a következők:

- Nincs
- Prémium verzió
- Egyszerű
- Standard
- Adattárházi
- Ingyenes

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ElasticPoolName
Annak a rugalmas készletnek a nevét adja meg, amelybe az SQL-adatbázist el szeretné helyezni.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FromDeletedDatabaseBackup
Jelzi, hogy ez a parancsmag visszaállítja az adatbázist egy törölt SQL-adatbázis biztonsági másolatával.
A törölt SQL-adatbázisok biztonsági másolatának beszerzéséhez használhatja az Get-AzureRMSqlDeletedDatabaseBackup parancsmagot.

```yaml
Type: SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromGeoBackup
Jelzi, hogy ez a parancsmag visszaállítja egy SQL-adatbázist egy geo-redundáns biztonsági másolatból.
Geo-redundáns biztonsági másolat készítéséhez használhatja az Get-AzureRMSqlDatabaseGeoBackup parancsmagot.

```yaml
Type: SwitchParameter
Parameter Sets: FromGeoBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromLongTermRetentionBackup
Azt jelzi, hogy ez a parancsmag hosszú távú adatmegőrzési biztonsági másolatból állítja vissza az SQL-adatbázisokat.

```yaml
Type: SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromPointInTimeBackup
Azt jelzi, hogy ez a parancsmag visszaállítja az SQL-adatbázist egy időpontos biztonsági másolatból.

```yaml
Type: SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PointInTime
Annak az időpontnak a időpontját adja meg **datetime** -objektumként, amelynek vissza szeretné ÁLLÍTANI az SQL-adatbázisát.
Ha **datetime** típusú objektumot szeretne kapni, használja a **Get-Date** parancsmagot.

Használja ezt a paramétert a *FromPointInTimeBackup* paraméterrel együtt.

```yaml
Type: DateTime
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag hozzárendeli az SQL-adatbázist.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A visszaállítandó erőforrás AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kiszolgálónév
Az SQL adatbázis-kiszolgáló nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjectiveName
A szolgáltatási cél nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetDatabaseName
Itt adhatja meg annak az adatbázisnak a nevét, amelynek vissza szeretné állítani.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis helyreállítása leállás esetén](https://go.microsoft.com/fwlink/?LinkId=746882)

[Azure SQL-adatbázis helyreállítása felhasználói hibából](https://go.microsoft.com/fwlink/?LinkId=746944)

[Get-AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[Get-AzureRMSqlDatabaseGeoBackup](./Get-AzureRMSqlDatabaseGeoBackup.md)

[Get-AzureRMSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)

