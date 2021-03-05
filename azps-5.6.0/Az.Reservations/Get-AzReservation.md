---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 427e715e055cd909d204f92aedd58eca9d7db0f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000310"
---
# <span data-ttu-id="09024-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="09024-101">Get-AzReservation</span></span>

## <span data-ttu-id="09024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09024-102">SYNOPSIS</span></span>
<span data-ttu-id="09024-103">Get `Reservation` s in a given reservation Order</span><span class="sxs-lookup"><span data-stu-id="09024-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="09024-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09024-104">SYNTAX</span></span>

### <span data-ttu-id="09024-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09024-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09024-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="09024-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09024-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="09024-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09024-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09024-108">DESCRIPTION</span></span>
<span data-ttu-id="09024-109">Egyetlen `Reservation` listán belüli `ReservationOrder` lista.</span><span class="sxs-lookup"><span data-stu-id="09024-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="09024-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09024-110">EXAMPLES</span></span>

### <span data-ttu-id="09024-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="09024-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="09024-112">A `Reservation` megadott listán belüli "s" `ReservationOrder` lista.</span><span class="sxs-lookup"><span data-stu-id="09024-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="09024-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="09024-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="09024-114">Konkrét `Reservation` részleteket olvashat.</span><span class="sxs-lookup"><span data-stu-id="09024-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="09024-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09024-115">PARAMETERS</span></span>

### <span data-ttu-id="09024-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09024-116">-DefaultProfile</span></span>
<span data-ttu-id="09024-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09024-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09024-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="09024-118">-ReservationId</span></span>
<span data-ttu-id="09024-119">Annak az azonosítónak `Reservation` az azonosítója, amit meg kell nézni</span><span class="sxs-lookup"><span data-stu-id="09024-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09024-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="09024-120">-ReservationOrder</span></span>
<span data-ttu-id="09024-121">Pipe object parameter for `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="09024-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09024-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="09024-122">-ReservationOrderId</span></span>
<span data-ttu-id="09024-123">A . `ReservationOrder` `Reservation`</span><span class="sxs-lookup"><span data-stu-id="09024-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="09024-124">Kötelező.</span><span class="sxs-lookup"><span data-stu-id="09024-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09024-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="09024-125">-ReservationOrderPage</span></span>
<span data-ttu-id="09024-126">Pipe object parameter for `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="09024-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09024-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09024-127">CommonParameters</span></span>
<span data-ttu-id="09024-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09024-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09024-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09024-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09024-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09024-130">INPUTS</span></span>

### <span data-ttu-id="09024-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="09024-131">System.Guid</span></span>

### <span data-ttu-id="09024-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="09024-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="09024-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="09024-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="09024-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09024-134">OUTPUTS</span></span>

### <span data-ttu-id="09024-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="09024-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="09024-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="09024-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="09024-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09024-137">NOTES</span></span>

## <span data-ttu-id="09024-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09024-138">RELATED LINKS</span></span>
