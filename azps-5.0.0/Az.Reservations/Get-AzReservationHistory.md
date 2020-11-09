---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300227"
---
# <span data-ttu-id="2b6a1-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="2b6a1-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="2b6a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6a1-103">`Reservation`Korábbi lépések</span><span class="sxs-lookup"><span data-stu-id="2b6a1-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="2b6a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b6a1-104">SYNTAX</span></span>

### <span data-ttu-id="2b6a1-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b6a1-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b6a1-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="2b6a1-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b6a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b6a1-107">DESCRIPTION</span></span>
<span data-ttu-id="2b6a1-108">A teljes módosítások listája `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="2b6a1-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="2b6a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2b6a1-109">EXAMPLES</span></span>

### <span data-ttu-id="2b6a1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2b6a1-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="2b6a1-111">Az adott foglalás korábbi verzióinak áttekintése</span><span class="sxs-lookup"><span data-stu-id="2b6a1-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="2b6a1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b6a1-112">PARAMETERS</span></span>

### <span data-ttu-id="2b6a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6a1-113">-DefaultProfile</span></span>
<span data-ttu-id="2b6a1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b6a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b6a1-115">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="2b6a1-115">-Reservation</span></span>
<span data-ttu-id="2b6a1-116">Pipe Object paraméter az `Reservation` s értékhez</span><span class="sxs-lookup"><span data-stu-id="2b6a1-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="2b6a1-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="2b6a1-117">-ReservationId</span></span>
<span data-ttu-id="2b6a1-118">A `Reservation` megjelenítendő előzmények ReservationId</span><span class="sxs-lookup"><span data-stu-id="2b6a1-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="2b6a1-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2b6a1-119">-ReservationOrderId</span></span>
<span data-ttu-id="2b6a1-120">Az a ReservationOrderId, amelyben `ReservationOrder` a `Reservation`</span><span class="sxs-lookup"><span data-stu-id="2b6a1-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="2b6a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6a1-121">CommonParameters</span></span>
<span data-ttu-id="2b6a1-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b6a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6a1-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2b6a1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6a1-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b6a1-124">INPUTS</span></span>

### <span data-ttu-id="2b6a1-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2b6a1-125">System.Guid</span></span>

### <span data-ttu-id="2b6a1-126">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="2b6a1-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="2b6a1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b6a1-127">OUTPUTS</span></span>

### <span data-ttu-id="2b6a1-128">Microsoft. Azure. commands. Reservations. models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="2b6a1-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="2b6a1-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b6a1-129">NOTES</span></span>

## <span data-ttu-id="2b6a1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b6a1-130">RELATED LINKS</span></span>
