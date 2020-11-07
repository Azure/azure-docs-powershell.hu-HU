---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840455"
---
# <span data-ttu-id="64f37-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="64f37-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="64f37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64f37-102">SYNOPSIS</span></span>
<span data-ttu-id="64f37-103">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="64f37-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="64f37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64f37-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64f37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64f37-105">DESCRIPTION</span></span>
<span data-ttu-id="64f37-106">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="64f37-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="64f37-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64f37-107">EXAMPLES</span></span>

### <span data-ttu-id="64f37-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="64f37-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="64f37-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64f37-109">PARAMETERS</span></span>

### <span data-ttu-id="64f37-110">-Force</span><span class="sxs-lookup"><span data-stu-id="64f37-110">-Force</span></span>
<span data-ttu-id="64f37-111">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="64f37-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="64f37-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="64f37-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="64f37-113">A beszerzések maximális száma az előfizetőktől</span><span class="sxs-lookup"><span data-stu-id="64f37-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="64f37-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="64f37-114">-OfferName</span></span>
<span data-ttu-id="64f37-115">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="64f37-115">Name of an offer.</span></span>

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

### <span data-ttu-id="64f37-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="64f37-116">-PlanLinkType</span></span>
<span data-ttu-id="64f37-117">A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="64f37-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="64f37-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="64f37-118">-PlanName</span></span>
<span data-ttu-id="64f37-119">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="64f37-119">Name of the plan.</span></span>

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

### <span data-ttu-id="64f37-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f37-120">-ResourceGroupName</span></span>
<span data-ttu-id="64f37-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="64f37-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="64f37-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64f37-122">-Confirm</span></span>
<span data-ttu-id="64f37-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64f37-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f37-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f37-124">-WhatIf</span></span>
<span data-ttu-id="64f37-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64f37-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64f37-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64f37-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f37-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f37-127">CommonParameters</span></span>
<span data-ttu-id="64f37-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64f37-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f37-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f37-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f37-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64f37-130">INPUTS</span></span>

## <span data-ttu-id="64f37-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64f37-131">OUTPUTS</span></span>

## <span data-ttu-id="64f37-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64f37-132">NOTES</span></span>

## <span data-ttu-id="64f37-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64f37-133">RELATED LINKS</span></span>

