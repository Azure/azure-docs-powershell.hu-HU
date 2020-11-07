---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cf68c40a13247d1101f6d25abac92f01ae1a0053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669481"
---
# <span data-ttu-id="c0b6c-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="c0b6c-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="c0b6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b6c-103">`Reservation`Korábbi lépések</span><span class="sxs-lookup"><span data-stu-id="c0b6c-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="c0b6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0b6c-104">SYNTAX</span></span>

### <span data-ttu-id="c0b6c-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0b6c-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0b6c-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="c0b6c-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0b6c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="c0b6c-108">A teljes módosítások listája `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c0b6c-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="c0b6c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c0b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="c0b6c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0b6c-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="c0b6c-111">Az adott foglalás korábbi verzióinak áttekintése</span><span class="sxs-lookup"><span data-stu-id="c0b6c-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="c0b6c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0b6c-112">PARAMETERS</span></span>

### <span data-ttu-id="c0b6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b6c-113">-DefaultProfile</span></span>
<span data-ttu-id="c0b6c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0b6c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b6c-115">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="c0b6c-115">-Reservation</span></span>
<span data-ttu-id="c0b6c-116">Pipe Object paraméter az `Reservation` s értékhez</span><span class="sxs-lookup"><span data-stu-id="c0b6c-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="c0b6c-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c0b6c-117">-ReservationId</span></span>
<span data-ttu-id="c0b6c-118">A `Reservation` megjelenítendő előzmények ReservationId</span><span class="sxs-lookup"><span data-stu-id="c0b6c-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="c0b6c-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c0b6c-119">-ReservationOrderId</span></span>
<span data-ttu-id="c0b6c-120">Az a ReservationOrderId, amelyben `ReservationOrder` a `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c0b6c-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="c0b6c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b6c-121">CommonParameters</span></span>
<span data-ttu-id="c0b6c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0b6c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b6c-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0b6c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b6c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0b6c-124">INPUTS</span></span>

### <span data-ttu-id="c0b6c-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c0b6c-125">System.Guid</span></span>

### <span data-ttu-id="c0b6c-126">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c0b6c-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c0b6c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0b6c-127">OUTPUTS</span></span>

### <span data-ttu-id="c0b6c-128">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="c0b6c-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="c0b6c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0b6c-129">NOTES</span></span>

## <span data-ttu-id="c0b6c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0b6c-130">RELATED LINKS</span></span>
