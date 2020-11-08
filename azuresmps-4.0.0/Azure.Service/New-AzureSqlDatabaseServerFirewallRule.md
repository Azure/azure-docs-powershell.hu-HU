---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015969"
---
# New-AzureSqlDatabaseServerFirewallRule

## Áttekintés
Tűzfal-szabályt hoz létre az Azure SQL adatbázis-kiszolgálón.

## SZINTAXISA

### IpRange (alapértelmezett)
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AllowAllAzureServices
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureSqlDatabaseServerFirewallRule** parancsmag a jelenlegi előfizetésben az Azure SQL adatbázis-kiszolgáló meghatározott példányában hoz létre tűzfal-szabályt.

A *StartIpAddress* és a *EndIpAddress* paraméterrel megadhatja, hogy az IP-címek milyen TARTOMÁNNYAL csatlakozzanak az Azure SQL-adatbázis kiszolgálójához.

Adja meg a *AllowAllAzureServices* paramétert egy olyan szabály létrehozásához, amely engedélyezi az Azure-kapcsolatokat a kiszolgálón.
A szabály a 0.0.0.0 végződésű IP-cím értékeit tartalmazza.
Ha nem ad meg tűzfal-szabályt, ez a parancsmag az alapértelmezett név AllowAllAzureServices rendeli hozzá.

## Példák

### Példa 1: tűzfalszabály létrehozása
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

Ez a parancs létrehoz egy FirewallRule24 a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón.
A parancs IP-címtartományt ad meg.

### 2. példa: szabály létrehozása, amely lehetővé teszi az összes Azure-szolgáltatás beállítását
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

Ez a parancs létrehoz egy AzureConnections nevű tűzfal-szabályt a lpqd0zbr8y nevű kiszolgálón, amely lehetővé teszi az Azure-kapcsolatokat.

### 3. példa: szabály létrehozása, amely lehetővé teszi az alapértelmezett nevű összes Azure-szolgáltatás létrehozását, amely lehetővé teszi az alapértelmezett nevet használó összes Azure-szolgáltatás beállítását
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

A parancs létrehoz egy tűzfal-szabályt a lpqd0zbr8y nevű kiszolgálón, amely lehetővé teszi az Azure-kapcsolatokat.
A parancs hozzárendeli az alapértelmezett szabály nevét AllowAllAzureServices.

## PARAMÉTEREK

### -AllowAllAzureServices
Jelzi, hogy ez a tűzfalszabály engedélyezi az összes Azure IP-cím elérését a kiszolgálón.

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndIpAddress
A szabályhoz tartozó IP-címtartomány utolsó értékét adja meg.

```yaml
Type: String
Parameter Sets: IpRange
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
Az új tűzfalszabály nevét adja meg.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Parameter Sets: IpRange
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

## KIMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Tűzfalszabály létrehozása](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


