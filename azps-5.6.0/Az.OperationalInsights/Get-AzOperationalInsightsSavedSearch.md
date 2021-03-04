---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921665"
---
# Get-AzOperationalInsightsSavedSearch

## SYNOPSIS
Visszaadja egy adott munkaterület összes mentett keresését.

## SZINTAXIS

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzOperationalInsightsSavedSearch** parancsmag visszaadja az erőforráscsoportban megadott munkaterület összes mentett keresését, ha nem ad meg mentett keresési azonosítót.
Ha megad egy mentett keresési azonosítót, akkor a rendszer az adott azonosítónak megfelelő mentett keresést adja vissza.

## PÉLDÁK

### 1. példa: Munkaterület összes mentett keresésének bekeresése
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

Ez a parancs a munkaterülethez társított összes mentett erőforrást leküldi.

### 2. példa: Adott mentett keresés keresése azonosító szerint
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

Ez a parancs egy adott mentett keresést kap az azonosító alapján.

## PARAMETERS

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

### -ResourceGroupName
Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.

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

### -SavedSearchId
Egy mentett keresési azonosítót ad meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceName
Munkaterület nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse

### Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure Operational Insights-parancsmagok](./Az.OperationalInsights.md)


