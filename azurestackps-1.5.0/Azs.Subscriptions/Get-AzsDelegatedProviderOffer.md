---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8034887f8b44bef5c3dd59f73186027af1a1e5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491299"
---
# <span data-ttu-id="989a1-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="989a1-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="989a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="989a1-102">SYNOPSIS</span></span>
<span data-ttu-id="989a1-103">A megadott delegált szolgáltatóhoz tartozó ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="989a1-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="989a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="989a1-104">SYNTAX</span></span>

### <span data-ttu-id="989a1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="989a1-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="989a1-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="989a1-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -Name <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="989a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="989a1-107">DESCRIPTION</span></span>
<span data-ttu-id="989a1-108">A megadott delegált szolgáltatóhoz tartozó ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="989a1-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="989a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="989a1-109">EXAMPLES</span></span>

### <span data-ttu-id="989a1-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="989a1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="989a1-111">A megadott delegált szolgáltatóhoz tartozó ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="989a1-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="989a1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="989a1-112">PARAMETERS</span></span>

### <span data-ttu-id="989a1-113">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="989a1-113">-DelegatedProviderId</span></span>
<span data-ttu-id="989a1-114">A delegált szolgáltató azonosítója</span><span class="sxs-lookup"><span data-stu-id="989a1-114">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989a1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="989a1-115">-Name</span></span>
<span data-ttu-id="989a1-116">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="989a1-116">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: OfferName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989a1-117">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="989a1-117">-Skip</span></span>
<span data-ttu-id="989a1-118">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="989a1-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989a1-119">-Top</span><span class="sxs-lookup"><span data-stu-id="989a1-119">-Top</span></span>
<span data-ttu-id="989a1-120">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="989a1-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="989a1-121">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="989a1-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989a1-122">CommonParameters</span></span>
<span data-ttu-id="989a1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="989a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989a1-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="989a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989a1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="989a1-125">INPUTS</span></span>

## <span data-ttu-id="989a1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="989a1-126">OUTPUTS</span></span>

### <span data-ttu-id="989a1-127">Microsoft. AzureStack. Management. előfizetés. models. Offer</span><span class="sxs-lookup"><span data-stu-id="989a1-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="989a1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="989a1-128">NOTES</span></span>

## <span data-ttu-id="989a1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="989a1-129">RELATED LINKS</span></span>

