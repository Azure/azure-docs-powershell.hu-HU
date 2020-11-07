---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671733"
---
# <span data-ttu-id="4fdc0-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="4fdc0-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="4fdc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdc0-103">Eltávolítja a megadott bérlői előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="4fdc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fdc0-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fdc0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fdc0-105">DESCRIPTION</span></span>
<span data-ttu-id="4fdc0-106">Eltávolítja a megadott bérlői előfizetést.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="4fdc0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4fdc0-107">EXAMPLES</span></span>

### <span data-ttu-id="4fdc0-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4fdc0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="4fdc0-109">A megadott bérlői előfizetés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="4fdc0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fdc0-110">PARAMETERS</span></span>

### <span data-ttu-id="4fdc0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4fdc0-111">-Force</span></span>
<span data-ttu-id="4fdc0-112">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="4fdc0-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fdc0-113">-SubscriptionId</span></span>
<span data-ttu-id="4fdc0-114">Előfizetés azonosítója paraméter</span><span class="sxs-lookup"><span data-stu-id="4fdc0-114">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="4fdc0-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fdc0-115">-Confirm</span></span>
<span data-ttu-id="4fdc0-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fdc0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fdc0-117">-WhatIf</span></span>
<span data-ttu-id="4fdc0-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fdc0-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fdc0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdc0-120">CommonParameters</span></span>
<span data-ttu-id="4fdc0-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fdc0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdc0-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fdc0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdc0-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fdc0-123">INPUTS</span></span>

## <span data-ttu-id="4fdc0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fdc0-124">OUTPUTS</span></span>

## <span data-ttu-id="4fdc0-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fdc0-125">NOTES</span></span>

## <span data-ttu-id="4fdc0-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fdc0-126">RELATED LINKS</span></span>

