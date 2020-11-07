---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 4873d093411c07af9b1a5389299e39ecca0a5f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837755"
---
# <span data-ttu-id="a1855-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a1855-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="a1855-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1855-102">SYNOPSIS</span></span>
<span data-ttu-id="a1855-103">A log metrikus verzió típusú triggert tartalmazó objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a1855-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="a1855-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1855-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1855-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1855-105">DESCRIPTION</span></span>
<span data-ttu-id="a1855-106">Létrehoz egy olyan objektumot, amely log metrikus triggert hoz létre, és nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a1855-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="a1855-107">Ez a metrika-lekérdezési szabály kiváltó feltétele, amelyet akkor kell használni, amikor az értesítéshez meg kell határoznia a metrika mértékét.</span><span class="sxs-lookup"><span data-stu-id="a1855-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="a1855-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a1855-108">EXAMPLES</span></span>

### <span data-ttu-id="a1855-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1855-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="a1855-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1855-110">PARAMETERS</span></span>

### <span data-ttu-id="a1855-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1855-111">-DefaultProfile</span></span>
<span data-ttu-id="a1855-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1855-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1855-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="a1855-113">-MetricColumn</span></span>
<span data-ttu-id="a1855-114">Az az oszlop, amelyen a metrikus érték összesítve van</span><span class="sxs-lookup"><span data-stu-id="a1855-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="a1855-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="a1855-115">-MetricTriggerType</span></span>
<span data-ttu-id="a1855-116">A metrika-indító típusa</span><span class="sxs-lookup"><span data-stu-id="a1855-116">The metric trigger type</span></span>

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

### <span data-ttu-id="a1855-117">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="a1855-117">-Threshold</span></span>
<span data-ttu-id="a1855-118">A metrika küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="a1855-118">The metric threshold value</span></span>

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

### <span data-ttu-id="a1855-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="a1855-119">-ThresholdOperator</span></span>
<span data-ttu-id="a1855-120">Metrikus küszöb operátor: GreaterThan, LessThan, egyenlő</span><span class="sxs-lookup"><span data-stu-id="a1855-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="a1855-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1855-121">CommonParameters</span></span>
<span data-ttu-id="a1855-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1855-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1855-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1855-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1855-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1855-124">INPUTS</span></span>

### <span data-ttu-id="a1855-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="a1855-125">None</span></span>

## <span data-ttu-id="a1855-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1855-126">OUTPUTS</span></span>

### <span data-ttu-id="a1855-127">Microsoft. Azure. commands. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a1855-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="a1855-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1855-128">NOTES</span></span>

## <span data-ttu-id="a1855-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1855-129">RELATED LINKS</span></span>
