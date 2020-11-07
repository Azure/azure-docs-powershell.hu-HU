---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840306"
---
# <span data-ttu-id="81527-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="81527-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="81527-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81527-102">SYNOPSIS</span></span>
<span data-ttu-id="81527-103">Törölje a megadott előfizetést.</span><span class="sxs-lookup"><span data-stu-id="81527-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="81527-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81527-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81527-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81527-105">DESCRIPTION</span></span>
<span data-ttu-id="81527-106">Törölje a megadott előfizetést.</span><span class="sxs-lookup"><span data-stu-id="81527-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="81527-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81527-107">EXAMPLES</span></span>

### <span data-ttu-id="81527-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="81527-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="81527-109">Törölje a megadott előfizetést.</span><span class="sxs-lookup"><span data-stu-id="81527-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="81527-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81527-110">PARAMETERS</span></span>

### <span data-ttu-id="81527-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81527-111">-SubscriptionId</span></span>
<span data-ttu-id="81527-112">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="81527-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="81527-113">-Force</span><span class="sxs-lookup"><span data-stu-id="81527-113">-Force</span></span>
<span data-ttu-id="81527-114">Előfizetés eltávolítása figyelmeztetés nélkül</span><span class="sxs-lookup"><span data-stu-id="81527-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="81527-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81527-115">-WhatIf</span></span>
<span data-ttu-id="81527-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81527-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81527-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81527-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81527-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81527-118">-Confirm</span></span>
<span data-ttu-id="81527-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81527-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81527-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81527-120">CommonParameters</span></span>
<span data-ttu-id="81527-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81527-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81527-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81527-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81527-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81527-123">INPUTS</span></span>

## <span data-ttu-id="81527-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81527-124">OUTPUTS</span></span>

## <span data-ttu-id="81527-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81527-125">NOTES</span></span>

## <span data-ttu-id="81527-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81527-126">RELATED LINKS</span></span>
