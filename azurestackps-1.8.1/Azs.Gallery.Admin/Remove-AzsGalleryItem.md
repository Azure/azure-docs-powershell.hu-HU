---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840770"
---
# <span data-ttu-id="39ca7-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="39ca7-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="39ca7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="39ca7-103">Adott gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="39ca7-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="39ca7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39ca7-104">SYNTAX</span></span>

### <span data-ttu-id="39ca7-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39ca7-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ca7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="39ca7-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ca7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="39ca7-107">DESCRIPTION</span></span>
<span data-ttu-id="39ca7-108">Adott gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="39ca7-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="39ca7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39ca7-109">EXAMPLES</span></span>

### <span data-ttu-id="39ca7-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="39ca7-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="39ca7-111">Gyűjtemény-elem törlése</span><span class="sxs-lookup"><span data-stu-id="39ca7-111">Delete a gallery item.</span></span>

## <span data-ttu-id="39ca7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39ca7-112">PARAMETERS</span></span>

### <span data-ttu-id="39ca7-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39ca7-113">-Name</span></span>
<span data-ttu-id="39ca7-114">A gyűjtemény elemeinek azonosítása</span><span class="sxs-lookup"><span data-stu-id="39ca7-114">Identity of the gallery item.</span></span>
<span data-ttu-id="39ca7-115">Tartalmazza a közzétevő nevét, az elem nevét, valamint tartalmazhat az időszak karakterrel elválasztott verziót.</span><span class="sxs-lookup"><span data-stu-id="39ca7-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ca7-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39ca7-116">-ResourceId</span></span>
<span data-ttu-id="39ca7-117">Teljes mértékben minősített Azure Resource id.</span><span class="sxs-lookup"><span data-stu-id="39ca7-117">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="39ca7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="39ca7-118">-Force</span></span>
<span data-ttu-id="39ca7-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39ca7-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="39ca7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ca7-120">-WhatIf</span></span>
<span data-ttu-id="39ca7-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39ca7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ca7-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39ca7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ca7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39ca7-123">-Confirm</span></span>
<span data-ttu-id="39ca7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39ca7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ca7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ca7-125">CommonParameters</span></span>
<span data-ttu-id="39ca7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39ca7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ca7-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ca7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ca7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39ca7-128">INPUTS</span></span>

## <span data-ttu-id="39ca7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39ca7-129">OUTPUTS</span></span>

## <span data-ttu-id="39ca7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39ca7-130">NOTES</span></span>

## <span data-ttu-id="39ca7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39ca7-131">RELATED LINKS</span></span>
