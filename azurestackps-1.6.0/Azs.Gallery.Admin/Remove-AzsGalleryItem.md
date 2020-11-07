---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671757"
---
# <span data-ttu-id="3ff07-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="3ff07-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="3ff07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ff07-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff07-103">Adott gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="3ff07-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="3ff07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ff07-104">SYNTAX</span></span>

### <span data-ttu-id="3ff07-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ff07-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff07-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff07-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ff07-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ff07-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff07-108">Adott gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="3ff07-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="3ff07-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3ff07-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff07-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3ff07-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="3ff07-111">Gyűjtemény-elem törlése</span><span class="sxs-lookup"><span data-stu-id="3ff07-111">Delete a gallery item.</span></span>

## <span data-ttu-id="3ff07-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ff07-112">PARAMETERS</span></span>

### <span data-ttu-id="3ff07-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ff07-113">-Force</span></span>
<span data-ttu-id="3ff07-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ff07-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3ff07-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ff07-115">-Name</span></span>
<span data-ttu-id="3ff07-116">A gyűjtemény elemeinek azonosítása</span><span class="sxs-lookup"><span data-stu-id="3ff07-116">Identity of the gallery item.</span></span>
<span data-ttu-id="3ff07-117">Tartalmazza a közzétevő nevét, az elem nevét, valamint tartalmazhat az időszak karakterrel elválasztott verziót.</span><span class="sxs-lookup"><span data-stu-id="3ff07-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="3ff07-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff07-118">-ResourceId</span></span>
<span data-ttu-id="3ff07-119">Teljes mértékben minősített Azure Resource id.</span><span class="sxs-lookup"><span data-stu-id="3ff07-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="3ff07-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ff07-120">-Confirm</span></span>
<span data-ttu-id="3ff07-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ff07-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff07-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff07-122">-WhatIf</span></span>
<span data-ttu-id="3ff07-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ff07-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff07-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ff07-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff07-125">CommonParameters</span></span>
<span data-ttu-id="3ff07-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ff07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff07-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff07-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff07-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ff07-128">INPUTS</span></span>

## <span data-ttu-id="3ff07-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ff07-129">OUTPUTS</span></span>

## <span data-ttu-id="3ff07-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ff07-130">NOTES</span></span>

## <span data-ttu-id="3ff07-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ff07-131">RELATED LINKS</span></span>

