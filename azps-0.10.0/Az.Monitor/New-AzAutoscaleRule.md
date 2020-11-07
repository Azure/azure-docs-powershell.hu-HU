---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: ac588fe9a82209cfd56c08f750fcd35945bc8af1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841982"
---
# <span data-ttu-id="0b1b7-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="0b1b7-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="0b1b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1b7-103">Egy automéretarányos szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="0b1b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b1b7-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b1b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b1b7-105">DESCRIPTION</span></span>
<span data-ttu-id="0b1b7-106">A **New-AzAutoscaleRule** parancsmag automatikusan létrehoz egy automéretarányos szabályt.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="0b1b7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0b1b7-107">EXAMPLES</span></span>

### <span data-ttu-id="0b1b7-108">1. példa: szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="0b1b7-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="0b1b7-109">Ez a parancs létrehoz egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-109">This command creates a rule.</span></span>

### <span data-ttu-id="0b1b7-110">2. példa: két szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="0b1b7-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="0b1b7-111">Az első parancs létrehoz egy szabályt a kérések metrikája számára, majd a $Rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="0b1b7-112">A második parancs létrehozza a kérések metrikájának második szabályát, majd a $Rule 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="0b1b7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b1b7-113">PARAMETERS</span></span>

### <span data-ttu-id="0b1b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1b7-114">-DefaultProfile</span></span>
<span data-ttu-id="0b1b7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0b1b7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b1b7-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="0b1b7-116">-MetricName</span></span>
<span data-ttu-id="0b1b7-117">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="0b1b7-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="0b1b7-118">-MetricResourceId</span></span>
<span data-ttu-id="0b1b7-119">A metrikus erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="0b1b7-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="0b1b7-120">-MetricStatistic</span></span>
<span data-ttu-id="0b1b7-121">A metrika statisztikáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="0b1b7-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b1b7-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b1b7-123">Átlagos</span><span class="sxs-lookup"><span data-stu-id="0b1b7-123">Average</span></span>
- <span data-ttu-id="0b1b7-124">Min</span><span class="sxs-lookup"><span data-stu-id="0b1b7-124">Min</span></span>
- <span data-ttu-id="0b1b7-125">Max</span><span class="sxs-lookup"><span data-stu-id="0b1b7-125">Max</span></span>
- <span data-ttu-id="0b1b7-126">SZUM</span><span class="sxs-lookup"><span data-stu-id="0b1b7-126">Sum</span></span>

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

### <span data-ttu-id="0b1b7-127">-Operátor</span><span class="sxs-lookup"><span data-stu-id="0b1b7-127">-Operator</span></span>
<span data-ttu-id="0b1b7-128">Az operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-128">Specifies the operator.</span></span>
<span data-ttu-id="0b1b7-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b1b7-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b1b7-130">Eredménye</span><span class="sxs-lookup"><span data-stu-id="0b1b7-130">Equals</span></span>
- <span data-ttu-id="0b1b7-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="0b1b7-131">NotEquals</span></span>
- <span data-ttu-id="0b1b7-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="0b1b7-132">GreaterThan</span></span>
- <span data-ttu-id="0b1b7-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="0b1b7-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="0b1b7-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="0b1b7-134">LessThan</span></span>
- <span data-ttu-id="0b1b7-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="0b1b7-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="0b1b7-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="0b1b7-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="0b1b7-137">A kihűtési időt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="0b1b7-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="0b1b7-138">-ScaleActionDirection</span></span>
<span data-ttu-id="0b1b7-139">A méretezési műveletek irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="0b1b7-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b1b7-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b1b7-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b1b7-141">None</span></span>
- <span data-ttu-id="0b1b7-142">Növelése</span><span class="sxs-lookup"><span data-stu-id="0b1b7-142">Increase</span></span>
- <span data-ttu-id="0b1b7-143">Csökkentése</span><span class="sxs-lookup"><span data-stu-id="0b1b7-143">Decrease</span></span>

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

