---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016295"
---
# Get-AzureSqlDatabaseCopy

## Áttekintés
A kapcsolatok másolási állapotának ellenőrzése

## SZINTAXISA

### ByServerNameOnly (alapértelmezett)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabaseCopy** parancsmag egy vagy több aktív másolási kapcsolat állapotát ellenőrzi.
Futtassa ezt a parancsmagot a Start-AzureSqlDatabaseCopy vagy Stop-AzureSqlDatabaseCopy parancsmag futtatása után.
Ellenőrizheti a másolati viszonyokat, az összes másolt kapcsolatot, illetve a másolt kapcsolatok szűrt listáját, például egy adott célkiszolgáló összes példányát.
Ezt a parancsmagot a forrás-vagy céladatbázis-kiszolgálót futtató kiszolgálón futtathatja.

Ez a parancsmag szinkronban van.
A parancsmag megakadályozza az Azure PowerShell-konzolt, amíg az nem egy állapotsort ad.

A *PartnerServer* és a *PartnerDatabase* paraméter nem kötelező.
Ha nem ad meg paramétert, ez a parancsmag a találatok táblázatát adja eredményül.
Ha csak egy adott adatbázis állapotát szeretné látni, adja meg mindkét paramétert.

## Példák

### Példa 1: adatbázis másolati állapotának beszerzése
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Ez a parancs megkapja a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis állapotát.
A *PartnerServer* paraméter korlátozza ezt a parancsot az bk0b8kf658-kiszolgálóra.

### 2. példa: a serverGet lévő összes példány állapotának lekérése
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Ez a parancs a lpqd0zbr8y nevű kiszolgálón minden aktív másolat állapotát megkapja.

## PARAMÉTEREK

### -Database (adatbázis)
Egy olyan objektumot ad meg, amely a Source Azure SQL-adatbázist jelöli.
Ez a parancsmag a paraméter által megadott adatbázis másolati állapotát kapja meg.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Egy adatbázist jelképező objektumot ad meg.
Ez a parancsmag a paraméter által megadott adatbázis másolati állapotát kapja meg.
Ez a paraméter elfogadja a csővezeték-bevitelt.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
A forrás adatbázis nevét adja meg.
Ez a parancsmag a paraméter által megadott adatbázis másolati állapotát kapja meg.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
A másodlagos adatbázis nevét adja meg.
Ha az adatbázis nem található meg a sys.dm_database_copies dinamikus kezelés nézetében, ez a parancsmag üres állapot-objektumot ad eredményül.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
A célként megadott adatbázist tároló kiszolgáló neve.
Ha a kiszolgáló nem található meg a sys.dm_database_copies dinamikus kezelés nézetében, ez a parancsmag üres állapot-objektumot ad eredményül.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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
Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis-másolat található.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database

## KIMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy

## MEGJEGYZI
* Hitelesítés: Ez a parancsmag tanúsítvány-alapú hitelesítést követel meg. Példa arra, hogy hogyan állíthatja be a jelenlegi előfizetést tanúsítványalapú hitelesítéssel, ha az New-AzureSqlDatabaseServerContext parancsmagot használja.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Azure SQL-adatbázis-parancsmagok](./Azure.SQLDatabase.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


