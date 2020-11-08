---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016783"
---
# <span data-ttu-id="ce7af-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ce7af-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="ce7af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce7af-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7af-103">Törölje a virtuális gép képét a platform képtárházában.</span><span class="sxs-lookup"><span data-stu-id="ce7af-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="ce7af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce7af-104">SYNTAX</span></span>

### <span data-ttu-id="ce7af-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce7af-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7af-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce7af-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce7af-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce7af-107">DESCRIPTION</span></span>
<span data-ttu-id="ce7af-108">Platform képének törlése</span><span class="sxs-lookup"><span data-stu-id="ce7af-108">Delete a platform image</span></span>

## <span data-ttu-id="ce7af-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ce7af-109">EXAMPLES</span></span>

### <span data-ttu-id="ce7af-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ce7af-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="ce7af-111">A meglévő platformon lévő képek törlése</span><span class="sxs-lookup"><span data-stu-id="ce7af-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="ce7af-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce7af-112">PARAMETERS</span></span>

### <span data-ttu-id="ce7af-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ce7af-113">-Force</span></span>
<span data-ttu-id="ce7af-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce7af-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ce7af-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="ce7af-115">-Location</span></span>
<span data-ttu-id="ce7af-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ce7af-116">Location of the resource.</span></span>

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

### <span data-ttu-id="ce7af-117">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="ce7af-117">-Offer</span></span>
<span data-ttu-id="ce7af-118">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="ce7af-118">Name of the offer.</span></span>

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

### <span data-ttu-id="ce7af-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ce7af-119">-Publisher</span></span>
<span data-ttu-id="ce7af-120">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="ce7af-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="ce7af-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce7af-121">-ResourceId</span></span>
<span data-ttu-id="ce7af-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ce7af-122">The resource id.</span></span>

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

### <span data-ttu-id="ce7af-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="ce7af-123">-Sku</span></span>
<span data-ttu-id="ce7af-124">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="ce7af-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="ce7af-125">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ce7af-125">-Version</span></span>
<span data-ttu-id="ce7af-126">A virtuális gép képének verziója.</span><span class="sxs-lookup"><span data-stu-id="ce7af-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="ce7af-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce7af-127">-Confirm</span></span>
<span data-ttu-id="ce7af-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce7af-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce7af-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7af-129">-WhatIf</span></span>
<span data-ttu-id="ce7af-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce7af-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce7af-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce7af-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce7af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7af-132">CommonParameters</span></span>
<span data-ttu-id="ce7af-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce7af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7af-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce7af-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7af-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce7af-135">INPUTS</span></span>

## <span data-ttu-id="ce7af-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce7af-136">OUTPUTS</span></span>

## <span data-ttu-id="ce7af-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce7af-137">NOTES</span></span>

## <span data-ttu-id="ce7af-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce7af-138">RELATED LINKS</span></span>

