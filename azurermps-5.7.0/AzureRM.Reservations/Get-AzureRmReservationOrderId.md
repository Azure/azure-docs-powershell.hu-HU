---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495273"
---
# <span data-ttu-id="defd7-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="defd7-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="defd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="defd7-102">SYNOPSIS</span></span>
<span data-ttu-id="defd7-103">A megfelelő azonosítók listájának beszerzése `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="defd7-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="defd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="defd7-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="defd7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="defd7-105">DESCRIPTION</span></span>
<span data-ttu-id="defd7-106">Az adott `ReservationOrder` előfizetésre alkalmazható e-s azonosítók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="defd7-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="defd7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="defd7-107">EXAMPLES</span></span>

### <span data-ttu-id="defd7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="defd7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="defd7-109">`ReservationOrder`Az alapértelmezett előfizetés alkalmazása</span><span class="sxs-lookup"><span data-stu-id="defd7-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="defd7-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="defd7-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="defd7-111">`ReservationOrder`A megadott előfizetés alkalmazása</span><span class="sxs-lookup"><span data-stu-id="defd7-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="defd7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="defd7-112">PARAMETERS</span></span>

### <span data-ttu-id="defd7-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="defd7-113">-SubscriptionId</span></span>
<span data-ttu-id="defd7-114">Az előfizetés azonosítója az alkalmazott s érték beszerzéséhez `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="defd7-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="defd7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defd7-115">CommonParameters</span></span>
<span data-ttu-id="defd7-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="defd7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defd7-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="defd7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defd7-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="defd7-118">INPUTS</span></span>

### <span data-ttu-id="defd7-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="defd7-119">None</span></span>

## <span data-ttu-id="defd7-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="defd7-120">OUTPUTS</span></span>

### <span data-ttu-id="defd7-121">Microsoft. Azure. commands. Reservations. models. PSAppliedReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="defd7-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="defd7-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="defd7-122">NOTES</span></span>

## <span data-ttu-id="defd7-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="defd7-123">RELATED LINKS</span></span>

