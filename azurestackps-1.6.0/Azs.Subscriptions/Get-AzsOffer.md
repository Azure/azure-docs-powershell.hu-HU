---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491647"
---
# <span data-ttu-id="d98a8-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="d98a8-101">Get-AzsOffer</span></span>

## <span data-ttu-id="d98a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d98a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d98a8-103">A nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d98a8-103">Get the list of public offers.</span></span>

## <span data-ttu-id="d98a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d98a8-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d98a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d98a8-105">DESCRIPTION</span></span>
<span data-ttu-id="d98a8-106">A nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d98a8-106">Get the list of public offers.</span></span>

## <span data-ttu-id="d98a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d98a8-107">EXAMPLES</span></span>

### <span data-ttu-id="d98a8-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d98a8-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="d98a8-109">A nyilvános ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d98a8-109">Get the list of public offers.</span></span>

## <span data-ttu-id="d98a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d98a8-110">PARAMETERS</span></span>

### <span data-ttu-id="d98a8-111">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="d98a8-111">-Skip</span></span>
<span data-ttu-id="d98a8-112">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="d98a8-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d98a8-113">-Top</span><span class="sxs-lookup"><span data-stu-id="d98a8-113">-Top</span></span>
<span data-ttu-id="d98a8-114">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="d98a8-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d98a8-115">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="d98a8-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d98a8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98a8-116">CommonParameters</span></span>
<span data-ttu-id="d98a8-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d98a8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98a8-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d98a8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98a8-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d98a8-119">INPUTS</span></span>

## <span data-ttu-id="d98a8-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d98a8-120">OUTPUTS</span></span>

### <span data-ttu-id="d98a8-121">Microsoft. AzureStack. Management. előfizetés. models. Offer</span><span class="sxs-lookup"><span data-stu-id="d98a8-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="d98a8-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d98a8-122">NOTES</span></span>

## <span data-ttu-id="d98a8-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d98a8-123">RELATED LINKS</span></span>

