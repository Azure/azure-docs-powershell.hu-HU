---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492756"
---
# <span data-ttu-id="8934a-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="8934a-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="8934a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8934a-102">SYNOPSIS</span></span>
<span data-ttu-id="8934a-103">Az s beszerzése `Reservation` adott foglalási sorrendben</span><span class="sxs-lookup"><span data-stu-id="8934a-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8934a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8934a-104">SYNTAX</span></span>

### <span data-ttu-id="8934a-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8934a-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8934a-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="8934a-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8934a-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="8934a-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8934a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8934a-108">DESCRIPTION</span></span>
<span data-ttu-id="8934a-109">`Reservation`Az s betű egyetlenen belül `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8934a-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="8934a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8934a-110">EXAMPLES</span></span>

### <span data-ttu-id="8934a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8934a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="8934a-112">`Reservation`A megadott listában lévő EK `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8934a-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="8934a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8934a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="8934a-114">Konkrét `Reservation` részleteket kaphat.</span><span class="sxs-lookup"><span data-stu-id="8934a-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="8934a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8934a-115">PARAMETERS</span></span>

### <span data-ttu-id="8934a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8934a-116">-DefaultProfile</span></span>
<span data-ttu-id="8934a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8934a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8934a-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8934a-118">-ReservationId</span></span>
<span data-ttu-id="8934a-119">A `Reservation` megtekinteni kívánt azonosító</span><span class="sxs-lookup"><span data-stu-id="8934a-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="8934a-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="8934a-120">-ReservationOrder</span></span>
<span data-ttu-id="8934a-121">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8934a-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="8934a-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8934a-122">-ReservationOrderId</span></span>
<span data-ttu-id="8934a-123">Az adott azonosítójú azonosítót `ReservationOrder` tartalmazó azonosító `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="8934a-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="8934a-124">Szükséges.</span><span class="sxs-lookup"><span data-stu-id="8934a-124">Required.</span></span>

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

### <span data-ttu-id="8934a-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="8934a-125">-ReservationOrderPage</span></span>
<span data-ttu-id="8934a-126">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8934a-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="8934a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8934a-127">CommonParameters</span></span>
<span data-ttu-id="8934a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8934a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8934a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8934a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8934a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8934a-130">INPUTS</span></span>

### <span data-ttu-id="8934a-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8934a-131">System.Guid</span></span>

### <span data-ttu-id="8934a-132">Microsoft. Azure. commands. Reservations. models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="8934a-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="8934a-133">Paraméterek: ReservationOrder (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8934a-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="8934a-134">Microsoft. Azure. commands. Reservations. models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="8934a-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="8934a-135">Paraméterek: ReservationOrderPage (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8934a-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="8934a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8934a-136">OUTPUTS</span></span>

### <span data-ttu-id="8934a-137">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="8934a-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="8934a-138">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="8934a-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8934a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8934a-139">NOTES</span></span>

## <span data-ttu-id="8934a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8934a-140">RELATED LINKS</span></span>
