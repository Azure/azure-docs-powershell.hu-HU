---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840140"
---
# <span data-ttu-id="caf6f-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="caf6f-101">New-AzsSubscription</span></span>

## <span data-ttu-id="caf6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="caf6f-102">SYNOPSIS</span></span>
<span data-ttu-id="caf6f-103">Előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="caf6f-103">Create a subscription.</span></span>

## <span data-ttu-id="caf6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="caf6f-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caf6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="caf6f-105">DESCRIPTION</span></span>
<span data-ttu-id="caf6f-106">Előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="caf6f-106">Create a subscription.</span></span>

## <span data-ttu-id="caf6f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="caf6f-107">EXAMPLES</span></span>

### <span data-ttu-id="caf6f-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="caf6f-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="caf6f-109">Előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="caf6f-109">Create a subscription.</span></span>

## <span data-ttu-id="caf6f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="caf6f-110">PARAMETERS</span></span>

### <span data-ttu-id="caf6f-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="caf6f-111">-OfferId</span></span>
<span data-ttu-id="caf6f-112">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="caf6f-112">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf6f-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="caf6f-113">-DisplayName</span></span>
<span data-ttu-id="caf6f-114">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="caf6f-114">Subscription name.</span></span>

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

### <span data-ttu-id="caf6f-115">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="caf6f-115">-TenantId</span></span>
<span data-ttu-id="caf6f-116">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="caf6f-116">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="caf6f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="caf6f-117">-SubscriptionId</span></span>
<span data-ttu-id="caf6f-118">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="caf6f-118">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf6f-119">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="caf6f-119">-State</span></span>
<span data-ttu-id="caf6f-120">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="caf6f-120">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf6f-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="caf6f-121">-Location</span></span>
<span data-ttu-id="caf6f-122">Az a hely, ahol az erőforrás hely.</span><span class="sxs-lookup"><span data-stu-id="caf6f-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf6f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf6f-123">-WhatIf</span></span>
<span data-ttu-id="caf6f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="caf6f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caf6f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="caf6f-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf6f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="caf6f-126">-Confirm</span></span>
<span data-ttu-id="caf6f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="caf6f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf6f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf6f-128">CommonParameters</span></span>
<span data-ttu-id="caf6f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="caf6f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf6f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf6f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf6f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="caf6f-131">INPUTS</span></span>

## <span data-ttu-id="caf6f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caf6f-132">OUTPUTS</span></span>

### <span data-ttu-id="caf6f-133">Microsoft. AzureStack. Management. előfizetés. modellek. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="caf6f-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="caf6f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="caf6f-134">NOTES</span></span>

## <span data-ttu-id="caf6f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caf6f-135">RELATED LINKS</span></span>
