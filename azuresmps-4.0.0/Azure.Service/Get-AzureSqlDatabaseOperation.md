---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016293"
---
# Get-AzureSqlDatabaseOperation

## Áttekintés
Az adatbázis-műveletek állapotát egy Azure-kiszolgálón kapja meg.

## SZINTAXISA

### ByConnectionContext (alapértelmezett)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabaseOperation** parancsmag az adatbázis-műveletek állapotát a megadott Azure-kiszolgálón kapja.
Ha csak a *kiszolgálónév* vagy a *ConnectionContext* paramétert adja meg, a parancsmag minden adatbázis-műveletet megkapja a kiszolgálón.
Ha az *adatbázis* vagy a *databasename* paraméter használatával is megadhat egy adatbázist, ez a parancsmag a megadott adatbázis összes műveletét megkapja.
Ha megad egy műveleti GUID azonosítót, a *kiszolgálónév* vagy a *ConnectionContext* , a parancsmag egyetlen adatbázis-műveletet kap.

## Példák

### Példa 1: adatbázis minden adatbázis-műveletének állapotának lekérése
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

Ez a parancs a kiszolgálón a Database17 nevű adatbázis minden műveletének állapotát beolvassa, és a kapcsolati környezet $Context adja meg.

### 2. példa: a kiszolgáló összes adatbázis-művelete állapotának beszerzése
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

Ez a parancs minden olyan adatbázis-művelet állapotát megjeleníti a kiszolgálón, amelyen a kapcsolati környezet $Context meg van határozva.

## PARAMÉTEREK

### -ConnectionContext
A kiszolgáló kapcsolati környezetét adja meg.

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
Egy Azure SQL-adatbázist jelképező objektumot ad meg.
Ha ezt a paramétert adja meg, a *kiszolgálónév* paramétert vagy a *ConnectionContext* paramétert kell megadnia.

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

### -DatabaseName
Az adatbázis nevét adja meg.
Ha ezt a paramétert adja meg, a *kiszolgálónév* paramétert vagy a *ConnectionContext* paramétert kell megadnia.

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

### -OperationGuid
Azt a műveleti azonosítót adja meg, amely egy bizonyos adatbázis-műveletnek felel meg, amelyre a parancsmag állapota bekerül.
A műveleti azonosítók beolvasásához az Azure SQL-adatbázisok vagy-kiszolgálók összes adatbázis-műveletét kéri.
Ha ezt a paramétert adja meg, a *kiszolgálónév* paramétert vagy a *ConnectionContext* paramétert kell megadnia.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
A kiszolgáló nevét adja meg.

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

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext

### System. GUID

## KIMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. database. DatabaseOperationResponseList []
Ez a parancsmag egy **DatabaseOperationResponseList** -objektumokból álló tömböt ad eredményül, ha több műveletet kap.

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. database. DatabaseOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://msdn.microsoft.com/library/ee336279.aspx)

[Adatbázis-művelet állapota](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Új – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


