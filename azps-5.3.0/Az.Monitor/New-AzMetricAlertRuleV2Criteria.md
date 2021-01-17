---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480051"
---
# <span data-ttu-id="d22f1-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d22f1-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="d22f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d22f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d22f1-103">Helyi feltételobjektumot hoz létre, amely új metrikus riasztás létrehozására használható</span><span class="sxs-lookup"><span data-stu-id="d22f1-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="d22f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d22f1-104">SYNTAX</span></span>

### <span data-ttu-id="d22f1-105">StaticThresholdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d22f1-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d22f1-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22f1-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d22f1-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22f1-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d22f1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d22f1-108">DESCRIPTION</span></span>
<span data-ttu-id="d22f1-109">A **New-AzMetricAlertRuleV2Criteria** parancsmag létrehoz egy bemeneti [Add-AzMetricAlertRuleV2 parancsmagként](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) használható helyi metrikus feltételobjektumot, amely egy új metrikus riasztási szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d22f1-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="d22f1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d22f1-110">EXAMPLES</span></span>

### <span data-ttu-id="d22f1-111">1. példa: Egyszerű metrikus riasztási feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="d22f1-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="d22f1-112">Ez a parancs egyszerű metrikus riasztási feltételeket hoz létre, amelyek használhatók a metrikus riasztási szabályban</span><span class="sxs-lookup"><span data-stu-id="d22f1-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="d22f1-113">2. példa: Dinamikus metrikus riasztási feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="d22f1-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="d22f1-114">Ez a parancs dinamikus metrikus riasztási feltételeket hoz létre, amelyek használhatók a metrikus riasztási szabályban</span><span class="sxs-lookup"><span data-stu-id="d22f1-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="d22f1-115">3. példa: Összetettebb metrikus riasztási feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="d22f1-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="d22f1-116">Ez a parancskészlet összetettebb riasztási feltételeket hoz létre, amelyek tartalmazzák a dimenziók kiválasztását</span><span class="sxs-lookup"><span data-stu-id="d22f1-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="d22f1-117">4. példa: Webteszt elérhetőségi feltételének létrehozása</span><span class="sxs-lookup"><span data-stu-id="d22f1-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="d22f1-118">Ez a parancs webtesztel való elérhetőségi feltételeket hoz létre, amelyek metrikus riasztási szabályban használhatók</span><span class="sxs-lookup"><span data-stu-id="d22f1-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="d22f1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d22f1-119">PARAMETERS</span></span>

### <span data-ttu-id="d22f1-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="d22f1-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="d22f1-121">Az Application Insights erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="d22f1-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="d22f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22f1-122">-DefaultProfile</span></span>
<span data-ttu-id="d22f1-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d22f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22f1-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d22f1-124">-DimensionSelection</span></span>
<span data-ttu-id="d22f1-125">A dimenziófeltételek listája</span><span class="sxs-lookup"><span data-stu-id="d22f1-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="d22f1-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="d22f1-126">-DynamicThreshold</span></span>
<span data-ttu-id="d22f1-127">Switch parameter for using Dynamic Threshold Type</span><span class="sxs-lookup"><span data-stu-id="d22f1-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="d22f1-128">-AtlanokAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="d22f1-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="d22f1-129">A pontok száma összesen</span><span class="sxs-lookup"><span data-stu-id="d22f1-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="d22f1-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="d22f1-130">-FailedLocationCount</span></span>
<span data-ttu-id="d22f1-131">A riasztást nem adó helyek minimális száma.</span><span class="sxs-lookup"><span data-stu-id="d22f1-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="d22f1-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="d22f1-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="d22f1-133">Az IgnoreDataBefore paraméter</span><span class="sxs-lookup"><span data-stu-id="d22f1-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="d22f1-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d22f1-134">-MetricName</span></span>
<span data-ttu-id="d22f1-135">A szabály metrikus neve</span><span class="sxs-lookup"><span data-stu-id="d22f1-135">The metric name for rule</span></span>

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

### <span data-ttu-id="d22f1-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="d22f1-136">-MetricNamespace</span></span>
<span data-ttu-id="d22f1-137">A mutató névtere</span><span class="sxs-lookup"><span data-stu-id="d22f1-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="d22f1-138">-Operátor</span><span class="sxs-lookup"><span data-stu-id="d22f1-138">-Operator</span></span>
<span data-ttu-id="d22f1-139">A szabály feltétel operátora</span><span class="sxs-lookup"><span data-stu-id="d22f1-139">The rule condition operator</span></span>

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

### <span data-ttu-id="d22f1-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="d22f1-140">-SkipMetricValidation</span></span>
<span data-ttu-id="d22f1-141">Lehetővé teszi, hogy riasztási szabályt hozzon létre egy olyan egyéni metrikán, amely még nincs megadva, a metrikák érvényesítésének kihagyása miatt</span><span class="sxs-lookup"><span data-stu-id="d22f1-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="d22f1-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="d22f1-142">-Threshold</span></span>
<span data-ttu-id="d22f1-143">A szabály feltételének küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="d22f1-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="d22f1-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="d22f1-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="d22f1-145">A szabály feltételének érzékenysége</span><span class="sxs-lookup"><span data-stu-id="d22f1-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="d22f1-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="d22f1-146">-TimeAggregation</span></span>
<span data-ttu-id="d22f1-147">Az ablakintervallumban több metrikus érték összesítésére használt összegzési művelet</span><span class="sxs-lookup"><span data-stu-id="d22f1-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="d22f1-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="d22f1-148">-ViolationCount</span></span>
<span data-ttu-id="d22f1-149">A riasztások bejelentéséhez minimálisan szükséges szabálysértések száma a kiválasztott visszanéző időkeretben</span><span class="sxs-lookup"><span data-stu-id="d22f1-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="d22f1-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="d22f1-150">-WebTest</span></span>
<span data-ttu-id="d22f1-151">Switch parameter for using availability criteria Type</span><span class="sxs-lookup"><span data-stu-id="d22f1-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="d22f1-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="d22f1-152">-WebTestId</span></span>
<span data-ttu-id="d22f1-153">Az Application Insights webes tesztazonosítója.</span><span class="sxs-lookup"><span data-stu-id="d22f1-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="d22f1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22f1-154">CommonParameters</span></span>
<span data-ttu-id="d22f1-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22f1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22f1-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d22f1-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22f1-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d22f1-157">INPUTS</span></span>

### <span data-ttu-id="d22f1-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="d22f1-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="d22f1-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d22f1-159">OUTPUTS</span></span>

### <span data-ttu-id="d22f1-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="d22f1-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="d22f1-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d22f1-161">NOTES</span></span>

## <span data-ttu-id="d22f1-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d22f1-162">RELATED LINKS</span></span>
