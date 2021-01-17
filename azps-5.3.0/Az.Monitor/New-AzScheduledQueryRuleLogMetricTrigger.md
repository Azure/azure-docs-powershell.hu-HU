---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467562"
---
# <span data-ttu-id="49b11-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="49b11-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="49b11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b11-102">SYNOPSIS</span></span>
<span data-ttu-id="49b11-103">Naplómetrika-eseményindító típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="49b11-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="49b11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49b11-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49b11-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49b11-105">DESCRIPTION</span></span>
<span data-ttu-id="49b11-106">Naplómetrika-eseményindító típusú objektumot hoz létre, és nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="49b11-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="49b11-107">Ez a metrikus lekérdezési szabály eseményindító feltétele, amely akkor használható, ha a riasztás metrikus mérési típusát kell állapotra alkalmaznia.</span><span class="sxs-lookup"><span data-stu-id="49b11-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="49b11-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49b11-108">EXAMPLES</span></span>

### <span data-ttu-id="49b11-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="49b11-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="49b11-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b11-110">PARAMETERS</span></span>

### <span data-ttu-id="49b11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b11-111">-DefaultProfile</span></span>
<span data-ttu-id="49b11-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49b11-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b11-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="49b11-113">-MetricColumn</span></span>
<span data-ttu-id="49b11-114">Az az oszlop, amelyen a metrikus érték összesítve van.</span><span class="sxs-lookup"><span data-stu-id="49b11-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="49b11-115">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="49b11-115">The input is not validated.</span></span> <span data-ttu-id="49b11-116">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="49b11-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="49b11-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="49b11-117">-MetricTriggerType</span></span>
<span data-ttu-id="49b11-118">A metrikus eseményindító típusa.</span><span class="sxs-lookup"><span data-stu-id="49b11-118">The metric trigger type.</span></span>
<span data-ttu-id="49b11-119">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="49b11-119">The input is not validated.</span></span> <span data-ttu-id="49b11-120">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="49b11-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="49b11-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="49b11-121">-Threshold</span></span>
<span data-ttu-id="49b11-122">A metrikus küszöbérték: Egymást követő, Összeg.</span><span class="sxs-lookup"><span data-stu-id="49b11-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="49b11-123">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="49b11-123">The input is not validated.</span></span> <span data-ttu-id="49b11-124">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="49b11-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="49b11-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="49b11-125">-ThresholdOperator</span></span>
<span data-ttu-id="49b11-126">A metrikus küszöbérték operátora: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="49b11-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="49b11-127">A rendszer nem ellenőrzi a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="49b11-127">The input is not validated.</span></span> <span data-ttu-id="49b11-128">A rendszer először ellenőrzi, New-AzScheduledQueryRule a rendszer.</span><span class="sxs-lookup"><span data-stu-id="49b11-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="49b11-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b11-129">CommonParameters</span></span>
<span data-ttu-id="49b11-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b11-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b11-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49b11-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b11-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49b11-132">INPUTS</span></span>

### <span data-ttu-id="49b11-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="49b11-133">None</span></span>

## <span data-ttu-id="49b11-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49b11-134">OUTPUTS</span></span>

### <span data-ttu-id="49b11-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="49b11-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="49b11-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49b11-136">NOTES</span></span>

## <span data-ttu-id="49b11-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49b11-137">RELATED LINKS</span></span>
