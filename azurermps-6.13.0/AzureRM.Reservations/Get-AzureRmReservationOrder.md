---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493968"
---
# <span data-ttu-id="f9492-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f9492-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="f9492-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9492-102">SYNOPSIS</span></span>
<span data-ttu-id="f9492-103">Beszerzése `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="f9492-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9492-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9492-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9492-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9492-105">DESCRIPTION</span></span>
<span data-ttu-id="f9492-106">Azoknak a személyeknek a listája, akikhez `ReservationOrder` a felhasználó hozzáfér a jelenlegi bérlői webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="f9492-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="f9492-107">Ha a ReservationOrderId paraméter be van állítva, akkor az adott ReservationOrder kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f9492-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="f9492-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f9492-108">EXAMPLES</span></span>

### <span data-ttu-id="f9492-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f9492-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="f9492-110">A `ReservationOrder` jelenlegi bérlői webhelyhez hozzáféréssel rendelkező felhasználók listája</span><span class="sxs-lookup"><span data-stu-id="f9492-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="f9492-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="f9492-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="f9492-112">`ReservationOrder`A megadott ReservationOrderId beszerzése</span><span class="sxs-lookup"><span data-stu-id="f9492-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="f9492-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9492-113">PARAMETERS</span></span>

### <span data-ttu-id="f9492-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9492-114">-DefaultProfile</span></span>
<span data-ttu-id="f9492-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9492-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9492-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f9492-116">-ReservationOrderId</span></span>
<span data-ttu-id="f9492-117">A felhasználó által megtekinteni kívánt konkrét ReservationOrder azonosítója</span><span class="sxs-lookup"><span data-stu-id="f9492-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="f9492-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9492-118">CommonParameters</span></span>
<span data-ttu-id="f9492-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9492-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9492-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9492-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9492-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9492-121">INPUTS</span></span>

### <span data-ttu-id="f9492-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="f9492-122">None</span></span>

## <span data-ttu-id="f9492-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9492-123">OUTPUTS</span></span>

### <span data-ttu-id="f9492-124">Microsoft. Azure. commands. Reservations. models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="f9492-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="f9492-125">Microsoft. Azure. commands. Reservations. models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="f9492-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="f9492-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9492-126">NOTES</span></span>

## <span data-ttu-id="f9492-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9492-127">RELATED LINKS</span></span>
