---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840351"
---
# <span data-ttu-id="47840-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="47840-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="47840-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47840-102">SYNOPSIS</span></span>
<span data-ttu-id="47840-103">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="47840-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="47840-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47840-104">SYNTAX</span></span>

### <span data-ttu-id="47840-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47840-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="47840-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="47840-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="47840-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="47840-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="47840-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="47840-108">DESCRIPTION</span></span>
<span data-ttu-id="47840-109">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="47840-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="47840-110">Példák</span><span class="sxs-lookup"><span data-stu-id="47840-110">EXAMPLES</span></span>

### <span data-ttu-id="47840-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="47840-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="47840-112">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="47840-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="47840-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47840-113">PARAMETERS</span></span>

### <span data-ttu-id="47840-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47840-114">-Name</span></span>
<span data-ttu-id="47840-115">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="47840-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="47840-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="47840-116">-OfferName</span></span>
<span data-ttu-id="47840-117">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="47840-117">Name of an offer.</span></span>

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

### <span data-ttu-id="47840-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47840-118">-ResourceGroupName</span></span>
<span data-ttu-id="47840-119">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="47840-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="47840-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47840-120">-ResourceId</span></span>
<span data-ttu-id="47840-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="47840-121">The resource id.</span></span>

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

### <span data-ttu-id="47840-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="47840-122">-Skip</span></span>
<span data-ttu-id="47840-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="47840-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="47840-124">-Top</span><span class="sxs-lookup"><span data-stu-id="47840-124">-Top</span></span>
<span data-ttu-id="47840-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="47840-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="47840-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="47840-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="47840-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47840-127">CommonParameters</span></span>
<span data-ttu-id="47840-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47840-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47840-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47840-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47840-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47840-130">INPUTS</span></span>

## <span data-ttu-id="47840-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47840-131">OUTPUTS</span></span>

### <span data-ttu-id="47840-132">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="47840-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="47840-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47840-133">NOTES</span></span>

## <span data-ttu-id="47840-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47840-134">RELATED LINKS</span></span>

