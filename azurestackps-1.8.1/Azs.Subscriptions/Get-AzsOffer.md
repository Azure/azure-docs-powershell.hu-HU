---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840637"
---
# <span data-ttu-id="a3ff4-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="a3ff4-101">Get-AzsOffer</span></span>

## <span data-ttu-id="a3ff4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ff4-103">A nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-103">Get the list of public offers.</span></span>

## <span data-ttu-id="a3ff4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3ff4-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3ff4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ff4-106">A nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-106">Get the list of public offers.</span></span>

## <span data-ttu-id="a3ff4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a3ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ff4-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="a3ff4-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="a3ff4-109">A nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-109">Get the list of public offers.</span></span>

## <span data-ttu-id="a3ff4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3ff4-110">PARAMETERS</span></span>

### <span data-ttu-id="a3ff4-111">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="a3ff4-111">-Skip</span></span>
<span data-ttu-id="a3ff4-112">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ff4-113">-Top</span><span class="sxs-lookup"><span data-stu-id="a3ff4-113">-Top</span></span>
<span data-ttu-id="a3ff4-114">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a3ff4-115">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ff4-116">-Szolgáltató</span><span class="sxs-lookup"><span data-stu-id="a3ff4-116">-Provider</span></span>
<span data-ttu-id="a3ff4-117">Választható paraméter a delegált szolgáltató nevének megadásához.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="a3ff4-118">Ezt a paramétert a program nem használja, és a jövőben megszűnik.</span><span class="sxs-lookup"><span data-stu-id="a3ff4-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ff4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ff4-119">CommonParameters</span></span>
<span data-ttu-id="a3ff4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3ff4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ff4-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ff4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ff4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3ff4-122">INPUTS</span></span>

## <span data-ttu-id="a3ff4-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3ff4-123">OUTPUTS</span></span>

### <span data-ttu-id="a3ff4-124">Microsoft. AzureStack. Management. előfizetés. models. Offer</span><span class="sxs-lookup"><span data-stu-id="a3ff4-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="a3ff4-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3ff4-125">NOTES</span></span>

## <span data-ttu-id="a3ff4-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3ff4-126">RELATED LINKS</span></span>
