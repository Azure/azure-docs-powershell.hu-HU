---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844890"
---
# <span data-ttu-id="ff24c-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="ff24c-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="ff24c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff24c-102">SYNOPSIS</span></span>
<span data-ttu-id="ff24c-103">Begyűjti a SubscriberUsageAggregates, amely a felhasználóktól UsageAggregates válik.</span><span class="sxs-lookup"><span data-stu-id="ff24c-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="ff24c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff24c-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ff24c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff24c-105">DESCRIPTION</span></span>
<span data-ttu-id="ff24c-106">Begyűjti a SubscriberUsageAggregates, amely a felhasználóktól UsageAggregates válik.</span><span class="sxs-lookup"><span data-stu-id="ff24c-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="ff24c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff24c-107">EXAMPLES</span></span>

### <span data-ttu-id="ff24c-108">Példa 1: a használati adatokat naponta összesítve kapja.</span><span class="sxs-lookup"><span data-stu-id="ff24c-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="ff24c-109">A használati adatokat az adott nap által összesített szolgáltatónál a minden bérlő számára a december 30 2019 (UTC) szerint kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="ff24c-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="ff24c-110">A ReportedStartTime és a ReportedEndTime a napokra kell kerekíteni.</span><span class="sxs-lookup"><span data-stu-id="ff24c-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="ff24c-111">Ha a szolgáltatás rendszergazdája néven ismert, az minden bérlői webhelyhez az összes használati adatot megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="ff24c-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="ff24c-112">2. példa: a használati adatokat az Hour összesítve kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ff24c-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="ff24c-113">A használati adatokat az Hour által összesítve, 2019 december 30-án (UTC-ben) kell 12am.</span><span class="sxs-lookup"><span data-stu-id="ff24c-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="ff24c-114">A ReportedStartTime és a ReportedEndTime órákra kerekítve kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ff24c-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="ff24c-115">Hasonlóképpen, ha a szolgáltatás rendszergazdája néven ismert, az minden bérlői webhelyhez tartozó összes használati adatot hatékonyan jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ff24c-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="ff24c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff24c-116">PARAMETERS</span></span>

### <span data-ttu-id="ff24c-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="ff24c-117">-AggregationGranularity</span></span>
<span data-ttu-id="ff24c-118">Összesítési részletesség.</span><span class="sxs-lookup"><span data-stu-id="ff24c-118">The aggregation granularity.</span></span>

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

### <span data-ttu-id="ff24c-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="ff24c-119">-ContinuationToken</span></span>
<span data-ttu-id="ff24c-120">A folytatólagos jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="ff24c-120">The continuation token.</span></span>

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

### <span data-ttu-id="ff24c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff24c-121">-DefaultProfile</span></span>
<span data-ttu-id="ff24c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff24c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ff24c-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="ff24c-123">-ReportedEndTime</span></span>
<span data-ttu-id="ff24c-124">A jelentés befejezési időpontja (kizárólagos)</span><span class="sxs-lookup"><span data-stu-id="ff24c-124">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="ff24c-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="ff24c-125">-ReportedStartTime</span></span>
<span data-ttu-id="ff24c-126">A bejelentett kezdési időpont (beleértve).</span><span class="sxs-lookup"><span data-stu-id="ff24c-126">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="ff24c-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="ff24c-127">-SubscriberId</span></span>
<span data-ttu-id="ff24c-128">A bérlői előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="ff24c-128">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="ff24c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff24c-129">-SubscriptionId</span></span>
<span data-ttu-id="ff24c-130">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ff24c-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ff24c-131">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ff24c-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ff24c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff24c-132">CommonParameters</span></span>
<span data-ttu-id="ff24c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff24c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff24c-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ff24c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff24c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff24c-135">INPUTS</span></span>

## <span data-ttu-id="ff24c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff24c-136">OUTPUTS</span></span>

### <span data-ttu-id="ff24c-137">Microsoft. Azure. PowerShell. parancsmagok. Commerce. models. Api20150601Preview. IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="ff24c-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="ff24c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff24c-138">NOTES</span></span>

## <span data-ttu-id="ff24c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff24c-139">RELATED LINKS</span></span>

