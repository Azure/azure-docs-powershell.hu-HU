---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840233"
---
# <span data-ttu-id="1e5b5-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="1e5b5-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="1e5b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5b5-103">A virtuálisgép-bővítmények lemezképének törlése</span><span class="sxs-lookup"><span data-stu-id="1e5b5-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="1e5b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e5b5-104">SYNTAX</span></span>

### <span data-ttu-id="1e5b5-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e5b5-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e5b5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5b5-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e5b5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e5b5-107">DESCRIPTION</span></span>
<span data-ttu-id="1e5b5-108">Törli a virtuálisgép-bővítmény megadott képét.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="1e5b5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1e5b5-109">EXAMPLES</span></span>

### <span data-ttu-id="1e5b5-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e5b5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="1e5b5-111">Platform képkiterjesztésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e5b5-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="1e5b5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e5b5-112">PARAMETERS</span></span>

### <span data-ttu-id="1e5b5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1e5b5-113">-Force</span></span>
<span data-ttu-id="1e5b5-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1e5b5-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="1e5b5-115">-Location</span></span>
<span data-ttu-id="1e5b5-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-116">Location of the resource.</span></span>

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

### <span data-ttu-id="1e5b5-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1e5b5-117">-Publisher</span></span>
<span data-ttu-id="1e5b5-118">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="1e5b5-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="1e5b5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5b5-119">-ResourceId</span></span>
<span data-ttu-id="1e5b5-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-120">The resource id.</span></span>

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

### <span data-ttu-id="1e5b5-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="1e5b5-121">-Type</span></span>
<span data-ttu-id="1e5b5-122">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-122">Type of extension.</span></span>

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

### <span data-ttu-id="1e5b5-123">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1e5b5-123">-Version</span></span>
<span data-ttu-id="1e5b5-124">A virtuális gép bővítményének képe.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="1e5b5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e5b5-125">-Confirm</span></span>
<span data-ttu-id="1e5b5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e5b5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5b5-127">-WhatIf</span></span>
<span data-ttu-id="1e5b5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5b5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e5b5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e5b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5b5-130">CommonParameters</span></span>
<span data-ttu-id="1e5b5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e5b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5b5-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5b5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5b5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e5b5-133">INPUTS</span></span>

## <span data-ttu-id="1e5b5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e5b5-134">OUTPUTS</span></span>

## <span data-ttu-id="1e5b5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e5b5-135">NOTES</span></span>

## <span data-ttu-id="1e5b5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e5b5-136">RELATED LINKS</span></span>

