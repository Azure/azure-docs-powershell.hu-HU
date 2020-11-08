---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015973"
---
# New-AzureSqlDatabase

## Áttekintés
Azure SQL-adatbázist hoz létre.

## SZINTAXISA

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureSqlDatabase** PARANCSMAG Azure SQL-adatbázist hoz létre.
A kiszolgálót a **New-AzureSqlDatabaseServerContext** parancsmaggal létrehozott Azure SQL adatbázis-kiszolgáló kapcsolati környezete segítségével adhatja meg.
Ha a kiszolgáló nevét adja meg, a parancsmag az aktuális Azure-előfizetési adatokkal hitelesíti a kiszolgáló elérésére vonatkozó kérést.

Amikor új adatbázist hoz létre az Azure SQL-adatbázis kiszolgálójának megadásával, a **New-AzureSqlDatabase** parancsmag ideiglenes kapcsolati környezetet hoz létre a megadott kiszolgálónév és az Azure aktuális előfizetési adatai alapján a művelet végrehajtásához.

## Példák

### Példa 1: adatbázis létrehozása
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Ez a parancs létrehoz egy Adatbázis1 nevű Azure SQL-adatbázist az Azure SQL-adatbázis kiszolgálójának kapcsolati környezetéhez $Context.

### 2. példa: adatbázis létrehozása az aktuális előfizetésben
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Ez a példa létrehoz egy Adatbázis1 nevű adatbázist a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón.
A parancsmag az aktuális Azure-előfizetési adatok alapján hitelesíti a kiszolgáló elérésére vonatkozó kérést.

## PARAMÉTEREK

### -Szétválogatás
Az új adatbázis egybevetését adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionContext
Annak a kiszolgálónak a kapcsolati környezetét adja meg, ahol ez a parancsmag létrehoz egy adatbázist.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Az új adatbázis nevét adja meg.

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

### – Kiadás
Az új Azure SQL-adatbázis kiadását adja meg.
Az érvényes értékek a következők: 

- Nincs
- Web
- Vállalati verzió
- Egyszerű
- Standard
-  Prémium verzió

Az alapértelmezett érték a web.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
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

### -MaxSizeBytes
Az adatbázis maximális méretét adja meg bájtban.
Ezt a paramétert vagy a *MaxSizeGB* paramétert is megadhatja.
A *MaxSizeGB* paraméter leírása az elfogadható értékekről a kiadás alapján című témakörben olvasható.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
Az adatbázis maximális méretét adja meg gigabájtban.
Ezt a paramétert vagy a *MaxSizeBytes* paramétert is megadhatja.
Az elfogadható értékek kiadás alapján eltérőek.

Alapvető kiadási értékek: 1 vagy 2

Szokásos kiadási értékek: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 vagy 250

Prémium kiadású értékek: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 vagy 500

Web Edition-értékek: 1 vagy 5

Üzleti kiadás értékei: 10, 20, 30, 40, 50, 100 vagy 150

```yaml
Type: Int32
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
Annak az Azure SQL adatbázis-kiszolgálónak a nevét adja meg, amely az új adatbázist tartalmazza.

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

### -ServiceObjective
Egy olyan objektumot ad meg, amely az új szolgáltatás célját (teljesítményszint) képviseli az adatbázishoz.
Ez az érték az adatbázishoz rendelt erőforrások szintjét jelöli.
Az érvényes értékek a következők: 

Alap: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 * standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) a legújabb SQL-adatbázis-frissítés V12 (előzetes verzió) része.
További információ: az Azure SQL Database V12 előzetes verzió újdonságai https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
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

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database

## MEGJEGYZI
* Ha törölni szeretne egy **új AzureSqlDatabase** létrehozott adatbázist, használja az Remove-AzureSqlDatabase parancsmagot.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Adatbázis létrehozása](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Új – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


