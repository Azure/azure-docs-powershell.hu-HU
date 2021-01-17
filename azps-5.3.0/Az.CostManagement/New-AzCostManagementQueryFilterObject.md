---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480508"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Memóriában létrehozott objektum létrehozása a QueryFilterhez

## SZINTAXIS

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## LEÍRÁS
Memóriában létrehozott objektum létrehozása a QueryFilterhez

## PÉLDÁK

### 1. példa: Lekérdezés szűrőobjektumának létrehozása költségkezelési exportáláshoz
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

Ez a parancs egy lekérdezésszűrő objektumot hoz létre a költségkezelési exportáláshoz.

## PARAMETERS

### -And
A logikai "ÉS" kifejezés.
Legalább 2 elemet kell tartalmazni.
Ennek létrehozásáról az AND tulajdonságokat és a kivonattáblát a JEGYZETEK szakaszban láthatja.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Méretek
Dimenziókra vonatkozó összehasonlító kifejezéssel rendelkezik.
Ennek létrehozásához a NOTES (JEGYZETEK) szakaszban láthatja a DIMENSIONS tulajdonságokat, és létrehozhat egy kivonattáblát.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Not
A logikai "NEM" kifejezés.
A NEM tulajdonságok létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban található.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vagy
A logikai "VAGY" kifejezés.
Legalább 2 elemet kell tartalmazni.
Ennek létrehozásáról a VAGY tulajdonságokat a NOTES (VAGY) című szakaszban, valamint egy kivonattáblát hozhat létre.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Egy címkéhez összehasonlító kifejezést ad meg.
A címkék tulajdonságainak létrehozásáról és a kivonattáblák létrehozásáról a NOTES (JEGYZETEK) című szakaszban található.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


ÉS <IQueryFilter[]>: A logikai "ÉS" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik
    - `Name <String>`: Az összehasonlításban használt oszlop neve.
    - `Operator <OperatorType>`: Az összehasonlításhoz használt operátor.
    - `Value <String[]>`: Az összehasonlításhoz használható értékek tömbje
  - `[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.
  - `[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad

<IQueryComparisonExpression>MÉRETEK: Dimenziók összehasonlító kifejezését tartalmazza.
  - `Name <String>`: Az összehasonlításban használt oszlop neve.
  - `Operator <OperatorType>`: Az összehasonlításhoz használt operátor.
  - `Value <String[]>`: Az összehasonlításhoz használható értékek tömbje

NOT <IQueryFilter> : A logikai "NOT" kifejezés.
  - `[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik
    - `Name <String>`: Az összehasonlításban használt oszlop neve.
    - `Operator <OperatorType>`: Az összehasonlításhoz használt operátor.
    - `Value <String[]>`: Az összehasonlításhoz használható értékek tömbje
  - `[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.
  - `[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad

OR <IQueryFilter[]>: A logikai "VAGY" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[And <IQueryFilter[]>]`: A logikai "ÉS" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[Dimensions <IQueryComparisonExpression>]`: Dimenzióhoz összehasonlító kifejezéssel rendelkezik
    - `Name <String>`: Az összehasonlításban használt oszlop neve.
    - `Operator <OperatorType>`: Az összehasonlításhoz használt operátor.
    - `Value <String[]>`: Az összehasonlításhoz használható értékek tömbje
  - `[Not <IQueryFilter>]`: A logikai "NEM" kifejezés.
  - `[Or <IQueryFilter[]>]`: A logikai "VAGY" kifejezés. Legalább 2 elemet kell tartalmazni.
  - `[Tag <IQueryComparisonExpression>]`: Egy címkéhez összehasonlító kifejezést is ad

CÍMKE: <IQueryComparisonExpression> Egy címkéhez összehasonlító kifejezést ad meg.
  - `Name <String>`: Az összehasonlításban használt oszlop neve.
  - `Operator <OperatorType>`: Az összehasonlításhoz használt operátor.
  - `Value <String[]>`: Az összehasonlításhoz használható értékek tömbje

## KAPCSOLÓDÓ HIVATKOZÁSOK

