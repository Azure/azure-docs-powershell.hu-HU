---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413064"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Egy Azure SQL-adatbázis másolási műveletének indítása.

## SZINTAXIS

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Start-AzureSqlDatabaseCopy** parancsmag egy egyszeres másolási műveletet vagy egy adott Azure SQL-adatbázis folyamatos másolási műveletét indítja el.
Ez a parancsmag nem tranzakciós.

Az eredeti adatbázis a forrásadatbázis.
A másolat a másodlagos vagy céladatbázis.
Folyamatos másolat esetén a forrás- és céladatbázisok nem ugyanazon a kiszolgálón találhatók, és a forrás- és céladatbázisokat tároló kiszolgálóknak ugyanannak az előfizetésnek a részeinek kell lennie.

Ha nem adja meg a *ContinuousCopy* paramétert, ez a parancsmag a forrásadatbázis egy egyszer használható másolatát hozza létre.
Amikor a válasz érkezik, a művelet továbbra is folyamatban lehet.
A műveletet figyelheti a Get-AzureSqlDatabaseCopy vagy Get-AzureSqlDatabaseOperation parancsmag használatával.

Ha a *ContinuousCopy* értéket adja meg, ez a parancsmag a forrásadatbázis folyamatos másolatát hozza létre.
Amikor a válasz érkezik, a művelet folyamatban lesz.
A műveletet a **Get-AzureSqlDatabaseCopy** vagy **a Get-AzureSqlDatabaseOperation segítségével figyelheti.**

Folyamatos másolatot online vagy offline adatbázisként is létrehozhat.
Az online folyamatos másolat az Azure SQLGeo-Replication-adatbázis aktív címtárának beállításához https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ használható.
Az offline folyamatos másolat az Azure SQLGeo-Replication-adatbázis standard Geo-Replication beállításához https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ használatos.

## PÉLDÁK

### 1. példa: Folyamatos adatbázis-másolat ütemezése
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Ez a parancs az Orders (Rendelések) adatbázis folyamatos másolatát ütemezi az lpqd0zbr8y nevű kiszolgálón.
A parancs létrehoz egy céladatbázist a bk0b8kf658 nevű kiszolgálón.

### 2. példa: Egyszeres példány létrehozása ugyanazon a kiszolgálón
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Ez a parancs létrehozza az Orders (Rendelések) adatbázis egy egyszeres másolatát az lpqd0zbr8y nevű kiszolgálón.
A parancs létrehoz egy OrdersCopy nevű példányt ugyanazon a kiszolgálón.

### 3. példa: Folyamatos offline adatbázis-példány ütemezése
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Ez a parancs az Orders (Rendelések) adatbázis folyamatos másolatát ütemezi az lpqd0zbr8y nevű kiszolgálón.
Ez a parancs létrehoz egy offline céladatbázist a bk0b8kf658 nevű kiszolgálón.

## PARAMETERS

### -ContinuousCopy
Azt jelzi, hogy az adatbázis másolata folyamatos másolat lesz (egy replika-adatbázis).
A folyamatos másolás nem támogatott ugyanazon a kiszolgálón.
Ha ez a paraméter nincs megadva, akkor a program egy egyszeres példányt hajt végre.
Az egyszeres példányban a forrás- és partneradatbázisnak ugyanazon a kiszolgálón kell lennie.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
A forrás Azure SQL-adatbázist képviselő objektumot ad meg.
Ez a paraméter elfogadja a folyamatbemenetet.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
A forrásadatbázis nevét adja meg.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
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

### -OfflineSecondary
Azt adja meg, hogy a folyamatos másolat aktív másolat helyett passzív másolat.
Ha a forrásadatbázis standard kiadású adatbázis, akkor ezt a paramétert kell megadni.
Ha ez a paraméter meg van adva, akkor *a ContinuousCopy* paramétert is meg kell adni.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
A céladatbázis nevét adja meg.
Ha a *ContinuousCopy* paramétert adja meg, a *PartnerDatabase* értékének meg kell egyeznie a forrásadatbázis nevével.
Ha nem a *ContinuousCopy* nevet adja meg, meg kell adnia a céladatbázis nevét, amely nem lehet más, mint a forrásadatbázis neve.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
A céladatbázist tároló kiszolgáló neve.
Ennek a kiszolgálónak ugyanabban az Azure-előfizetésben kell lennie, mint a forrásadatbázis-kiszolgálónak.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## KIMENETEK

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## MEGJEGYZÉSEK
* Hitelesítés: Ez a parancsmag tanúsítványalapú hitelesítést igényel. Ha például tanúsítványalapú hitelesítéssel állíthatja be az aktuális előfizetést, tekintse meg a New-AzureSqlDatabaseServerContext parancsmagot.
* Figyelés: A kiszolgálón aktív egy vagy több folyamatos másolási kapcsolat állapotának ellenőrzéséhez használja a **Get-AzureSqlDatabaseCopy** parancsmagot. Ha a folyamatos másolási kapcsolat forrásán és célértékénél is ellenőriznie kell a műveletek állapotát, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Műveletek az Azure SQL-adatbázisokban](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Adatbázis-másolás létrehozása](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


