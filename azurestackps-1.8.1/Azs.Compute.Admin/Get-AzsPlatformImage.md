---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840583"
---
# <span data-ttu-id="4585f-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="4585f-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="4585f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4585f-102">SYNOPSIS</span></span>
<span data-ttu-id="4585f-103">A platform képtárházba betöltött virtuális gép képeit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4585f-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="4585f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4585f-104">SYNTAX</span></span>

### <span data-ttu-id="4585f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4585f-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4585f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4585f-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4585f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4585f-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4585f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4585f-108">DESCRIPTION</span></span>
<span data-ttu-id="4585f-109">A platform képeit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4585f-109">Returns platform images.</span></span>

## <span data-ttu-id="4585f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4585f-110">EXAMPLES</span></span>

### <span data-ttu-id="4585f-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4585f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="4585f-112">A platform képtárházában a helyi helyre betöltött virtuális gép képeit számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4585f-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="4585f-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4585f-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="4585f-114">Speciális platformot tartalmazó kép beszerzése</span><span class="sxs-lookup"><span data-stu-id="4585f-114">Get a specific platform image.</span></span>

## <span data-ttu-id="4585f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4585f-115">PARAMETERS</span></span>

### <span data-ttu-id="4585f-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="4585f-116">-Location</span></span>
<span data-ttu-id="4585f-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4585f-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-118">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="4585f-118">-Offer</span></span>
<span data-ttu-id="4585f-119">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="4585f-119">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4585f-120">-Publisher</span></span>
<span data-ttu-id="4585f-121">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="4585f-121">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4585f-122">-ResourceId</span></span>
<span data-ttu-id="4585f-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4585f-123">The resource id.</span></span>

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

### <span data-ttu-id="4585f-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="4585f-124">-Sku</span></span>
<span data-ttu-id="4585f-125">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="4585f-125">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-126">-Verzió</span><span class="sxs-lookup"><span data-stu-id="4585f-126">-Version</span></span>
<span data-ttu-id="4585f-127">A platform képének verziója.</span><span class="sxs-lookup"><span data-stu-id="4585f-127">The version of the platform image.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4585f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4585f-128">CommonParameters</span></span>
<span data-ttu-id="4585f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4585f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4585f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4585f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4585f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4585f-131">INPUTS</span></span>

## <span data-ttu-id="4585f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4585f-132">OUTPUTS</span></span>

### <span data-ttu-id="4585f-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="4585f-133">PlatformImageObject</span></span>

## <span data-ttu-id="4585f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4585f-134">NOTES</span></span>

## <span data-ttu-id="4585f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4585f-135">RELATED LINKS</span></span>

