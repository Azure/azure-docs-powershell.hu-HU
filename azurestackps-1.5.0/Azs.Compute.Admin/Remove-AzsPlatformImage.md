---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 947bb6b453d92897f7901a00ed5a43efa4ac640e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491047"
---
# <span data-ttu-id="abdd2-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="abdd2-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="abdd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abdd2-102">SYNOPSIS</span></span>
<span data-ttu-id="abdd2-103">Törölje a virtuális gép képét a platform képtárházában.</span><span class="sxs-lookup"><span data-stu-id="abdd2-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="abdd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abdd2-104">SYNTAX</span></span>

### <span data-ttu-id="abdd2-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abdd2-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abdd2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="abdd2-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abdd2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="abdd2-107">DESCRIPTION</span></span>
<span data-ttu-id="abdd2-108">Platform képének törlése</span><span class="sxs-lookup"><span data-stu-id="abdd2-108">Delete a platform image</span></span>

## <span data-ttu-id="abdd2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="abdd2-109">EXAMPLES</span></span>

### <span data-ttu-id="abdd2-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="abdd2-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="abdd2-111">A meglévő platformon lévő képek törlése</span><span class="sxs-lookup"><span data-stu-id="abdd2-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="abdd2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abdd2-112">PARAMETERS</span></span>

### <span data-ttu-id="abdd2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="abdd2-113">-Force</span></span>
<span data-ttu-id="abdd2-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abdd2-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="abdd2-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="abdd2-115">-Location</span></span>
<span data-ttu-id="abdd2-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="abdd2-116">Location of the resource.</span></span>

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

### <span data-ttu-id="abdd2-117">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="abdd2-117">-Offer</span></span>
<span data-ttu-id="abdd2-118">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="abdd2-118">Name of the offer.</span></span>

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

### <span data-ttu-id="abdd2-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="abdd2-119">-Publisher</span></span>
<span data-ttu-id="abdd2-120">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="abdd2-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="abdd2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abdd2-121">-ResourceId</span></span>
<span data-ttu-id="abdd2-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="abdd2-122">The resource id.</span></span>

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

### <span data-ttu-id="abdd2-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="abdd2-123">-Sku</span></span>
<span data-ttu-id="abdd2-124">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="abdd2-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="abdd2-125">-Verzió</span><span class="sxs-lookup"><span data-stu-id="abdd2-125">-Version</span></span>
<span data-ttu-id="abdd2-126">A virtuális gép képének verziója.</span><span class="sxs-lookup"><span data-stu-id="abdd2-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="abdd2-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abdd2-127">-Confirm</span></span>
<span data-ttu-id="abdd2-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abdd2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abdd2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abdd2-129">-WhatIf</span></span>
<span data-ttu-id="abdd2-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abdd2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abdd2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abdd2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abdd2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdd2-132">CommonParameters</span></span>
<span data-ttu-id="abdd2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abdd2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdd2-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abdd2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdd2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdd2-135">INPUTS</span></span>

## <span data-ttu-id="abdd2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdd2-136">OUTPUTS</span></span>

## <span data-ttu-id="abdd2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abdd2-137">NOTES</span></span>

## <span data-ttu-id="abdd2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abdd2-138">RELATED LINKS</span></span>

