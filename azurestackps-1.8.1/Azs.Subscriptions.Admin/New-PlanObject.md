---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840480"
---
# <span data-ttu-id="c4102-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="c4102-101">New-PlanObject</span></span>

## <span data-ttu-id="c4102-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4102-102">SYNOPSIS</span></span>
<span data-ttu-id="c4102-103">A terv az olyan kvóták és funkciók csomagját jelenti, amelyek a bérlők számára elérhetők.</span><span class="sxs-lookup"><span data-stu-id="c4102-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="c4102-104">A bérlő ezt a csomagot egy ajánlaton keresztül is megszerezheti, és a Felhőbeli szolgáltatásokhoz való hozzáférését frissítheti.</span><span class="sxs-lookup"><span data-stu-id="c4102-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="c4102-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4102-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="c4102-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4102-106">DESCRIPTION</span></span>
<span data-ttu-id="c4102-107">A terv az olyan kvóták és funkciók csomagját jelenti, amelyek a bérlők számára elérhetők.</span><span class="sxs-lookup"><span data-stu-id="c4102-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="c4102-108">A bérlő ezt a csomagot egy ajánlaton keresztül is megszerezheti, és a Felhőbeli szolgáltatásokhoz való hozzáférését frissítheti.</span><span class="sxs-lookup"><span data-stu-id="c4102-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="c4102-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c4102-109">EXAMPLES</span></span>

### <span data-ttu-id="c4102-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c4102-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c4102-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="c4102-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="c4102-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4102-112">PARAMETERS</span></span>

### <span data-ttu-id="c4102-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c4102-113">-Description</span></span>
<span data-ttu-id="c4102-114">A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="c4102-114">Description of the plan.</span></span>

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

### <span data-ttu-id="c4102-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c4102-115">-DisplayName</span></span>
<span data-ttu-id="c4102-116">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="c4102-116">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c4102-117">-ExternalReferenceId</span></span>
<span data-ttu-id="c4102-118">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="c4102-118">External reference identifier.</span></span>

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

### <span data-ttu-id="c4102-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c4102-119">-Id</span></span>
<span data-ttu-id="c4102-120">Az erőforrás URI-ja.</span><span class="sxs-lookup"><span data-stu-id="c4102-120">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="c4102-121">-Location</span></span>
<span data-ttu-id="c4102-122">Az a hely, ahol az erőforrás hely.</span><span class="sxs-lookup"><span data-stu-id="c4102-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4102-123">-Name</span></span>
<span data-ttu-id="c4102-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c4102-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="c4102-125">-QuotaIds</span></span>
<span data-ttu-id="c4102-126">A csomag alatti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="c4102-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="c4102-127">-SkuIds</span></span>
<span data-ttu-id="c4102-128">SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="c4102-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="c4102-129">-SubscriptionCount</span></span>
<span data-ttu-id="c4102-130">Előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="c4102-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-131">-Címkék</span><span class="sxs-lookup"><span data-stu-id="c4102-131">-Tags</span></span>
<span data-ttu-id="c4102-132">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="c4102-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4102-133">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="c4102-133">-Type</span></span>
<span data-ttu-id="c4102-134">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="c4102-134">Type of resource.</span></span>

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

### <span data-ttu-id="c4102-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4102-135">CommonParameters</span></span>
<span data-ttu-id="c4102-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4102-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4102-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4102-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4102-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4102-138">INPUTS</span></span>

## <span data-ttu-id="c4102-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4102-139">OUTPUTS</span></span>

## <span data-ttu-id="c4102-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4102-140">NOTES</span></span>

## <span data-ttu-id="c4102-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4102-141">RELATED LINKS</span></span>

