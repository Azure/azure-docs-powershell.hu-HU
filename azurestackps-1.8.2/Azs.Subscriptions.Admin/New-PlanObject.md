---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017164"
---
# <span data-ttu-id="e97bf-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="e97bf-101">New-PlanObject</span></span>

## <span data-ttu-id="e97bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e97bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e97bf-103">A terv az olyan kvóták és funkciók csomagját jelenti, amelyek a bérlők számára elérhetők.</span><span class="sxs-lookup"><span data-stu-id="e97bf-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="e97bf-104">A bérlő ezt a csomagot egy ajánlaton keresztül is megszerezheti, és a Felhőbeli szolgáltatásokhoz való hozzáférését frissítheti.</span><span class="sxs-lookup"><span data-stu-id="e97bf-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="e97bf-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e97bf-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="e97bf-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="e97bf-106">DESCRIPTION</span></span>
<span data-ttu-id="e97bf-107">A terv az olyan kvóták és funkciók csomagját jelenti, amelyek a bérlők számára elérhetők.</span><span class="sxs-lookup"><span data-stu-id="e97bf-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="e97bf-108">A bérlő ezt a csomagot egy ajánlaton keresztül is megszerezheti, és a Felhőbeli szolgáltatásokhoz való hozzáférését frissítheti.</span><span class="sxs-lookup"><span data-stu-id="e97bf-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="e97bf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e97bf-109">EXAMPLES</span></span>

### <span data-ttu-id="e97bf-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e97bf-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e97bf-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="e97bf-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e97bf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e97bf-112">PARAMETERS</span></span>

### <span data-ttu-id="e97bf-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e97bf-113">-Description</span></span>
<span data-ttu-id="e97bf-114">A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="e97bf-114">Description of the plan.</span></span>

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

### <span data-ttu-id="e97bf-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e97bf-115">-DisplayName</span></span>
<span data-ttu-id="e97bf-116">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="e97bf-116">Display name.</span></span>

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

### <span data-ttu-id="e97bf-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e97bf-117">-ExternalReferenceId</span></span>
<span data-ttu-id="e97bf-118">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="e97bf-118">External reference identifier.</span></span>

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

### <span data-ttu-id="e97bf-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e97bf-119">-Id</span></span>
<span data-ttu-id="e97bf-120">Az erőforrás URI-ja.</span><span class="sxs-lookup"><span data-stu-id="e97bf-120">URI of the resource.</span></span>

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

### <span data-ttu-id="e97bf-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="e97bf-121">-Location</span></span>
<span data-ttu-id="e97bf-122">Az a hely, ahol az erőforrás hely.</span><span class="sxs-lookup"><span data-stu-id="e97bf-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="e97bf-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e97bf-123">-Name</span></span>
<span data-ttu-id="e97bf-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e97bf-124">Name of the resource.</span></span>

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

### <span data-ttu-id="e97bf-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="e97bf-125">-QuotaIds</span></span>
<span data-ttu-id="e97bf-126">A csomag alatti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="e97bf-126">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="e97bf-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="e97bf-127">-SkuIds</span></span>
<span data-ttu-id="e97bf-128">SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="e97bf-128">SKU identifiers.</span></span>

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

### <span data-ttu-id="e97bf-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="e97bf-129">-SubscriptionCount</span></span>
<span data-ttu-id="e97bf-130">Előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="e97bf-130">Subscription count.</span></span>

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

### <span data-ttu-id="e97bf-131">-Címkék</span><span class="sxs-lookup"><span data-stu-id="e97bf-131">-Tags</span></span>
<span data-ttu-id="e97bf-132">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="e97bf-132">List of key-value pairs.</span></span>

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

### <span data-ttu-id="e97bf-133">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e97bf-133">-Type</span></span>
<span data-ttu-id="e97bf-134">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="e97bf-134">Type of resource.</span></span>

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

### <span data-ttu-id="e97bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97bf-135">CommonParameters</span></span>
<span data-ttu-id="e97bf-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e97bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97bf-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e97bf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97bf-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e97bf-138">INPUTS</span></span>

## <span data-ttu-id="e97bf-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e97bf-139">OUTPUTS</span></span>

## <span data-ttu-id="e97bf-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e97bf-140">NOTES</span></span>

## <span data-ttu-id="e97bf-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e97bf-141">RELATED LINKS</span></span>

