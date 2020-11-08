---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015845"
---
# Start-AzureSqlDatabaseCopy

## Áttekintés
Egy Azure SQL-adatbázis másolási műveletét indítja el.

## SZINTAXISA

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

## Leírás
A **Start-AzureSqlDatabaseCopy** parancsmag egyszeres másolási műveletet vagy egy bizonyos Azure SQL-adatbázis folyamatos másolási műveletét indítja el.
Ez a parancsmag nem tranzakciós.

Az eredeti adatbázis a forrás adatbázis.
A másolat a másodlagos vagy a cél adatbázis.
Folyamatos másolás esetén a forrás-és a célként megadott adatbázis nem használható ugyanazon a kiszolgálón, és a forrás-és a célként megadott adatbázisokat tároló kiszolgálók ugyanahhoz az előfizetéshez tartoznak.

Ha nem adja meg a *ContinuousCopy* paramétert, ez a parancsmag a forrásadatbázis egyszer használatos példányát hozza létre.
A válasz fogadásakor a művelet továbbra is folyamatban van.
A műveletet a Get-AzureSqlDatabaseCopy vagy Get-AzureSqlDatabaseOperation parancsmag használatával figyelheti.

Ha megad egy *ContinuousCopy* , ez a parancsmag létrehoz egy folytonos másolatot a forrás adatbázisról.
Ha a válasz érkezik, a művelet folyamatban lesz.
A műveletet a **Get-AzureSqlDatabaseCopy** vagy a **Get-AzureSqlDatabaseOperation** segítségével is figyelheti.

Folyamatos másolatot hozhat létre online vagy offline adatbázisként.
Az online folytonos másolat az aktív Geo-Replication Azure SQL-adatbázis konfigurálására szolgál https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
A kapcsolat nélküli folyamatos másolat az Azure SQL-adatbázis normál Geo-Replicationének konfigurálására szolgál https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## Példák

### Példa 1: folytonos adatbázis-példány ütemezése
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Ez a parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis folyamatos másolatát ütemezi.
A parancs létrehoz egy céladatbáziset a bk0b8kf658 nevű kiszolgálón.

### 2. példa: egyidejű másolat létrehozása ugyanazon a kiszolgálón
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Ezzel a paranccsal létrehozhatja a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis egyszeres másolatát.
A parancs létrehoz egy OrdersCopy nevű példányt ugyanazon a kiszolgálón.

### 3. példa: folyamatos Offline adatbázis-példány ütemezése
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Ez a parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis folyamatos másolatát ütemezi.
Ez a parancs létrehoz egy offline céladatbázis-adatbázist a bk0b8kf658 nevű kiszolgálón.

## PARAMÉTEREK

### -ContinuousCopy
Azt jelzi, hogy az adatbázis másolása folyamatos másolatként (replika-adatbázis) fog szerepelni.
A folyamatos másolás nem támogatott ugyanazon a kiszolgálón belül.
Ha ez a paraméter nincs megadva, az alkalmazás egyszeres másolatot hajt végre.
Egyszeres másolat esetén a forrás-és a partner adatbázisnak ugyanazon a kiszolgálón kell lennie.

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

### -Database (adatbázis)
Egy olyan objektumot ad meg, amely a Source Azure SQL-adatbázist jelöli.
Ez a paraméter elfogadja a csővezeték-bevitelt.

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
A forrás adatbázis nevét adja meg.

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

### -OfflineSecondary
Azt adja meg, hogy egy folytonos másolat nem aktív másolat, hanem passzív másolat.
Ha a forrásadatbázis normál kiadású adatbázis, akkor ez a paraméter szükséges.
Ha ezt a paramétert adja meg, akkor a *ContinuousCopy* is meg kell adni.

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
Ha a *ContinuousCopy* paramétert adja meg, a *PartnerDatabase* értékének egyeznie kell a forrás adatbázis nevével.
Ha nem adja meg a *ContinuousCopy* , meg kell adnia a céladatbázis nevét, amely a forrás adatbázis nevétől eltérő lehet.

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
A célként megadott adatbázist tároló kiszolgáló neve.
A kiszolgálónak ugyanazon az Azure-előfizetésben kell lennie, mint a forrás adatbázis-kiszolgáló.

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
Annak a kiszolgálónak a nevét adja meg, amelyen a forrás adatbázis található.

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

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy

## MEGJEGYZI
* Hitelesítés: Ez a parancsmag tanúsítvány-alapú hitelesítést követel meg. Ha egy példa arra, hogy hogyan állíthatja be az aktuális előfizetést tanúsítványalapú hitelesítéssel, olvassa el New-AzureSqlDatabaseServerContext parancsmagot.
* Figyelés: Ha a kiszolgálón aktív egy vagy több folyamatos másolási kapcsolat állapotát szeretné ellenőrizni, használja a **Get-AzureSqlDatabaseCopy** parancsmagot. Ha ellenőrizni szeretné a műveletek állapotát a folyamatos másolási kapcsolat forrása és célja között, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Adatbázis-másolat indítása](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Azure SQL-adatbázis-parancsmagok](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


