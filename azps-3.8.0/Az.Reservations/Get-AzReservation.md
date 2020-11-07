---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846818"
---
# <span data-ttu-id="e1740-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="e1740-101">Get-AzReservation</span></span>

## <span data-ttu-id="e1740-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1740-102">SYNOPSIS</span></span>
<span data-ttu-id="e1740-103">Az s beszerzése `Reservation` adott foglalási sorrendben</span><span class="sxs-lookup"><span data-stu-id="e1740-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="e1740-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1740-104">SYNTAX</span></span>

### <span data-ttu-id="e1740-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1740-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1740-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e1740-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1740-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="e1740-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1740-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1740-108">DESCRIPTION</span></span>
<span data-ttu-id="e1740-109">`Reservation`Az s betű egyetlenen belül `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e1740-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="e1740-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e1740-110">EXAMPLES</span></span>

### <span data-ttu-id="e1740-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1740-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e1740-112">`Reservation`A megadott listában lévő EK `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e1740-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="e1740-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1740-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="e1740-114">Konkrét `Reservation` részleteket kaphat.</span><span class="sxs-lookup"><span data-stu-id="e1740-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="e1740-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1740-115">PARAMETERS</span></span>

### <span data-ttu-id="e1740-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1740-116">-DefaultProfile</span></span>
<span data-ttu-id="e1740-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1740-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1740-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="e1740-118">-ReservationId</span></span>
<span data-ttu-id="e1740-119">A `Reservation` megtekinteni kívánt azonosító</span><span class="sxs-lookup"><span data-stu-id="e1740-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="e1740-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="e1740-120">-ReservationOrder</span></span>
<span data-ttu-id="e1740-121">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e1740-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="e1740-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e1740-122">-ReservationOrderId</span></span>
<span data-ttu-id="e1740-123">Az adott azonosítójú azonosítót `ReservationOrder` tartalmazó azonosító `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e1740-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="e1740-124">Szükséges.</span><span class="sxs-lookup"><span data-stu-id="e1740-124">Required.</span></span>

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

### <span data-ttu-id="e1740-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="e1740-125">-ReservationOrderPage</span></span>
<span data-ttu-id="e1740-126">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e1740-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="e1740-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1740-127">CommonParameters</span></span>
<span data-ttu-id="e1740-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1740-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1740-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1740-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1740-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1740-130">INPUTS</span></span>

### <span data-ttu-id="e1740-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e1740-131">System.Guid</span></span>

### <span data-ttu-id="e1740-132">Microsoft. Azure. commands. Reservations. models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="e1740-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="e1740-133">Microsoft. Azure. commands. Reservations. models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="e1740-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="e1740-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1740-134">OUTPUTS</span></span>

### <span data-ttu-id="e1740-135">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="e1740-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="e1740-136">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="e1740-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e1740-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1740-137">NOTES</span></span>

## <span data-ttu-id="e1740-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1740-138">RELATED LINKS</span></span>
