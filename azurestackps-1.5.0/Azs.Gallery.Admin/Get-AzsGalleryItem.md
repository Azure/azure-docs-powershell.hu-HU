---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491140"
---
# <span data-ttu-id="b95f5-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b95f5-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="b95f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b95f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b95f5-103">A gyűjtemény felsorolja a gyűjtemény elemeit.</span><span class="sxs-lookup"><span data-stu-id="b95f5-103">Lists gallery items.</span></span>

## <span data-ttu-id="b95f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b95f5-104">SYNTAX</span></span>

### <span data-ttu-id="b95f5-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b95f5-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="b95f5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b95f5-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="b95f5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b95f5-107">DESCRIPTION</span></span>
<span data-ttu-id="b95f5-108">Az Azure halom piactéren elérhető gyűjtemény-elemek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b95f5-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="b95f5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b95f5-109">EXAMPLES</span></span>

### <span data-ttu-id="b95f5-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b95f5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="b95f5-111">A lista gyűjtemény elemei.</span><span class="sxs-lookup"><span data-stu-id="b95f5-111">List gallery items.</span></span>

### <span data-ttu-id="b95f5-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b95f5-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="b95f5-113">Gyűjtemény-elem beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="b95f5-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="b95f5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b95f5-114">PARAMETERS</span></span>

### <span data-ttu-id="b95f5-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b95f5-115">-Name</span></span>
<span data-ttu-id="b95f5-116">A gyűjtemény elemeinek azonosítása</span><span class="sxs-lookup"><span data-stu-id="b95f5-116">Identity of the gallery item.</span></span>
<span data-ttu-id="b95f5-117">Tartalmazza a közzétevő nevét, az elem nevét, valamint tartalmazhat az időszak karakterrel elválasztott verziót.</span><span class="sxs-lookup"><span data-stu-id="b95f5-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="b95f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95f5-118">CommonParameters</span></span>
<span data-ttu-id="b95f5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b95f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95f5-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95f5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95f5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b95f5-121">INPUTS</span></span>

## <span data-ttu-id="b95f5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b95f5-122">OUTPUTS</span></span>

### <span data-ttu-id="b95f5-123">Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="b95f5-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="b95f5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b95f5-124">NOTES</span></span>

## <span data-ttu-id="b95f5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b95f5-125">RELATED LINKS</span></span>

