---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325818"
---
# <span data-ttu-id="faa01-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="faa01-101">Split-AzReservation</span></span>

## <span data-ttu-id="faa01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faa01-102">SYNOPSIS</span></span>
<span data-ttu-id="faa01-103">Split a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="faa01-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="faa01-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="faa01-104">SYNTAX</span></span>

### <span data-ttu-id="faa01-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="faa01-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa01-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="faa01-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faa01-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="faa01-107">DESCRIPTION</span></span>
<span data-ttu-id="faa01-108">Az a `Reservation` érték `Reservation` felosztása két s-re a megadott mennyiségeloszlással.</span><span class="sxs-lookup"><span data-stu-id="faa01-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="faa01-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="faa01-109">EXAMPLES</span></span>

### <span data-ttu-id="faa01-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="faa01-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="faa01-111">A megadott érték felosztása `Reservation` `Reservation` két s-re a megfelelő mennyiségekkel</span><span class="sxs-lookup"><span data-stu-id="faa01-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="faa01-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faa01-112">PARAMETERS</span></span>

### <span data-ttu-id="faa01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa01-113">-DefaultProfile</span></span>
<span data-ttu-id="faa01-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="faa01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa01-115">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="faa01-115">-Quantity</span></span>
<span data-ttu-id="faa01-116">A két szám mennyiségmezője vesszővel elválasztott `Reservation` egész számokkal</span><span class="sxs-lookup"><span data-stu-id="faa01-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="faa01-117">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="faa01-117">-Reservation</span></span>
<span data-ttu-id="faa01-118">Pipe object parameter for `Reservation`</span><span class="sxs-lookup"><span data-stu-id="faa01-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="faa01-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="faa01-119">-ReservationId</span></span>
<span data-ttu-id="faa01-120">A `Reservation` felosztani következő azonosítója</span><span class="sxs-lookup"><span data-stu-id="faa01-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="faa01-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="faa01-121">-ReservationOrderId</span></span>
<span data-ttu-id="faa01-122">Annak az `ReservationOrder` azonosítónak az azonosítója, amely a `Reservation` felosztani kívánt felhasználót tartalmazza</span><span class="sxs-lookup"><span data-stu-id="faa01-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="faa01-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faa01-123">-Confirm</span></span>
<span data-ttu-id="faa01-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="faa01-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa01-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa01-125">-WhatIf</span></span>
<span data-ttu-id="faa01-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="faa01-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faa01-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="faa01-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa01-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa01-128">CommonParameters</span></span>
<span data-ttu-id="faa01-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa01-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa01-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faa01-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa01-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="faa01-131">INPUTS</span></span>

### <span data-ttu-id="faa01-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="faa01-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="faa01-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="faa01-133">OUTPUTS</span></span>

### <span data-ttu-id="faa01-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="faa01-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="faa01-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="faa01-135">NOTES</span></span>

## <span data-ttu-id="faa01-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="faa01-136">RELATED LINKS</span></span>
