---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837000"
---
# <span data-ttu-id="3422a-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="3422a-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="3422a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3422a-102">SYNOPSIS</span></span>
<span data-ttu-id="3422a-103">Egy előfizetési csomag törlése</span><span class="sxs-lookup"><span data-stu-id="3422a-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="3422a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3422a-104">SYNTAX</span></span>

### <span data-ttu-id="3422a-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3422a-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3422a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3422a-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3422a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3422a-107">DESCRIPTION</span></span>
<span data-ttu-id="3422a-108">Egy előfizetési csomag törlése</span><span class="sxs-lookup"><span data-stu-id="3422a-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="3422a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3422a-109">EXAMPLES</span></span>

### <span data-ttu-id="3422a-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3422a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="3422a-111">Előfizetési csomag törlése</span><span class="sxs-lookup"><span data-stu-id="3422a-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="3422a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3422a-112">PARAMETERS</span></span>

### <span data-ttu-id="3422a-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="3422a-113">-AcquisitionId</span></span>
<span data-ttu-id="3422a-114">A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="3422a-114">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="3422a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3422a-115">-Force</span></span>
<span data-ttu-id="3422a-116">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="3422a-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="3422a-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3422a-117">-ResourceId</span></span>
<span data-ttu-id="3422a-118">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3422a-118">The resource id.</span></span>

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

### <span data-ttu-id="3422a-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3422a-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="3422a-120">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3422a-120">The target subscription ID.</span></span>

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

### <span data-ttu-id="3422a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3422a-121">-Confirm</span></span>
<span data-ttu-id="3422a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3422a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3422a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3422a-123">-WhatIf</span></span>
<span data-ttu-id="3422a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3422a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3422a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3422a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3422a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3422a-126">CommonParameters</span></span>
<span data-ttu-id="3422a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3422a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3422a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3422a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3422a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3422a-129">INPUTS</span></span>

## <span data-ttu-id="3422a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3422a-130">OUTPUTS</span></span>

## <span data-ttu-id="3422a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3422a-131">NOTES</span></span>

## <span data-ttu-id="3422a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3422a-132">RELATED LINKS</span></span>

