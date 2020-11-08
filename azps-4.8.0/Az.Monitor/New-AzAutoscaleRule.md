---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184431"
---
# <span data-ttu-id="840ac-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="840ac-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="840ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="840ac-102">SYNOPSIS</span></span>
<span data-ttu-id="840ac-103">Egy automéretarányos szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="840ac-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="840ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="840ac-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="840ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="840ac-105">DESCRIPTION</span></span>
<span data-ttu-id="840ac-106">A **New-AzAutoscaleRule** parancsmag automatikusan létrehoz egy automéretarányos szabályt.</span><span class="sxs-lookup"><span data-stu-id="840ac-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="840ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="840ac-107">EXAMPLES</span></span>

### <span data-ttu-id="840ac-108">1. példa: szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="840ac-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="840ac-109">Ez a parancs létrehoz egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="840ac-109">This command creates a rule.</span></span>

### <span data-ttu-id="840ac-110">2. példa: két szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="840ac-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="840ac-111">Az első parancs létrehoz egy szabályt a kérések metrikája számára, majd a $Rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="840ac-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="840ac-112">A második parancs létrehozza a kérések metrikájának második szabályát, majd a $Rule 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="840ac-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="840ac-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="840ac-113">Example 3</span></span>

<span data-ttu-id="840ac-114">Egy automéretarányos szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="840ac-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="840ac-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="840ac-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="840ac-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="840ac-116">PARAMETERS</span></span>

### <span data-ttu-id="840ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="840ac-117">-DefaultProfile</span></span>
<span data-ttu-id="840ac-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="840ac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="840ac-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="840ac-119">-MetricName</span></span>
<span data-ttu-id="840ac-120">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-120">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="840ac-121">-MetricResourceId</span></span>
<span data-ttu-id="840ac-122">A metrikus erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-122">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="840ac-123">-MetricStatistic</span></span>
<span data-ttu-id="840ac-124">A metrika statisztikáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="840ac-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="840ac-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="840ac-126">Átlagos</span><span class="sxs-lookup"><span data-stu-id="840ac-126">Average</span></span>
- <span data-ttu-id="840ac-127">Min</span><span class="sxs-lookup"><span data-stu-id="840ac-127">Min</span></span>
- <span data-ttu-id="840ac-128">Max</span><span class="sxs-lookup"><span data-stu-id="840ac-128">Max</span></span>
- <span data-ttu-id="840ac-129">SZUM</span><span class="sxs-lookup"><span data-stu-id="840ac-129">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-130">-Operátor</span><span class="sxs-lookup"><span data-stu-id="840ac-130">-Operator</span></span>
<span data-ttu-id="840ac-131">Az operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-131">Specifies the operator.</span></span>
<span data-ttu-id="840ac-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="840ac-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="840ac-133">Eredménye</span><span class="sxs-lookup"><span data-stu-id="840ac-133">Equals</span></span>
- <span data-ttu-id="840ac-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="840ac-134">NotEquals</span></span>
- <span data-ttu-id="840ac-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="840ac-135">GreaterThan</span></span>
- <span data-ttu-id="840ac-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="840ac-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="840ac-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="840ac-137">LessThan</span></span>
- <span data-ttu-id="840ac-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="840ac-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="840ac-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="840ac-140">A kihűtési időt adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-140">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="840ac-141">-ScaleActionDirection</span></span>
<span data-ttu-id="840ac-142">A méretezési műveletek irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="840ac-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="840ac-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="840ac-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="840ac-144">None</span></span>
- <span data-ttu-id="840ac-145">Növelése</span><span class="sxs-lookup"><span data-stu-id="840ac-145">Increase</span></span>
- <span data-ttu-id="840ac-146">Csökkentése</span><span class="sxs-lookup"><span data-stu-id="840ac-146">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases:
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="840ac-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="840ac-148">A méretarány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-148">Specifies the scale type.</span></span>
<span data-ttu-id="840ac-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="840ac-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="840ac-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="840ac-150">ChangeSize</span></span>
- <span data-ttu-id="840ac-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="840ac-151">ChangeCount</span></span>
- <span data-ttu-id="840ac-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="840ac-152">PercentChangeCount</span></span>
- <span data-ttu-id="840ac-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="840ac-153">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases:
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="840ac-154">-ScaleActionValue</span></span>
<span data-ttu-id="840ac-155">A Művelettípus értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-155">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-156">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="840ac-156">-Threshold</span></span>
<span data-ttu-id="840ac-157">A metrikus érték küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-157">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="840ac-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="840ac-159">Az idő összesítése operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="840ac-160">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="840ac-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="840ac-161">Átlagos</span><span class="sxs-lookup"><span data-stu-id="840ac-161">Average</span></span>
- <span data-ttu-id="840ac-162">Minimális</span><span class="sxs-lookup"><span data-stu-id="840ac-162">Minimum</span></span>
- <span data-ttu-id="840ac-163">Maximális</span><span class="sxs-lookup"><span data-stu-id="840ac-163">Maximum</span></span>
- <span data-ttu-id="840ac-164">Utolsó</span><span class="sxs-lookup"><span data-stu-id="840ac-164">Last</span></span>
- <span data-ttu-id="840ac-165">Összeg, darabszám</span><span class="sxs-lookup"><span data-stu-id="840ac-165">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="840ac-166">-TimeGrain</span></span>
<span data-ttu-id="840ac-167">A gabona időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-167">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="840ac-168">-TimeWindow</span></span>
<span data-ttu-id="840ac-169">Az időablakot adja meg.</span><span class="sxs-lookup"><span data-stu-id="840ac-169">Specifies the time window.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="840ac-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="840ac-170">CommonParameters</span></span>
<span data-ttu-id="840ac-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="840ac-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="840ac-172">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="840ac-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="840ac-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="840ac-173">INPUTS</span></span>

### <span data-ttu-id="840ac-174">System. String</span><span class="sxs-lookup"><span data-stu-id="840ac-174">System.String</span></span>

### <span data-ttu-id="840ac-175">Microsoft. Azure. Management. monitor. Management. models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="840ac-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="840ac-176">Microsoft. Azure. Management. monitor. Management. models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="840ac-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="840ac-177">System. Double</span><span class="sxs-lookup"><span data-stu-id="840ac-177">System.Double</span></span>

### <span data-ttu-id="840ac-178">Microsoft. Azure. Management. monitor. Management. models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="840ac-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="840ac-179">System. időszak</span><span class="sxs-lookup"><span data-stu-id="840ac-179">System.TimeSpan</span></span>

### <span data-ttu-id="840ac-180">Microsoft. Azure. Management. monitor. Management. models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="840ac-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="840ac-181">Microsoft. Azure. Management. monitor. Management. models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="840ac-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="840ac-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="840ac-182">OUTPUTS</span></span>

### <span data-ttu-id="840ac-183">Microsoft. Azure. Management. monitor. Management. models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="840ac-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="840ac-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="840ac-184">NOTES</span></span>

## <span data-ttu-id="840ac-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="840ac-185">RELATED LINKS</span></span>

[<span data-ttu-id="840ac-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="840ac-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="840ac-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="840ac-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="840ac-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="840ac-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="840ac-189">Új – AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="840ac-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="840ac-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="840ac-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


