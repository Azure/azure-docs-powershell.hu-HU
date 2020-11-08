---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018064"
---
# <span data-ttu-id="8b117-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="8b117-101">Split-AzReservation</span></span>

## <span data-ttu-id="8b117-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b117-102">SYNOPSIS</span></span>
<span data-ttu-id="8b117-103">A (Split `Reservation` )</span><span class="sxs-lookup"><span data-stu-id="8b117-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="8b117-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b117-104">SYNTAX</span></span>

### <span data-ttu-id="8b117-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b117-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b117-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="8b117-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b117-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b117-107">DESCRIPTION</span></span>
<span data-ttu-id="8b117-108">Az a-tól két s-ig osztotta a `Reservation` `Reservation` megadott mennyiség eloszlását.</span><span class="sxs-lookup"><span data-stu-id="8b117-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="8b117-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8b117-109">EXAMPLES</span></span>

### <span data-ttu-id="8b117-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8b117-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="8b117-111">A megadott mennyiséget két s-ra felosztja `Reservation` `Reservation` a megfelelő mennyiséggel.</span><span class="sxs-lookup"><span data-stu-id="8b117-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="8b117-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b117-112">PARAMETERS</span></span>

### <span data-ttu-id="8b117-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b117-113">-DefaultProfile</span></span>
<span data-ttu-id="8b117-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b117-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b117-115">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="8b117-115">-Quantity</span></span>
<span data-ttu-id="8b117-116">Vesszővel elválasztott egész számok a két s mennyiség mezőhöz `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8b117-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b117-117">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="8b117-117">-Reservation</span></span>
<span data-ttu-id="8b117-118">Pipe Object paraméter `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8b117-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b117-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8b117-119">-ReservationId</span></span>
<span data-ttu-id="8b117-120">A `Reservation` felosztott azonosító azonosítója</span><span class="sxs-lookup"><span data-stu-id="8b117-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b117-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8b117-121">-ReservationOrderId</span></span>
<span data-ttu-id="8b117-122">Annak az azonosítójának a megadására szolgáló azonosítója, amelyet `ReservationOrder` a `Reservation` felhasználó szeretne megosztani</span><span class="sxs-lookup"><span data-stu-id="8b117-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b117-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8b117-123">-Confirm</span></span>
<span data-ttu-id="8b117-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8b117-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b117-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b117-125">-WhatIf</span></span>
<span data-ttu-id="8b117-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8b117-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b117-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8b117-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b117-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b117-128">CommonParameters</span></span>
<span data-ttu-id="8b117-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b117-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b117-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8b117-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b117-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b117-131">INPUTS</span></span>

### <span data-ttu-id="8b117-132">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="8b117-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8b117-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b117-133">OUTPUTS</span></span>

### <span data-ttu-id="8b117-134">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="8b117-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8b117-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b117-135">NOTES</span></span>

## <span data-ttu-id="8b117-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b117-136">RELATED LINKS</span></span>
