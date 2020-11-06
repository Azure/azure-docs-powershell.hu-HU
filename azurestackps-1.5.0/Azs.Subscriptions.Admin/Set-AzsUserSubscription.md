---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 106293e9d959aefe25ae3e4b27519639a39193d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491191"
---
# <span data-ttu-id="e07d0-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e07d0-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="e07d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e07d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e07d0-103">A megadott felhasználói előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="e07d0-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="e07d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e07d0-104">SYNTAX</span></span>

### <span data-ttu-id="e07d0-105">Set (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e07d0-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07d0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07d0-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07d0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e07d0-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e07d0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e07d0-108">DESCRIPTION</span></span>
<span data-ttu-id="e07d0-109">A megadott felhasználói előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="e07d0-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="e07d0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e07d0-110">EXAMPLES</span></span>

### <span data-ttu-id="e07d0-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e07d0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="e07d0-112">Előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="e07d0-112">Updates a subscription</span></span>

## <span data-ttu-id="e07d0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e07d0-113">PARAMETERS</span></span>

### <span data-ttu-id="e07d0-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e07d0-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="e07d0-115">Fölérendelt DelegatedProvider-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="e07d0-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="e07d0-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e07d0-116">-DisplayName</span></span>
<span data-ttu-id="e07d0-117">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="e07d0-117">Subscription name.</span></span>

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

### <span data-ttu-id="e07d0-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e07d0-118">-ExternalReferenceId</span></span>
<span data-ttu-id="e07d0-119">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="e07d0-119">External reference identifier.</span></span>

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

### <span data-ttu-id="e07d0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e07d0-120">-InputObject</span></span>
<span data-ttu-id="e07d0-121">A szövegbeviteli objektum típusa: Microsoft. AzureStack. Management. Network. admin. models. quote.</span><span class="sxs-lookup"><span data-stu-id="e07d0-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

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

### <span data-ttu-id="e07d0-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="e07d0-122">-Location</span></span>
<span data-ttu-id="e07d0-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e07d0-123">Location of the resource.</span></span>

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

### <span data-ttu-id="e07d0-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e07d0-124">-OfferId</span></span>
<span data-ttu-id="e07d0-125">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="e07d0-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="e07d0-126">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="e07d0-126">-Owner</span></span>
<span data-ttu-id="e07d0-127">Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="e07d0-127">Subscription owner.</span></span>

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

### <span data-ttu-id="e07d0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07d0-128">-ResourceId</span></span>
<span data-ttu-id="e07d0-129">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e07d0-129">The resource ID.</span></span>

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

### <span data-ttu-id="e07d0-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="e07d0-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="e07d0-131">Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="e07d0-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="e07d0-132">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="e07d0-132">-State</span></span>
<span data-ttu-id="e07d0-133">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="e07d0-133">Subscription state.</span></span>

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

### <span data-ttu-id="e07d0-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e07d0-134">-SubscriptionId</span></span>
<span data-ttu-id="e07d0-135">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e07d0-135">Subscription identifier.</span></span>

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

### <span data-ttu-id="e07d0-136">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="e07d0-136">-TenantId</span></span>
<span data-ttu-id="e07d0-137">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="e07d0-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="e07d0-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e07d0-138">-Confirm</span></span>
<span data-ttu-id="e07d0-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e07d0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07d0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07d0-140">-WhatIf</span></span>
<span data-ttu-id="e07d0-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e07d0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07d0-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e07d0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07d0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07d0-143">CommonParameters</span></span>
<span data-ttu-id="e07d0-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e07d0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07d0-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e07d0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07d0-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e07d0-146">INPUTS</span></span>

## <span data-ttu-id="e07d0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e07d0-147">OUTPUTS</span></span>

### <span data-ttu-id="e07d0-148">Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés</span><span class="sxs-lookup"><span data-stu-id="e07d0-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="e07d0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e07d0-149">NOTES</span></span>

## <span data-ttu-id="e07d0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e07d0-150">RELATED LINKS</span></span>

