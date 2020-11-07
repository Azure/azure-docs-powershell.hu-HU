---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9212655ecb5f67dbf459548c48ff6d25420a8537
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837001"
---
# <span data-ttu-id="8af60-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="8af60-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="8af60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8af60-102">SYNOPSIS</span></span>
<span data-ttu-id="8af60-103">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="8af60-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="8af60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8af60-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8af60-105">DESCRIPTION</span></span>
<span data-ttu-id="8af60-106">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="8af60-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="8af60-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8af60-107">EXAMPLES</span></span>

### <span data-ttu-id="8af60-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8af60-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="8af60-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8af60-109">PARAMETERS</span></span>

### <span data-ttu-id="8af60-110">-Force</span><span class="sxs-lookup"><span data-stu-id="8af60-110">-Force</span></span>
<span data-ttu-id="8af60-111">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="8af60-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="8af60-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="8af60-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="8af60-113">A beszerzések maximális száma az előfizetőktől</span><span class="sxs-lookup"><span data-stu-id="8af60-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="8af60-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="8af60-114">-OfferName</span></span>
<span data-ttu-id="8af60-115">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="8af60-115">Name of an offer.</span></span>

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

### <span data-ttu-id="8af60-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="8af60-116">-PlanLinkType</span></span>
<span data-ttu-id="8af60-117">A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="8af60-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="8af60-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8af60-118">-PlanName</span></span>
<span data-ttu-id="8af60-119">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="8af60-119">Name of the plan.</span></span>

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

### <span data-ttu-id="8af60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af60-120">-ResourceGroupName</span></span>
<span data-ttu-id="8af60-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="8af60-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8af60-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8af60-122">-Confirm</span></span>
<span data-ttu-id="8af60-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8af60-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af60-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af60-124">-WhatIf</span></span>
<span data-ttu-id="8af60-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8af60-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af60-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8af60-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af60-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af60-127">CommonParameters</span></span>
<span data-ttu-id="8af60-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8af60-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af60-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af60-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af60-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af60-130">INPUTS</span></span>

## <span data-ttu-id="8af60-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af60-131">OUTPUTS</span></span>

## <span data-ttu-id="8af60-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8af60-132">NOTES</span></span>

## <span data-ttu-id="8af60-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8af60-133">RELATED LINKS</span></span>

