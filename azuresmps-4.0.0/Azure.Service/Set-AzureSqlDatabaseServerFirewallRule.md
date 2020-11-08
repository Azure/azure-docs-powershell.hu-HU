---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015863"
---
# Set-AzureSqlDatabaseServerFirewallRule

## Áttekintés
A meglévő tűzfalszabályok módosítása egy Azure SQL-adatbázis-kiszolgálón.

## SZINTAXISA

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureSqlDatabaseServerFirewallRule** parancsmag az Azure SQL-adatbázis kiszolgálójának megadott példányában módosítja az IP-cím és a záró IP-cím értékét.

## Példák

### Példa 1: tűzfalszabály módosítása
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

Ez a parancs módosítja a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón a FirewallRule24 nevű tűzfal-szabály kezdő IP-címét és IP-címét.

## PARAMÉTEREK

### -EndIpAddress
A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.

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

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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
Annak a tűzfal-szabálynak a neve, amelyet a parancsmag módosított.

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

### -Kiszolgálónév
A kiszolgáló nevét adja meg.
Ez a parancsmag létrehoz egy tűzfal-szabályt azon a kiszolgálón, amelyen a parancsmag meg van határozva.
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

### -StartIpAddress
A tűzfalszabály IP-címtartomány kezdetének értékét adja meg.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext

## KIMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Tűzfalszabály beállítása](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Új – AzureSqlDatabaseServerFirewallRule](./New-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)


