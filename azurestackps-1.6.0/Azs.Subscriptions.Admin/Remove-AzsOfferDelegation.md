---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec978cebfaa12f574ce20638347839fd70099df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491572"
---
# <span data-ttu-id="589f3-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="589f3-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="589f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="589f3-102">SYNOPSIS</span></span>
<span data-ttu-id="589f3-103">Az ajánlat-delegálás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="589f3-103">Removes the offer delegation</span></span>

## <span data-ttu-id="589f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="589f3-104">SYNTAX</span></span>

### <span data-ttu-id="589f3-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="589f3-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="589f3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="589f3-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="589f3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="589f3-107">DESCRIPTION</span></span>
<span data-ttu-id="589f3-108">Az ajánlat-delegálás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="589f3-108">Removes the offer delegation</span></span>

## <span data-ttu-id="589f3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="589f3-109">EXAMPLES</span></span>

### <span data-ttu-id="589f3-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="589f3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="589f3-111">Az ajánlat-delegálás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="589f3-111">Removes the offer delegation</span></span>

## <span data-ttu-id="589f3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="589f3-112">PARAMETERS</span></span>

### <span data-ttu-id="589f3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="589f3-113">-Force</span></span>
<span data-ttu-id="589f3-114">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="589f3-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="589f3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="589f3-115">-Name</span></span>
<span data-ttu-id="589f3-116">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="589f3-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="589f3-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="589f3-117">-OfferName</span></span>
<span data-ttu-id="589f3-118">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="589f3-118">Name of an offer.</span></span>

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

### <span data-ttu-id="589f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="589f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="589f3-120">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="589f3-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="589f3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="589f3-121">-ResourceId</span></span>
<span data-ttu-id="589f3-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="589f3-122">The resource id.</span></span>

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

### <span data-ttu-id="589f3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="589f3-123">-Confirm</span></span>
<span data-ttu-id="589f3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="589f3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="589f3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="589f3-125">-WhatIf</span></span>
<span data-ttu-id="589f3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="589f3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="589f3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="589f3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="589f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589f3-128">CommonParameters</span></span>
<span data-ttu-id="589f3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="589f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589f3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="589f3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589f3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="589f3-131">INPUTS</span></span>

## <span data-ttu-id="589f3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="589f3-132">OUTPUTS</span></span>

## <span data-ttu-id="589f3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="589f3-133">NOTES</span></span>

## <span data-ttu-id="589f3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="589f3-134">RELATED LINKS</span></span>

