---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492200"
---
# <span data-ttu-id="c3112-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="c3112-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="c3112-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3112-102">SYNOPSIS</span></span>
<span data-ttu-id="c3112-103">Az s beszerzése `Reservation` adott foglalási sorrendben</span><span class="sxs-lookup"><span data-stu-id="c3112-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3112-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3112-104">SYNTAX</span></span>

### <span data-ttu-id="c3112-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3112-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="c3112-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="c3112-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="c3112-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3112-107">DESCRIPTION</span></span>
<span data-ttu-id="c3112-108">`Reservation`Az s betű egyetlenen belül `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="c3112-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="c3112-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c3112-109">EXAMPLES</span></span>

### <span data-ttu-id="c3112-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3112-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="c3112-111">`Reservation`A megadott listában lévő EK `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="c3112-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="c3112-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3112-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="c3112-113">Konkrét `Reservation` részleteket kaphat.</span><span class="sxs-lookup"><span data-stu-id="c3112-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="c3112-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3112-114">PARAMETERS</span></span>

### <span data-ttu-id="c3112-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c3112-115">-ReservationId</span></span>
<span data-ttu-id="c3112-116">A `Reservation` megtekinteni kívánt azonosító</span><span class="sxs-lookup"><span data-stu-id="c3112-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3112-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="c3112-117">-ReservationOrder</span></span>
<span data-ttu-id="c3112-118">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="c3112-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3112-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c3112-119">-ReservationOrderId</span></span>
<span data-ttu-id="c3112-120">Az adott azonosítójú azonosítót `ReservationOrder` tartalmazó azonosító `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c3112-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="c3112-121">Szükséges.</span><span class="sxs-lookup"><span data-stu-id="c3112-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3112-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="c3112-122">-ReservationOrderPage</span></span>
<span data-ttu-id="c3112-123">Pipe Object paraméter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="c3112-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3112-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3112-124">CommonParameters</span></span>
<span data-ttu-id="c3112-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3112-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3112-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3112-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3112-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3112-127">INPUTS</span></span>

### <span data-ttu-id="c3112-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c3112-128">System.String</span></span>
<span data-ttu-id="c3112-129">Microsoft. Azure. commands. Reservations. models. PSReservationOrder Microsoft. Azure. commands. Reservations. models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="c3112-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="c3112-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3112-130">OUTPUTS</span></span>

### <span data-ttu-id="c3112-131">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="c3112-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="c3112-132">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c3112-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c3112-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3112-133">NOTES</span></span>

## <span data-ttu-id="c3112-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3112-134">RELATED LINKS</span></span>

