---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 6e50269e98a942d425f914eed5cc0a75938d0e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002863"
---
# <span data-ttu-id="13d64-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="13d64-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="13d64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13d64-102">SYNOPSIS</span></span>
<span data-ttu-id="13d64-103">Helyi feltétel típusú objektumot hoz létre, amellyel új metrikus riasztást hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="13d64-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="13d64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13d64-104">SYNTAX</span></span>

### <span data-ttu-id="13d64-105">StaticThresholdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13d64-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d64-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13d64-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d64-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="13d64-107">DESCRIPTION</span></span>
<span data-ttu-id="13d64-108">A **New-AzMetricAlertRuleV2Criteria** parancsmag létrehoz egy helyi metrikus feltételt, amely az új metrikus riasztási szabályt létrehozó Add-AzMetricAlertRuleV2 parancsmagként használható.</span><span class="sxs-lookup"><span data-stu-id="13d64-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="13d64-109">Példák</span><span class="sxs-lookup"><span data-stu-id="13d64-109">EXAMPLES</span></span>

### <span data-ttu-id="13d64-110">Példa 1: egyszerű metrikus figyelmeztetési feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="13d64-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="13d64-111">Ez a parancs egy egyszerű metrikus riasztási feltételt hoz létre, melyet metrikus riasztási szabályban használhat</span><span class="sxs-lookup"><span data-stu-id="13d64-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="13d64-112">2. példa: dinamikus metrikus figyelmeztetési feltételek létrehozása</span><span class="sxs-lookup"><span data-stu-id="13d64-112">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="13d64-113">Ez a parancs a metrikus figyelmeztetési szabályokban használható dinamikus metrikus riasztási feltételeket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="13d64-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="13d64-114">3. példa: összetettebb metrikus riasztási feltételek létrehozása</span><span class="sxs-lookup"><span data-stu-id="13d64-114">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="13d64-115">Ez a parancs összetettebb metrikus riasztási feltételeket hoz létre, beleértve a dimenzió kijelölését</span><span class="sxs-lookup"><span data-stu-id="13d64-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="13d64-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13d64-116">PARAMETERS</span></span>

### <span data-ttu-id="13d64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d64-117">-DefaultProfile</span></span>
<span data-ttu-id="13d64-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13d64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d64-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="13d64-119">-DimensionSelection</span></span>
<span data-ttu-id="13d64-120">A dimenzió feltételeinek listája</span><span class="sxs-lookup"><span data-stu-id="13d64-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="13d64-121">-DynamicThreshold</span></span>
<span data-ttu-id="13d64-122">Kapcsoló paraméter a dinamikus küszöb típus használatához</span><span class="sxs-lookup"><span data-stu-id="13d64-122">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="13d64-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="13d64-124">A vizsgált pontok teljes száma</span><span class="sxs-lookup"><span data-stu-id="13d64-124">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="13d64-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="13d64-126">A IgnoreDataBefore paraméter</span><span class="sxs-lookup"><span data-stu-id="13d64-126">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="13d64-127">-MetricName</span></span>
<span data-ttu-id="13d64-128">A szabály metrikájának neve</span><span class="sxs-lookup"><span data-stu-id="13d64-128">The metric name for rule</span></span>

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

### <span data-ttu-id="13d64-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="13d64-129">-MetricNamespace</span></span>
<span data-ttu-id="13d64-130">A metrika névtere</span><span class="sxs-lookup"><span data-stu-id="13d64-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-131">-Operátor</span><span class="sxs-lookup"><span data-stu-id="13d64-131">-Operator</span></span>
<span data-ttu-id="13d64-132">A szabály feltételének operátora</span><span class="sxs-lookup"><span data-stu-id="13d64-132">The rule condition operator</span></span>

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

### <span data-ttu-id="13d64-133">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="13d64-133">-Threshold</span></span>
<span data-ttu-id="13d64-134">A szabály feltételének küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="13d64-134">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="13d64-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="13d64-136">A szabály feltételének érzékenysége</span><span class="sxs-lookup"><span data-stu-id="13d64-136">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-137">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="13d64-137">-TimeAggregation</span></span>
<span data-ttu-id="13d64-138">Az ablak intervallumában több metrikus érték összesítésére használt összesítési művelet</span><span class="sxs-lookup"><span data-stu-id="13d64-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="13d64-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="13d64-139">-ViolationCount</span></span>
<span data-ttu-id="13d64-140">Az értesítés megadásához szükséges, a kijelölt lookback időablakában szükséges szabálysértések minimális száma</span><span class="sxs-lookup"><span data-stu-id="13d64-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d64-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d64-141">CommonParameters</span></span>
<span data-ttu-id="13d64-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13d64-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d64-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13d64-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d64-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d64-144">INPUTS</span></span>

### <span data-ttu-id="13d64-145">Microsoft. Azure. Command. detekintés. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="13d64-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="13d64-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d64-146">OUTPUTS</span></span>

### <span data-ttu-id="13d64-147">Microsoft. Azure. commands. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="13d64-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="13d64-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13d64-148">NOTES</span></span>

## <span data-ttu-id="13d64-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13d64-149">RELATED LINKS</span></span>
