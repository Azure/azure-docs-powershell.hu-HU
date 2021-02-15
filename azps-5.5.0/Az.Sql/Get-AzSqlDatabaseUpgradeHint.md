---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145739"
---
# Get-AzSqlDatabaseUpgradeHint

## SYNOPSIS
Az adatbázisokra vonatkozó árszint-tippeket kap.

## SZINTAXIS

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzSqlDatabaseUpgradeHint** parancsmag árazási szintmutatókat kap az Azure SQL-adatbázis frissítésében.
Azok az adatbázisok, amelyek továbbra is a webes és vállalati árazási szinteken maradnak, tippeket kap az új alapszintű, normál vagy prémiumszintű árszintre való frissítéshez.
Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.

## PÉLDÁK

### 1. példa: Javaslatok a kiszolgáló összes adatbázisához
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Ez a parancs frissítési tippeket ad vissza a Kiszolgáló01 nevű kiszolgálón található összes adatbázishoz.

### 2. példa: Javaslatok lekérte adott adatbázisra
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Ez a parancs frissítési tippeket ad vissza egy adott adatbázishoz.

### 3. példa: Javaslat minden olyan adatbázishoz, amely nem rugalmas adatbáziskészletben található
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

Ez a parancs frissítési tippeket ad vissza minden olyan adatbázishoz, amely nem rugalmas adatbáziskészletben található.

### 4. példa: Javaslatok a kiszolgálón található összes adatbázishoz szűrés használatával
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

Ez a parancs frissítési tippeket ad vissza a Kiszolgáló01 kiszolgáló összes olyan adatbázisához, amely az "Adatbázis" kezdetű.

## PARAMETERS

### -DatabaseName
Annak az SQL-adatbázisnak a neve, amelyhez ez a parancsmag frissítési tippet kap.
Ha nem ad meg adatbázist, ez a parancsmag tippeket kap a logikai kiszolgálón található összes adatbázishoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ExcludeElasticPoolCandidates
Azt jelzi, hogy a rugalmas adatbáziskészletek adatbázisai ki vannak-e zárva a visszaadott javaslatokból.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.

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
Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja frissítési tippet kap.

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

### System.Boolean

## KIMENETEK

### Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzSqlDatabaseExpanded](./Get-AzSqlDatabaseExpanded.md)

[Get-AzSqlElasticPoolRecommendation](./Get-AzSqlElasticPoolRecommendation.md)


