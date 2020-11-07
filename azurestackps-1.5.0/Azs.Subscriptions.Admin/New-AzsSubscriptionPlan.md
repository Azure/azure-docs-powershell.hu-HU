---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aee9eab2ce04c1b9454fcf133edc290e887caf50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671717"
---
# <span data-ttu-id="46325-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="46325-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="46325-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46325-102">SYNOPSIS</span></span>
<span data-ttu-id="46325-103">Előfizetési csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="46325-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="46325-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46325-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46325-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46325-105">DESCRIPTION</span></span>
<span data-ttu-id="46325-106">Előfizetési csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="46325-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="46325-107">Példák</span><span class="sxs-lookup"><span data-stu-id="46325-107">EXAMPLES</span></span>

### <span data-ttu-id="46325-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="46325-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="46325-109">Előfizetési csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="46325-109">Create an subscription plan.</span></span>

## <span data-ttu-id="46325-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46325-110">PARAMETERS</span></span>

### <span data-ttu-id="46325-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="46325-111">-AcquisitionId</span></span>
<span data-ttu-id="46325-112">A beszerzési azonosító.</span><span class="sxs-lookup"><span data-stu-id="46325-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46325-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="46325-113">-PlanId</span></span>
<span data-ttu-id="46325-114">Megtervezi az azonosítót a bérlői előfizetési környezetben.</span><span class="sxs-lookup"><span data-stu-id="46325-114">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46325-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46325-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="46325-116">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="46325-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46325-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46325-117">-Confirm</span></span>
<span data-ttu-id="46325-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46325-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46325-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46325-119">-WhatIf</span></span>
<span data-ttu-id="46325-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46325-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46325-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46325-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46325-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46325-122">CommonParameters</span></span>
<span data-ttu-id="46325-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46325-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46325-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46325-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46325-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46325-125">INPUTS</span></span>

## <span data-ttu-id="46325-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46325-126">OUTPUTS</span></span>

### <span data-ttu-id="46325-127">Microsoft. AzureStack. Management. Subscriptions. admin. models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="46325-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="46325-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46325-128">NOTES</span></span>

## <span data-ttu-id="46325-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46325-129">RELATED LINKS</span></span>

