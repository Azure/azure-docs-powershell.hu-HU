---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505731"
---
# <span data-ttu-id="d0b13-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="d0b13-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="d0b13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0b13-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b13-103">`Reservation`Korábbi lépések</span><span class="sxs-lookup"><span data-stu-id="d0b13-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0b13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0b13-104">SYNTAX</span></span>

### <span data-ttu-id="d0b13-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0b13-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0b13-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d0b13-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0b13-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0b13-107">DESCRIPTION</span></span>
<span data-ttu-id="d0b13-108">A teljes módosítások listája `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d0b13-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="d0b13-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d0b13-109">EXAMPLES</span></span>

### <span data-ttu-id="d0b13-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0b13-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="d0b13-111">Az adott foglalás korábbi verzióinak áttekintése</span><span class="sxs-lookup"><span data-stu-id="d0b13-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="d0b13-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0b13-112">PARAMETERS</span></span>

### <span data-ttu-id="d0b13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b13-113">-DefaultProfile</span></span>
<span data-ttu-id="d0b13-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0b13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b13-115">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="d0b13-115">-Reservation</span></span>
<span data-ttu-id="d0b13-116">Pipe Object paraméter az `Reservation` s értékhez</span><span class="sxs-lookup"><span data-stu-id="d0b13-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="d0b13-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d0b13-117">-ReservationId</span></span>
<span data-ttu-id="d0b13-118">A `Reservation` megjelenítendő előzmények ReservationId</span><span class="sxs-lookup"><span data-stu-id="d0b13-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="d0b13-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d0b13-119">-ReservationOrderId</span></span>
<span data-ttu-id="d0b13-120">Az a ReservationOrderId, amelyben `ReservationOrder` a `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d0b13-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="d0b13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b13-121">CommonParameters</span></span>
<span data-ttu-id="d0b13-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0b13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b13-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b13-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b13-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0b13-124">INPUTS</span></span>

### <span data-ttu-id="d0b13-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d0b13-125">System.Guid</span></span>

### <span data-ttu-id="d0b13-126">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d0b13-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="d0b13-127">Paraméterek: foglalás (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0b13-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="d0b13-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0b13-128">OUTPUTS</span></span>

### <span data-ttu-id="d0b13-129">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="d0b13-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="d0b13-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0b13-130">NOTES</span></span>

## <span data-ttu-id="d0b13-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0b13-131">RELATED LINKS</span></span>
