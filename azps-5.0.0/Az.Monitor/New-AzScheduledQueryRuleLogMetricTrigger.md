---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187290"
---
# <span data-ttu-id="5adda-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5adda-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="5adda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5adda-102">SYNOPSIS</span></span>
<span data-ttu-id="5adda-103">A log metrikus triggert tartalmazó objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5adda-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="5adda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5adda-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5adda-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5adda-105">DESCRIPTION</span></span>
<span data-ttu-id="5adda-106">Létrehoz egy olyan objektumot, amely log metrikus triggert hoz létre, és nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5adda-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="5adda-107">Ez a metrika-lekérdezési szabály kiváltó feltétele, amelyet akkor kell használni, amikor az értesítéshez meg kell határoznia a metrika mértékét.</span><span class="sxs-lookup"><span data-stu-id="5adda-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="5adda-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5adda-108">EXAMPLES</span></span>

### <span data-ttu-id="5adda-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5adda-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="5adda-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5adda-110">PARAMETERS</span></span>

### <span data-ttu-id="5adda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5adda-111">-DefaultProfile</span></span>
<span data-ttu-id="5adda-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5adda-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5adda-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="5adda-113">-MetricColumn</span></span>
<span data-ttu-id="5adda-114">Az az oszlop, amelyre a metrika értékét összesíti.</span><span class="sxs-lookup"><span data-stu-id="5adda-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="5adda-115">A program nem ellenőrzi a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="5adda-115">The input is not validated.</span></span> <span data-ttu-id="5adda-116">A program először ellenőrzi, hogy New-AzScheduledQueryRule-e előbb.</span><span class="sxs-lookup"><span data-stu-id="5adda-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5adda-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="5adda-117">-MetricTriggerType</span></span>
<span data-ttu-id="5adda-118">A metrika-indító típusa.</span><span class="sxs-lookup"><span data-stu-id="5adda-118">The metric trigger type.</span></span>
<span data-ttu-id="5adda-119">A program nem ellenőrzi a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="5adda-119">The input is not validated.</span></span> <span data-ttu-id="5adda-120">A program először ellenőrzi, hogy New-AzScheduledQueryRule-e előbb.</span><span class="sxs-lookup"><span data-stu-id="5adda-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5adda-121">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="5adda-121">-Threshold</span></span>
<span data-ttu-id="5adda-122">A metrika küszöbértéke: egymást követő, összesen.</span><span class="sxs-lookup"><span data-stu-id="5adda-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="5adda-123">A program nem ellenőrzi a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="5adda-123">The input is not validated.</span></span> <span data-ttu-id="5adda-124">A program először ellenőrzi, hogy New-AzScheduledQueryRule-e előbb.</span><span class="sxs-lookup"><span data-stu-id="5adda-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5adda-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="5adda-125">-ThresholdOperator</span></span>
<span data-ttu-id="5adda-126">Metrikus küszöb operátor: GreaterThan, LessThan, egyenlő.</span><span class="sxs-lookup"><span data-stu-id="5adda-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="5adda-127">A program nem ellenőrzi a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="5adda-127">The input is not validated.</span></span> <span data-ttu-id="5adda-128">A program először ellenőrzi, hogy New-AzScheduledQueryRule-e előbb.</span><span class="sxs-lookup"><span data-stu-id="5adda-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5adda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5adda-129">CommonParameters</span></span>
<span data-ttu-id="5adda-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5adda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5adda-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5adda-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5adda-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5adda-132">INPUTS</span></span>

### <span data-ttu-id="5adda-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="5adda-133">None</span></span>

## <span data-ttu-id="5adda-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5adda-134">OUTPUTS</span></span>

### <span data-ttu-id="5adda-135">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5adda-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="5adda-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5adda-136">NOTES</span></span>

## <span data-ttu-id="5adda-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5adda-137">RELATED LINKS</span></span>
