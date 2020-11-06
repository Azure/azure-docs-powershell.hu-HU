---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 33544da0c95e6b53da2a0dc189ca0dfe538da270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490867"
---
# <span data-ttu-id="20f8e-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="20f8e-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="20f8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="20f8e-103">Új előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="20f8e-103">Create a new subscription.</span></span>

## <span data-ttu-id="20f8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20f8e-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20f8e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20f8e-105">DESCRIPTION</span></span>
<span data-ttu-id="20f8e-106">Új előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="20f8e-106">Create a new subscription.</span></span>

## <span data-ttu-id="20f8e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="20f8e-107">EXAMPLES</span></span>

### <span data-ttu-id="20f8e-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="20f8e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="20f8e-109">Új felhasználói előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="20f8e-109">Creates a new user subscription</span></span>

## <span data-ttu-id="20f8e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20f8e-110">PARAMETERS</span></span>

### <span data-ttu-id="20f8e-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20f8e-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="20f8e-112">Fölérendelt DelegatedProvider-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="20f8e-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f8e-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="20f8e-113">-DisplayName</span></span>
<span data-ttu-id="20f8e-114">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="20f8e-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f8e-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="20f8e-115">-ExternalReferenceId</span></span>
<span data-ttu-id="20f8e-116">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="20f8e-116">External reference identifier.</span></span>

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

### <span data-ttu-id="20f8e-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="20f8e-117">-OfferId</span></span>
<span data-ttu-id="20f8e-118">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="20f8e-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f8e-119">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="20f8e-119">-Owner</span></span>
<span data-ttu-id="20f8e-120">Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="20f8e-120">Subscription owner.</span></span>

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

### <span data-ttu-id="20f8e-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="20f8e-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="20f8e-122">Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="20f8e-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f8e-123">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="20f8e-123">-State</span></span>
<span data-ttu-id="20f8e-124">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="20f8e-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f8e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20f8e-125">-SubscriptionId</span></span>
<span data-ttu-id="20f8e-126">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="20f8e-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f8e-127">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="20f8e-127">-TenantId</span></span>
<span data-ttu-id="20f8e-128">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="20f8e-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="20f8e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20f8e-129">-Confirm</span></span>
<span data-ttu-id="20f8e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20f8e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f8e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f8e-131">-WhatIf</span></span>
<span data-ttu-id="20f8e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20f8e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20f8e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20f8e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f8e-134">CommonParameters</span></span>
<span data-ttu-id="20f8e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20f8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f8e-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f8e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f8e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20f8e-137">INPUTS</span></span>

## <span data-ttu-id="20f8e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20f8e-138">OUTPUTS</span></span>

### <span data-ttu-id="20f8e-139">Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés</span><span class="sxs-lookup"><span data-stu-id="20f8e-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="20f8e-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20f8e-140">NOTES</span></span>

## <span data-ttu-id="20f8e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20f8e-141">RELATED LINKS</span></span>

