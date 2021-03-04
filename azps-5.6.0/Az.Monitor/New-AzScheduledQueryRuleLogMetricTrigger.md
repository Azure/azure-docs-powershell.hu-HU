---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 0270c9bf6d543455772095a6d0fe3f0f1a55a416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931826"
---
# <span data-ttu-id="84e46-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="84e46-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="84e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e46-102">SYNOPSIS</span></span>
<span data-ttu-id="84e46-103">Naplómetrika-eseményindító típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="84e46-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="84e46-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84e46-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84e46-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84e46-105">DESCRIPTION</span></span>
<span data-ttu-id="84e46-106">Naplómetrika-eseményindító típusú objektumot hoz létre, és nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="84e46-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="84e46-107">Ez a metrikus lekérdezési szabály eseményindító feltétele, amely akkor használható, ha a riasztás metrikus mérési típusát kell állapotra alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="84e46-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="84e46-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84e46-108">EXAMPLES</span></span>

### <span data-ttu-id="84e46-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="84e46-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="84e46-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84e46-110">PARAMETERS</span></span>

### <span data-ttu-id="84e46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e46-111">-DefaultProfile</span></span>
<span data-ttu-id="84e46-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84e46-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84e46-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="84e46-113">-MetricColumn</span></span>
<span data-ttu-id="84e46-114">Az az oszlop, amelyen a metrikus érték összesítve van.</span><span class="sxs-lookup"><span data-stu-id="84e46-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="84e46-115">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="84e46-115">The input is not validated.</span></span> <span data-ttu-id="84e46-116">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="84e46-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e46-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="84e46-117">-MetricTriggerType</span></span>
<span data-ttu-id="84e46-118">A metrikus eseményindító típusa.</span><span class="sxs-lookup"><span data-stu-id="84e46-118">The metric trigger type.</span></span>
<span data-ttu-id="84e46-119">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="84e46-119">The input is not validated.</span></span> <span data-ttu-id="84e46-120">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="84e46-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e46-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="84e46-121">-Threshold</span></span>
<span data-ttu-id="84e46-122">A metrikus küszöbérték: Egymást követő, Összeg.</span><span class="sxs-lookup"><span data-stu-id="84e46-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="84e46-123">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="84e46-123">The input is not validated.</span></span> <span data-ttu-id="84e46-124">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="84e46-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e46-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="84e46-125">-ThresholdOperator</span></span>
<span data-ttu-id="84e46-126">A metrikus küszöbérték operátora: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="84e46-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="84e46-127">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="84e46-127">The input is not validated.</span></span> <span data-ttu-id="84e46-128">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="84e46-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e46-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e46-129">CommonParameters</span></span>
<span data-ttu-id="84e46-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e46-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e46-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84e46-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e46-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84e46-132">INPUTS</span></span>

### <span data-ttu-id="84e46-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="84e46-133">None</span></span>

## <span data-ttu-id="84e46-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84e46-134">OUTPUTS</span></span>

### <span data-ttu-id="84e46-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="84e46-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="84e46-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84e46-136">NOTES</span></span>

## <span data-ttu-id="84e46-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84e46-137">RELATED LINKS</span></span>
