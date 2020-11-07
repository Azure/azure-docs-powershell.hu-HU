---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840154"
---
# <span data-ttu-id="92da4-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="92da4-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="92da4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92da4-102">SYNOPSIS</span></span>
<span data-ttu-id="92da4-103">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="92da4-103">Delete the specified offer.</span></span>

## <span data-ttu-id="92da4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92da4-104">SYNTAX</span></span>

### <span data-ttu-id="92da4-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92da4-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92da4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="92da4-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92da4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92da4-107">DESCRIPTION</span></span>
<span data-ttu-id="92da4-108">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="92da4-108">Delete the specified offer.</span></span>

## <span data-ttu-id="92da4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="92da4-109">EXAMPLES</span></span>

### <span data-ttu-id="92da4-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="92da4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="92da4-111">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="92da4-111">Delete the specified offer.</span></span>

## <span data-ttu-id="92da4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92da4-112">PARAMETERS</span></span>

### <span data-ttu-id="92da4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="92da4-113">-Force</span></span>
<span data-ttu-id="92da4-114">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="92da4-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="92da4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92da4-115">-Name</span></span>
<span data-ttu-id="92da4-116">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="92da4-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92da4-117">-ResourceGroupName</span></span>
<span data-ttu-id="92da4-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="92da4-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92da4-119">-ResourceId</span></span>
<span data-ttu-id="92da4-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="92da4-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92da4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92da4-121">-Confirm</span></span>
<span data-ttu-id="92da4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92da4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92da4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92da4-123">-WhatIf</span></span>
<span data-ttu-id="92da4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92da4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92da4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92da4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92da4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92da4-126">CommonParameters</span></span>
<span data-ttu-id="92da4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92da4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92da4-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92da4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92da4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92da4-129">INPUTS</span></span>

## <span data-ttu-id="92da4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92da4-130">OUTPUTS</span></span>

## <span data-ttu-id="92da4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92da4-131">NOTES</span></span>

## <span data-ttu-id="92da4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92da4-132">RELATED LINKS</span></span>

