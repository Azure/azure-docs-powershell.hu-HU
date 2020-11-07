---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678987"
---
# <span data-ttu-id="c8132-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c8132-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="c8132-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8132-102">SYNOPSIS</span></span>
<span data-ttu-id="c8132-103">Egy automéretarányos szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8132-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8132-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8132-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8132-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8132-105">DESCRIPTION</span></span>
<span data-ttu-id="c8132-106">A **New-AzureRmAutoscaleRule** parancsmag automatikusan létrehoz egy automéretarányos szabályt.</span><span class="sxs-lookup"><span data-stu-id="c8132-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="c8132-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8132-107">EXAMPLES</span></span>

### <span data-ttu-id="c8132-108">1. példa: szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="c8132-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c8132-109">Ez a parancs létrehoz egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="c8132-109">This command creates a rule.</span></span>

### <span data-ttu-id="c8132-110">2. példa: két szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="c8132-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c8132-111">Az első parancs létrehoz egy szabályt a kérések metrikája számára, majd a $Rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c8132-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="c8132-112">A második parancs létrehozza a kérések metrikájának második szabályát, majd a $Rule 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c8132-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="c8132-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8132-113">PARAMETERS</span></span>

### <span data-ttu-id="c8132-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8132-114">-DefaultProfile</span></span>
<span data-ttu-id="c8132-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c8132-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="c8132-116">-MetricName</span></span>
<span data-ttu-id="c8132-117">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="c8132-118">-MetricResourceId</span></span>
<span data-ttu-id="c8132-119">A metrikus erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="c8132-120">-MetricStatistic</span></span>
<span data-ttu-id="c8132-121">A metrika statisztikáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="c8132-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c8132-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8132-123">Átlagos</span><span class="sxs-lookup"><span data-stu-id="c8132-123">Average</span></span>
- <span data-ttu-id="c8132-124">Min</span><span class="sxs-lookup"><span data-stu-id="c8132-124">Min</span></span>
- <span data-ttu-id="c8132-125">Max</span><span class="sxs-lookup"><span data-stu-id="c8132-125">Max</span></span>
- <span data-ttu-id="c8132-126">SZUM</span><span class="sxs-lookup"><span data-stu-id="c8132-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-127">-Operátor</span><span class="sxs-lookup"><span data-stu-id="c8132-127">-Operator</span></span>
<span data-ttu-id="c8132-128">Az operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-128">Specifies the operator.</span></span>
<span data-ttu-id="c8132-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c8132-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8132-130">Eredménye</span><span class="sxs-lookup"><span data-stu-id="c8132-130">Equals</span></span>
- <span data-ttu-id="c8132-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="c8132-131">NotEquals</span></span>
- <span data-ttu-id="c8132-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="c8132-132">GreaterThan</span></span>
- <span data-ttu-id="c8132-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c8132-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="c8132-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="c8132-134">LessThan</span></span>
- <span data-ttu-id="c8132-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c8132-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="c8132-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="c8132-137">A kihűtési időt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="c8132-138">-ScaleActionDirection</span></span>
<span data-ttu-id="c8132-139">A méretezési műveletek irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="c8132-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c8132-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8132-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="c8132-141">None</span></span>
- <span data-ttu-id="c8132-142">Növelése</span><span class="sxs-lookup"><span data-stu-id="c8132-142">Increase</span></span>
- <span data-ttu-id="c8132-143">Csökkentése</span><span class="sxs-lookup"><span data-stu-id="c8132-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="c8132-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="c8132-145">A méretarány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-145">Specifies the scale type.</span></span>
<span data-ttu-id="c8132-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c8132-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8132-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="c8132-147">ChangeSize</span></span>
- <span data-ttu-id="c8132-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="c8132-148">ChangeCount</span></span>
- <span data-ttu-id="c8132-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="c8132-149">PercentChangeCount</span></span>
- <span data-ttu-id="c8132-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="c8132-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="c8132-151">-ScaleActionValue</span></span>
<span data-ttu-id="c8132-152">A Művelettípus értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-153">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="c8132-153">-Threshold</span></span>
<span data-ttu-id="c8132-154">A metrikus érték küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="c8132-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="c8132-156">Az idő összesítése operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="c8132-157">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c8132-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8132-158">Átlagos</span><span class="sxs-lookup"><span data-stu-id="c8132-158">Average</span></span>
- <span data-ttu-id="c8132-159">Minimális</span><span class="sxs-lookup"><span data-stu-id="c8132-159">Minimum</span></span>
- <span data-ttu-id="c8132-160">Maximális</span><span class="sxs-lookup"><span data-stu-id="c8132-160">Maximum</span></span>
- <span data-ttu-id="c8132-161">Utolsó</span><span class="sxs-lookup"><span data-stu-id="c8132-161">Last</span></span>
- <span data-ttu-id="c8132-162">Összeg, darabszám</span><span class="sxs-lookup"><span data-stu-id="c8132-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c8132-163">-TimeGrain</span></span>
<span data-ttu-id="c8132-164">A gabona időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="c8132-165">-TimeWindow</span></span>
<span data-ttu-id="c8132-166">Az időablakot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8132-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8132-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8132-167">CommonParameters</span></span>
<span data-ttu-id="c8132-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8132-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8132-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8132-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8132-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8132-170">INPUTS</span></span>

### <span data-ttu-id="c8132-171">Nincs</span><span class="sxs-lookup"><span data-stu-id="c8132-171">None</span></span>
<span data-ttu-id="c8132-172">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c8132-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8132-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8132-173">OUTPUTS</span></span>

### <span data-ttu-id="c8132-174">Microsoft. Azure. Management. monitor. Management. models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="c8132-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="c8132-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8132-175">NOTES</span></span>

## <span data-ttu-id="c8132-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8132-176">RELATED LINKS</span></span>

[<span data-ttu-id="c8132-177">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c8132-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="c8132-178">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="c8132-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="c8132-179">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c8132-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="c8132-180">Új – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c8132-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="c8132-181">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c8132-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


