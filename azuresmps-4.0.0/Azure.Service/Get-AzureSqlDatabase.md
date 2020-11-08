---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016298"
---
# Get-AzureSqlDatabase

## Áttekintés
Egy vagy több adatbázis beolvasása

## SZINTAXISA

### ByConnectionContext (alapértelmezett)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabase** parancsmag egy Azure SQL-adatbázis egy vagy több példányát kéri egy Azure SQL adatbázis-kiszolgálóról.
Megadhatja azt a kiszolgálót, amely a **New-AzureSqlDatabaseServerContext** parancsmaggal létrehozott Azure SQL adatbázis-kiszolgáló kapcsolati környezettel rendelkezik.
Ha az Azure SQL-adatbázis kiszolgálójának nevét adja meg, a parancsmag az aktuális Azure-előfizetési adatokkal hitelesíti a kiszolgáló elérésére vonatkozó kérést.

Ha nem ad meg adatbázist, a **Get-AzureSqlDatabase** parancsmag a megadott kiszolgáló összes adatbázisát adja eredményül.

Helyreállítható ledobott adatbázisok beolvasása:

Helyreállítható ledobott adatbázisok beolvasása a *RestorableDropped* paraméter használatával.
Az összes helyreállítható ledobott adatbázis visszaadásához használja a *RestorableDropped* paramétert a *databasename* és a *DatabaseDeletionDate* nélkül.
Egy bizonyos helyreállítható ledobott adatbázis visszaadásához használja a *RestorableDropped* paramétert a *databasename* és a *DatabaseDeletionDate* paraméterrel.
Ha a *databasename* paraméterrel egy bizonyos helyreállítható ledobott adatbázist keres, akkor a *DatabaseDeletionDate* paramétert is tartalmaznia kell, és a megadott *DatabaseDeletionDate* értéknek tartalmaznia kell egy ezredmásodpercet, hogy megfeleljen a kívánt adatbázisnak.

A **Get-AzureSqlDatabase** parancsmag a kiszolgálón található összes helyreállítható, illetve a *databasename* és a *DatabaseDeletionDate* -ban egyaránt megfelelő adatbázis esetén visszaadott adatbázist ad vissza.
Ha olyan helyreállítható, visszavezethető adatbázisokat szeretne visszaadni, amelyek eltérő feltételekkel (például az összes helyreállítható ledobott adatbázissal) felelnek meg

## Példák

### Példa 1: az összes adatbázis lekérése a kiszolgálón
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Ez a parancs a lpqd0zbr8y nevű kiszolgálón lekérdezi az összes adatbázist.

### 2. példa: az összes helyreállítható ledobott adatbázis lekérése a kiszolgálón
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

Ez a parancs a lpqd0zbr8y nevű kiszolgálón lekéri az összes helyreállítható ledobott adatbázist.

### 3. példa: adatbázis lekérése a kapcsolati környezet által meghatározott kiszolgálóról
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Ez a parancs a Database01 nevű adatbázist a kapcsolati környezet $Context által megadott kiszolgálóról kéri le.

### 4. példa: adatbázis-objektum tárolása egy változóban
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Ez a parancs a Database01 nevű adatbázist a lpqd0zbr8y nevű kiszolgálóról lekérdezi.
A parancs a $Database 01 változóban tárolja az adatbázis-objektumot.

### Példa 5: helyreállítható ledobott adatbázis beolvasása
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

Ez a parancs beolvassa a Database01 nevű, 11/9/2012 nevű, a lpqd0zbr8y nevű kiszolgálóról törölt visszaállító adatbázist.
Ez a parancs az eredményt a $DroppedDB változóban tárolja.

### 6. példa: az összes helyreállítható ledobott adatbázis lekérése a kiszolgálón és a találatok szűrése
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

Ez a parancs beolvassa az összes helyreállítható ledobott adatbázist a lpqd0zbr8y nevű kiszolgálón, majd az eredményeket csak a ContactDB nevű adatbázisokra szűri.

## PARAMÉTEREK

### -ConnectionContext
Annak a kiszolgálónak a kapcsolati környezetét adja meg, amelyből adatbázist szeretne beolvasni.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Database (adatbázis)
Itt adhatja meg azt az adatbázist, amely a parancsmag által lekérdezett adatbázist jelöli.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
A törlés dátumát és időpontját adja meg.
Ha a *RestorableDropped* paramétert adja meg, ezt a paramétert akkor adja meg, ha a törlés dátuma és időpontja alapján visszaállíthatja a helyreállítható ledobott adatbázist.

A *DatabaseDeletionDate* paraméternek tartalmaznia kell egy ezredmásodpercet a kívánt adatbázis időpontjának megfelelően.
Az érték megadásával milliszekundum nélkül az adatbázis nem található.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Itt adhatja meg annak az adatbázisnak a nevét, amely a parancsmagot kéri.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDropped
Azt jelzi, hogy ez a parancsmag az *adatbázis* -objektumok helyett az *RestorableDroppedDatabase* -objektumokat adja eredményül.
A *DatabaseDeletionDate* paraméterrel kiválaszthat egy bizonyos helyreállítható ledobott adatbázist.

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

### -RestorableDroppedDatabase
Itt adhatja meg azt az objektumot, amely a parancsmag által beolvasott helyreállítható adatbázisnak a megfelelője.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kiszolgálónév
Megadja annak a kiszolgálónak a nevét, amely a parancsmag által lekérdezett adatbázist tartalmazza.
A parancsmag az aktuális Azure-előfizetést használja a kiszolgáló eléréséhez.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. RestorableDroppedDatabase

## KIMENETEK

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
Ez a parancsmag egy *adatbázis* -objektumot ad eredményül, ha nem adja meg a *RestorableDropped* paramétert.

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
Ez a parancsmag *RestorableDroppedDatabase* -objektumot ad eredményül, ha a *RestorableDropped* paramétert adja meg.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Új – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Új – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


