---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672264"
---
# <span data-ttu-id="b2946-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="b2946-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="b2946-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2946-102">SYNOPSIS</span></span>
<span data-ttu-id="b2946-103">Egy erőforrás metrikus értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2946-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2946-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2946-104">SYNTAX</span></span>

### <span data-ttu-id="b2946-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="b2946-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2946-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="b2946-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2946-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2946-107">DESCRIPTION</span></span>
<span data-ttu-id="b2946-108">A **Get-AzureRmMetric** parancsmag egy adott erőforrás metrikus értékeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2946-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="b2946-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2946-109">EXAMPLES</span></span>

### <span data-ttu-id="b2946-110">Példa 1: mérőszám beszerzése összegzett kimenettel</span><span class="sxs-lookup"><span data-stu-id="b2946-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="b2946-111">Ez a parancs 1 percen keresztül beolvassa a website3 metrikus értékeit.</span><span class="sxs-lookup"><span data-stu-id="b2946-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="b2946-112">2. példa: mérőszám beszerzése részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="b2946-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="b2946-113">Ez a parancs 1 percen keresztül beolvassa a website3 metrikus értékeit.</span><span class="sxs-lookup"><span data-stu-id="b2946-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="b2946-114">A kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="b2946-114">The output is detailed.</span></span>

### <span data-ttu-id="b2946-115">3. példa: részletes kimenet beszerzése adott metrika esetén</span><span class="sxs-lookup"><span data-stu-id="b2946-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
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

<span data-ttu-id="b2946-116">Ez a parancs részletesen Kinyeri a kérések metrikáját.</span><span class="sxs-lookup"><span data-stu-id="b2946-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="b2946-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2946-117">PARAMETERS</span></span>

### <span data-ttu-id="b2946-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="b2946-118">-AggregationType</span></span>
<span data-ttu-id="b2946-119">A lekérdezés összesítési típusa</span><span class="sxs-lookup"><span data-stu-id="b2946-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2946-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2946-120">-DefaultProfile</span></span>
<span data-ttu-id="b2946-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2946-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2946-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b2946-122">-DetailedOutput</span></span>
<span data-ttu-id="b2946-123">Azt jelzi, hogy ez a parancsmag részletes kimenetet jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="b2946-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="b2946-124">A program alapértelmezés szerint összesíti a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b2946-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2946-125">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="b2946-125">-EndTime</span></span>
<span data-ttu-id="b2946-126">A lekérdezés befejezési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="b2946-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="b2946-127">Az alapértelmezett időpont az aktuális idő.</span><span class="sxs-lookup"><span data-stu-id="b2946-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2946-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b2946-128">-MetricName</span></span>
<span data-ttu-id="b2946-129">A metrikák neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2946-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2946-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2946-130">-ResourceId</span></span>
<span data-ttu-id="b2946-131">A metrika erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2946-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2946-132">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="b2946-132">-StartTime</span></span>
<span data-ttu-id="b2946-133">A lekérdezés kezdési időpontját adja meg helyi időben.</span><span class="sxs-lookup"><span data-stu-id="b2946-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="b2946-134">Az alapértelmezett időpont az aktuális helyi idő, egy óra mínusz.</span><span class="sxs-lookup"><span data-stu-id="b2946-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2946-135">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="b2946-135">-TimeGrain</span></span>
<span data-ttu-id="b2946-136">A metrika **időszak** -objektumként való időpontját adja meg a hh: mm: SS formátumban.</span><span class="sxs-lookup"><span data-stu-id="b2946-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2946-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2946-137">CommonParameters</span></span>
<span data-ttu-id="b2946-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2946-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2946-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2946-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2946-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2946-140">INPUTS</span></span>

### <span data-ttu-id="b2946-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="b2946-141">None</span></span>
<span data-ttu-id="b2946-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b2946-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2946-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2946-143">OUTPUTS</span></span>

### <span data-ttu-id="b2946-144">Microsoft. Azure. Command. detekintés. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="b2946-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="b2946-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2946-145">NOTES</span></span>

## <span data-ttu-id="b2946-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2946-146">RELATED LINKS</span></span>

[<span data-ttu-id="b2946-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b2946-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


