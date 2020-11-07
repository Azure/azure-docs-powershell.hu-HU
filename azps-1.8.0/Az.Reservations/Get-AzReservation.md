---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: d7eab73fbe6bed4a51df7c5056a0dc52787de845
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669486"
---
# <span data-ttu-id="17a6f-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="17a6f-101">Get-AzReservation</span></span>

## <span data-ttu-id="17a6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="17a6f-103">Az s beszerzése `Reservation` adott foglalási sorrendben</span><span class="sxs-lookup"><span data-stu-id="17a6f-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="17a6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17a6f-104">SYNTAX</span></span>

### <span data-ttu-id="17a6f-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17a6f-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17a6f-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="17a6f-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17a6f-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="17a6f-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17a6f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="17a6f-108">DESCRIPTION</span></span>
<span data-ttu-id="17a6f-109">`Reservation`Az s betű egyetlenen belül `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="17a6f-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="17a6f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="17a6f-110">EXAMPLES</span></span>

### <span data-ttu-id="17a6f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="17a6f-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="17a6f-112">`Reservation`A megadott listában lévő EK `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="17a6f-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="17a6f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="17a6f-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="17a6f-114">Konkrét `Reservation` részleteket kaphat.</span><span class="sxs-lookup"><span data-stu-id="17a6f-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="17a6f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17a6f-115">PARAMETERS</span></span>

### <span data-ttu-id="17a6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a6f-116">-DefaultProfile</span></span>
<span data-ttu-id="17a6f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17a6f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17a6f-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="17a6f-118">-ReservationId</span></span>
<span data-ttu-id="17a6f-119">A `Reservation` megtekinteni kívánt azonosító</span><span class="sxs-lookup"><span data-stu-id="17a6f-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="17a6f-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="17a6f-120">-ReservationOrder</span></span>
<span data-ttu-id="17a6f-121">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="17a6f-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="17a6f-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="17a6f-122">-ReservationOrderId</span></span>
<span data-ttu-id="17a6f-123">Az adott azonosítójú azonosítót `ReservationOrder` tartalmazó azonosító `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="17a6f-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="17a6f-124">Szükséges.</span><span class="sxs-lookup"><span data-stu-id="17a6f-124">Required.</span></span>

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

### <span data-ttu-id="17a6f-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="17a6f-125">-ReservationOrderPage</span></span>
<span data-ttu-id="17a6f-126">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="17a6f-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="17a6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a6f-127">CommonParameters</span></span>
<span data-ttu-id="17a6f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17a6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a6f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17a6f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a6f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17a6f-130">INPUTS</span></span>

### <span data-ttu-id="17a6f-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="17a6f-131">System.Guid</span></span>

### <span data-ttu-id="17a6f-132">Microsoft. Azure. commands. Reservations. models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="17a6f-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="17a6f-133">Microsoft. Azure. commands. Reservations. models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="17a6f-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="17a6f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17a6f-134">OUTPUTS</span></span>

### <span data-ttu-id="17a6f-135">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="17a6f-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="17a6f-136">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="17a6f-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="17a6f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17a6f-137">NOTES</span></span>

## <span data-ttu-id="17a6f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17a6f-138">RELATED LINKS</span></span>
