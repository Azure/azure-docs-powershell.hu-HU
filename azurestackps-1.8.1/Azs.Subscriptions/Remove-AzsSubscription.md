---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840646"
---
# <span data-ttu-id="701e8-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="701e8-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="701e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="701e8-102">SYNOPSIS</span></span>
<span data-ttu-id="701e8-103">Törölje a megadott előfizetést.</span><span class="sxs-lookup"><span data-stu-id="701e8-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="701e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="701e8-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="701e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="701e8-105">DESCRIPTION</span></span>
<span data-ttu-id="701e8-106">Törölje a megadott előfizetést.</span><span class="sxs-lookup"><span data-stu-id="701e8-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="701e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="701e8-107">EXAMPLES</span></span>

### <span data-ttu-id="701e8-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="701e8-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="701e8-109">Törölje a megadott előfizetést.</span><span class="sxs-lookup"><span data-stu-id="701e8-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="701e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="701e8-110">PARAMETERS</span></span>

### <span data-ttu-id="701e8-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="701e8-111">-SubscriptionId</span></span>
<span data-ttu-id="701e8-112">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="701e8-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="701e8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="701e8-113">-Force</span></span>
<span data-ttu-id="701e8-114">Előfizetés eltávolítása figyelmeztetés nélkül</span><span class="sxs-lookup"><span data-stu-id="701e8-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="701e8-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="701e8-115">-WhatIf</span></span>
<span data-ttu-id="701e8-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="701e8-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="701e8-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="701e8-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="701e8-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="701e8-118">-Confirm</span></span>
<span data-ttu-id="701e8-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="701e8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="701e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="701e8-120">CommonParameters</span></span>
<span data-ttu-id="701e8-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="701e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="701e8-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="701e8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="701e8-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="701e8-123">INPUTS</span></span>

## <span data-ttu-id="701e8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="701e8-124">OUTPUTS</span></span>

## <span data-ttu-id="701e8-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="701e8-125">NOTES</span></span>

## <span data-ttu-id="701e8-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="701e8-126">RELATED LINKS</span></span>
