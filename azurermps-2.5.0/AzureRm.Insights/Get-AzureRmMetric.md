---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
ms.openlocfilehash: 5a0594bc1a90457874a590628076daf7e7d49d8d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848297"
---
# <span data-ttu-id="fb912-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="fb912-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="fb912-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb912-102">SYNOPSIS</span></span>
<span data-ttu-id="fb912-103">Egy erőforrás metrikus értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb912-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb912-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb912-104">SYNTAX</span></span>

### <span data-ttu-id="fb912-105">GetWithDefaultParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb912-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb912-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="fb912-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb912-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb912-107">DESCRIPTION</span></span>
<span data-ttu-id="fb912-108">A **Get-AzureRmMetric** parancsmag egy adott erőforrás metrikus értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb912-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="fb912-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fb912-109">EXAMPLES</span></span>

### <span data-ttu-id="fb912-110">Példa 1: mérőszám beszerzése összegzett kimenettel</span><span class="sxs-lookup"><span data-stu-id="fb912-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="fb912-111">Ez a parancs 1 percen keresztül beolvassa a website3 metrikus értékeit.</span><span class="sxs-lookup"><span data-stu-id="fb912-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="fb912-112">2. példa: mérőszám beszerzése részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="fb912-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="fb912-113">Ez a parancs 1 percen keresztül beolvassa a website3 metrikus értékeit.</span><span class="sxs-lookup"><span data-stu-id="fb912-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="fb912-114">A kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="fb912-114">The output is detailed.</span></span>

### <span data-ttu-id="fb912-115">3. példa: részletes kimenet beszerzése adott metrika esetén</span><span class="sxs-lookup"><span data-stu-id="fb912-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricNames "Requests" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="fb912-116">Ez a parancs részletesen Kinyeri a kérések metrikáját.</span><span class="sxs-lookup"><span data-stu-id="fb912-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="fb912-117">Példa 4: az összegzett kimenet beolvasása adott metrika esetén a megadott szűrővel</span><span class="sxs-lookup"><span data-stu-id="fb912-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzureRmMetricFilter -Dimension City -Operator eq -Values "Seattle","Toronto"), (New-AzureRmMetricDimensionFilter -Dimension AuthenticationType -Operator eq -Values User))

PS C:\> Get-AzureRmMetricValues -ResourceId <resourcId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="fb912-118">Ez a parancs az oldalmegtekintések metrikájának összesített kimenetét adja meg a megadott Dimes szűrővel és összesítési típussal.</span><span class="sxs-lookup"><span data-stu-id="fb912-118">This command gets summarized output for the PageViews metric with specified dimesion filter and aggregation type.</span></span>

## <span data-ttu-id="fb912-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb912-119">PARAMETERS</span></span>

### <span data-ttu-id="fb912-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="fb912-120">-AggregationType</span></span>
<span data-ttu-id="fb912-121">A lekérdezés összesítési típusa</span><span class="sxs-lookup"><span data-stu-id="fb912-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb912-122">-DefaultProfile</span></span>
<span data-ttu-id="fb912-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb912-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb912-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="fb912-124">-DetailedOutput</span></span>
<span data-ttu-id="fb912-125">Azt jelzi, hogy ez a parancsmag részletes kimenetet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="fb912-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="fb912-126">A program alapértelmezés szerint összesíti a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fb912-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-127">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="fb912-127">-EndTime</span></span>
<span data-ttu-id="fb912-128">A lekérdezés befejezési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="fb912-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="fb912-129">Az alapértelmezett időpont az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="fb912-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="fb912-130">-MetricFilter</span></span>
<span data-ttu-id="fb912-131">A metrika dimenzió szűrőt adja meg az érték lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="fb912-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="fb912-132">-MetricName</span></span>
<span data-ttu-id="fb912-133">A metrikák neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb912-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="fb912-134">-MetricNamespace</span></span>
<span data-ttu-id="fb912-135">A metrikus névteret adja meg a mérőszámok lekérdezéséhez.</span><span class="sxs-lookup"><span data-stu-id="fb912-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="fb912-136">-OrderBy</span></span>
<span data-ttu-id="fb912-137">A találatok rendezéséhez és a rendezés irányához használt összesítést adja meg (példa: SZUM ASC).</span><span class="sxs-lookup"><span data-stu-id="fb912-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb912-138">-ResourceId</span></span>
<span data-ttu-id="fb912-139">A metrika erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb912-139">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="fb912-140">-ResultType</span></span>
<span data-ttu-id="fb912-141">A visszaadott eredmény (metaadat vagy adatok) meghatározása.</span><span class="sxs-lookup"><span data-stu-id="fb912-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-142">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="fb912-142">-StartTime</span></span>
<span data-ttu-id="fb912-143">A lekérdezés kezdési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="fb912-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="fb912-144">Az alapértelmezett időpont az aktuális helyi idő, egy óra mínusz.</span><span class="sxs-lookup"><span data-stu-id="fb912-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="fb912-145">-TimeGrain</span></span>
<span data-ttu-id="fb912-146">A metrika **időszak** -objektumként való időpontját adja meg a hh: mm: SS formátumban.</span><span class="sxs-lookup"><span data-stu-id="fb912-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="fb912-147">-Top</span><span class="sxs-lookup"><span data-stu-id="fb912-147">-Top</span></span>
<span data-ttu-id="fb912-148">A lekérdezni kívánt rekordok maximális számát adja meg (alapértelmezett: 10), amelyet az $filter meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="fb912-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb912-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb912-149">CommonParameters</span></span>
<span data-ttu-id="fb912-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb912-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb912-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb912-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb912-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb912-152">INPUTS</span></span>

### <span data-ttu-id="fb912-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fb912-153">System.String</span></span>

### <span data-ttu-id="fb912-154">System. időszak</span><span class="sxs-lookup"><span data-stu-id="fb912-154">System.TimeSpan</span></span>

### <span data-ttu-id="fb912-155">System. null ' 1 [[Microsoft. Azure. Management. monitor. models. AggregationType, Microsoft. Azure. Management. monitor, Version = 0.19.1.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fb912-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fb912-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fb912-156">System.DateTime</span></span>

### <span data-ttu-id="fb912-157">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fb912-157">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fb912-158">System. null ' 1 [[Microsoft. Azure. Management. monitor. models. ResultType, Microsoft. Azure. Management. monitor, Version = 0.19.1.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fb912-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fb912-159">System. string []</span><span class="sxs-lookup"><span data-stu-id="fb912-159">System.String[]</span></span>

### <span data-ttu-id="fb912-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb912-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb912-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb912-161">OUTPUTS</span></span>

### <span data-ttu-id="fb912-162">Microsoft. Azure. commands. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="fb912-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="fb912-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb912-163">NOTES</span></span>

## <span data-ttu-id="fb912-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb912-164">RELATED LINKS</span></span>

<span data-ttu-id="fb912-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md) 
 [Új – AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="fb912-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


