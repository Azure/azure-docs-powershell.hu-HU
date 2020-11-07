---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840149"
---
# <span data-ttu-id="18eba-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="18eba-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="18eba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18eba-102">SYNOPSIS</span></span>
<span data-ttu-id="18eba-103">Frissíti az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="18eba-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="18eba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18eba-104">SYNTAX</span></span>

### <span data-ttu-id="18eba-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18eba-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18eba-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="18eba-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18eba-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="18eba-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18eba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="18eba-108">DESCRIPTION</span></span>
<span data-ttu-id="18eba-109">Frissíti az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="18eba-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="18eba-110">Példák</span><span class="sxs-lookup"><span data-stu-id="18eba-110">EXAMPLES</span></span>

### <span data-ttu-id="18eba-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="18eba-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="18eba-112">Frissíti az ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="18eba-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="18eba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18eba-113">PARAMETERS</span></span>

### <span data-ttu-id="18eba-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18eba-114">-InputObject</span></span>
<span data-ttu-id="18eba-115">A Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation típusú beviteli objektum.</span><span class="sxs-lookup"><span data-stu-id="18eba-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18eba-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="18eba-116">-Location</span></span>
<span data-ttu-id="18eba-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="18eba-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eba-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18eba-118">-Name</span></span>
<span data-ttu-id="18eba-119">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="18eba-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eba-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="18eba-120">-OfferName</span></span>
<span data-ttu-id="18eba-121">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="18eba-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18eba-122">-ResourceGroupName</span></span>
<span data-ttu-id="18eba-123">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="18eba-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18eba-124">-ResourceId</span></span>
<span data-ttu-id="18eba-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="18eba-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18eba-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18eba-126">-SubscriptionId</span></span>
<span data-ttu-id="18eba-127">A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="18eba-127">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eba-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18eba-128">-Confirm</span></span>
<span data-ttu-id="18eba-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18eba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18eba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18eba-130">-WhatIf</span></span>
<span data-ttu-id="18eba-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18eba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18eba-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18eba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18eba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18eba-133">CommonParameters</span></span>
<span data-ttu-id="18eba-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18eba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18eba-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18eba-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18eba-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18eba-136">INPUTS</span></span>

## <span data-ttu-id="18eba-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18eba-137">OUTPUTS</span></span>

### <span data-ttu-id="18eba-138">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="18eba-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="18eba-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18eba-139">NOTES</span></span>

## <span data-ttu-id="18eba-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18eba-140">RELATED LINKS</span></span>

