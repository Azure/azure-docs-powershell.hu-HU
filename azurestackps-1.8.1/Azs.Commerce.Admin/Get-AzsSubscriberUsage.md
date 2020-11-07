---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840810"
---
# <span data-ttu-id="47b5a-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="47b5a-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="47b5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="47b5a-103">Használati adatainak lekérdezése a megadott időszak.</span><span class="sxs-lookup"><span data-stu-id="47b5a-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="47b5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47b5a-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="47b5a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="47b5a-106">Használati adatainak lekérdezése a megadott időszak.</span><span class="sxs-lookup"><span data-stu-id="47b5a-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="47b5a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="47b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="47b5a-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="47b5a-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="47b5a-109">Az elmúlt 24 óra használati adatainak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="47b5a-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="47b5a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="47b5a-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="47b5a-111">-SubscriberId</span></span>
<span data-ttu-id="47b5a-112">A bérlői előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="47b5a-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="47b5a-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="47b5a-113">-ReportedStartTime</span></span>
<span data-ttu-id="47b5a-114">A bejelentett kezdési időpont (beleértve).</span><span class="sxs-lookup"><span data-stu-id="47b5a-114">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="47b5a-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="47b5a-115">-AggregationGranularity</span></span>
<span data-ttu-id="47b5a-116">Összesítési részletesség.</span><span class="sxs-lookup"><span data-stu-id="47b5a-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="47b5a-117">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="47b5a-117">-Skip</span></span>
<span data-ttu-id="47b5a-118">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="47b5a-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="47b5a-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="47b5a-119">-ReportedEndTime</span></span>
<span data-ttu-id="47b5a-120">A jelentés befejezési időpontja (kizárólagos)</span><span class="sxs-lookup"><span data-stu-id="47b5a-120">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="47b5a-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="47b5a-121">-ContinuationToken</span></span>
<span data-ttu-id="47b5a-122">A folytatólagos jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="47b5a-122">The continuation token.</span></span>

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

### <span data-ttu-id="47b5a-123">-Top</span><span class="sxs-lookup"><span data-stu-id="47b5a-123">-Top</span></span>
<span data-ttu-id="47b5a-124">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="47b5a-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="47b5a-125">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="47b5a-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="47b5a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b5a-126">CommonParameters</span></span>
<span data-ttu-id="47b5a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47b5a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b5a-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b5a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b5a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47b5a-129">INPUTS</span></span>

## <span data-ttu-id="47b5a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47b5a-130">OUTPUTS</span></span>

### <span data-ttu-id="47b5a-131">Microsoft. AzureStack. Management. Commerce. admin. models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="47b5a-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="47b5a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47b5a-132">NOTES</span></span>

## <span data-ttu-id="47b5a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47b5a-133">RELATED LINKS</span></span>
