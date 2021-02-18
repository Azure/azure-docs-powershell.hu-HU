---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405618"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
Folyamatos másolási kapcsolatot szüntet meg.

## SZINTAXIS

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Adatbázis-adatbázis
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Stop-AzureSqlDatabaseCopy** parancsmag megszakítja a folyamatos másolási kapcsolatot.
Ez a parancsmag leállítja az adatmozgást a forrásadatbázis és a másodlagos vagy céladatbázis között, majd a másodlagos adatbázis állapotát önálló online adatbázisként módosítja.

A folyamatos másolási kapcsolatot, a megszüntetést vagy a tervezett megszüntetést és a kényszeres megszüntetést kétféleképpen lehet megszüntetni lehetséges adatvesztéssel.
A forrásadatbázist tartalmazó kiszolgálón futtathatja ezt a parancsmagot megszüntetés vagy kényszerített megszüntetés módban.
A másodlagos adatbázist tartalmazó kiszolgálón kényszerített megszüntetést kell használnia.

A tervezett megszüntetés addig vár, amíg a forrásadatbázisban lekötött tranzakciók a parancsmag futtatásakor a másodlagos adatbázisba replikálódnak.
A kényszerített megszüntetés nem várja meg a lekötött tranzakciók replikációját, és a másodlagos adatbázisban adatvesztést okozhat.

A replikáció állapota függőben van, de csak a kényszerített megszüntetés képes megszüntetni a folyamatos másolási kapcsolatot.
Ha a replikáció állapota FÜGGŐBEN van, a nem kényszerített megszüntetés nem támogatott.

## PÉLDÁK

### 1. példa: Folyamatos másolási kapcsolat megszüntetése
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Ez a parancs megszünteti az Orders (Rendelések) nevű adatbázis folyamatos másolási kapcsolatát az lpqd0zbr8y nevű kiszolgálón.
A bk0b8kf658 nevű kiszolgáló tárolja a másodlagos adatbázist.

### 2. példa: Folytonos másolási kapcsolat megszüntetése
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Az első parancs az Orders (Rendelések) nevű adatbázis adatbázis-másolási kapcsolatát kapja meg az lpqd0zbr8y nevű kiszolgálón.

A második parancs a másodlagos adatbázist tartalmazó kiszolgáló folyamatos másolási kapcsolatát szünteti meg.

## PARAMETERS

### -Database
A forrás Azure SQL-adatbázist képviselő objektumot ad meg.
Ez a parancsmag megszakítja a paraméterként megadott adatbázis folyamatos másolási kapcsolatát.

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
Ez a parancsmag megszakítja a paraméterként megadott adatbázis folyamatos másolási kapcsolatát.
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
Egy adatbázis nevét adja meg.
Ez a parancsmag megszakítja a paraméterként megadott adatbázis folyamatos másolási kapcsolatát.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

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

### -ForcedTermination
Azt jelzi, hogy ez a parancsmag a folyamatos másolási kapcsolat kényszerített megszűnését okozza.
A kényszerített megszüntetés adatvesztést okozhat.
Ha a parancsmagot a céladatbázist tároló kiszolgálón futtatni, meg kell adnia ezt a paramétert.
Ha ezt a parancsmagot a forrásadatbázist tartalmazó kiszolgálón futtatni, ha a másodlagos adatbázis nem érhető el, meg kell adnia ezt a paramétert.

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

### -PartnerDatabase
A másodlagos adatbázis nevét adja meg.
Ha megad egy nevet, annak meg kell egyeznie a forrásadatbázis nevével.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
A céladatbázist tároló kiszolgáló neve.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
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
Annak a kiszolgálónak a nevét adja meg, amelyen a forrásadatbázis található.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## KIMENETEK

### Nincs

## MEGJEGYZÉSEK
* Hitelesítés: Ez a parancsmag tanúsítványalapú hitelesítést igényel. Ha például tanúsítványalapú hitelesítéssel állíthatja be az aktuális előfizetést, tekintse meg a **New-AzureSqlDatabaseServerContext** parancsmagot.
* Korlátozások: A másodlagos adatbázist tartalmazó kiszolgálón csak a kényszerített megszüntetés támogatott.
* A megszűnés hatása a korábbi másodlagos adatbázisra: A megszüntetés után a másodlagos adatbázis független adatbázissá válik. Ha már befejeződött a másodlagos adatbázis létrehozása, az adatbázis megszüntetése után az adatbázis teljes hozzáférésre van megnyitva. Ha a forrásadatbázis írási és írási adatbázis, a korábbi másodlagos adatbázis is írási és írási adatbázissá válik.

  Ha a bevetés folyamatban van, a rendszer megszakítja a bevetést, és a korábbi másodlagos adatbázis soha nem lesz látható a másodlagos adatbázist tartalmazó kiszolgálón.

* A forrásadatbázist írási módra állíthatja. Ez garantálja, hogy a rendszer a megszűnés után szinkronizálja a forrás- és a másodlagos adatbázisokat, és biztosítja, hogy a megszüntetés során ne legyen tranzakciók lekötöttek. A megszüntetés befejeződése után állítsa vissza a forrást írási és olvasási módba. Ha szükséges, a korábbi másodlagos adatbázist írási-olvasási módra is beállíthatja.
* Figyelés: Ha a folyamatos másolási kapcsolat forrásán és célszámán is ellenőriznie kell a műveletek állapotát, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Műveletek az Azure SQL-adatbázisokban](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Adatbázis-másolás vége](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


