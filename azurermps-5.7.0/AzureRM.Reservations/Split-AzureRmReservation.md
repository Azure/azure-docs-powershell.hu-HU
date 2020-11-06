---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495275"
---
# <span data-ttu-id="797bf-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="797bf-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="797bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="797bf-102">SYNOPSIS</span></span>
<span data-ttu-id="797bf-103">A (Split `Reservation` )</span><span class="sxs-lookup"><span data-stu-id="797bf-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="797bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="797bf-104">SYNTAX</span></span>

### <span data-ttu-id="797bf-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="797bf-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797bf-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="797bf-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="797bf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="797bf-107">DESCRIPTION</span></span>
<span data-ttu-id="797bf-108">Az a-tól két s-ig osztotta a `Reservation` `Reservation` megadott mennyiség eloszlását.</span><span class="sxs-lookup"><span data-stu-id="797bf-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="797bf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="797bf-109">EXAMPLES</span></span>

### <span data-ttu-id="797bf-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="797bf-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="797bf-111">A megadott mennyiséget két s-ra felosztja `Reservation` `Reservation` a megfelelő mennyiséggel.</span><span class="sxs-lookup"><span data-stu-id="797bf-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="797bf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="797bf-112">PARAMETERS</span></span>

### <span data-ttu-id="797bf-113">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="797bf-113">-Quantity</span></span>
<span data-ttu-id="797bf-114">Vesszővel elválasztott egész számok a két s mennyiség mezőhöz `Reservation`</span><span class="sxs-lookup"><span data-stu-id="797bf-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797bf-115">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="797bf-115">-Reservation</span></span>
<span data-ttu-id="797bf-116">Pipe Object paraméter `Reservation`</span><span class="sxs-lookup"><span data-stu-id="797bf-116">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="797bf-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="797bf-117">-ReservationId</span></span>
<span data-ttu-id="797bf-118">A `Reservation` felosztott azonosító azonosítója</span><span class="sxs-lookup"><span data-stu-id="797bf-118">Id of the `Reservation` to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797bf-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="797bf-119">-ReservationOrderId</span></span>
<span data-ttu-id="797bf-120">Annak az azonosítójának a megadására szolgáló azonosítója, amelyet `ReservationOrder` a `Reservation` felhasználó szeretne megosztani</span><span class="sxs-lookup"><span data-stu-id="797bf-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797bf-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="797bf-121">-Confirm</span></span>
<span data-ttu-id="797bf-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="797bf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="797bf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="797bf-123">-WhatIf</span></span>
<span data-ttu-id="797bf-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="797bf-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="797bf-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="797bf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="797bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797bf-126">CommonParameters</span></span>
<span data-ttu-id="797bf-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="797bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797bf-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="797bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797bf-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="797bf-129">INPUTS</span></span>

### <span data-ttu-id="797bf-130">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="797bf-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="797bf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="797bf-131">OUTPUTS</span></span>

### <span data-ttu-id="797bf-132">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Reservations. models. PSReservation, Microsoft. Azure. commands. Reservations, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="797bf-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="797bf-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="797bf-133">NOTES</span></span>

## <span data-ttu-id="797bf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="797bf-134">RELATED LINKS</span></span>

