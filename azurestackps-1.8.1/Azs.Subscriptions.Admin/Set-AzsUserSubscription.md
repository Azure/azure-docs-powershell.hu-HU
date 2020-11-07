---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840466"
---
# <span data-ttu-id="707fe-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="707fe-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="707fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="707fe-102">SYNOPSIS</span></span>
<span data-ttu-id="707fe-103">A megadott felhasználói előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="707fe-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="707fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="707fe-104">SYNTAX</span></span>

### <span data-ttu-id="707fe-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="707fe-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="707fe-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="707fe-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="707fe-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="707fe-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="707fe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="707fe-108">DESCRIPTION</span></span>
<span data-ttu-id="707fe-109">A megadott felhasználói előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="707fe-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="707fe-110">Példák</span><span class="sxs-lookup"><span data-stu-id="707fe-110">EXAMPLES</span></span>

### <span data-ttu-id="707fe-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="707fe-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="707fe-112">Előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="707fe-112">Updates a subscription</span></span>

## <span data-ttu-id="707fe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="707fe-113">PARAMETERS</span></span>

### <span data-ttu-id="707fe-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="707fe-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="707fe-115">Fölérendelt DelegatedProvider-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="707fe-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="707fe-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="707fe-116">-DisplayName</span></span>
<span data-ttu-id="707fe-117">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="707fe-117">Subscription name.</span></span>

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

### <span data-ttu-id="707fe-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="707fe-118">-ExternalReferenceId</span></span>
<span data-ttu-id="707fe-119">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="707fe-119">External reference identifier.</span></span>

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

### <span data-ttu-id="707fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="707fe-120">-InputObject</span></span>
<span data-ttu-id="707fe-121">A szövegbeviteli objektum típusa: Microsoft. AzureStack. Management. Network. admin. models. quote.</span><span class="sxs-lookup"><span data-stu-id="707fe-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="707fe-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="707fe-122">-Location</span></span>
<span data-ttu-id="707fe-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="707fe-123">Location of the resource.</span></span>

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

### <span data-ttu-id="707fe-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="707fe-124">-OfferId</span></span>
<span data-ttu-id="707fe-125">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="707fe-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="707fe-126">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="707fe-126">-Owner</span></span>
<span data-ttu-id="707fe-127">Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="707fe-127">Subscription owner.</span></span>

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

### <span data-ttu-id="707fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="707fe-128">-ResourceId</span></span>
<span data-ttu-id="707fe-129">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="707fe-129">The resource ID.</span></span>

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

### <span data-ttu-id="707fe-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="707fe-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="707fe-131">Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="707fe-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="707fe-132">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="707fe-132">-State</span></span>
<span data-ttu-id="707fe-133">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="707fe-133">Subscription state.</span></span>

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

### <span data-ttu-id="707fe-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="707fe-134">-SubscriptionId</span></span>
<span data-ttu-id="707fe-135">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="707fe-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707fe-136">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="707fe-136">-TenantId</span></span>
<span data-ttu-id="707fe-137">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="707fe-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="707fe-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="707fe-138">-Confirm</span></span>
<span data-ttu-id="707fe-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="707fe-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="707fe-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707fe-140">-WhatIf</span></span>
<span data-ttu-id="707fe-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="707fe-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="707fe-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="707fe-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="707fe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707fe-143">CommonParameters</span></span>
<span data-ttu-id="707fe-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="707fe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707fe-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="707fe-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707fe-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="707fe-146">INPUTS</span></span>

## <span data-ttu-id="707fe-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="707fe-147">OUTPUTS</span></span>

### <span data-ttu-id="707fe-148">Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés</span><span class="sxs-lookup"><span data-stu-id="707fe-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="707fe-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="707fe-149">NOTES</span></span>

## <span data-ttu-id="707fe-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="707fe-150">RELATED LINKS</span></span>

