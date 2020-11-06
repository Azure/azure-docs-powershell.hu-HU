---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491635"
---
# <span data-ttu-id="6e0a0-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="6e0a0-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="6e0a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0a0-103">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="6e0a0-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="6e0a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e0a0-104">SYNTAX</span></span>

### <span data-ttu-id="6e0a0-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e0a0-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e0a0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e0a0-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e0a0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6e0a0-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e0a0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e0a0-108">DESCRIPTION</span></span>
<span data-ttu-id="6e0a0-109">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="6e0a0-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="6e0a0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6e0a0-110">EXAMPLES</span></span>

### <span data-ttu-id="6e0a0-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6e0a0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="6e0a0-112">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="6e0a0-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="6e0a0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e0a0-113">PARAMETERS</span></span>

### <span data-ttu-id="6e0a0-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6e0a0-114">-DisplayName</span></span>
<span data-ttu-id="6e0a0-115">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="6e0a0-115">Subscription name.</span></span>

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

### <span data-ttu-id="6e0a0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e0a0-116">-InputObject</span></span>
<span data-ttu-id="6e0a0-117">A Posbbily módosított hálózati kvótáját a Get-AzsNetworkQuota adja vissza.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="6e0a0-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="6e0a0-118">-Location</span></span>
<span data-ttu-id="6e0a0-119">Az a hely, ahol az erőforrás hely.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="6e0a0-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="6e0a0-120">-OfferId</span></span>
<span data-ttu-id="6e0a0-121">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="6e0a0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e0a0-122">-ResourceId</span></span>
<span data-ttu-id="6e0a0-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-123">The resource ID.</span></span>

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

### <span data-ttu-id="6e0a0-124">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="6e0a0-124">-State</span></span>
<span data-ttu-id="6e0a0-125">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="6e0a0-125">Subscription state.</span></span>

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

### <span data-ttu-id="6e0a0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e0a0-126">-SubscriptionId</span></span>
<span data-ttu-id="6e0a0-127">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="6e0a0-128">-Címkék</span><span class="sxs-lookup"><span data-stu-id="6e0a0-128">-Tags</span></span>
<span data-ttu-id="6e0a0-129">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="6e0a0-130">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="6e0a0-130">-TenantId</span></span>
<span data-ttu-id="6e0a0-131">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="6e0a0-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="6e0a0-132">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="6e0a0-132">-Type</span></span>
<span data-ttu-id="6e0a0-133">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-133">Type of resource.</span></span>

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

### <span data-ttu-id="6e0a0-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e0a0-134">-Confirm</span></span>
<span data-ttu-id="6e0a0-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e0a0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e0a0-136">-WhatIf</span></span>
<span data-ttu-id="6e0a0-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e0a0-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e0a0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e0a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0a0-139">CommonParameters</span></span>
<span data-ttu-id="6e0a0-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e0a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0a0-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e0a0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0a0-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e0a0-142">INPUTS</span></span>

## <span data-ttu-id="6e0a0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e0a0-143">OUTPUTS</span></span>

### <span data-ttu-id="6e0a0-144">Microsoft. AzureStack. Management. előfizetés. modellek. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="6e0a0-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="6e0a0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e0a0-145">NOTES</span></span>

## <span data-ttu-id="6e0a0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e0a0-146">RELATED LINKS</span></span>

