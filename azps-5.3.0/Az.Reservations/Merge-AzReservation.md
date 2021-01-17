---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377969"
---
# <span data-ttu-id="bce11-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="bce11-101">Merge-AzReservation</span></span>

## <span data-ttu-id="bce11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce11-102">SYNOPSIS</span></span>
<span data-ttu-id="bce11-103">Két s `Reservation` egyesítése.</span><span class="sxs-lookup"><span data-stu-id="bce11-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="bce11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bce11-104">SYNTAX</span></span>

### <span data-ttu-id="bce11-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bce11-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce11-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="bce11-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce11-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bce11-107">DESCRIPTION</span></span>
<span data-ttu-id="bce11-108">A megadott `Reservation` értékeket egyesítheti egy új. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="bce11-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="bce11-109">Az egyesítés alatt lévő két fájlnak `Reservation` azonos tulajdonságokkal kell bírnie.</span><span class="sxs-lookup"><span data-stu-id="bce11-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="bce11-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bce11-110">EXAMPLES</span></span>

### <span data-ttu-id="bce11-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bce11-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="bce11-112">A megadott két érték `Reservation` egyesítése egybe `Reservation`</span><span class="sxs-lookup"><span data-stu-id="bce11-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="bce11-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bce11-113">PARAMETERS</span></span>

### <span data-ttu-id="bce11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce11-114">-DefaultProfile</span></span>
<span data-ttu-id="bce11-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bce11-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce11-116">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="bce11-116">-Reservation</span></span>
<span data-ttu-id="bce11-117">Vesszővel elválasztott karakterláncok két egyesítendő Foglalásazonosítóból</span><span class="sxs-lookup"><span data-stu-id="bce11-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce11-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="bce11-118">-ReservationId</span></span>
<span data-ttu-id="bce11-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="bce11-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce11-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="bce11-120">-ReservationOrderId</span></span>
<span data-ttu-id="bce11-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="bce11-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="bce11-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bce11-122">-Confirm</span></span>
<span data-ttu-id="bce11-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bce11-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce11-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce11-124">-WhatIf</span></span>
<span data-ttu-id="bce11-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bce11-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bce11-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bce11-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce11-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce11-127">CommonParameters</span></span>
<span data-ttu-id="bce11-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce11-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce11-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bce11-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce11-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bce11-130">INPUTS</span></span>

### <span data-ttu-id="bce11-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="bce11-131">None</span></span>

## <span data-ttu-id="bce11-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce11-132">OUTPUTS</span></span>

### <span data-ttu-id="bce11-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="bce11-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="bce11-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bce11-134">NOTES</span></span>

## <span data-ttu-id="bce11-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bce11-135">RELATED LINKS</span></span>
