---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669472"
---
# <span data-ttu-id="502c2-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="502c2-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="502c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="502c2-102">SYNOPSIS</span></span>
<span data-ttu-id="502c2-103">A megfelelő azonosítók listájának beszerzése `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="502c2-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="502c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="502c2-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="502c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="502c2-105">DESCRIPTION</span></span>
<span data-ttu-id="502c2-106">Az adott `ReservationOrder` előfizetésre alkalmazható e-s azonosítók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="502c2-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="502c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="502c2-107">EXAMPLES</span></span>

### <span data-ttu-id="502c2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="502c2-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="502c2-109">`ReservationOrder`Az alapértelmezett előfizetés alkalmazása</span><span class="sxs-lookup"><span data-stu-id="502c2-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="502c2-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="502c2-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="502c2-111">`ReservationOrder`A megadott előfizetés alkalmazása</span><span class="sxs-lookup"><span data-stu-id="502c2-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="502c2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="502c2-112">PARAMETERS</span></span>

### <span data-ttu-id="502c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502c2-113">-DefaultProfile</span></span>
<span data-ttu-id="502c2-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="502c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="502c2-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="502c2-115">-SubscriptionId</span></span>
<span data-ttu-id="502c2-116">Az előfizetés azonosítója az alkalmazott s érték beszerzéséhez `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="502c2-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="502c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502c2-117">CommonParameters</span></span>
<span data-ttu-id="502c2-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="502c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502c2-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502c2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502c2-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="502c2-120">INPUTS</span></span>

### <span data-ttu-id="502c2-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="502c2-121">None</span></span>

## <span data-ttu-id="502c2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="502c2-122">OUTPUTS</span></span>

### <span data-ttu-id="502c2-123">Microsoft. Azure. Management. Reservations. models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="502c2-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="502c2-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="502c2-124">NOTES</span></span>

## <span data-ttu-id="502c2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="502c2-125">RELATED LINKS</span></span>
