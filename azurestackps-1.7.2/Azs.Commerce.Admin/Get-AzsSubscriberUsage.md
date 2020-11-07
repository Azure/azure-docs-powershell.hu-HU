---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839315"
---
# <span data-ttu-id="2f653-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="2f653-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="2f653-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f653-102">SYNOPSIS</span></span>
<span data-ttu-id="2f653-103">Használati adatainak lekérdezése a megadott időszak.</span><span class="sxs-lookup"><span data-stu-id="2f653-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="2f653-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f653-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2f653-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f653-105">DESCRIPTION</span></span>
<span data-ttu-id="2f653-106">Használati adatainak lekérdezése a megadott időszak.</span><span class="sxs-lookup"><span data-stu-id="2f653-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="2f653-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f653-107">EXAMPLES</span></span>

### <span data-ttu-id="2f653-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f653-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="2f653-109">Az elmúlt 24 óra használati adatainak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="2f653-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="2f653-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f653-110">PARAMETERS</span></span>

### <span data-ttu-id="2f653-111">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="2f653-111">-AggregationGranularity</span></span>
<span data-ttu-id="2f653-112">Összesítési részletesség.</span><span class="sxs-lookup"><span data-stu-id="2f653-112">The aggregation granularity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f653-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2f653-113">-ContinuationToken</span></span>
<span data-ttu-id="2f653-114">A folytatólagos jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="2f653-114">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f653-115">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="2f653-115">-ReportedEndTime</span></span>
<span data-ttu-id="2f653-116">A jelentés befejezési időpontja (kizárólagos)</span><span class="sxs-lookup"><span data-stu-id="2f653-116">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f653-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="2f653-117">-ReportedStartTime</span></span>
<span data-ttu-id="2f653-118">A bejelentett kezdési időpont (beleértve).</span><span class="sxs-lookup"><span data-stu-id="2f653-118">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f653-119">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2f653-119">-Skip</span></span>
<span data-ttu-id="2f653-120">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="2f653-120">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f653-121">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="2f653-121">-SubscriberId</span></span>
<span data-ttu-id="2f653-122">A bérlői előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="2f653-122">The tenant subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f653-123">-Top</span><span class="sxs-lookup"><span data-stu-id="2f653-123">-Top</span></span>
<span data-ttu-id="2f653-124">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="2f653-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2f653-125">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="2f653-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f653-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f653-126">CommonParameters</span></span>
<span data-ttu-id="2f653-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f653-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f653-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f653-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f653-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f653-129">INPUTS</span></span>

## <span data-ttu-id="2f653-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f653-130">OUTPUTS</span></span>

### <span data-ttu-id="2f653-131">Microsoft. AzureStack. Management. Commerce. admin. models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="2f653-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="2f653-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f653-132">NOTES</span></span>

## <span data-ttu-id="2f653-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f653-133">RELATED LINKS</span></span>