### <span data-ttu-id="0b1b7-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="0b1b7-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="0b1b7-145">A méretarány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-145">Specifies the scale type.</span></span>
<span data-ttu-id="0b1b7-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b1b7-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b1b7-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="0b1b7-147">ChangeSize</span></span>
- <span data-ttu-id="0b1b7-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="0b1b7-148">ChangeCount</span></span>
- <span data-ttu-id="0b1b7-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="0b1b7-149">PercentChangeCount</span></span>
- <span data-ttu-id="0b1b7-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="0b1b7-150">ExactCount</span></span>

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

### <span data-ttu-id="0b1b7-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="0b1b7-151">-ScaleActionValue</span></span>
<span data-ttu-id="0b1b7-152">A Művelettípus értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="0b1b7-153">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="0b1b7-153">-Threshold</span></span>
<span data-ttu-id="0b1b7-154">A metrikus érték küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="0b1b7-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="0b1b7-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="0b1b7-156">Az idő összesítése operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="0b1b7-157">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0b1b7-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b1b7-158">Átlagos</span><span class="sxs-lookup"><span data-stu-id="0b1b7-158">Average</span></span>
- <span data-ttu-id="0b1b7-159">Minimális</span><span class="sxs-lookup"><span data-stu-id="0b1b7-159">Minimum</span></span>
- <span data-ttu-id="0b1b7-160">Maximális</span><span class="sxs-lookup"><span data-stu-id="0b1b7-160">Maximum</span></span>
- <span data-ttu-id="0b1b7-161">Utolsó</span><span class="sxs-lookup"><span data-stu-id="0b1b7-161">Last</span></span>
- <span data-ttu-id="0b1b7-162">Összeg, darabszám</span><span class="sxs-lookup"><span data-stu-id="0b1b7-162">Total, Count</span></span>

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

### <span data-ttu-id="0b1b7-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="0b1b7-163">-TimeGrain</span></span>
<span data-ttu-id="0b1b7-164">A gabona időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="0b1b7-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="0b1b7-165">-TimeWindow</span></span>
<span data-ttu-id="0b1b7-166">Az időablakot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="0b1b7-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1b7-167">CommonParameters</span></span>
<span data-ttu-id="0b1b7-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b1b7-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1b7-169">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1b7-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b1b7-170">INPUTS</span></span>

### <span data-ttu-id="0b1b7-171">System. String</span><span class="sxs-lookup"><span data-stu-id="0b1b7-171">System.String</span></span>

### <span data-ttu-id="0b1b7-172">Microsoft. Azure. Management. monitor. Management. models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="0b1b7-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="0b1b7-173">Microsoft. Azure. Management. monitor. Management. models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="0b1b7-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="0b1b7-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="0b1b7-174">System.Double</span></span>

### <span data-ttu-id="0b1b7-175">Microsoft. Azure. Management. monitor. Management. models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="0b1b7-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="0b1b7-176">System. időszak</span><span class="sxs-lookup"><span data-stu-id="0b1b7-176">System.TimeSpan</span></span>

### <span data-ttu-id="0b1b7-177">Microsoft. Azure. Management. monitor. Management. models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="0b1b7-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="0b1b7-178">Microsoft. Azure. Management. monitor. Management. models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="0b1b7-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="0b1b7-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b1b7-179">OUTPUTS</span></span>

### <span data-ttu-id="0b1b7-180">Microsoft. Azure. Management. monitor. Management. models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="0b1b7-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="0b1b7-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b1b7-181">NOTES</span></span>

## <span data-ttu-id="0b1b7-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b1b7-182">RELATED LINKS</span></span>

[<span data-ttu-id="0b1b7-183">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="0b1b7-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="0b1b7-184">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="0b1b7-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="0b1b7-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="0b1b7-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="0b1b7-186">Új – AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="0b1b7-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="0b1b7-187">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="0b1b7-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


