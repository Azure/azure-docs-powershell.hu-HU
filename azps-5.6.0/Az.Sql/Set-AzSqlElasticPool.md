---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 564bd475b8574f30f8d00cc1a374bc11b4a93ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924417"
---
# Set-AzSqlElasticPool

## SYNOPSIS
Módosítja egy rugalmas adatbáziskészlet tulajdonságait az Azure SQL-adatbázisban.

## SZINTAXIS

### DtuBasedPool (alapértelmezett)
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### VcoreBasedPool
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzSqlElasticPool** parancsmag beállítja egy rugalmas készlet tulajdonságait az Azure SQL-adatbázisban. Ez a parancsmag képes módosítani a készletenkénti eDTUsokat *(Dtu),* a tárterület maximális méretét készletenként *(StorageMB),* adatbázisonkénti maximális eDTUs értékeket *(DatabaseDtuMax)* és adatbázisonkénti minimális eDTUs-értékeket *(DatabaseDtuMin*).
Több paraméter (*-Dtu, -DatabaseDtuMin és -DatabaseDtuMax*) esetén a beállított érték szerepel az adott paraméter érvényes értékeinek listájában. Egy szabványos 100 eDTU-készlet esetén például a -DatabaseDtuMax érték csak 10, 20, 50 vagy 100 lehet.  Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

## PÉLDÁK

### 1. példa: Rugalmas készlet tulajdonságainak módosítása
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

Ez a parancs módosítja egy rugalmasságipool01 nevű rugalmas készlet tulajdonságait. A parancs 1000-re állítja a rugalmas készlet DTUs-ját, és beállítja a minimális és a maximális DTUs-t.

### 2. példa: Rugalmas készlet maximális tárterületméretének módosítása
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

Ez a parancs módosítja egy rugalmasságipool01 nevű rugalmas készlet tulajdonságait. A parancs egy rugalmas készlet maximális tárterületét 2 TB-osra állítja.

### 3. példa

Módosítja egy rugalmas adatbáziskészlet tulajdonságait az Azure SQL-adatbázisban. (automatikusan generált)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## PARAMETERS

### -AsJob
Parancsmag futtatása a háttérben

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

### -ComputeGeneráció
A hozzárendelni megfelelő számítási generálás.

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMax
Azt adja meg, hogy a készlet bármelyik adatbázisa legfeljebb hány DTUs-t képes igénybeni.
Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
A különböző kiadások alapértelmezett értékei a következők:
- Alapszintű.  5 DTUs
- Normál. 100 DTUs
- Prémium verzió. 125 DTUs

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMin
Megadja, hogy a rugalmas készlet hány DTUs-t garantál a készlet összes adatbázisának.
Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Az alapértelmezett érték nulla (0).

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMax
Az SqlAzure-adatbázis által a készletben megengedett maximális VCore-szám.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMin
Az SqlAzure-adatbázis által a készletben felhasznált minimális VCore-szám.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dtu
A rugalmas készlet megosztott DTUS-inak teljes számát adja meg.
Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
A különböző kiadások alapértelmezett értékei a következők:
- Alapszintű. 100 DTUs
- Normál. 100 DTUs
- Prémium verzió. 125 DTUs

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
A rugalmas készlet Azure SQL-adatbázisának kiadását határozza meg. A kiadás nem változtatható meg. A paraméter elfogadható értékei a következőek:
- Nincs
- Alapszintű
- Normál
- Prémium
- DataWarehouse
- Ingyenes
- Nyújtás
- GeneralPurpose
- BusinessCritical

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

### -ElasticPoolName
A rugalmas készlet nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseType
Az Azure Sql-adatbázis licenctípusa.

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

### -MaintenanceConfigurationId
Az SQL rugalmassági készlet karbantartási konfigurációs azonosítója.

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

### -ResourceGroupName
Annak az erőforráscsoportnak a neve, amelyhez a rugalmas készlet hozzá van rendelve.

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

### -ServerName
A rugalmas készletet tartalmazó kiszolgáló neve.

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

### -StorageMB
A rugalmas készlet tárterületkorlátját határozza meg megabájtban. További információért lásd a New-AzSqlElasticPool parancsmagot.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címkék
Egy olyan kulcsérték-párok szótárát adja meg, amelyekhez a parancsmag hash táblázat formájában társítja a rugalmas készletet. Például: `@{key0="value0";"key 1"=$null;key2="value2"}`

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
A Vcore teljes megosztott száma az Sql Azure Rugalmas készlethez.

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
The zone redundancy to associate with the Azure Sql Elastic Pool

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzSqlElasticPool](./Get-AzSqlElasticPool.md)

[Get-AzSqlElasticPoolActivity](./Get-AzSqlElasticPoolActivity.md)

[Get-AzSqlElasticPoolDatabase](./Get-AzSqlElasticPoolDatabase.md)

[New-AzSqlElasticPool](./New-AzSqlElasticPool.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
