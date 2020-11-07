---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 3db5c7bf9665498236c3d0dacf05107926ed45eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669479"
---
# <span data-ttu-id="4ee48-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="4ee48-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="4ee48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ee48-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee48-103">Beszerzése `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="4ee48-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="4ee48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ee48-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ee48-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ee48-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee48-106">Azoknak a személyeknek a listája, akikhez `ReservationOrder` a felhasználó hozzáfér a jelenlegi bérlői webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="4ee48-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="4ee48-107">Ha a ReservationOrderId paraméter be van állítva, akkor az adott ReservationOrder kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4ee48-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="4ee48-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4ee48-108">EXAMPLES</span></span>

### <span data-ttu-id="4ee48-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ee48-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="4ee48-110">A `ReservationOrder` jelenlegi bérlői webhelyhez hozzáféréssel rendelkező felhasználók listája</span><span class="sxs-lookup"><span data-stu-id="4ee48-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="4ee48-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="4ee48-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="4ee48-112">`ReservationOrder`A megadott ReservationOrderId beszerzése</span><span class="sxs-lookup"><span data-stu-id="4ee48-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="4ee48-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ee48-113">PARAMETERS</span></span>

### <span data-ttu-id="4ee48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee48-114">-DefaultProfile</span></span>
<span data-ttu-id="4ee48-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ee48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee48-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="4ee48-116">-ReservationOrderId</span></span>
<span data-ttu-id="4ee48-117">A felhasználó által megtekinteni kívánt konkrét ReservationOrder azonosítója</span><span class="sxs-lookup"><span data-stu-id="4ee48-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee48-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee48-118">CommonParameters</span></span>
<span data-ttu-id="4ee48-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ee48-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee48-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee48-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee48-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ee48-121">INPUTS</span></span>

### <span data-ttu-id="4ee48-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="4ee48-122">None</span></span>

## <span data-ttu-id="4ee48-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ee48-123">OUTPUTS</span></span>

### <span data-ttu-id="4ee48-124">Microsoft. Azure. commands. Reservations. models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="4ee48-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="4ee48-125">Microsoft. Azure. commands. Reservations. models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="4ee48-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="4ee48-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ee48-126">NOTES</span></span>

## <span data-ttu-id="4ee48-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ee48-127">RELATED LINKS</span></span>
