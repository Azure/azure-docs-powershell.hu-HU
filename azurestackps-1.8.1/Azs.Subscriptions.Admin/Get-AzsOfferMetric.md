---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840506"
---
# <span data-ttu-id="85026-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="85026-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="85026-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85026-102">SYNOPSIS</span></span>
<span data-ttu-id="85026-103">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="85026-103">Get the offer metrics.</span></span>

## <span data-ttu-id="85026-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85026-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="85026-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85026-105">DESCRIPTION</span></span>
<span data-ttu-id="85026-106">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="85026-106">Get the offer metrics.</span></span>

## <span data-ttu-id="85026-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85026-107">EXAMPLES</span></span>

### <span data-ttu-id="85026-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="85026-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="85026-109">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="85026-109">Get the offer metrics.</span></span>

## <span data-ttu-id="85026-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85026-110">PARAMETERS</span></span>

### <span data-ttu-id="85026-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="85026-111">-OfferName</span></span>
<span data-ttu-id="85026-112">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="85026-112">Name of an offer.</span></span>

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

### <span data-ttu-id="85026-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85026-113">-ResourceGroupName</span></span>
<span data-ttu-id="85026-114">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="85026-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="85026-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85026-115">CommonParameters</span></span>
<span data-ttu-id="85026-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85026-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85026-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85026-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85026-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85026-118">INPUTS</span></span>

## <span data-ttu-id="85026-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85026-119">OUTPUTS</span></span>

### <span data-ttu-id="85026-120">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. metrikus</span><span class="sxs-lookup"><span data-stu-id="85026-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="85026-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85026-121">NOTES</span></span>

## <span data-ttu-id="85026-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85026-122">RELATED LINKS</span></span>

