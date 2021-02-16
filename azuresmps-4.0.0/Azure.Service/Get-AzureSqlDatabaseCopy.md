---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402422"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
A másolási kapcsolatok állapotát ellenőrzi.

## SZINTAXIS

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

### Adatbázis-adatbázis
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzureSqlDatabaseCopy** parancsmag egy vagy több aktív másolási kapcsolat állapotát ellenőrzi.
Futtassa ezt a parancsmagot a Start-AzureSqlDatabaseCopy vagy Stop-AzureSqlDatabaseCopy futtatása után.
Ellenőrizheti egy adott másolási kapcsolatot, az összes másolási kapcsolatot vagy a másolási kapcsolatok szűrt listáját, például egy adott célkiszolgáló összes példányát.
Ezt a parancsmagot a forrás- vagy céladatbázist tároló kiszolgálón futtathatja.

Ez a parancsmag szinkron.
A parancsmag letiltja az Azure PowerShell-konzolt, amíg egy állapotobjektumot nem ad vissza.

A *PartnerServer* és *a PartnerDatabase* paraméter megadása nem kötelező.
Ha egyik paramétert sem adja meg, ez a parancsmag eredménytáblát ad eredményül.
Ha csak egy adott adatbázis állapotát látni, adja meg mindkét paramétert.

## PÉLDÁK

### 1. példa: Adatbázis másolási állapotának ellenőrzése
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Ez a parancs az Orders (Rendelések) nevű adatbázis állapotát kapja meg az lpqd0zbr8y nevű kiszolgálón.
A *PartnerServer* paraméter a parancsot a bk0b8kf658-kiszolgálóra korlátozza.

### 2. példa: A kiszolgálón található összes példány állapotának ellenőrzéseA kiszolgálón található összes példány állapotának megtekintése
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Ez a parancs az lpqd0zbr8y nevű kiszolgálón lévő összes aktív példány állapotát kapja meg.

## PARAMETERS

### -Database
A forrás Azure SQL-adatbázist képviselő objektumot ad meg.
Ez a parancsmag a paraméter által megadott adatbázis másolási állapotát kapja meg.

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
Egy adatbázist képviselő objektumot ad meg.
Ez a parancsmag a paraméter által megadott adatbázis másolási állapotát kapja meg.
Ez a paraméter elfogadja a folyamatbemenetet.

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
A forrásadatbázis nevét adja meg.
Ez a parancsmag a paraméter által megadott adatbázis másolási állapotát kapja meg.

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
Ha ez az adatbázis nem található meg a sys.dm_database_copies dinamikus kezelési nézetben, ez a parancsmag üres állapotobjektumot ad vissza.

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
A céladatbázist tároló kiszolgáló neve.
Ha ez a kiszolgáló nem található meg a sys.dm_database_copies dinamikus kezelési nézetben, ez a parancsmag üres állapotobjektumot ad vissza.

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
Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.
Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.

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

### -ServerName
Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis másolata található.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## KIMENETEK

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## MEGJEGYZÉSEK
* Hitelesítés: Ez a parancsmag tanúsítványalapú hitelesítést igényel. Ha például tanúsítványalapú hitelesítéssel állíthatja be az aktuális előfizetést, tekintse meg a New-AzureSqlDatabaseServerContext parancsmagot.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Műveletek az Azure SQL-adatbázisokban](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


