---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840083"
---
# <span data-ttu-id="d6dd1-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="d6dd1-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="d6dd1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dd1-103">A virtuálisgép-bővítmények lemezképének törlése</span><span class="sxs-lookup"><span data-stu-id="d6dd1-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="d6dd1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6dd1-104">SYNTAX</span></span>

### <span data-ttu-id="d6dd1-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6dd1-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6dd1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6dd1-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6dd1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6dd1-107">DESCRIPTION</span></span>
<span data-ttu-id="d6dd1-108">Törli a virtuálisgép-bővítmény megadott képét.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="d6dd1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6dd1-109">EXAMPLES</span></span>

### <span data-ttu-id="d6dd1-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6dd1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="d6dd1-111">Platform képkiterjesztésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d6dd1-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="d6dd1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6dd1-112">PARAMETERS</span></span>

### <span data-ttu-id="d6dd1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d6dd1-113">-Force</span></span>
<span data-ttu-id="d6dd1-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d6dd1-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="d6dd1-115">-Location</span></span>
<span data-ttu-id="d6dd1-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-116">Location of the resource.</span></span>

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

### <span data-ttu-id="d6dd1-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d6dd1-117">-Publisher</span></span>
<span data-ttu-id="d6dd1-118">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="d6dd1-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="d6dd1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6dd1-119">-ResourceId</span></span>
<span data-ttu-id="d6dd1-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-120">The resource id.</span></span>

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

### <span data-ttu-id="d6dd1-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="d6dd1-121">-Type</span></span>
<span data-ttu-id="d6dd1-122">A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-122">Type of extension.</span></span>

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

### <span data-ttu-id="d6dd1-123">-Verzió</span><span class="sxs-lookup"><span data-stu-id="d6dd1-123">-Version</span></span>
<span data-ttu-id="d6dd1-124">A virtuális gép bővítményének képe.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="d6dd1-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6dd1-125">-Confirm</span></span>
<span data-ttu-id="d6dd1-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6dd1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6dd1-127">-WhatIf</span></span>
<span data-ttu-id="d6dd1-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6dd1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6dd1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6dd1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dd1-130">CommonParameters</span></span>
<span data-ttu-id="d6dd1-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6dd1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dd1-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6dd1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dd1-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6dd1-133">INPUTS</span></span>

## <span data-ttu-id="d6dd1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6dd1-134">OUTPUTS</span></span>

## <span data-ttu-id="d6dd1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6dd1-135">NOTES</span></span>

## <span data-ttu-id="d6dd1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6dd1-136">RELATED LINKS</span></span>

