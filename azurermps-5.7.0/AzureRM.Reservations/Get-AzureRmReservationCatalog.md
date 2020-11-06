---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495278"
---
# <span data-ttu-id="ccc0b-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="ccc0b-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="ccc0b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccc0b-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc0b-103">A rendelkezésre álló foglalás katalógusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ccc0b-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccc0b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccc0b-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="ccc0b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccc0b-105">DESCRIPTION</span></span>
<span data-ttu-id="ccc0b-106">A megadott Azure-előfizetéshez lefoglalt példányok vásárlásához rendelkezésre álló régiók és SKU-ók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="ccc0b-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="ccc0b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccc0b-107">EXAMPLES</span></span>

### <span data-ttu-id="ccc0b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccc0b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="ccc0b-109">Az alapértelmezett előfizetés katalógusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ccc0b-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="ccc0b-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="ccc0b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="ccc0b-111">A megadott előfizetés katalógusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ccc0b-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="ccc0b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccc0b-112">PARAMETERS</span></span>

### <span data-ttu-id="ccc0b-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccc0b-113">-SubscriptionId</span></span>
<span data-ttu-id="ccc0b-114">Az előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="ccc0b-114">Id of the subscription</span></span>

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

### <span data-ttu-id="ccc0b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc0b-115">CommonParameters</span></span>
<span data-ttu-id="ccc0b-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccc0b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc0b-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc0b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc0b-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc0b-118">INPUTS</span></span>

### <span data-ttu-id="ccc0b-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="ccc0b-119">None</span></span>

## <span data-ttu-id="ccc0b-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc0b-120">OUTPUTS</span></span>

### <span data-ttu-id="ccc0b-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Reservations. models. PSCatalog, Microsoft. Azure. commands. Reservations, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ccc0b-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ccc0b-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccc0b-122">NOTES</span></span>

## <span data-ttu-id="ccc0b-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccc0b-123">RELATED LINKS</span></span>

