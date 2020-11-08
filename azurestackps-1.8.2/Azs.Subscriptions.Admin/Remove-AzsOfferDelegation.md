---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016746"
---
# <span data-ttu-id="c4ead-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c4ead-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="c4ead-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4ead-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ead-103">Az ajánlat-delegálás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c4ead-103">Removes the offer delegation</span></span>

## <span data-ttu-id="c4ead-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4ead-104">SYNTAX</span></span>

### <span data-ttu-id="c4ead-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4ead-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ead-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4ead-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4ead-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4ead-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ead-108">Az ajánlat-delegálás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c4ead-108">Removes the offer delegation</span></span>

## <span data-ttu-id="c4ead-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c4ead-109">EXAMPLES</span></span>

### <span data-ttu-id="c4ead-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4ead-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="c4ead-111">Az ajánlat-delegálás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c4ead-111">Removes the offer delegation</span></span>

## <span data-ttu-id="c4ead-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4ead-112">PARAMETERS</span></span>

### <span data-ttu-id="c4ead-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c4ead-113">-Force</span></span>
<span data-ttu-id="c4ead-114">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="c4ead-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="c4ead-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4ead-115">-Name</span></span>
<span data-ttu-id="c4ead-116">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="c4ead-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="c4ead-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c4ead-117">-OfferName</span></span>
<span data-ttu-id="c4ead-118">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="c4ead-118">Name of an offer.</span></span>

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

### <span data-ttu-id="c4ead-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ead-119">-ResourceGroupName</span></span>
<span data-ttu-id="c4ead-120">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="c4ead-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c4ead-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4ead-121">-ResourceId</span></span>
<span data-ttu-id="c4ead-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c4ead-122">The resource id.</span></span>

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

### <span data-ttu-id="c4ead-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4ead-123">-Confirm</span></span>
<span data-ttu-id="c4ead-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4ead-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ead-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ead-125">-WhatIf</span></span>
<span data-ttu-id="c4ead-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4ead-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ead-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4ead-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ead-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ead-128">CommonParameters</span></span>
<span data-ttu-id="c4ead-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4ead-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ead-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ead-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ead-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4ead-131">INPUTS</span></span>

## <span data-ttu-id="c4ead-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4ead-132">OUTPUTS</span></span>

## <span data-ttu-id="c4ead-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4ead-133">NOTES</span></span>

## <span data-ttu-id="c4ead-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4ead-134">RELATED LINKS</span></span>

