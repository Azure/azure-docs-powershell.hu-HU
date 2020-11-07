---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840513"
---
# <span data-ttu-id="39b16-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="39b16-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="39b16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39b16-102">SYNOPSIS</span></span>
<span data-ttu-id="39b16-103">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="39b16-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="39b16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39b16-104">SYNTAX</span></span>

### <span data-ttu-id="39b16-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39b16-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="39b16-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="39b16-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="39b16-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="39b16-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="39b16-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="39b16-108">DESCRIPTION</span></span>
<span data-ttu-id="39b16-109">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="39b16-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="39b16-110">Példák</span><span class="sxs-lookup"><span data-stu-id="39b16-110">EXAMPLES</span></span>

### <span data-ttu-id="39b16-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="39b16-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="39b16-112">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="39b16-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="39b16-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39b16-113">PARAMETERS</span></span>

### <span data-ttu-id="39b16-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39b16-114">-Name</span></span>
<span data-ttu-id="39b16-115">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="39b16-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="39b16-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="39b16-116">-OfferName</span></span>
<span data-ttu-id="39b16-117">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="39b16-117">Name of an offer.</span></span>

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

### <span data-ttu-id="39b16-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b16-118">-ResourceGroupName</span></span>
<span data-ttu-id="39b16-119">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="39b16-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="39b16-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39b16-120">-ResourceId</span></span>
<span data-ttu-id="39b16-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="39b16-121">The resource id.</span></span>

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

### <span data-ttu-id="39b16-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="39b16-122">-Skip</span></span>
<span data-ttu-id="39b16-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="39b16-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="39b16-124">-Top</span><span class="sxs-lookup"><span data-stu-id="39b16-124">-Top</span></span>
<span data-ttu-id="39b16-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="39b16-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="39b16-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="39b16-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="39b16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b16-127">CommonParameters</span></span>
<span data-ttu-id="39b16-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39b16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b16-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b16-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b16-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39b16-130">INPUTS</span></span>

## <span data-ttu-id="39b16-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39b16-131">OUTPUTS</span></span>

### <span data-ttu-id="39b16-132">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="39b16-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="39b16-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39b16-133">NOTES</span></span>

## <span data-ttu-id="39b16-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39b16-134">RELATED LINKS</span></span>

