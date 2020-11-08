---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015426"
---
# Start-AzureSqlDatabaseRestore

## Áttekintés
Időpontot ad vissza az adatbázis időpontjában.

## SZINTAXISA

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureSqlDatabaseRestore** parancsmag egy egyszerű, normál vagy prémium adatbázis időpontjának visszaállítását végzi.
Az Azure SQL-adatbázis az alapszintű adatbázis biztonsági másolatait 7 nappal, a 14 napra szóló standardot és a 35 napokra szóló prémium verziót őrzi meg.
A visszaállítási művelet új adatbázist hoz létre.
Ha a forrásadatbázis nem törlődik, a *SourceDatabaseName* és a *TargetDatabaseName* paraméternek eltérő értékűnek kell lennie.

Az Azure SQL-adatbázis jelenleg nem támogatja a Cross Server Restore-t.
A forrás-és a célkiszolgáló nevének egyeznie kell.

## Példák

### Példa 1: objektumként megadott adatbázis visszaállítása időpontra
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Az első parancs a Server01 nevű kiszolgálón a Database17 nevű adatbázis adatbázis-objektumát kapja, majd a $Database változóban tárolja.

A második parancs visszaállítja az adatbázist egy adott időpontra.
A parancs az új adatbázis nevét adja meg.

### 2. példa: név szerint meghatározott adatbázis visszaállítása időpontra
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

A parancs visszaállítja a Database17 nevű adatbázist adott időpontra.
A parancs az új adatbázis nevét adja meg.

### 3. példa: az adott időpontig objektumként megadott leejtett adatbázis visszaállítása
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

Az első parancs a Server01 nevű kiszolgálón a Database01 nevű adatbázis adatbázis-objektumát kapja.
A parancs a *RestorableDropped* paramétert adja meg.
Ezért a parancsmag a megadott visszaállítási pontra visszaállíthatja a helyreállítható adatbázisokat.
A parancs a $Database változóban tárolja az adatbázis-objektumot.

A második parancs visszaállítja az $Database által megadott eldobott adatbázist.
A parancs az új adatbázis nevét adja meg.

## PARAMÉTEREK

### -PointInTime
Az adatbázis visszaállítási pontját adja meg.
Amikor befejezte a visszaállítási műveletet, az adatbázis visszakerül az állapotra, amely a paraméter által megadott dátum és idő szerint van meghatározva.
Alapértelmezés szerint ez a parancsmag az aktuális időpontra van beállítva, és egy leejtett adatbázis esetében az adatbázis elvetésének időpontját használja.

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
Jelzi, hogy ez a parancsmag visszaállíthatja a helyreállítható ledobott adatbázist.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag visszaállítja.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Az adatbázis törlésének dátumát és időpontját adja meg.
Ha a tényleges adatbázis-törlési időpontot adja meg, akkor az ezredmásodpercet is tartalmaznia kell.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Annak az élő adatbázisnak a nevét adja meg, amelyre a parancsmag visszaállítja.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Itt adhatja meg azt az objektumot, amely a parancsmag által visszaállítható visszaállító adatbázist jelképezi.
Ha **RestorableDroppedDatabase** objektumot szeretne beolvasni, használja az Get-AzureSqlDatabase parancsmagot, és adja meg a *RestorableDropped* paramétert.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Annak a kiszolgálónak a neve, amelyen a forrásadatbázis él és fut, vagy amelyen a forrásadatbázis a törlés előtt futott.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Annak az új adatbázisnak a neve, amely a visszaállítási műveletet hozza létre.

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

### -TargetServerName
Annak a kiszolgálónak a nevét adja meg, amelyre a parancsmag visszaállítja az adatbázist.

Az Azure SQL-adatbázis jelenleg nem támogatja a Cross Server Restore-t.
A forrás-és a célkiszolgáló nevének egyeznie kell.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database

## KIMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. RestoreDatabaseOperation

## MEGJEGYZI
* A parancsmag futtatásához tanúsítványon alapuló hitelesítést kell használnia. Futtassa az alábbi parancsokat azon a számítógépen, amelyen a parancsmag futtatható: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Adatbázis-visszaállítási kérés létrehozása](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


