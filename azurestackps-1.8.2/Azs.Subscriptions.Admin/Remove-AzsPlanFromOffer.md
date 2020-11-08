---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016772"
---
# <span data-ttu-id="61bb9-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="61bb9-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="61bb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="61bb9-103">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="61bb9-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="61bb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61bb9-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61bb9-105">DESCRIPTION</span></span>
<span data-ttu-id="61bb9-106">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="61bb9-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="61bb9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="61bb9-107">EXAMPLES</span></span>

### <span data-ttu-id="61bb9-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="61bb9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="61bb9-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61bb9-109">PARAMETERS</span></span>

### <span data-ttu-id="61bb9-110">-Force</span><span class="sxs-lookup"><span data-stu-id="61bb9-110">-Force</span></span>
<span data-ttu-id="61bb9-111">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="61bb9-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="61bb9-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="61bb9-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="61bb9-113">A beszerzések maximális száma az előfizetőktől</span><span class="sxs-lookup"><span data-stu-id="61bb9-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bb9-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="61bb9-114">-OfferName</span></span>
<span data-ttu-id="61bb9-115">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="61bb9-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bb9-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="61bb9-116">-PlanLinkType</span></span>
<span data-ttu-id="61bb9-117">A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="61bb9-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="61bb9-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="61bb9-118">-PlanName</span></span>
<span data-ttu-id="61bb9-119">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="61bb9-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bb9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bb9-120">-ResourceGroupName</span></span>
<span data-ttu-id="61bb9-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="61bb9-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bb9-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="61bb9-122">-Confirm</span></span>
<span data-ttu-id="61bb9-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61bb9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bb9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bb9-124">-WhatIf</span></span>
<span data-ttu-id="61bb9-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="61bb9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bb9-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61bb9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bb9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bb9-127">CommonParameters</span></span>
<span data-ttu-id="61bb9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61bb9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bb9-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bb9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bb9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61bb9-130">INPUTS</span></span>

## <span data-ttu-id="61bb9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61bb9-131">OUTPUTS</span></span>

## <span data-ttu-id="61bb9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61bb9-132">NOTES</span></span>

## <span data-ttu-id="61bb9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61bb9-133">RELATED LINKS</span></span>

