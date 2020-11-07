---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839734"
---
# <span data-ttu-id="7453f-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="7453f-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="7453f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7453f-102">SYNOPSIS</span></span>
<span data-ttu-id="7453f-103">Összekapcsolja a csomagot az ajánlattal.</span><span class="sxs-lookup"><span data-stu-id="7453f-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="7453f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7453f-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7453f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7453f-105">DESCRIPTION</span></span>
<span data-ttu-id="7453f-106">Összekapcsolja a csomagot az ajánlattal.</span><span class="sxs-lookup"><span data-stu-id="7453f-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="7453f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7453f-107">EXAMPLES</span></span>

### <span data-ttu-id="7453f-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7453f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="7453f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7453f-109">PARAMETERS</span></span>

### <span data-ttu-id="7453f-110">-Force</span><span class="sxs-lookup"><span data-stu-id="7453f-110">-Force</span></span>
<span data-ttu-id="7453f-111">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="7453f-111">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7453f-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="7453f-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="7453f-113">A beszerzések maximális száma az előfizetőktől</span><span class="sxs-lookup"><span data-stu-id="7453f-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7453f-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="7453f-114">-OfferName</span></span>
<span data-ttu-id="7453f-115">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="7453f-115">Name of an offer.</span></span>

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

### <span data-ttu-id="7453f-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="7453f-116">-PlanLinkType</span></span>
<span data-ttu-id="7453f-117">A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="7453f-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="7453f-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="7453f-118">-PlanName</span></span>
<span data-ttu-id="7453f-119">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="7453f-119">Name of the plan.</span></span>

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

### <span data-ttu-id="7453f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7453f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7453f-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="7453f-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7453f-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7453f-122">-Confirm</span></span>
<span data-ttu-id="7453f-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7453f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7453f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7453f-124">-WhatIf</span></span>
<span data-ttu-id="7453f-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7453f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7453f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7453f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7453f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7453f-127">CommonParameters</span></span>
<span data-ttu-id="7453f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7453f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7453f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7453f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7453f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7453f-130">INPUTS</span></span>

## <span data-ttu-id="7453f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7453f-131">OUTPUTS</span></span>

## <span data-ttu-id="7453f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7453f-132">NOTES</span></span>

## <span data-ttu-id="7453f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7453f-133">RELATED LINKS</span></span>

