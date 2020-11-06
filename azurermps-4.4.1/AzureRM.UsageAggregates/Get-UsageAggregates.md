---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM.UsageAggregates
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
ms.openlocfilehash: 1c5c705ec55889182a38d1586559f59d57e2d366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494595"
---
# <span data-ttu-id="3c7db-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="3c7db-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="3c7db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c7db-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7db-103">Megkapja a bejelentett Azure-előfizetés használati adatait.</span><span class="sxs-lookup"><span data-stu-id="3c7db-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c7db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c7db-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c7db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c7db-105">DESCRIPTION</span></span>
<span data-ttu-id="3c7db-106">A **Get-UsageAggregates** parancsmag az Azure-előfizetés használati adatainak összegzéséhez a következő tulajdonságokat kapja:</span><span class="sxs-lookup"><span data-stu-id="3c7db-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 

- <span data-ttu-id="3c7db-107">A felhasználás jelentésének kezdési és befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="3c7db-107">Start and end times of when the usage was reported.</span></span>

- <span data-ttu-id="3c7db-108">Összesítési pontosság (naponta vagy óránként)</span><span class="sxs-lookup"><span data-stu-id="3c7db-108">Aggregation precision, either daily or hourly.</span></span>

- <span data-ttu-id="3c7db-109">Az adott erőforrás több példányának a példány szintű részletei.</span><span class="sxs-lookup"><span data-stu-id="3c7db-109">Instance level detail for multiple instances of the same resource.</span></span>

<span data-ttu-id="3c7db-110">Konzisztens eredmények esetén a visszaadott adatok attól függnek, hogy az Azure-erőforrás mikor jelentette a használati adatokat.</span><span class="sxs-lookup"><span data-stu-id="3c7db-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>

<span data-ttu-id="3c7db-111">További információt az Azure számlázási REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c -hivatkozás ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) a Microsoft Developer Network Library) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c7db-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="3c7db-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3c7db-112">EXAMPLES</span></span>

### <span data-ttu-id="3c7db-113">Példa 1: előfizetés adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="3c7db-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="3c7db-114">Ez a parancs beolvassa az 5/2/2015 és az 5/5/2015 közötti előfizetés használati adatainak jelentését.</span><span class="sxs-lookup"><span data-stu-id="3c7db-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="3c7db-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c7db-115">PARAMETERS</span></span>

### <span data-ttu-id="3c7db-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="3c7db-116">-AggregationGranularity</span></span>
<span data-ttu-id="3c7db-117">Az érték összesítési pontosságát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c7db-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="3c7db-118">Az érvényes értékek: naponta és óránként.</span><span class="sxs-lookup"><span data-stu-id="3c7db-118">Valid values are: Daily and Hourly.</span></span>

<span data-ttu-id="3c7db-119">Az alapértelmezett érték naponta.</span><span class="sxs-lookup"><span data-stu-id="3c7db-119">The default value is Daily.</span></span>

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

### <span data-ttu-id="3c7db-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="3c7db-120">-ContinuationToken</span></span>
<span data-ttu-id="3c7db-121">Az előző hívás válasz törzséről lekért folytatási tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c7db-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="3c7db-122">Nagy eredményhalmaz esetén a válaszokat a folytatólagos tokenek segítségével lapozhatja.</span><span class="sxs-lookup"><span data-stu-id="3c7db-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="3c7db-123">A folytatási token könyvjelzőként szolgál a folyamathoz.</span><span class="sxs-lookup"><span data-stu-id="3c7db-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="3c7db-124">Ha nem adja meg ezt a paramétert, az adatai a *ReportedStartTime* megadott nap vagy óra elejétől kezdve olvashatók.</span><span class="sxs-lookup"><span data-stu-id="3c7db-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="3c7db-125">Azt javasoljuk, hogy kövesse a válasz az oldalra című következő hivatkozást, de az adatot.</span><span class="sxs-lookup"><span data-stu-id="3c7db-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="3c7db-126">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="3c7db-126">-ReportedEndTime</span></span>
<span data-ttu-id="3c7db-127">Az erőforrás-használat Azure számlázási rendszerbe való felvételének bejelentett befejezési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c7db-127">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>

<span data-ttu-id="3c7db-128">Az Azure egy olyan kiosztott rendszer, amely több adatközpontot tartalmaz világszerte, így az Erőforrás kihasználtsága között az Erőforrás kihasználtsága és a számlázási rendszer, amikor a használati esemény elérte a számlázási rendszert, az Erőforrás kihasználtsága időpontját jelenti.</span><span class="sxs-lookup"><span data-stu-id="3c7db-128">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="3c7db-129">Annak érdekében, hogy az előfizetéshez az adott időszakra bejelentett összes használati eseményt beszerezze, a lekérdezés a bejelentett idő szerint történjen.</span><span class="sxs-lookup"><span data-stu-id="3c7db-129">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="3c7db-130">Annak ellenére, hogy a megadott idő szerint lekérdezést kérdez le, a parancsmag összesíti a válasz adatmennyiségét az erőforrás kihasználtsági ideje alapján.</span><span class="sxs-lookup"><span data-stu-id="3c7db-130">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="3c7db-131">Az erőforrás-használati adatok a hasznos kimutatás az adatok elemzéséhez.</span><span class="sxs-lookup"><span data-stu-id="3c7db-131">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="3c7db-132">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="3c7db-132">-ReportedStartTime</span></span>
<span data-ttu-id="3c7db-133">Megadja, hogy milyen kezdési idő legyen látható az erőforrás-használat Azure számlázási rendszerben való felvételekor.</span><span class="sxs-lookup"><span data-stu-id="3c7db-133">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="3c7db-134">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="3c7db-134">-ShowDetails</span></span>
<span data-ttu-id="3c7db-135">Azt jelzi, hogy ez a parancsmag a használati adatokból példány-szintű részleteket ad-e eredményül.</span><span class="sxs-lookup"><span data-stu-id="3c7db-135">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>

<span data-ttu-id="3c7db-136">Az alapértelmezett érték $True.</span><span class="sxs-lookup"><span data-stu-id="3c7db-136">The default value is $True.</span></span>

<span data-ttu-id="3c7db-137">Ha $False, a szolgáltatás összesíti az eredményeket a kiszolgáló oldalán, és így kevesebb összesített csoportot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3c7db-137">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="3c7db-138">Ha például három webhelyet futtat, alapértelmezés szerint három elem jelenik meg a webhely-felhasználáshoz.</span><span class="sxs-lookup"><span data-stu-id="3c7db-138">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="3c7db-139">Az érték $False esetén azonban minden adat ugyanahhoz a **subscriptionId** , **meterId** , **usageStartTime** és **usageEndTime** van összecsukva egyetlen sorba.</span><span class="sxs-lookup"><span data-stu-id="3c7db-139">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

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

### <span data-ttu-id="3c7db-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7db-140">-DefaultProfile</span></span>
<span data-ttu-id="3c7db-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c7db-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7db-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7db-142">CommonParameters</span></span>
<span data-ttu-id="3c7db-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c7db-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7db-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7db-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7db-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c7db-145">INPUTS</span></span>

## <span data-ttu-id="3c7db-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c7db-146">OUTPUTS</span></span>

### <span data-ttu-id="3c7db-147">Microsoft. Azure. Commerce. UsageAggregates. models. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="3c7db-147">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="3c7db-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c7db-148">NOTES</span></span>

## <span data-ttu-id="3c7db-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c7db-149">RELATED LINKS</span></span>

