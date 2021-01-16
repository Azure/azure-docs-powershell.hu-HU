---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366462"
---
# Get-AzStreamAnalyticsDefaultFunctionDefinition

## SYNOPSIS
A Stream Analytics függvényének alapértelmezett definícióját kapja meg.

## SZINTAXIS

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzStreamAnalyticsDefaultFunctionDefinition Parancsmag** megkapja az Azure Stream Analytics egy függvényének alapértelmezett definícióját.
A függvények létrehozásához használhatja New-AzStreamAnalyticsFunction alapértelmezett definíciót és parancsmagot.
A függvények létrehozása előtt módosíthatja az alapértelmezett definíciót.

## PÉLDÁK

### 1. példa: A Stream Analytics függvény alapértelmezett definíciójának lekérte
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

Ez a parancs a ScoreTweet nevű függvény alapértelmezett definícióját kapja meg a fájlon RetrieveDefaultDefinitionRequest.jsparaméterekkel.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -File
Egy .json fájl elérési útját adja meg, amely a lekérés alapértelmezett függvénydefiníciós kérésének JSON (JavaScript Object Notation) ábrázolását tartalmazza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Annak a Stream Analytics-feladatnak a nevét adja meg, amelyhez a függvények tartoznak.
Ez a parancsmag a paraméter által megadott feladat egyik függvényének alapértelmezett definícióját kapja meg.

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

### -Name
Annak a Stream Analytics függvénynek a neve, amelyhez ez a parancsmag az alapértelmezett definíciót kapja.

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
Annak az erőforráscsoportnak a nevét adja meg, amelyhez a Stream Analytics függvény tartozik.
Ez a parancsmag a paraméter által megadott csoporthoz függvénydefiníciót kap.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzStreamAnalyticsFunction](./New-AzStreamAnalyticsFunction.md)


