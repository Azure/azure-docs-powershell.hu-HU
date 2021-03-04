---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: 193c0c8b263f7ceee62cc7cb99c47769a22c7633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933938"
---
# <span data-ttu-id="47c64-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="47c64-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="47c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47c64-102">SYNOPSIS</span></span>
<span data-ttu-id="47c64-103">Automatikus skálázási szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47c64-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="47c64-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47c64-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47c64-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47c64-105">DESCRIPTION</span></span>
<span data-ttu-id="47c64-106">Az **Új-AzAutoscaleRule** parancsmag létrehoz egy automatikus skálázási szabályt.</span><span class="sxs-lookup"><span data-stu-id="47c64-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="47c64-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47c64-107">EXAMPLES</span></span>

### <span data-ttu-id="47c64-108">1. példa: Szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="47c64-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="47c64-109">Ez a parancs létrehoz egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="47c64-109">This command creates a rule.</span></span>

### <span data-ttu-id="47c64-110">2. példa: Két szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="47c64-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="47c64-111">Az első parancs létrehoz egy szabályt a Kérelmek metrikára, majd azt a $Rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="47c64-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="47c64-112">A második parancs létrehoz egy második szabályt a Kérelmek mutatóhoz, majd a $Rule 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="47c64-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="47c64-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="47c64-113">Example 3</span></span>

<span data-ttu-id="47c64-114">Automatikus skálázási szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47c64-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="47c64-115">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="47c64-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="47c64-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47c64-116">PARAMETERS</span></span>

### <span data-ttu-id="47c64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c64-117">-DefaultProfile</span></span>
<span data-ttu-id="47c64-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="47c64-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47c64-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="47c64-119">-MetricName</span></span>
<span data-ttu-id="47c64-120">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="47c64-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="47c64-121">-MetricResourceId</span></span>
<span data-ttu-id="47c64-122">A metrikus erőforrásazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="47c64-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="47c64-123">-MetricStatistic</span></span>
<span data-ttu-id="47c64-124">A metrikus statisztika megadása.</span><span class="sxs-lookup"><span data-stu-id="47c64-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="47c64-125">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="47c64-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47c64-126">Átlag</span><span class="sxs-lookup"><span data-stu-id="47c64-126">Average</span></span>
- <span data-ttu-id="47c64-127">Min</span><span class="sxs-lookup"><span data-stu-id="47c64-127">Min</span></span>
- <span data-ttu-id="47c64-128">Max</span><span class="sxs-lookup"><span data-stu-id="47c64-128">Max</span></span>
- <span data-ttu-id="47c64-129">Összeg</span><span class="sxs-lookup"><span data-stu-id="47c64-129">Sum</span></span>

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

### <span data-ttu-id="47c64-130">-Operátor</span><span class="sxs-lookup"><span data-stu-id="47c64-130">-Operator</span></span>
<span data-ttu-id="47c64-131">Az operátort határozza meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-131">Specifies the operator.</span></span>
<span data-ttu-id="47c64-132">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="47c64-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47c64-133">Egyenlő</span><span class="sxs-lookup"><span data-stu-id="47c64-133">Equals</span></span>
- <span data-ttu-id="47c64-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="47c64-134">NotEquals</span></span>
- <span data-ttu-id="47c64-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="47c64-135">GreaterThan</span></span>
- <span data-ttu-id="47c64-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="47c64-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="47c64-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="47c64-137">LessThan</span></span>
- <span data-ttu-id="47c64-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="47c64-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="47c64-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="47c64-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="47c64-140">Az Automatikus skálázás művelet lehűtődési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="47c64-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="47c64-141">-ScaleActionDirection</span></span>
<span data-ttu-id="47c64-142">A méretezési művelet irányát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="47c64-143">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="47c64-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47c64-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="47c64-144">None</span></span>
- <span data-ttu-id="47c64-145">Növekedés</span><span class="sxs-lookup"><span data-stu-id="47c64-145">Increase</span></span>
- <span data-ttu-id="47c64-146">Csökkenés</span><span class="sxs-lookup"><span data-stu-id="47c64-146">Decrease</span></span>

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

### <span data-ttu-id="47c64-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="47c64-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="47c64-148">A méretarány típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-148">Specifies the scale type.</span></span>
<span data-ttu-id="47c64-149">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="47c64-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47c64-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="47c64-150">ChangeSize</span></span>
- <span data-ttu-id="47c64-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="47c64-151">ChangeCount</span></span>
- <span data-ttu-id="47c64-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="47c64-152">PercentChangeCount</span></span>
- <span data-ttu-id="47c64-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="47c64-153">ExactCount</span></span>

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

### <span data-ttu-id="47c64-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="47c64-154">-ScaleActionValue</span></span>
<span data-ttu-id="47c64-155">A művelet értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="47c64-156">-Threshold</span><span class="sxs-lookup"><span data-stu-id="47c64-156">-Threshold</span></span>
<span data-ttu-id="47c64-157">A metrikus érték küszöbértékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="47c64-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="47c64-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="47c64-159">Az időösszesítő operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="47c64-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="47c64-160">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="47c64-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47c64-161">Átlag</span><span class="sxs-lookup"><span data-stu-id="47c64-161">Average</span></span>
- <span data-ttu-id="47c64-162">Minimum</span><span class="sxs-lookup"><span data-stu-id="47c64-162">Minimum</span></span>
- <span data-ttu-id="47c64-163">Maximum</span><span class="sxs-lookup"><span data-stu-id="47c64-163">Maximum</span></span>
- <span data-ttu-id="47c64-164">Utolsó</span><span class="sxs-lookup"><span data-stu-id="47c64-164">Last</span></span>
- <span data-ttu-id="47c64-165">Összesen, Darab</span><span class="sxs-lookup"><span data-stu-id="47c64-165">Total, Count</span></span>

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

### <span data-ttu-id="47c64-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="47c64-166">-TimeGrain</span></span>
<span data-ttu-id="47c64-167">Az időszemét.</span><span class="sxs-lookup"><span data-stu-id="47c64-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="47c64-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="47c64-168">-TimeWindow</span></span>
<span data-ttu-id="47c64-169">Az időkeret megadása.</span><span class="sxs-lookup"><span data-stu-id="47c64-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="47c64-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c64-170">CommonParameters</span></span>
<span data-ttu-id="47c64-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c64-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c64-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47c64-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c64-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47c64-173">INPUTS</span></span>

### <span data-ttu-id="47c64-174">System.String</span><span class="sxs-lookup"><span data-stu-id="47c64-174">System.String</span></span>

### <span data-ttu-id="47c64-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="47c64-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="47c64-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="47c64-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="47c64-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="47c64-177">System.Double</span></span>

### <span data-ttu-id="47c64-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="47c64-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="47c64-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="47c64-179">System.TimeSpan</span></span>

### <span data-ttu-id="47c64-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="47c64-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="47c64-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="47c64-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="47c64-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47c64-182">OUTPUTS</span></span>

### <span data-ttu-id="47c64-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="47c64-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="47c64-184">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47c64-184">NOTES</span></span>

## <span data-ttu-id="47c64-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47c64-185">RELATED LINKS</span></span>

[<span data-ttu-id="47c64-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="47c64-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="47c64-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="47c64-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="47c64-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="47c64-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="47c64-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="47c64-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="47c64-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="47c64-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


