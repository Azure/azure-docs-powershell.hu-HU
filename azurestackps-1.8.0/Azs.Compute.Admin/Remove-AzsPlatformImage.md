---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840234"
---
# <span data-ttu-id="4427d-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="4427d-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="4427d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4427d-102">SYNOPSIS</span></span>
<span data-ttu-id="4427d-103">Törölje a virtuális gép képét a platform képtárházában.</span><span class="sxs-lookup"><span data-stu-id="4427d-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="4427d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4427d-104">SYNTAX</span></span>

### <span data-ttu-id="4427d-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4427d-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4427d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4427d-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4427d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4427d-107">DESCRIPTION</span></span>
<span data-ttu-id="4427d-108">Platform képének törlése</span><span class="sxs-lookup"><span data-stu-id="4427d-108">Delete a platform image</span></span>

## <span data-ttu-id="4427d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4427d-109">EXAMPLES</span></span>

### <span data-ttu-id="4427d-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4427d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="4427d-111">A meglévő platformon lévő képek törlése</span><span class="sxs-lookup"><span data-stu-id="4427d-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="4427d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4427d-112">PARAMETERS</span></span>

### <span data-ttu-id="4427d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4427d-113">-Force</span></span>
<span data-ttu-id="4427d-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4427d-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4427d-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="4427d-115">-Location</span></span>
<span data-ttu-id="4427d-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4427d-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4427d-117">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="4427d-117">-Offer</span></span>
<span data-ttu-id="4427d-118">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="4427d-118">Name of the offer.</span></span>

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

### <span data-ttu-id="4427d-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4427d-119">-Publisher</span></span>
<span data-ttu-id="4427d-120">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="4427d-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="4427d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4427d-121">-ResourceId</span></span>
<span data-ttu-id="4427d-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4427d-122">The resource id.</span></span>

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

### <span data-ttu-id="4427d-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="4427d-123">-Sku</span></span>
<span data-ttu-id="4427d-124">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="4427d-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="4427d-125">-Verzió</span><span class="sxs-lookup"><span data-stu-id="4427d-125">-Version</span></span>
<span data-ttu-id="4427d-126">A virtuális gép képének verziója.</span><span class="sxs-lookup"><span data-stu-id="4427d-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="4427d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4427d-127">-Confirm</span></span>
<span data-ttu-id="4427d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4427d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4427d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4427d-129">-WhatIf</span></span>
<span data-ttu-id="4427d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4427d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4427d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4427d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4427d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4427d-132">CommonParameters</span></span>
<span data-ttu-id="4427d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4427d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4427d-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4427d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4427d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4427d-135">INPUTS</span></span>

## <span data-ttu-id="4427d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4427d-136">OUTPUTS</span></span>

## <span data-ttu-id="4427d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4427d-137">NOTES</span></span>

## <span data-ttu-id="4427d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4427d-138">RELATED LINKS</span></span>

