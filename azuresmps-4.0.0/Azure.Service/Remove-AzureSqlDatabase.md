---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016108"
---
# Remove-AzureSqlDatabase

## Áttekintés
Azure SQL-adatbázis törlése

## SZINTAXISA

### ByNameWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureSqlDatabase** parancsmag a kiszolgáló kapcsolati környezete vagy a kiszolgálónév alapján törli az Azure SQL-adatbázist.
Az Azure SQL Database Server kapcsolati környezetét a **New-AzureSqlDatabaseServerContext** parancsmaggal hozhatja létre, és ezt a parancsmagot használva használhatja.

Ha egy adatbázist egy Azure SQL-adatbázis kiszolgálójának megadásával törlünk, a **Remove-AzureSqlDatabase** parancsmag a nevet és az aktuális Azure-előfizetési adatokat használja a művelet végrehajtásához.

## Példák

### 1. példa: adatbázis eltávolítása
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Ez a parancs eltávolítja az Database01 nevű adatbázist az Azure SQL Database Server kapcsolati környezetből $Contextból.

### 2. példa: adatbázis eltávolítása kiszolgálónév használatával
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Ez a parancs eltávolítja a Database01 nevű adatbázist az lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálóról.

### 3. példa: adatbázis eltávolítása a csővezeték használatával
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Ez a példa bemutatja az adatbázis-objektum csővezetéken keresztüli továbbításának alternatív módszerét.

## PARAMÉTEREK

### -ConnectionContext
Annak a kiszolgálónak a kapcsolati környezetét adja meg, amelyből a parancsmag eltávolítja az adatbázist.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Database (adatbázis)
Egy olyan objektumot ad meg, amely a parancsmag által eltávolított adatbázisnak felel meg.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Annak az adatbázisnak a nevét adja meg, amely a parancsmagot eltávolítja.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Lehetővé teszi, hogy a művelet a felhasználó megerősítésének megkérdezése nélkül legyen elvégezhető.

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
Annak a kiszolgálónak a nevét adja meg, amelyen a parancsmag törli az adatbázist.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
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

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database

## KIMENETEK

## MEGJEGYZI
* A művelet súlyossága miatt alapértelmezés szerint ez a parancsmag kéri a megerősítést. A megerősítés kihagyásához adja meg az *erő* paramétert.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Adatbázis törlése](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Új – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Új – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


