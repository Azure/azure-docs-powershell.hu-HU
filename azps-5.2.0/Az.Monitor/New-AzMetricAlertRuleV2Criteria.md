---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331601"
---
# <span data-ttu-id="d8cfc-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d8cfc-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="d8cfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cfc-103">Helyi feltételobjektumot hoz létre, amely új metrikus riasztás létrehozására használható</span><span class="sxs-lookup"><span data-stu-id="d8cfc-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="d8cfc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8cfc-104">SYNTAX</span></span>

### <span data-ttu-id="d8cfc-105">StaticThresholdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8cfc-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8cfc-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8cfc-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8cfc-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8cfc-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8cfc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8cfc-108">DESCRIPTION</span></span>
<span data-ttu-id="d8cfc-109">A **New-AzMetricAlertRuleV2Criteria** parancsmag létrehoz egy bemeneti [Add-AzMetricAlertRuleV2 parancsmagként](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) használható helyi metrikus feltételobjektumot, amely egy új metrikus riasztási szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d8cfc-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="d8cfc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8cfc-110">EXAMPLES</span></span>

### <span data-ttu-id="d8cfc-111">1. példa: Egyszerű metrikus riasztási feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="d8cfc-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="d8cfc-112">Ez a parancs egyszerű metrikus riasztási feltételeket hoz létre, amelyek használhatók a metrikus riasztási szabályban</span><span class="sxs-lookup"><span data-stu-id="d8cfc-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="d8cfc-113">2. példa: Dinamikus metrikus riasztási feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="d8cfc-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="d8cfc-114">Ez a parancs dinamikus metrikus riasztási feltételeket hoz létre, amelyek használhatók a metrikus riasztási szabályban</span><span class="sxs-lookup"><span data-stu-id="d8cfc-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="d8cfc-115">3. példa: Összetettebb metrikus riasztási feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="d8cfc-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="d8cfc-116">Ez a parancskészlet összetettebb riasztási feltételeket hoz létre, amelyek tartalmazzák a dimenziók kiválasztását</span><span class="sxs-lookup"><span data-stu-id="d8cfc-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="d8cfc-117">4. példa: Webteszt elérhetőségi feltételének létrehozása</span><span class="sxs-lookup"><span data-stu-id="d8cfc-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="d8cfc-118">Ez a parancs webtesztel való elérhetőségi feltételeket hoz létre, amelyek metrikus riasztási szabályban használhatók</span><span class="sxs-lookup"><span data-stu-id="d8cfc-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="d8cfc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8cfc-119">PARAMETERS</span></span>

### <span data-ttu-id="d8cfc-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="d8cfc-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="d8cfc-121">Az Application Insights erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8cfc-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cfc-122">-DefaultProfile</span></span>
<span data-ttu-id="d8cfc-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8cfc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8cfc-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d8cfc-124">-DimensionSelection</span></span>
<span data-ttu-id="d8cfc-125">A dimenziófeltételek listája</span><span class="sxs-lookup"><span data-stu-id="d8cfc-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="d8cfc-126">-DynamicThreshold</span></span>
<span data-ttu-id="d8cfc-127">Switch parameter for using Dynamic Threshold Type</span><span class="sxs-lookup"><span data-stu-id="d8cfc-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="d8cfc-128">-AtlanokAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="d8cfc-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="d8cfc-129">A pontok száma összesen</span><span class="sxs-lookup"><span data-stu-id="d8cfc-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="d8cfc-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="d8cfc-130">-FailedLocationCount</span></span>
<span data-ttu-id="d8cfc-131">A riasztást feladó sikertelen helyek minimális száma.</span><span class="sxs-lookup"><span data-stu-id="d8cfc-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="d8cfc-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="d8cfc-133">Az IgnoreDataBefore paraméter</span><span class="sxs-lookup"><span data-stu-id="d8cfc-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="d8cfc-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d8cfc-134">-MetricName</span></span>
<span data-ttu-id="d8cfc-135">A szabály metrikus neve</span><span class="sxs-lookup"><span data-stu-id="d8cfc-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="d8cfc-136">-MetricNamespace</span></span>
<span data-ttu-id="d8cfc-137">A metrika névtere</span><span class="sxs-lookup"><span data-stu-id="d8cfc-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-138">-Operátor</span><span class="sxs-lookup"><span data-stu-id="d8cfc-138">-Operator</span></span>
<span data-ttu-id="d8cfc-139">A szabály feltétel operátora</span><span class="sxs-lookup"><span data-stu-id="d8cfc-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="d8cfc-140">-SkipMetricValidation</span></span>
<span data-ttu-id="d8cfc-141">Lehetővé teszi, hogy riasztási szabályt hozzon létre egy olyan egyéni metrikán, amely még nincs megadva, a metrikák érvényesítésének kihagyása miatt</span><span class="sxs-lookup"><span data-stu-id="d8cfc-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="d8cfc-142">-Threshold</span></span>
<span data-ttu-id="d8cfc-143">A szabály feltételének küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="d8cfc-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="d8cfc-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="d8cfc-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="d8cfc-145">A szabály feltételének érzékenysége</span><span class="sxs-lookup"><span data-stu-id="d8cfc-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="d8cfc-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="d8cfc-146">-TimeAggregation</span></span>
<span data-ttu-id="d8cfc-147">Az ablakintervallumban több metrikus érték összesítésére használt összegzési művelet</span><span class="sxs-lookup"><span data-stu-id="d8cfc-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="d8cfc-148">-ViolationCount</span></span>
<span data-ttu-id="d8cfc-149">A riasztások bejelentéséhez minimálisan szükséges szabálysértések száma a kiválasztott visszanéző időkeretben</span><span class="sxs-lookup"><span data-stu-id="d8cfc-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="d8cfc-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="d8cfc-150">-WebTest</span></span>
<span data-ttu-id="d8cfc-151">Switch parameter for using availability criteria Type</span><span class="sxs-lookup"><span data-stu-id="d8cfc-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="d8cfc-152">-WebTestId</span></span>
<span data-ttu-id="d8cfc-153">Az Application Insights webes tesztazonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8cfc-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cfc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cfc-154">CommonParameters</span></span>
<span data-ttu-id="d8cfc-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cfc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cfc-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8cfc-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cfc-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8cfc-157">INPUTS</span></span>

### <span data-ttu-id="d8cfc-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="d8cfc-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="d8cfc-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8cfc-159">OUTPUTS</span></span>

### <span data-ttu-id="d8cfc-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="d8cfc-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="d8cfc-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8cfc-161">NOTES</span></span>

## <span data-ttu-id="d8cfc-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8cfc-162">RELATED LINKS</span></span>
