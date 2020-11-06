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
ms.locfileid: "93491144"
---
# <span data-ttu-id="85010-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="85010-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="85010-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85010-102">SYNOPSIS</span></span>
<span data-ttu-id="85010-103">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="85010-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="85010-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85010-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85010-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85010-105">DESCRIPTION</span></span>
<span data-ttu-id="85010-106">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="85010-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="85010-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85010-107">EXAMPLES</span></span>

### <span data-ttu-id="85010-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="85010-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="85010-109">Új gyűjtemény létrehozása elem létrehozása</span><span class="sxs-lookup"><span data-stu-id="85010-109">Create a new gallery item.</span></span>

## <span data-ttu-id="85010-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85010-110">PARAMETERS</span></span>

### <span data-ttu-id="85010-111">-Force</span><span class="sxs-lookup"><span data-stu-id="85010-111">-Force</span></span>
<span data-ttu-id="85010-112">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85010-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="85010-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="85010-113">-GalleryItemUri</span></span>
<span data-ttu-id="85010-114">Az URI-elem a JSON-fájl gyűjteményében.</span><span class="sxs-lookup"><span data-stu-id="85010-114">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="85010-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="85010-115">-Confirm</span></span>
<span data-ttu-id="85010-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85010-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85010-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85010-117">-WhatIf</span></span>
<span data-ttu-id="85010-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="85010-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85010-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85010-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85010-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85010-120">CommonParameters</span></span>
<span data-ttu-id="85010-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85010-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85010-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85010-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85010-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85010-123">INPUTS</span></span>

## <span data-ttu-id="85010-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85010-124">OUTPUTS</span></span>

### <span data-ttu-id="85010-125">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="85010-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="85010-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85010-126">NOTES</span></span>

## <span data-ttu-id="85010-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85010-127">RELATED LINKS</span></span>

