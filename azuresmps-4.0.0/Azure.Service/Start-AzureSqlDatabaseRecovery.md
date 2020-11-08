---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015423"
---
# Start-AzureSqlDatabaseRecovery

## Áttekintés
Egy adatbázis visszaállítási kérését kezdeményezi.

## SZINTAXISA

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureSqlDatabaseRecovery** parancsmag visszahívási kérést kezdeményez egy élő vagy ledobott adatbázishoz.
Ez a parancsmag támogatja az adatbázis utolsó ismert elérhető biztonsági másolatát használó alapszintű helyreállítást.
A helyreállítási művelet új adatbázist hoz létre.
Ha ugyanazon a kiszolgálón visszaállít egy élő adatbázist, az új adatbázisnak meg kell adnia egy másik nevet.

Ha egy adatbázis időpontját szeretné visszaállítani, használja inkább a **Start-AzureSqlDatabaseRestore** parancsmagot.

## Példák

### Példa 1: objektumként megadott adatbázis helyreállítása
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

Az első parancs az adatbázis-objektumot a **Get-AzureSqlRecoverableDatabase** parancsmag segítségével kapja meg.
A parancs az objektumot a $Database változóban tárolja.

A második parancs visszanyeri az adatbázis $Database-ban tárolt adatbázisát.

### 2. példa: név szerint megadott adatbázis helyreállítása
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

A parancs az adatbázis nevével visszanyeri az adatbázist.

## PARAMÉTEREK

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

### -SourceDatabase
Azt az adatbázis-objektumot adja meg, amely a parancsmag által helyreállított adatbázisnak felel meg.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag visszanyeri.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Annak a kiszolgálónak a neve, amelyen a forrásadatbázis él és fut, vagy amelyen a forrásadatbázis a törlés előtt futott.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
A helyreállított adatbázis nevét adja meg.
Ha a forrásadatbázis továbbra is él, a forrás-adatbázis nevétől eltérő nevet kell megadnia.

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

### -TargetServerName
Megadja annak a kiszolgálónak a nevét, amelynek az adatbázisát vissza szeretné állítani.
Egy adatbázis visszaállítható ugyanazon a kiszolgálón vagy egy másik kiszolgálón is.

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

### Microsoft. WindowsAzure. Management. SQL. models. RecoverableDatabase

## KIMENETEK

### Microsoft. WindowsAzure. Management. SQL. models. RecoverDatabaseOperation

## MEGJEGYZI
* A parancsmag futtatásához tanúsítványon alapuló hitelesítést kell használnia. Futtassa az alábbi parancsokat azon a számítógépen, amelyen futtatja ezt a parancsmagot: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Adatbázis-helyreállítási kérés létrehozása](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Geo-replikáció az Azure SQL-adatbázisban](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[Start-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


