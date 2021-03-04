---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 5c06c8e95d85e6a2b9f7c8449859edd94d9568b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923386"
---
# Add-AzSqlDatabaseToFailoverGroup

## SYNOPSIS
Hozzáad egy vagy több adatbázist egy Azure SQL-adatbázis feladatátvételi csoportjához.

## SZINTAXIS

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Hozzáad egy vagy több adatbázist egy Azure SQL-adatbázis feladatátvételi csoportjának elsődleges kiszolgálóhoz a feladatátvételi csoporthoz. Az adatbázisok nem lehetek másodlagos adatbázisok a meglévő replikációs kapcsolatokban. A parancs elindítja az esetleges hozzáadott adatbázisok georeplikációját a feladatátvételi csoport másodlagos kiszolgálójára.
Ha olyan adatbázis-objektumokat keres, amelyek az "-Database" paramétert kitöltik, használja (például) a Get-AzSqlDatabase parancsmagot.
A feladatátvételi csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.

## PÉLDÁK

### 1. példa
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

Ez a parancs egy adatbázist ad hozzá a feladatátvételi csoporthoz a bemászva.

### 2. példa
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

Ez a parancs hozzáadja a kiszolgáló összes adatbázisát egy feladatátvételi csoporthoz.

### 3. példa
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

Ez a parancs hozzáadja a rugalmas készletben található összes adatbázist egy feladatátvételi csoporthoz.

## PARAMETERS

### -Database
A feladatátvételi csoport elsődleges kiszolgálójának egy vagy több Azure SQL-adatbázisát hozzá kell adni a feladatátvételi csoporthoz.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -FailoverGroupName
Az Azure SQL-adatbázis feladatátvételi csoportjának neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

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
A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]

## KIMENETEK

### Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzSqlDatabaseFailoverGroup](./New-AzSqlDatabaseFailoverGroup.md)

[Set-AzSqlDatabaseFailoverGroup](./Set-AzSqlDatabaseFailoverGroup.md)

[Get-AzSqlDatabaseFailoverGroup](./Get-AzSqlDatabaseFailoverGroup.md)

[Remove-AzSqlDatabaseFromFailoverGroup](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[Switch-AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[Remove-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
