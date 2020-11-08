---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015572"
---
# Get-AzureSqlDatabaseServerFirewallRule

## Áttekintés
Tűzfal-szabályok beolvasása az Azure SQL adatbázis-kiszolgálón.

## SZINTAXISA

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabaseServerFirewallRule** parancsmag tűzfal-szabályokat kap az Azure SQL-adatbázis-kiszolgálók egy példányához.
Ha a tűzfal szabályát név szerint adja meg, ez a parancsmag információt ad a tűzfalszabályról.
Máskülönben a parancsmag információt ad a megadott Azure SQL-adatbázis-kiszolgálón lévő összes tűzfal-szabályról.

## Példák

### Példa 1: a tűzfal összes szabályának beolvasása a kiszolgálón
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

Ez a parancs a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón a tűzfalszabályok összes szabályát megkapja.

### 2. példa: tűzfalszabály beszerzése a neve alapján
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

Ez a parancs a FirewallRule24 nevű tűzfal-szabályt a lpqd0zbr8y nevű kiszolgálón kapja meg.

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

### -RuleName
Annak a tűzfal-szabálynak a neve, amely a parancsmagot kapja.

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

### -Kiszolgálónév
A kiszolgáló nevét adja meg.
Ez a parancsmag tűzfal-szabályokat kap a kiszolgálótól, amelyre ez a paraméter adja meg.
Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext

## KIMENETEK

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Tűzfal-szabályok listázása](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Új – AzureSqlDatabaseServerFirewallRule](./New-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


