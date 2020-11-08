---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016559"
---
# Get-AzureSqlRecoverableDatabase

## Áttekintés
Helyreállítható adatbázisokat kap egy megadott kiszolgálóról.

## SZINTAXISA

### AllDatabasesOnGivenServer (alapértelmezett)
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GivenDatabaseOnGivenServer
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### GivenDatabaseObject
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlRecoverableDatabase** parancsmag visszanyerhető adatbázisokat kap egy megadott kiszolgálóról.
Ez a parancsmag meghatározott helyreállítható adatbázis vagy a kiszolgálón található összes helyreállítható adatbázis bevezetésére szolgál.

## Példák

### Példa 1: a helyreállítható adatbázisok beszerzése
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

Ez a parancs a Server01 nevű kiszolgálón a helyreállítható adatbázisokat kapja meg.

### 2. példa: meghatározott helyreállítható adatbázis beszerzése
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

A parancs beolvassa a Database17 nevű adatbázist a Server01 nevű kiszolgálón.

## PARAMÉTEREK

### -Database (adatbázis)
Itt adhatja meg azt az objektumot, amely a parancsmag által elérhető helyreállítható adatbázisnak felel meg.

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Annak a helyreállítható adatbázisnak a nevét adja meg, amely a parancsmagot kapja.

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
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

### -Kiszolgálónév
Annak a kiszolgálónak a neve, amelyből a parancsmag helyreállítható adatbázisokat kap.

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
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

### Microsoft. WindowsAzure. Management. SQL. models. RecoverableDatabase

## KIMENETEK

### IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## MEGJEGYZI
* A parancsmag futtatásához tanúsítványon alapuló hitelesítést kell használnia. Futtassa az alábbi parancsokat azon a számítógépen, amelyen a parancsmag futtatható: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Helyreállítható adatbázis beszerzése](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


