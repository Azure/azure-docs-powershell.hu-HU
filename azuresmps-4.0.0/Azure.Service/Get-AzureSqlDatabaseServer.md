---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015571"
---
# Get-AzureSqlDatabaseServer

## Áttekintés
Információt kap az Azure SQL-adatbázis kiszolgálóiról.

## SZINTAXISA

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabaseServer** parancsmag információt kap az Azure SQL Database Server példányairól az aktuális előfizetésben.
Ha a kiszolgálót név szerint adja meg, ez a parancsmag egy olyan objektumot ad eredményül, amely a kiszolgálón lévő információkat tartalmazza.
Egyéb esetben a parancsmag az összes kiszolgálóról ad információt.

## Példák

### 1. példa: információk kérése az összes kiszolgálóról
```
PS C:\> Get-AzureSqlDatabaseServer
```

Ez a parancs a jelenlegi előfizetésben az Azure SQL-adatbázis kiszolgálójának összes példányáról ad információt.

### 2. példa: információk kérése egy adott kiszolgálóról
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

Ez a parancs információt ad eredményül a lpqd0zbr8y nevű kiszolgálóról.

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

### -Kiszolgálónév
Annak a kiszolgálónak a nevét adja meg, amely a parancsmagot eltávolítja.
Adja meg a kiszolgáló nevét, nem a teljesen minősített DNS-nevet.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext

## KIMENETEK

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Kiszolgálók listája](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Új – AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[Remove-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)

[Set-AzureSqlDatabaseServer](./Set-AzureSqlDatabaseServer.md)


