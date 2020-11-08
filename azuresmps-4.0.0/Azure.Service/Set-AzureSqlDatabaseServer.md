---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015864"
---
# Set-AzureSqlDatabaseServer

## Áttekintés
Módosítja egy Azure SQL-adatbázis kiszolgálójának tulajdonságait.

## SZINTAXISA

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureSqlDatabaseServer** parancsmag az Azure SQL Database Server adott példányának tulajdonságait módosítja.
Az aktuális kiadásban csak a kiszolgáló rendszergazdai fiók jelszavát tudja frissíteni.

## Példák

### Példa 1: a kiszolgáló jelszavának módosítása
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

Ez a parancs módosítja a lpqd0zbr8y nevű Azure SQL Database Server rendszergazdai fiókjának jelszavát.

## PARAMÉTEREK

### -AdminPassword
Az Azure SQL adatbázis-kiszolgáló rendszergazdai fiókjának jelszavát adja meg.
Meg kell adnia egy erős jelszót.
További információt az [erős jelszavak](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) a Microsoft fejlesztői hálózata) című témakörben talál.

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

### -Kiszolgálónév
Itt adhatja meg annak a kiszolgálónak a nevét, amelyet a parancsmag módosított.
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

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServer](./Get-AzureSqlDatabaseServer.md)

[Új – AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[Remove-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)


