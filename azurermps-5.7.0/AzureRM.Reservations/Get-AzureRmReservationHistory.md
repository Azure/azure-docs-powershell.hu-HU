---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500432"
---
# <span data-ttu-id="59969-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="59969-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="59969-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59969-102">SYNOPSIS</span></span>
<span data-ttu-id="59969-103">`Reservation`Korábbi lépések</span><span class="sxs-lookup"><span data-stu-id="59969-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59969-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59969-104">SYNTAX</span></span>

### <span data-ttu-id="59969-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59969-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="59969-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="59969-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="59969-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="59969-107">DESCRIPTION</span></span>
<span data-ttu-id="59969-108">A teljes módosítások listája `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="59969-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="59969-109">Példák</span><span class="sxs-lookup"><span data-stu-id="59969-109">EXAMPLES</span></span>

### <span data-ttu-id="59969-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59969-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="59969-111">Az adott foglalás korábbi verzióinak áttekintése</span><span class="sxs-lookup"><span data-stu-id="59969-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="59969-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59969-112">PARAMETERS</span></span>

### <span data-ttu-id="59969-113">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="59969-113">-Reservation</span></span>
<span data-ttu-id="59969-114">Pipe Object paraméter az `Reservation` s értékhez</span><span class="sxs-lookup"><span data-stu-id="59969-114">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="59969-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="59969-115">-ReservationId</span></span>
<span data-ttu-id="59969-116">A `Reservation` megjelenítendő előzmények ReservationId</span><span class="sxs-lookup"><span data-stu-id="59969-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="59969-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="59969-117">-ReservationOrderId</span></span>
<span data-ttu-id="59969-118">Az a ReservationOrderId, amelyben `ReservationOrder` a `Reservation`</span><span class="sxs-lookup"><span data-stu-id="59969-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="59969-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59969-119">CommonParameters</span></span>
<span data-ttu-id="59969-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59969-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59969-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59969-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59969-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59969-122">INPUTS</span></span>

### <span data-ttu-id="59969-123">System. String</span><span class="sxs-lookup"><span data-stu-id="59969-123">System.String</span></span>
<span data-ttu-id="59969-124">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="59969-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="59969-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59969-125">OUTPUTS</span></span>

### <span data-ttu-id="59969-126">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="59969-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="59969-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59969-127">NOTES</span></span>

## <span data-ttu-id="59969-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59969-128">RELATED LINKS</span></span>

