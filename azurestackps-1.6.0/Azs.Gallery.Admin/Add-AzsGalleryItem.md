---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491384"
---
# <span data-ttu-id="b52e8-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b52e8-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="b52e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b52e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b52e8-103">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="b52e8-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="b52e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b52e8-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b52e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b52e8-105">DESCRIPTION</span></span>
<span data-ttu-id="b52e8-106">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="b52e8-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="b52e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b52e8-107">EXAMPLES</span></span>

### <span data-ttu-id="b52e8-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b52e8-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="b52e8-109">Új gyűjtemény létrehozása elem létrehozása</span><span class="sxs-lookup"><span data-stu-id="b52e8-109">Create a new gallery item.</span></span>

## <span data-ttu-id="b52e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b52e8-110">PARAMETERS</span></span>

### <span data-ttu-id="b52e8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b52e8-111">-Force</span></span>
<span data-ttu-id="b52e8-112">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b52e8-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b52e8-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="b52e8-113">-GalleryItemUri</span></span>
<span data-ttu-id="b52e8-114">Az URI-elem a JSON-fájl gyűjteményében.</span><span class="sxs-lookup"><span data-stu-id="b52e8-114">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b52e8-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b52e8-115">-Confirm</span></span>
<span data-ttu-id="b52e8-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b52e8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b52e8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b52e8-117">-WhatIf</span></span>
<span data-ttu-id="b52e8-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b52e8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b52e8-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b52e8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b52e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52e8-120">CommonParameters</span></span>
<span data-ttu-id="b52e8-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b52e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52e8-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b52e8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52e8-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b52e8-123">INPUTS</span></span>

## <span data-ttu-id="b52e8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b52e8-124">OUTPUTS</span></span>

### <span data-ttu-id="b52e8-125">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="b52e8-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="b52e8-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b52e8-126">NOTES</span></span>

## <span data-ttu-id="b52e8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b52e8-127">RELATED LINKS</span></span>

