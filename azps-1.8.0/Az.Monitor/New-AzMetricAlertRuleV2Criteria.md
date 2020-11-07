---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835030"
---
# <span data-ttu-id="f5fc4-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f5fc4-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="f5fc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="f5fc4-103">Helyi feltétel típusú objektumot hoz létre, amellyel új metrikus riasztást hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="f5fc4-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="f5fc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5fc4-104">SYNTAX</span></span>

### <span data-ttu-id="f5fc4-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5fc4-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5fc4-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5fc4-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5fc4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5fc4-107">DESCRIPTION</span></span>
<span data-ttu-id="f5fc4-108">A **New-AzMetricAlertRuleV2Criteria** parancsmag létrehoz egy helyi metrikus feltételt, amely az új metrikus riasztási szabályt létrehozó Add-AzMetricAlertRuleV2 parancsmagként használható.</span><span class="sxs-lookup"><span data-stu-id="f5fc4-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="f5fc4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5fc4-109">EXAMPLES</span></span>

### <span data-ttu-id="f5fc4-110">Példa 1: egyszerű metrikus figyelmeztetési feltétel létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5fc4-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="f5fc4-111">Ez a parancs egy egyszerű metrikus riasztási feltételt hoz létre, melyet metrikus riasztási szabályban használhat</span><span class="sxs-lookup"><span data-stu-id="f5fc4-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="f5fc4-112">2. példa: összetettebb metrikus riasztási feltételek létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5fc4-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="f5fc4-113">Ez a parancs összetettebb metrikus riasztási feltételeket hoz létre, beleértve a dimenzió kijelölését</span><span class="sxs-lookup"><span data-stu-id="f5fc4-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="f5fc4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5fc4-114">PARAMETERS</span></span>

### <span data-ttu-id="f5fc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5fc4-115">-DefaultProfile</span></span>
<span data-ttu-id="f5fc4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5fc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f5fc4-117">-DimensionSelection</span></span>
<span data-ttu-id="f5fc4-118">A dimenzió feltételeinek listája</span><span class="sxs-lookup"><span data-stu-id="f5fc4-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="f5fc4-119">-DynamicThreshold</span></span>
<span data-ttu-id="f5fc4-120">A szabály feltételének dinamikus küszöbe</span><span class="sxs-lookup"><span data-stu-id="f5fc4-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="f5fc4-121">-FailingPeriod</span></span>
<span data-ttu-id="f5fc4-122">A szabály feltételének hibás időszaka</span><span class="sxs-lookup"><span data-stu-id="f5fc4-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="f5fc4-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="f5fc4-124">A IgnoreDataBefore paraméter</span><span class="sxs-lookup"><span data-stu-id="f5fc4-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="f5fc4-125">-MetricName</span></span>
<span data-ttu-id="f5fc4-126">A szabály metrikájának neve</span><span class="sxs-lookup"><span data-stu-id="f5fc4-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="f5fc4-127">-MetricNamespace</span></span>
<span data-ttu-id="f5fc4-128">A metrika névtere</span><span class="sxs-lookup"><span data-stu-id="f5fc4-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-129">-Operátor</span><span class="sxs-lookup"><span data-stu-id="f5fc4-129">-Operator</span></span>
<span data-ttu-id="f5fc4-130">A szabály feltételének operátora</span><span class="sxs-lookup"><span data-stu-id="f5fc4-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-131">-Érzékenység</span><span class="sxs-lookup"><span data-stu-id="f5fc4-131">-Sensitivity</span></span>
<span data-ttu-id="f5fc4-132">A szabály feltételének érzékenysége</span><span class="sxs-lookup"><span data-stu-id="f5fc4-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-133">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="f5fc4-133">-Threshold</span></span>
<span data-ttu-id="f5fc4-134">A szabály feltételének küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="f5fc4-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-135">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="f5fc4-135">-TimeAggregation</span></span>
<span data-ttu-id="f5fc4-136">Az ablak intervallumában több metrikus érték összesítésére használt összesítési művelet</span><span class="sxs-lookup"><span data-stu-id="f5fc4-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="f5fc4-137">-TotalPeriod</span></span>
<span data-ttu-id="f5fc4-138">A szabály feltételének teljes időtartama</span><span class="sxs-lookup"><span data-stu-id="f5fc4-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fc4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5fc4-139">CommonParameters</span></span>
<span data-ttu-id="f5fc4-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5fc4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f5fc4-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5fc4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5fc4-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5fc4-142">INPUTS</span></span>

### <span data-ttu-id="f5fc4-143">Microsoft. Azure. Command. detekintés. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="f5fc4-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="f5fc4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5fc4-144">OUTPUTS</span></span>

### <span data-ttu-id="f5fc4-145">Microsoft. Azure. commands. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="f5fc4-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="f5fc4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5fc4-146">NOTES</span></span>

## <span data-ttu-id="f5fc4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5fc4-147">RELATED LINKS</span></span>
