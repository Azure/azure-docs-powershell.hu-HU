---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa4bd73f9300daf8ca17e3a11d884e06e9852234
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839697"
---
# <span data-ttu-id="b6ad6-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="b6ad6-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="b6ad6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ad6-103">A megadott csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6ad6-103">Removes the specified plan</span></span>

## <span data-ttu-id="b6ad6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6ad6-104">SYNTAX</span></span>

### <span data-ttu-id="b6ad6-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6ad6-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6ad6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6ad6-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ad6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6ad6-107">DESCRIPTION</span></span>
<span data-ttu-id="b6ad6-108">A megadott csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6ad6-108">Removes the specified plan</span></span>

## <span data-ttu-id="b6ad6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b6ad6-109">EXAMPLES</span></span>

### <span data-ttu-id="b6ad6-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b6ad6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="b6ad6-111">A megadott csomag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6ad6-111">Removes the specified plan</span></span>

## <span data-ttu-id="b6ad6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="b6ad6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b6ad6-113">-Force</span></span>
<span data-ttu-id="b6ad6-114">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="b6ad6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6ad6-115">-Name</span></span>
<span data-ttu-id="b6ad6-116">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-116">Name of the plan.</span></span>

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

### <span data-ttu-id="b6ad6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ad6-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6ad6-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b6ad6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6ad6-119">-ResourceId</span></span>
<span data-ttu-id="b6ad6-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-120">The resource id.</span></span>

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

### <span data-ttu-id="b6ad6-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6ad6-121">-Confirm</span></span>
<span data-ttu-id="b6ad6-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ad6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ad6-123">-WhatIf</span></span>
<span data-ttu-id="b6ad6-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ad6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ad6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ad6-126">CommonParameters</span></span>
<span data-ttu-id="b6ad6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6ad6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ad6-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ad6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ad6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6ad6-129">INPUTS</span></span>

## <span data-ttu-id="b6ad6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6ad6-130">OUTPUTS</span></span>

## <span data-ttu-id="b6ad6-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6ad6-131">NOTES</span></span>

## <span data-ttu-id="b6ad6-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6ad6-132">RELATED LINKS</span></span>

