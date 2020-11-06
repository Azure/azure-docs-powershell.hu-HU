---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504144"
---
# <span data-ttu-id="9e689-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="9e689-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="9e689-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e689-102">SYNOPSIS</span></span>
<span data-ttu-id="9e689-103">Egy automéretarányos szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9e689-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e689-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e689-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e689-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e689-105">DESCRIPTION</span></span>
<span data-ttu-id="9e689-106">A **New-AzureRmAutoscaleRule** parancsmag automatikusan létrehoz egy automéretarányos szabályt.</span><span class="sxs-lookup"><span data-stu-id="9e689-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="9e689-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e689-107">EXAMPLES</span></span>

### <span data-ttu-id="9e689-108">1. példa: szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e689-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="9e689-109">Ez a parancs létrehoz egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="9e689-109">This command creates a rule.</span></span>

### <span data-ttu-id="9e689-110">2. példa: két szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e689-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="9e689-111">Az első parancs létrehoz egy szabályt a kérések metrikája számára, majd a $Rule 1 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9e689-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="9e689-112">A második parancs létrehozza a kérések metrikájának második szabályát, majd a $Rule 2 változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9e689-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="9e689-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e689-113">PARAMETERS</span></span>

### <span data-ttu-id="9e689-114">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9e689-114">-MetricName</span></span>
<span data-ttu-id="9e689-115">A metrika nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-115">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="9e689-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="9e689-116">-MetricResourceId</span></span>
<span data-ttu-id="9e689-117">A metrikus erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-117">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="9e689-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="9e689-118">-MetricStatistic</span></span>
<span data-ttu-id="9e689-119">A metrika statisztikáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="9e689-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9e689-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e689-121">Átlagos</span><span class="sxs-lookup"><span data-stu-id="9e689-121">Average</span></span>
- <span data-ttu-id="9e689-122">Min</span><span class="sxs-lookup"><span data-stu-id="9e689-122">Min</span></span>
- <span data-ttu-id="9e689-123">Max</span><span class="sxs-lookup"><span data-stu-id="9e689-123">Max</span></span>
- <span data-ttu-id="9e689-124">SZUM</span><span class="sxs-lookup"><span data-stu-id="9e689-124">Sum</span></span>

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

### <span data-ttu-id="9e689-125">-Operátor</span><span class="sxs-lookup"><span data-stu-id="9e689-125">-Operator</span></span>
<span data-ttu-id="9e689-126">Az operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-126">Specifies the operator.</span></span>
<span data-ttu-id="9e689-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9e689-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e689-128">Eredménye</span><span class="sxs-lookup"><span data-stu-id="9e689-128">Equals</span></span>
- <span data-ttu-id="9e689-129">NotEquals</span><span class="sxs-lookup"><span data-stu-id="9e689-129">NotEquals</span></span>
- <span data-ttu-id="9e689-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="9e689-130">GreaterThan</span></span>
- <span data-ttu-id="9e689-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="9e689-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="9e689-132">LessThan</span><span class="sxs-lookup"><span data-stu-id="9e689-132">LessThan</span></span>
- <span data-ttu-id="9e689-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="9e689-133">LessThanOrEqual</span></span>

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

### <span data-ttu-id="9e689-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="9e689-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="9e689-135">A kihűtési időt adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-135">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="9e689-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="9e689-136">-ScaleActionDirection</span></span>
<span data-ttu-id="9e689-137">A méretezési műveletek irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="9e689-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9e689-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e689-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e689-139">None</span></span>
- <span data-ttu-id="9e689-140">Növelése</span><span class="sxs-lookup"><span data-stu-id="9e689-140">Increase</span></span>
- <span data-ttu-id="9e689-141">Csökkentése</span><span class="sxs-lookup"><span data-stu-id="9e689-141">Decrease</span></span>

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

### <span data-ttu-id="9e689-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="9e689-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="9e689-143">A méretarány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-143">Specifies the scale type.</span></span>
<span data-ttu-id="9e689-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9e689-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e689-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="9e689-145">ChangeSize</span></span>
- <span data-ttu-id="9e689-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="9e689-146">ChangeCount</span></span>
- <span data-ttu-id="9e689-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="9e689-147">PercentChangeCount</span></span>
- <span data-ttu-id="9e689-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="9e689-148">ExactCount</span></span>

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

### <span data-ttu-id="9e689-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="9e689-149">-ScaleActionValue</span></span>
<span data-ttu-id="9e689-150">A Művelettípus értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-150">Specifies the action value.</span></span>

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

### <span data-ttu-id="9e689-151">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="9e689-151">-Threshold</span></span>
<span data-ttu-id="9e689-152">A metrikus érték küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-152">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="9e689-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="9e689-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="9e689-154">Az idő összesítése operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="9e689-155">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9e689-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e689-156">Átlagos</span><span class="sxs-lookup"><span data-stu-id="9e689-156">Average</span></span>
- <span data-ttu-id="9e689-157">Minimális</span><span class="sxs-lookup"><span data-stu-id="9e689-157">Minimum</span></span>
- <span data-ttu-id="9e689-158">Maximális</span><span class="sxs-lookup"><span data-stu-id="9e689-158">Maximum</span></span>
- <span data-ttu-id="9e689-159">Utolsó</span><span class="sxs-lookup"><span data-stu-id="9e689-159">Last</span></span>
- <span data-ttu-id="9e689-160">Összeg, darabszám</span><span class="sxs-lookup"><span data-stu-id="9e689-160">Total, Count</span></span>

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

### <span data-ttu-id="9e689-161">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="9e689-161">-TimeGrain</span></span>
<span data-ttu-id="9e689-162">A gabona időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-162">Specifies the time grain.</span></span>

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

### <span data-ttu-id="9e689-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="9e689-163">-TimeWindow</span></span>
<span data-ttu-id="9e689-164">Az időablakot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e689-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="9e689-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e689-165">-DefaultProfile</span></span>
<span data-ttu-id="9e689-166">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e689-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e689-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e689-167">CommonParameters</span></span>
<span data-ttu-id="9e689-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e689-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e689-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e689-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e689-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e689-170">INPUTS</span></span>

## <span data-ttu-id="9e689-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e689-171">OUTPUTS</span></span>

### <span data-ttu-id="9e689-172">Microsoft. Azure. Management. monitor. Management. models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="9e689-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="9e689-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e689-173">NOTES</span></span>

## <span data-ttu-id="9e689-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e689-174">RELATED LINKS</span></span>

[<span data-ttu-id="9e689-175">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9e689-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9e689-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="9e689-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="9e689-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9e689-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9e689-178">Új – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9e689-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="9e689-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9e689-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


