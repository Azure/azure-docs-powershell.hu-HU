---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8228a8605462b71fce598c7dc44454a16e1d7c90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840070"
---
# <span data-ttu-id="225e5-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="225e5-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="225e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="225e5-102">SYNOPSIS</span></span>
<span data-ttu-id="225e5-103">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="225e5-103">Get the offer metrics.</span></span>

## <span data-ttu-id="225e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="225e5-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="225e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="225e5-105">DESCRIPTION</span></span>
<span data-ttu-id="225e5-106">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="225e5-106">Get the offer metrics.</span></span>

## <span data-ttu-id="225e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="225e5-107">EXAMPLES</span></span>

### <span data-ttu-id="225e5-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="225e5-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="225e5-109">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="225e5-109">Get the offer metrics.</span></span>

## <span data-ttu-id="225e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="225e5-110">PARAMETERS</span></span>

### <span data-ttu-id="225e5-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="225e5-111">-OfferName</span></span>
<span data-ttu-id="225e5-112">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="225e5-112">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225e5-113">-ResourceGroupName</span></span>
<span data-ttu-id="225e5-114">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="225e5-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225e5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225e5-115">CommonParameters</span></span>
<span data-ttu-id="225e5-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="225e5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225e5-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225e5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225e5-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="225e5-118">INPUTS</span></span>

## <span data-ttu-id="225e5-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="225e5-119">OUTPUTS</span></span>

### <span data-ttu-id="225e5-120">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. metrikus</span><span class="sxs-lookup"><span data-stu-id="225e5-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="225e5-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="225e5-121">NOTES</span></span>

## <span data-ttu-id="225e5-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="225e5-122">RELATED LINKS</span></span>

