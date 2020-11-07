---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840290"
---
# <span data-ttu-id="689ef-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="689ef-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="689ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="689ef-102">SYNOPSIS</span></span>
<span data-ttu-id="689ef-103">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="689ef-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="689ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="689ef-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="689ef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="689ef-105">DESCRIPTION</span></span>
<span data-ttu-id="689ef-106">Feltölti a szolgáltató gyűjteményének elemét a tárolóba.</span><span class="sxs-lookup"><span data-stu-id="689ef-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="689ef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="689ef-107">EXAMPLES</span></span>

### <span data-ttu-id="689ef-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="689ef-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="689ef-109">Új gyűjtemény létrehozása elem létrehozása</span><span class="sxs-lookup"><span data-stu-id="689ef-109">Create a new gallery item.</span></span>

## <span data-ttu-id="689ef-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="689ef-110">PARAMETERS</span></span>

### <span data-ttu-id="689ef-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="689ef-111">-GalleryItemUri</span></span>
<span data-ttu-id="689ef-112">Az URI-elem a JSON-fájl gyűjteményében.</span><span class="sxs-lookup"><span data-stu-id="689ef-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="689ef-113">-Force</span><span class="sxs-lookup"><span data-stu-id="689ef-113">-Force</span></span>
<span data-ttu-id="689ef-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="689ef-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="689ef-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="689ef-115">-WhatIf</span></span>
<span data-ttu-id="689ef-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="689ef-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="689ef-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="689ef-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="689ef-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="689ef-118">-Confirm</span></span>
<span data-ttu-id="689ef-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="689ef-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="689ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689ef-120">CommonParameters</span></span>
<span data-ttu-id="689ef-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="689ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689ef-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="689ef-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689ef-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="689ef-123">INPUTS</span></span>

## <span data-ttu-id="689ef-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="689ef-124">OUTPUTS</span></span>

### <span data-ttu-id="689ef-125">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="689ef-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="689ef-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="689ef-126">NOTES</span></span>

## <span data-ttu-id="689ef-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="689ef-127">RELATED LINKS</span></span>
