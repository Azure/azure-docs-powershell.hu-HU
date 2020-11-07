---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840877"
---
# <span data-ttu-id="b4773-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b4773-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="b4773-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4773-102">SYNOPSIS</span></span>
<span data-ttu-id="b4773-103">A gyűjtemény felsorolja a gyűjtemény elemeit.</span><span class="sxs-lookup"><span data-stu-id="b4773-103">Lists gallery items.</span></span>

## <span data-ttu-id="b4773-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4773-104">SYNTAX</span></span>

### <span data-ttu-id="b4773-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4773-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="b4773-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b4773-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="b4773-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4773-107">DESCRIPTION</span></span>
<span data-ttu-id="b4773-108">Az Azure halom piactéren elérhető gyűjtemény-elemek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b4773-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="b4773-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b4773-109">EXAMPLES</span></span>

### <span data-ttu-id="b4773-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="b4773-110">EXAMPLE 1</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="b4773-111">A lista gyűjtemény elemei.</span><span class="sxs-lookup"><span data-stu-id="b4773-111">List gallery items.</span></span>

### <span data-ttu-id="b4773-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b4773-112">EXAMPLE 2</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="b4773-113">Gyűjtemény-elem beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="b4773-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="b4773-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4773-114">PARAMETERS</span></span>

### <span data-ttu-id="b4773-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4773-115">-Name</span></span>
<span data-ttu-id="b4773-116">A gyűjtemény elemeinek azonosítása</span><span class="sxs-lookup"><span data-stu-id="b4773-116">Identity of the gallery item.</span></span>
<span data-ttu-id="b4773-117">Tartalmazza a közzétevő nevét, az elem nevét, valamint tartalmazhat az időszak karakterrel elválasztott verziót.</span><span class="sxs-lookup"><span data-stu-id="b4773-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4773-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4773-118">CommonParameters</span></span>
<span data-ttu-id="b4773-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4773-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4773-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4773-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4773-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4773-121">INPUTS</span></span>

## <span data-ttu-id="b4773-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4773-122">OUTPUTS</span></span>

### <span data-ttu-id="b4773-123">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="b4773-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="b4773-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4773-124">NOTES</span></span>

## <span data-ttu-id="b4773-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4773-125">RELATED LINKS</span></span>
