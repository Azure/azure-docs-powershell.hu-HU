---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 101d522c1f8ae3b44545bdb204bad01fbe21df9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184425"
---
# <span data-ttu-id="96204-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="96204-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="96204-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96204-102">SYNOPSIS</span></span>
<span data-ttu-id="96204-103">Helyi feltétel típusú objektumot hoz létre, amellyel új metrikus riasztást hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="96204-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="96204-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96204-104">SYNTAX</span></span>

### <span data-ttu-id="96204-105">StaticThresholdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96204-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96204-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96204-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96204-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="96204-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96204-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="96204-108">DESCRIPTION</span></span>
<span data-ttu-id="96204-109">A **New-AzMetricAlertRuleV2Criteria** parancsmag létrehoz egy helyi metrikus feltételt, amely az új metrikus riasztási szabályt létrehozó Add-AzMetricAlertRuleV2 parancsmagként használható.</span><span class="sxs-lookup"><span data-stu-id="96204-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="96204-110">Példák</span><span class="sxs-lookup"><span data-stu-id="96204-110">EXAMPLES</span></span>

### <span data-ttu-id="96204-111">Példa 1: egyszerű metrikus figyelmeztetési feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="96204-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="96204-112">Ez a parancs egy egyszerű metrikus riasztási feltételt hoz létre, melyet metrikus riasztási szabályban használhat</span><span class="sxs-lookup"><span data-stu-id="96204-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="96204-113">2. példa: dinamikus metrikus figyelmeztetési feltételek létrehozása</span><span class="sxs-lookup"><span data-stu-id="96204-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="96204-114">Ez a parancs a metrikus figyelmeztetési szabályokban használható dinamikus metrikus riasztási feltételeket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="96204-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="96204-115">3. példa: összetettebb metrikus riasztási feltételek létrehozása</span><span class="sxs-lookup"><span data-stu-id="96204-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="96204-116">Ez a parancs összetettebb metrikus riasztási feltételeket hoz létre, beleértve a dimenzió kijelölését</span><span class="sxs-lookup"><span data-stu-id="96204-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="96204-117">Példa 4: webteszt elérhetőségi feltételeinek létrehozása</span><span class="sxs-lookup"><span data-stu-id="96204-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="96204-118">Ez a parancs egy olyan webteszt elérhetőségi feltételt hoz létre, amelyet metrikus riasztási szabályban használhat</span><span class="sxs-lookup"><span data-stu-id="96204-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="96204-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96204-119">PARAMETERS</span></span>

### <span data-ttu-id="96204-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="96204-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="96204-121">Az alkalmazás betekintést nyújt az erőforrás-azonosítóra.</span><span class="sxs-lookup"><span data-stu-id="96204-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="96204-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96204-122">-DefaultProfile</span></span>
<span data-ttu-id="96204-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96204-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96204-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="96204-124">-DimensionSelection</span></span>
<span data-ttu-id="96204-125">A dimenzió feltételeinek listája</span><span class="sxs-lookup"><span data-stu-id="96204-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="96204-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="96204-126">-DynamicThreshold</span></span>
<span data-ttu-id="96204-127">Kapcsoló paraméter a dinamikus küszöb típus használatához</span><span class="sxs-lookup"><span data-stu-id="96204-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="96204-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="96204-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="96204-129">A vizsgált pontok teljes száma</span><span class="sxs-lookup"><span data-stu-id="96204-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="96204-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="96204-130">-FailedLocationCount</span></span>
<span data-ttu-id="96204-131">A sikertelen helyek minimális száma riasztás kiemeléséhez.</span><span class="sxs-lookup"><span data-stu-id="96204-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="96204-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="96204-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="96204-133">A IgnoreDataBefore paraméter</span><span class="sxs-lookup"><span data-stu-id="96204-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="96204-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="96204-134">-MetricName</span></span>
<span data-ttu-id="96204-135">A szabály metrikájának neve</span><span class="sxs-lookup"><span data-stu-id="96204-135">The metric name for rule</span></span>

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

### <span data-ttu-id="96204-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="96204-136">-MetricNamespace</span></span>
<span data-ttu-id="96204-137">A metrika névtere</span><span class="sxs-lookup"><span data-stu-id="96204-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="96204-138">-Operátor</span><span class="sxs-lookup"><span data-stu-id="96204-138">-Operator</span></span>
<span data-ttu-id="96204-139">A szabály feltételének operátora</span><span class="sxs-lookup"><span data-stu-id="96204-139">The rule condition operator</span></span>

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

### <span data-ttu-id="96204-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="96204-140">-SkipMetricValidation</span></span>
<span data-ttu-id="96204-141">Lehetővé teszi a riasztási szabályok létrehozásának egy olyan egyéni metrikát, amely még nincs elküldve, mert így a metrika érvényesítése kimarad</span><span class="sxs-lookup"><span data-stu-id="96204-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="96204-142">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="96204-142">-Threshold</span></span>
<span data-ttu-id="96204-143">A szabály feltételének küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="96204-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="96204-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="96204-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="96204-145">A szabály feltételének érzékenysége</span><span class="sxs-lookup"><span data-stu-id="96204-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="96204-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="96204-146">-TimeAggregation</span></span>
<span data-ttu-id="96204-147">Az ablak intervallumában több metrikus érték összesítésére használt összesítési művelet</span><span class="sxs-lookup"><span data-stu-id="96204-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="96204-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="96204-148">-ViolationCount</span></span>
<span data-ttu-id="96204-149">Az értesítés megadásához szükséges, a kijelölt lookback időablakában szükséges szabálysértések minimális száma</span><span class="sxs-lookup"><span data-stu-id="96204-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="96204-150">-Webteszt</span><span class="sxs-lookup"><span data-stu-id="96204-150">-WebTest</span></span>
<span data-ttu-id="96204-151">Kapcsoló paraméter a elérhetőségi feltételek típusának használatához</span><span class="sxs-lookup"><span data-stu-id="96204-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="96204-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="96204-152">-WebTestId</span></span>
<span data-ttu-id="96204-153">Az alkalmazás betekintést nyújt a webes teszt-azonosítóba.</span><span class="sxs-lookup"><span data-stu-id="96204-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="96204-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96204-154">CommonParameters</span></span>
<span data-ttu-id="96204-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96204-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96204-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96204-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96204-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96204-157">INPUTS</span></span>

### <span data-ttu-id="96204-158">Microsoft. Azure. Command. detekintés. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="96204-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="96204-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96204-159">OUTPUTS</span></span>

### <span data-ttu-id="96204-160">Microsoft. Azure. commands. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="96204-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="96204-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96204-161">NOTES</span></span>

## <span data-ttu-id="96204-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96204-162">RELATED LINKS</span></span>
