---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840152"
---
# <span data-ttu-id="74c31-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="74c31-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="74c31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74c31-102">SYNOPSIS</span></span>
<span data-ttu-id="74c31-103">Egy előfizetési csomag törlése</span><span class="sxs-lookup"><span data-stu-id="74c31-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="74c31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74c31-104">SYNTAX</span></span>

### <span data-ttu-id="74c31-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74c31-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74c31-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="74c31-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74c31-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="74c31-107">DESCRIPTION</span></span>
<span data-ttu-id="74c31-108">Egy előfizetési csomag törlése</span><span class="sxs-lookup"><span data-stu-id="74c31-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="74c31-109">Példák</span><span class="sxs-lookup"><span data-stu-id="74c31-109">EXAMPLES</span></span>

### <span data-ttu-id="74c31-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="74c31-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="74c31-111">Előfizetési csomag törlése</span><span class="sxs-lookup"><span data-stu-id="74c31-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="74c31-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74c31-112">PARAMETERS</span></span>

### <span data-ttu-id="74c31-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="74c31-113">-AcquisitionId</span></span>
<span data-ttu-id="74c31-114">A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="74c31-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c31-115">-Force</span><span class="sxs-lookup"><span data-stu-id="74c31-115">-Force</span></span>
<span data-ttu-id="74c31-116">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="74c31-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="74c31-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74c31-117">-ResourceId</span></span>
<span data-ttu-id="74c31-118">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="74c31-118">The resource id.</span></span>

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

### <span data-ttu-id="74c31-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74c31-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="74c31-120">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="74c31-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="74c31-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74c31-121">-Confirm</span></span>
<span data-ttu-id="74c31-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74c31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c31-123">-WhatIf</span></span>
<span data-ttu-id="74c31-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74c31-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c31-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74c31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c31-126">CommonParameters</span></span>
<span data-ttu-id="74c31-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74c31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c31-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c31-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c31-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74c31-129">INPUTS</span></span>

## <span data-ttu-id="74c31-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74c31-130">OUTPUTS</span></span>

## <span data-ttu-id="74c31-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74c31-131">NOTES</span></span>

## <span data-ttu-id="74c31-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74c31-132">RELATED LINKS</span></span>

