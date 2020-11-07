---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840153"
---
# <span data-ttu-id="e45c7-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="e45c7-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="e45c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e45c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e45c7-103">A megadott csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e45c7-103">Removes the specified plan</span></span>

## <span data-ttu-id="e45c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e45c7-104">SYNTAX</span></span>

### <span data-ttu-id="e45c7-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e45c7-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e45c7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e45c7-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e45c7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e45c7-107">DESCRIPTION</span></span>
<span data-ttu-id="e45c7-108">A megadott csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e45c7-108">Removes the specified plan</span></span>

## <span data-ttu-id="e45c7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e45c7-109">EXAMPLES</span></span>

### <span data-ttu-id="e45c7-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e45c7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="e45c7-111">A megadott csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e45c7-111">Removes the specified plan</span></span>

## <span data-ttu-id="e45c7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e45c7-112">PARAMETERS</span></span>

### <span data-ttu-id="e45c7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e45c7-113">-Force</span></span>
<span data-ttu-id="e45c7-114">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="e45c7-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="e45c7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e45c7-115">-Name</span></span>
<span data-ttu-id="e45c7-116">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="e45c7-116">Name of the plan.</span></span>

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

### <span data-ttu-id="e45c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="e45c7-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="e45c7-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e45c7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e45c7-119">-ResourceId</span></span>
<span data-ttu-id="e45c7-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e45c7-120">The resource id.</span></span>

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

### <span data-ttu-id="e45c7-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e45c7-121">-Confirm</span></span>
<span data-ttu-id="e45c7-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e45c7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45c7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45c7-123">-WhatIf</span></span>
<span data-ttu-id="e45c7-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e45c7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45c7-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e45c7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45c7-126">CommonParameters</span></span>
<span data-ttu-id="e45c7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e45c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45c7-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45c7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45c7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e45c7-129">INPUTS</span></span>

## <span data-ttu-id="e45c7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e45c7-130">OUTPUTS</span></span>

## <span data-ttu-id="e45c7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e45c7-131">NOTES</span></span>

## <span data-ttu-id="e45c7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e45c7-132">RELATED LINKS</span></span>

