---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1EDFCAC4-6A66-4124-8192-B7F0D3C5BCFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertHistory.md
ms.openlocfilehash: 4c8b53cbf5cbea2905f9957df7c45a0d29e61835
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500848"
---
# <span data-ttu-id="0d489-101">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="0d489-101">Get-AzureRmAlertHistory</span></span>

## <span data-ttu-id="0d489-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d489-102">SYNOPSIS</span></span>
<span data-ttu-id="0d489-103">Megkapja az értesítések előzményeit.</span><span class="sxs-lookup"><span data-stu-id="0d489-103">Gets the history of alerts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d489-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d489-104">SYNTAX</span></span>

```
Get-AzureRmAlertHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d489-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d489-105">DESCRIPTION</span></span>
<span data-ttu-id="0d489-106">A **Get-AzureRmAlertHistory** parancsmag a bekapcsolt üzenetek, a letiltott, a kiégett és a megoldott üzenetek előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0d489-106">The **Get-AzureRmAlertHistory** cmdlet gets the history of alerts as they are enabled, disabled, fired, resolved, and so on.</span></span>

## <span data-ttu-id="0d489-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0d489-107">EXAMPLES</span></span>

### <span data-ttu-id="0d489-108">Példa 1: az értesítési előzmények beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d489-108">Example 1: Get the alert history</span></span>
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
EventChannels        : Admin, Operation
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
EventChannels        : Admin, Operation
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
EventChannels        : Admin, Operation
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

<span data-ttu-id="0d489-109">Ez a parancs a jelenlegi előfizetés megadott időkeretének figyelmeztetési előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0d489-109">This command gets the alert history for the specified time frame for the current subscription.</span></span>

### <span data-ttu-id="0d489-110">2. példa: adott erőforrás riasztási előzményeinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="0d489-110">Example 2: Get alert history for a specified resource</span></span>
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
EventChannels        : Admin, Operation
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
EventChannels        : Admin, Operation
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

<span data-ttu-id="0d489-111">Ez a parancs a megadott erőforráshoz kapcsolódó figyelmeztetési szabályhoz kapcsolódó eseményeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0d489-111">This command gets the alert rule-related events for a specified resource.</span></span>

## <span data-ttu-id="0d489-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d489-112">PARAMETERS</span></span>

### <span data-ttu-id="0d489-113">-Hívó</span><span class="sxs-lookup"><span data-stu-id="0d489-113">-Caller</span></span>
<span data-ttu-id="0d489-114">A hívót adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d489-114">Specifies the caller.</span></span>

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

### <span data-ttu-id="0d489-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="0d489-115">-DetailedOutput</span></span>
<span data-ttu-id="0d489-116">A kimenet minden részletét megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="0d489-116">Displays full details in the output.</span></span>

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

### <span data-ttu-id="0d489-117">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="0d489-117">-EndTime</span></span>
<span data-ttu-id="0d489-118">A lekérdezés befejezési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="0d489-118">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="0d489-119">Az alapértelmezett időpont az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="0d489-119">The default is the current time.</span></span>

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

### <span data-ttu-id="0d489-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d489-120">-ResourceId</span></span>
<span data-ttu-id="0d489-121">Megadja, hogy a szabály melyik erőforrás-AZONOSÍTÓval van társítva.</span><span class="sxs-lookup"><span data-stu-id="0d489-121">Specifies the resource ID the rule is associated with.</span></span>

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

### <span data-ttu-id="0d489-122">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="0d489-122">-StartTime</span></span>
<span data-ttu-id="0d489-123">A lekérdezés kezdési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="0d489-123">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="0d489-124">Az alapértelmezett időpont az aktuális helyi idő, egy óra mínusz.</span><span class="sxs-lookup"><span data-stu-id="0d489-124">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="0d489-125">-Állapot</span><span class="sxs-lookup"><span data-stu-id="0d489-125">-Status</span></span>
<span data-ttu-id="0d489-126">Az állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d489-126">Specifies the status.</span></span>

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

### <span data-ttu-id="0d489-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d489-127">-DefaultProfile</span></span>
<span data-ttu-id="0d489-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d489-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d489-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d489-129">CommonParameters</span></span>
<span data-ttu-id="0d489-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d489-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d489-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d489-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d489-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d489-132">INPUTS</span></span>

## <span data-ttu-id="0d489-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d489-133">OUTPUTS</span></span>

### <span data-ttu-id="0d489-134">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. detekintés. OutputClasses. IPSEventData]</span><span class="sxs-lookup"><span data-stu-id="0d489-134">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSEventData]</span></span>

## <span data-ttu-id="0d489-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d489-135">NOTES</span></span>

## <span data-ttu-id="0d489-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d489-136">RELATED LINKS</span></span>

[<span data-ttu-id="0d489-137">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="0d489-137">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="0d489-138">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0d489-138">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="0d489-139">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0d489-139">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="0d489-140">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="0d489-140">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="0d489-141">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="0d489-141">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


