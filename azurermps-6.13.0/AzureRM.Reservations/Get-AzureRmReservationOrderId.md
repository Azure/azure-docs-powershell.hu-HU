---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: 1e60ca2ce1a845fa460e14a4e99b921fa4c085ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493966"
---
# <span data-ttu-id="4afa9-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="4afa9-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="4afa9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4afa9-102">SYNOPSIS</span></span>
<span data-ttu-id="4afa9-103">A megfelelő azonosítók listájának beszerzése `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="4afa9-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4afa9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4afa9-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4afa9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4afa9-105">DESCRIPTION</span></span>
<span data-ttu-id="4afa9-106">Az adott `ReservationOrder` előfizetésre alkalmazható e-s azonosítók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4afa9-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="4afa9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4afa9-107">EXAMPLES</span></span>

### <span data-ttu-id="4afa9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4afa9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="4afa9-109">`ReservationOrder`Az alapértelmezett előfizetés alkalmazása</span><span class="sxs-lookup"><span data-stu-id="4afa9-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="4afa9-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="4afa9-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="4afa9-111">`ReservationOrder`A megadott előfizetés alkalmazása</span><span class="sxs-lookup"><span data-stu-id="4afa9-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="4afa9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4afa9-112">PARAMETERS</span></span>

### <span data-ttu-id="4afa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afa9-113">-DefaultProfile</span></span>
<span data-ttu-id="4afa9-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4afa9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4afa9-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4afa9-115">-SubscriptionId</span></span>
<span data-ttu-id="4afa9-116">Az előfizetés azonosítója az alkalmazott s érték beszerzéséhez `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="4afa9-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="4afa9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afa9-117">CommonParameters</span></span>
<span data-ttu-id="4afa9-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4afa9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afa9-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4afa9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afa9-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afa9-120">INPUTS</span></span>

### <span data-ttu-id="4afa9-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="4afa9-121">None</span></span>

## <span data-ttu-id="4afa9-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afa9-122">OUTPUTS</span></span>

### <span data-ttu-id="4afa9-123">Microsoft. Azure. Management. Reservations. models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="4afa9-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="4afa9-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4afa9-124">NOTES</span></span>

## <span data-ttu-id="4afa9-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4afa9-125">RELATED LINKS</span></span>
