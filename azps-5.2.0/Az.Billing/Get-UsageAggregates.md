---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335730"
---
# <span data-ttu-id="1d331-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="1d331-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="1d331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d331-102">SYNOPSIS</span></span>
<span data-ttu-id="1d331-103">Itt olvashatja be az Azure-előfizetés használati adatait.</span><span class="sxs-lookup"><span data-stu-id="1d331-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="1d331-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d331-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d331-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d331-105">DESCRIPTION</span></span>
<span data-ttu-id="1d331-106">A **Get-UsageAggregates** parancsmag az alábbi tulajdonságok alapján összesíti az Azure-előfizetés használati adatait:</span><span class="sxs-lookup"><span data-stu-id="1d331-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="1d331-107">A használat jelentésének kezdő és záró időpontja.</span><span class="sxs-lookup"><span data-stu-id="1d331-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="1d331-108">Az összesítés pontossága napi vagy óránkénti.</span><span class="sxs-lookup"><span data-stu-id="1d331-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="1d331-109">Példányszintű részletek ugyanannak az erőforrásnak több példányához.</span><span class="sxs-lookup"><span data-stu-id="1d331-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="1d331-110">Az egységes eredmény érdekében a visszaadott adatok azon alapulnak, hogy mikor jelente meg a használati adatokat az Azure-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1d331-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="1d331-111">További információt az Azure Billing REST API Reference https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) (a Microsoft Developer Network tárában) található.</span><span class="sxs-lookup"><span data-stu-id="1d331-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="1d331-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d331-112">EXAMPLES</span></span>

### <span data-ttu-id="1d331-113">1. példa: Előfizetési adatok lekérése</span><span class="sxs-lookup"><span data-stu-id="1d331-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="1d331-114">Ez a parancs beolvassa az előfizetéshez jelentett használati adatokat 2015.05.02. és 2015.05.05. között.</span><span class="sxs-lookup"><span data-stu-id="1d331-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="1d331-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d331-115">PARAMETERS</span></span>

### <span data-ttu-id="1d331-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="1d331-116">-AggregationGranularity</span></span>
<span data-ttu-id="1d331-117">Az adatok összesítési pontosságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d331-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="1d331-118">Érvényes értékek: Naponta és Óránként.</span><span class="sxs-lookup"><span data-stu-id="1d331-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="1d331-119">Az alapértelmezett érték a Naponta érték.</span><span class="sxs-lookup"><span data-stu-id="1d331-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d331-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="1d331-120">-ContinuationToken</span></span>
<span data-ttu-id="1d331-121">Az előző hívásban a válasz törzséből beolvasott folytatási jogkivonatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d331-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="1d331-122">Nagy eredményhalmaz esetén a válaszokat a folytatási jogkivonatok használatával lapelik.</span><span class="sxs-lookup"><span data-stu-id="1d331-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="1d331-123">A folytatási jogkivonat könyvjelzőként szolgál az előrehaladáshoz.</span><span class="sxs-lookup"><span data-stu-id="1d331-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="1d331-124">Ha nem adja meg ezt a paramétert, az adatok beolvasása a ReportedStartTime-ban megadott nap vagy óra *elejéről történik.*</span><span class="sxs-lookup"><span data-stu-id="1d331-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="1d331-125">Azt javasoljuk, hogy az adatokkal együtt kövesse a lapra adott válasz következő hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="1d331-125">We recommend that you follow the next link in the response to page though the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d331-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d331-126">-DefaultProfile</span></span>
<span data-ttu-id="1d331-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d331-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d331-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="1d331-128">-ReportedEndTime</span></span>
<span data-ttu-id="1d331-129">Megadja az Erőforrás-használat Azure számlázási rendszerben való rögzítésekor jelentett záró időt.</span><span class="sxs-lookup"><span data-stu-id="1d331-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="1d331-130">Az Azure egy elosztott rendszer, amely világszerte több adatközpontot is áttűn, így késéssel számolhat az erőforrás-felhasználás ideje , vagyis az erőforrás kihasználtsága és a számlázási rendszer elérése között( ez az erőforrás-használat által jelentett idő).</span><span class="sxs-lookup"><span data-stu-id="1d331-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="1d331-131">Az előfizetés adott időszakra jelentett összes használati eseményének lekérdezése a jelentett idő alapján történt.</span><span class="sxs-lookup"><span data-stu-id="1d331-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="1d331-132">Bár a lekérdezést a jelentett idő alapján kell lekérdezni, a parancsmag összesíti a válaszadatokat az erőforrás kihasználtsága szerint.</span><span class="sxs-lookup"><span data-stu-id="1d331-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="1d331-133">Az erőforrás-használati adatok hasznos kimutatások az adatok elemzéséhez.</span><span class="sxs-lookup"><span data-stu-id="1d331-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d331-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="1d331-134">-ReportedStartTime</span></span>
<span data-ttu-id="1d331-135">Megadja az Erőforrás-használat Azure számlázási rendszerben való rögzítésekor jelentett kezdési időt.</span><span class="sxs-lookup"><span data-stu-id="1d331-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d331-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="1d331-136">-ShowDetails</span></span>
<span data-ttu-id="1d331-137">Azt jelzi, hogy ez a parancsmag példányszintű adatokat ad-e vissza a használati adatokkal együtt.</span><span class="sxs-lookup"><span data-stu-id="1d331-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="1d331-138">Az alapértelmezett érték $True.</span><span class="sxs-lookup"><span data-stu-id="1d331-138">The default value is $True.</span></span>
<span data-ttu-id="1d331-139">Ha $False, a szolgáltatás összesíti az eredményeket a kiszolgáló oldalán, és így kevesebb összesítő csoportot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="1d331-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="1d331-140">Ha például három webhelyet futtat, alapértelmezés szerint három sort fog kapni webhely-használatra.</span><span class="sxs-lookup"><span data-stu-id="1d331-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="1d331-141">Ha azonban az értéket $False, az ugyanannak az **előfizetésiIdnek,** a **meterIdnek,** a **usageStartTime-nak** és a **usageEndTime-nak** az összes adata egyetlen sorelembe lesz összecsukva.</span><span class="sxs-lookup"><span data-stu-id="1d331-141">However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d331-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d331-142">CommonParameters</span></span>
<span data-ttu-id="1d331-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d331-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d331-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d331-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d331-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d331-145">INPUTS</span></span>

### <span data-ttu-id="1d331-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="1d331-146">None</span></span>

## <span data-ttu-id="1d331-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d331-147">OUTPUTS</span></span>

### <span data-ttu-id="1d331-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="1d331-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="1d331-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d331-149">NOTES</span></span>

## <span data-ttu-id="1d331-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d331-150">RELATED LINKS</span></span>
