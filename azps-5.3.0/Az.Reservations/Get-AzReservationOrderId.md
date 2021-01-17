---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377984"
---
# <span data-ttu-id="923ea-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="923ea-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="923ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="923ea-102">SYNOPSIS</span></span>
<span data-ttu-id="923ea-103">A megfelelő `ReservationOrder` azonosítók listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="923ea-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="923ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="923ea-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="923ea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="923ea-105">DESCRIPTION</span></span>
<span data-ttu-id="923ea-106">Szerezze be az előfizetésre alkalmazható `ReservationOrder` azonosítókat.</span><span class="sxs-lookup"><span data-stu-id="923ea-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="923ea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="923ea-107">EXAMPLES</span></span>

### <span data-ttu-id="923ea-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="923ea-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="923ea-109">Alkalmazás az `ReservationOrder` alapértelmezett előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="923ea-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="923ea-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="923ea-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="923ea-111">A megadott `ReservationOrder` előfizetésre alkalmazott alkalmazás</span><span class="sxs-lookup"><span data-stu-id="923ea-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="923ea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="923ea-112">PARAMETERS</span></span>

### <span data-ttu-id="923ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923ea-113">-DefaultProfile</span></span>
<span data-ttu-id="923ea-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="923ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="923ea-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="923ea-115">-SubscriptionId</span></span>
<span data-ttu-id="923ea-116">Az alkalmazott előfizetés azonosítója `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="923ea-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="923ea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923ea-117">CommonParameters</span></span>
<span data-ttu-id="923ea-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923ea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923ea-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="923ea-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923ea-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="923ea-120">INPUTS</span></span>

### <span data-ttu-id="923ea-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="923ea-121">None</span></span>

## <span data-ttu-id="923ea-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="923ea-122">OUTPUTS</span></span>

### <span data-ttu-id="923ea-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="923ea-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="923ea-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="923ea-124">NOTES</span></span>

## <span data-ttu-id="923ea-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="923ea-125">RELATED LINKS</span></span>
