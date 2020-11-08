---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016946"
---
# <span data-ttu-id="09771-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="09771-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="09771-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09771-102">SYNOPSIS</span></span>
<span data-ttu-id="09771-103">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="09771-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="09771-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09771-104">SYNTAX</span></span>

### <span data-ttu-id="09771-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09771-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09771-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="09771-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09771-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="09771-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09771-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="09771-108">DESCRIPTION</span></span>
<span data-ttu-id="09771-109">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="09771-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="09771-110">Példák</span><span class="sxs-lookup"><span data-stu-id="09771-110">EXAMPLES</span></span>

### <span data-ttu-id="09771-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="09771-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="09771-112">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="09771-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="09771-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09771-113">PARAMETERS</span></span>

### <span data-ttu-id="09771-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="09771-114">-OfferId</span></span>
<span data-ttu-id="09771-115">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="09771-115">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-116">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="09771-116">-Type</span></span>
<span data-ttu-id="09771-117">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="09771-117">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-118">-Címkék</span><span class="sxs-lookup"><span data-stu-id="09771-118">-Tags</span></span>
<span data-ttu-id="09771-119">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="09771-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09771-120">-SubscriptionId</span></span>
<span data-ttu-id="09771-121">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="09771-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-122">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="09771-122">-State</span></span>
<span data-ttu-id="09771-123">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="09771-123">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-124">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="09771-124">-TenantId</span></span>
<span data-ttu-id="09771-125">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="09771-125">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="09771-126">-DisplayName</span></span>
<span data-ttu-id="09771-127">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="09771-127">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="09771-128">-Location</span></span>
<span data-ttu-id="09771-129">Az a hely, ahol az erőforrás hely.</span><span class="sxs-lookup"><span data-stu-id="09771-129">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09771-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09771-130">-ResourceId</span></span>
<span data-ttu-id="09771-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="09771-131">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09771-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09771-132">-InputObject</span></span>
<span data-ttu-id="09771-133">A Posbbily módosított hálózati kvótáját a Get-AzsNetworkQuota adja vissza.</span><span class="sxs-lookup"><span data-stu-id="09771-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09771-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09771-134">-WhatIf</span></span>
<span data-ttu-id="09771-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09771-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09771-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09771-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09771-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09771-137">-Confirm</span></span>
<span data-ttu-id="09771-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09771-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09771-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09771-139">CommonParameters</span></span>
<span data-ttu-id="09771-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09771-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09771-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09771-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09771-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09771-142">INPUTS</span></span>

## <span data-ttu-id="09771-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09771-143">OUTPUTS</span></span>

### <span data-ttu-id="09771-144">Microsoft. AzureStack. Management. előfizetés. modellek. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="09771-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="09771-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09771-145">NOTES</span></span>

## <span data-ttu-id="09771-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09771-146">RELATED LINKS</span></span>
