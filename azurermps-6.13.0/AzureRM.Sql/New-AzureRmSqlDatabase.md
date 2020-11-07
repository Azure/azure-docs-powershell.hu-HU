---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679815"
---
# New-AzureRmSqlDatabase

## Áttekintés
Adatbázis vagy rugalmas adatbázis létrehozása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### DtuBasedDatabase (alapértelmezett)
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VcoreBasedDatabase
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmSqlDatabase** PARANCSMAG Azure SQL-adatbázist hoz létre.
Rugalmas adatbázist úgy is létrehozhat, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.

## Példák

### Példa 1: adatbázis létrehozása egy megadott kiszolgálón
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

A parancs létrehoz egy Database01 nevű adatbázist a kiszolgálók Server01.

### 2. példa: rugalmas adatbázis létrehozása egy megadott kiszolgálón
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

A parancs létrehoz egy Database02 nevű adatbázist a ElasticPool01 nevű rugalmas készletben a kiszolgálói Server01.

### 3. példa: vcore-adatbázis létrehozása egy megadott kiszolgálón
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

Ez a parancs létrehoz egy Database03 nevű vcore-adatbázist a kiszolgálói Server01.

## PARAMÉTEREK

### -AsJob
A parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CatalogCollation
Az SQL adatbázis-katalógus egybevetésének nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollationName
Az SQL-adatbázis egybevetésének nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeGeneration
A hozzárendelni kívánt számítási generálás.

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Az adatbázis nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Kiadás
Az adatbázishoz hozzárendelni kívánt kiadást adja meg. A paraméter elfogadható értékei a következők:
- Nincs
- Egyszerű
- Standard
- Prémium verzió
- Adattárházi
- Ingyenes
- Nyúlik
- GeneralPurpose
- BusinessCritical

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolName
Annak a rugalmas készletnek a nevét adja meg, amelyben az adatbázist el szeretné helyezni.

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Az Azure SQL-adatbázis licenc típusa.

```yaml
Type: System.String
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

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReadScale
Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestedServiceObjectiveName
Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SampleName
Az adatbázis létrehozásakor alkalmazandó minta-séma neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kiszolgálónév
Az adatbázist tároló kiszolgáló nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címkék
A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre a parancsmag társítva van az új adatbázissal. Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VCore
Az Azure SQL-adatbázis vcore száma

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
A zóna redundancia az Azure SQL-adatbázishoz való társításhoz

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

## KIMENETEK

### Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[Új – AzureRmSqlElasticPool](./New-AzureRmSqlElasticPool.md)

[Új – AzureRmSqlServer](./New-AzureRmSqlServer.md)

[Remove-AzureRmSqlDatabase](./Remove-AzureRmSqlDatabase.md)

[Önéletrajz – AzureRmSqlDatabase](./Resume-AzureRmSqlDatabase.md)

[Set-AzureRmSqlDatabase](./Set-AzureRmSqlDatabase.md)

[Felfüggesztés – AzureRmSqlDatabase](./Suspend-AzureRmSqlDatabase.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)

