---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25411a71a6d8233be55ab25ac99487da0b44bd0b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840451"
---
# <span data-ttu-id="5f8c6-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="5f8c6-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="5f8c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8c6-103">Eltávolítja a megadott bérlői előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5f8c6-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="5f8c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f8c6-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f8c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f8c6-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8c6-106">Eltávolítja a megadott bérlői előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5f8c6-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="5f8c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5f8c6-107">EXAMPLES</span></span>

### <span data-ttu-id="5f8c6-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f8c6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="5f8c6-109">A megadott bérlői előfizetés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5f8c6-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="5f8c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f8c6-110">PARAMETERS</span></span>

### <span data-ttu-id="5f8c6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5f8c6-111">-Force</span></span>
<span data-ttu-id="5f8c6-112">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="5f8c6-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="5f8c6-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f8c6-113">-SubscriptionId</span></span>
<span data-ttu-id="5f8c6-114">Előfizetés azonosítója paraméter</span><span class="sxs-lookup"><span data-stu-id="5f8c6-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f8c6-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f8c6-115">-Confirm</span></span>
<span data-ttu-id="5f8c6-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f8c6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f8c6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f8c6-117">-WhatIf</span></span>
<span data-ttu-id="5f8c6-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f8c6-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f8c6-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f8c6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f8c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8c6-120">CommonParameters</span></span>
<span data-ttu-id="5f8c6-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f8c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8c6-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8c6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8c6-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f8c6-123">INPUTS</span></span>

## <span data-ttu-id="5f8c6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f8c6-124">OUTPUTS</span></span>

## <span data-ttu-id="5f8c6-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f8c6-125">NOTES</span></span>

## <span data-ttu-id="5f8c6-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f8c6-126">RELATED LINKS</span></span>

