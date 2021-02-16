---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148147"
---
# Update-AzDataLakeAnalyticsComputePolicy

## SYNOPSIS
Frissíti a Data Lake Analytics számítási házirendszabályát egy adott AAD-entitáshoz.

## SZINTAXIS

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Update-AzDataLakeAnalyticsComputePolicy** frissíti a megadott számítási házirendszabályt egy Azure Data Lake Analytics-fiók adott AAD-entitásához.

## PÉLDÁK

### 1. példa: Egy szabály frissítése egy számítási házirendben
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

Ez a parancs frissíti a "myPolicy" házirendet a "contosoadla" fiókban, hogy a felhasználó ne küldjön be 5-ösnél több elemzési egységben található feladatot.

### 2. példa: Számítási házirend létrehozása mindkét szabályfrissítéssel
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

Ez a parancs létrehoz egy "myPolicy" nevű házirendet a "contosoadla" fiókban, hogy a felhasználó ne küldjön be 5-től több elemzési egységből vagy 100-asnál alacsonyabb prioritású feladatot.

## PARAMETERS

### -Account
Annak a fióknak a neve, amelyben frissíteni szeretné a számítási házirendet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
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

### -MaxAnalyticsUnitsPerJob
A házirendhez a maximális támogatott elemzési egység egy feladathoz. Ezt vagy a MinPriorityPerJob paramétert, vagy mindkét paramétert meg kell adni.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinPriorityPerJob
A házirend minimális támogatott prioritása feladatonként. Ezt vagy a MaxAnalyticsUnitsPerJob paramétert, vagy mindkét paramétert meg kell adni.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
A frissítenie kell a számítási házirend neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a neve, amelyben a fiók létezik.
Nem kötelező, és megpróbálja felderítni, ha nem áll rendelkezésre.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
