---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840071"
---
# <span data-ttu-id="87ed5-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="87ed5-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="87ed5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="87ed5-103">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="87ed5-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="87ed5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87ed5-104">SYNTAX</span></span>

### <span data-ttu-id="87ed5-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87ed5-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="87ed5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="87ed5-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="87ed5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87ed5-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="87ed5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="87ed5-108">DESCRIPTION</span></span>
<span data-ttu-id="87ed5-109">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="87ed5-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="87ed5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="87ed5-110">EXAMPLES</span></span>

### <span data-ttu-id="87ed5-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="87ed5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="87ed5-112">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="87ed5-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="87ed5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87ed5-113">PARAMETERS</span></span>

### <span data-ttu-id="87ed5-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87ed5-114">-Name</span></span>
<span data-ttu-id="87ed5-115">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="87ed5-115">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed5-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="87ed5-116">-OfferName</span></span>
<span data-ttu-id="87ed5-117">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="87ed5-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ed5-118">-ResourceGroupName</span></span>
<span data-ttu-id="87ed5-119">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="87ed5-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed5-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87ed5-120">-ResourceId</span></span>
<span data-ttu-id="87ed5-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="87ed5-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87ed5-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="87ed5-122">-Skip</span></span>
<span data-ttu-id="87ed5-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="87ed5-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed5-124">-Top</span><span class="sxs-lookup"><span data-stu-id="87ed5-124">-Top</span></span>
<span data-ttu-id="87ed5-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="87ed5-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="87ed5-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="87ed5-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ed5-127">CommonParameters</span></span>
<span data-ttu-id="87ed5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87ed5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ed5-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ed5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ed5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87ed5-130">INPUTS</span></span>

## <span data-ttu-id="87ed5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87ed5-131">OUTPUTS</span></span>

### <span data-ttu-id="87ed5-132">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="87ed5-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="87ed5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87ed5-133">NOTES</span></span>

## <span data-ttu-id="87ed5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87ed5-134">RELATED LINKS</span></span>

