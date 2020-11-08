---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015865"
---
# Set-AzureSqlDatabase

## Áttekintés
Az Azure SQL-adatbázisok tulajdonságainak beállítása.

## SZINTAXISA

### ByNameWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureSqlDatabase** parancsmag az Azure SQL-adatbázisok tulajdonságait állítja be.
Megadhatja az adatbázist név szerint, vagy átadhat egy Azure SQL adatbázis-objektumot a csővezetéken keresztül.
Megadhatja a kiszolgálót név szerint, vagy átadhatja az Azure SQL-adatbázis kiszolgálójának kapcsolati környezetét.
A **New-AzureSqlDatabaseServerContext** parancsmag futtatásával kapcsolati környezetet hozhat létre.
Ha a kiszolgálót név szerint adja meg, a parancsmag az aktuális Azure-előfizetés adatait használja a kérés hitelesítéséhez.

## Példák

### Példa 1: adatbázis méretének módosítása kapcsolati környezet használatával
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

Ebben a példában a Database01 nevű adatbázis méretét módosítja az Azure SQL Database Server kapcsolati környezetének $Context.

### 2. példa: az adatbázis méretének módosítása kiszolgálónév használatával
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

Ebben a példában a lpqd0zbr8y nevű kiszolgálón a Database01 nevű adatbázis méretének 20 GB-ra változik.

## PARAMÉTEREK

### -ConnectionContext
A kiszolgáló kapcsolati környezetét adja meg.

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
Egy olyan objektumot ad meg, amely a parancsmag által módosított Azure SQL-adatbázist jelöli.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Annak az adatbázisnak a neve, amelyet a parancsmag módosított.

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

### – Kiadás
Az Azure SQL-adatbázis új kiadását adja meg.
Az érvényes értékek a következők: 

- Nincs
- Web
- Vállalati verzió
- Egyszerű
- Standard
-  Prémium verzió

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
Lehetővé teszi a művelet befejezését a megerősítés kérése nélkül.

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
Az adatbázis új maximális méretét adja meg bájtban.
Ezt a paramétert vagy a *MaxSizeGB* paramétert is megadhatja.
A *MaxSizeGB* paramétert az elfogadható értékekről a kiadás alapján című témakörben tekintheti meg.

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
Az adatbázis új maximális méretét adja meg gigabájtban.
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

### -NewDatabaseName
Az adatbázis új nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
A frissített Azure SQL-adatbázis értékét számítja ki.

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
Annak a kiszolgálónak a neve, amely a parancsmag által módosított adatbázist tartalmazza.

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

### -ServiceObjective
Egy olyan objektumot ad meg, amely az adatbázis új szolgáltatás célját (teljesítményi szintjét) jelképezi.
Az érvényes értékek a következők: 

- Alap: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

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

### – Szinkronizálás
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

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Adatbázis frissítése](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Új – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Új – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


