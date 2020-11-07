---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840107"
---
# <span data-ttu-id="c825d-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="c825d-101">New-AzsSubscription</span></span>

## <span data-ttu-id="c825d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c825d-102">SYNOPSIS</span></span>
<span data-ttu-id="c825d-103">Előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="c825d-103">Create a subscription.</span></span>

## <span data-ttu-id="c825d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c825d-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c825d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c825d-105">DESCRIPTION</span></span>
<span data-ttu-id="c825d-106">Előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="c825d-106">Create a subscription.</span></span>

## <span data-ttu-id="c825d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c825d-107">EXAMPLES</span></span>

### <span data-ttu-id="c825d-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c825d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="c825d-109">Előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="c825d-109">Create a subscription.</span></span>

## <span data-ttu-id="c825d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c825d-110">PARAMETERS</span></span>

### <span data-ttu-id="c825d-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c825d-111">-DisplayName</span></span>
<span data-ttu-id="c825d-112">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="c825d-112">Subscription name.</span></span>

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

### <span data-ttu-id="c825d-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="c825d-113">-Location</span></span>
<span data-ttu-id="c825d-114">Az a hely, ahol az erőforrás hely.</span><span class="sxs-lookup"><span data-stu-id="c825d-114">Location where resource is location.</span></span>

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

### <span data-ttu-id="c825d-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="c825d-115">-OfferId</span></span>
<span data-ttu-id="c825d-116">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="c825d-116">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="c825d-117">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c825d-117">-State</span></span>
<span data-ttu-id="c825d-118">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="c825d-118">Subscription state.</span></span>

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

### <span data-ttu-id="c825d-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c825d-119">-SubscriptionId</span></span>
<span data-ttu-id="c825d-120">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c825d-120">Subscription identifier.</span></span>

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

### <span data-ttu-id="c825d-121">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="c825d-121">-TenantId</span></span>
<span data-ttu-id="c825d-122">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="c825d-122">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="c825d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c825d-123">-Confirm</span></span>
<span data-ttu-id="c825d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c825d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c825d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c825d-125">-WhatIf</span></span>
<span data-ttu-id="c825d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c825d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c825d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c825d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c825d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c825d-128">CommonParameters</span></span>
<span data-ttu-id="c825d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c825d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c825d-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c825d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c825d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c825d-131">INPUTS</span></span>

## <span data-ttu-id="c825d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c825d-132">OUTPUTS</span></span>

### <span data-ttu-id="c825d-133">Microsoft. AzureStack. Management. előfizetés. modellek. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="c825d-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="c825d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c825d-134">NOTES</span></span>

## <span data-ttu-id="c825d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c825d-135">RELATED LINKS</span></span>

