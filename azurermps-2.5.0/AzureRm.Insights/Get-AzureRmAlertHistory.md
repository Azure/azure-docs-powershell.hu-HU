---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1EDFCAC4-6A66-4124-8192-B7F0D3C5BCFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalerthistory
schema: 2.0.0
ms.openlocfilehash: b1e8680a960a9dead6f4dea19fc1bf822dec6916
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850837"
---
# Get-AzureRmAlertHistory

## Áttekintés
Megkapja az értesítések előzményeit.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmAlertHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmAlertHistory** parancsmag a bekapcsolt üzenetek, a letiltott, a kiégett és a megoldott üzenetek előzményeit kapja meg.

## Példák

### Példa 1: az értesítési előzmények beszerzése
```
PS C:\>Get-AzureRmAlertHistory -StartTime 2015-02-11T11:00:00 -EndTime 2015-02-11T12:00:00 -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' has been resolved for Website: 
                       garyyang1 (Default-Web-EastUS) 
EventDataId          : 769fab1c-fc9f-4e18-bc3a-fa79fbdd3616
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:14:45 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/769fab1c-fc
                       9f-4e18-bc3a-fa79fbdd3616/ticks/635592788857929926
Level                : Informational
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
OperationName        : ResolveAlert
Properties           : 
                       RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleDescription: 
                       Threshold      : 3
                       WindowSizeInMinutes: 5
                       Aggregation    : Total
                       Operator       : GreaterThan
                       MetricName     : CpuTime
                       MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Resolved
SubmissionTimestamp  : 2/11/2015 7:14:45 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            : 
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' was activated for Website: garyyang1
                       (Default-Web-EastUS) 
EventDataId          : 66277c94-2097-4f5f-860d-e585f1206cd7
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:04:46 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.web/sites/garyyang1/events/66277c94-2097-4f5f-860d-e585f1206cd7/ticks/6355927828650595
                       14
Level                : Error
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
OperationName        : ActivateAlert
Properties           : 
                       RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleDescription: 
                       Threshold      : 3
                       WindowSizeInMinutes: 5
                       Aggregation    : Total
                       Operator       : GreaterThan
                       MetricName     : CpuTime
                       MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.web
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.web/sites/garyyang1
Status               : Activated
SubmissionTimestamp  : 2/11/2015 7:04:46 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            : 
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' was activated for Website: garyyang1
                       (Default-Web-EastUS) 
EventDataId          : ec9f7b3c-c6ea-4b45-bd15-ff43e38491e3
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:04:46 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/ec9f7b3c-c6
                       ea-4b45-bd15-ff43e38491e3/ticks/635592782865059514
Level                : Error
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
OperationName        : ActivateAlert
Properties           : 
                       RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
                       RuleDescription: 
                       Threshold      : 3
                       WindowSizeInMinutes: 5
                       Aggregation    : Total
                       Operator       : GreaterThan
                       MetricName     : CpuTime
                       MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Activated
SubmissionTimestamp  : 2/11/2015 7:04:46 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

Ez a parancs a jelenlegi előfizetés megadott időkeretének figyelmeztetési előzményeit kapja meg.

### 2. példa: adott erőforrás riasztási előzményeinek beolvasása
```
PS C:\>Get-AzureRmAlertHistory -StartTime 2015-02-11T11:00:00 -EndTime 2015-02-11T12:00:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d" -DetailedOutput

Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' has been resolved for Website: 
                       garyyang1 (Default-Web-EastUS) 
EventDataId          : 769fab1c-fc9f-4e18-bc3a-fa79fbdd3616
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:14:45 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/769fab1c-fc
                       9f-4e18-bc3a-fa79fbdd3616/ticks/635592788857929926
Level                : Informational
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzg4ODU3OTI5OTI2
OperationName        : ResolveAlert
Properties           : 
RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleDescription: 
Threshold      : 3
WindowSizeInMinutes: 5
Aggregation    : Total
Operator       : GreaterThan
MetricName     : CpuTime
MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Resolved
SubmissionTimestamp  : 2/11/2015 7:14:45 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            : 
Authorization        : 
Caller               : Microsoft.Insights/alertRules
Claims               : 
                       http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/alertRules
CorrelationId        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
Description          : 'CpuTime GreaterThan 3 ([Count]) in the last 5 minutes' was activated for Website: garyyang1
                       (Default-Web-EastUS) 
EventDataId          : ec9f7b3c-c6ea-4b45-bd15-ff43e38491e3
EventName            : Alert
EventSource          : microsoft.insights/alertrules
EventTimestamp       : 2/11/2015 7:04:46 PM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/events/ec9f7b3c-c6
                       ea-4b45-bd15-ff43e38491e3/ticks/635592782865059514
Level                : Error
OperationId          : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d/incidents/L3N1YnNj
                       cmlwdGlvbnMvYTkzZmIwN2MtNmM5My00MGJlLWJmM2ItNGYwZGViYTEwZjRiL3Jlc291cmNlR3JvdXBzL0RlZmF1bHQtV2Vi
                       LUVhc3RVUy9wcm92aWRlcnMvbWljcm9zb2Z0Lmluc2lnaHRzL2FsZXJ0cnVsZXMvY2hlY2tydWxlMy00YjEzNTQwMS1hMzBj
                       LTQyMjQtYWUyMS1mYTUzYTViZDI1M2QwNjM1NTkyNzgyODY1MDU5NTE0
OperationName        : ActivateAlert
Properties           : 
RuleUri        : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleName       : checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
RuleDescription: 
Threshold      : 3
WindowSizeInMinutes: 5
Aggregation    : Total
Operator       : GreaterThan
MetricName     : CpuTime
MetricUnit     : Count
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/alertrules/checkrule3-4b135401-a30c-4224-ae21-fa53a5bd253d
Status               : Activated
SubmissionTimestamp  : 2/11/2015 7:04:46 PM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

Ez a parancs a megadott erőforráshoz kapcsolódó figyelmeztetési szabályhoz kapcsolódó eseményeket kapja meg.

## PARAMÉTEREK

### -Hívó
A hívót adja meg.

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

### -DetailedOutput
A kimenet minden részletét megjeleníti.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -A befejezési időpont
A lekérdezés befejezési időpontját adja meg helyi időben.
Az alapértelmezett időpont az aktuális idő.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Megadja, hogy a szabály melyik erőforrás-AZONOSÍTÓval van társítva.

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

### -Kezdő időpont
A lekérdezés kezdési időpontját adja meg helyi időben.
Az alapértelmezett időpont az aktuális helyi idő, egy óra mínusz.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
Az állapotot adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. null ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

### System. Management. Automation. SwitchParameter

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSEventData

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK



[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Get-AzureRmAlertRule](./Get-AzureRmAlertRule.md)

[Remove-AzureRmAlertRule](./Remove-AzureRmAlertRule.md)


