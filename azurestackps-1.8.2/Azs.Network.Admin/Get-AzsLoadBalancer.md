---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016951"
---
# <span data-ttu-id="e279e-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e279e-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="e279e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e279e-102">SYNOPSIS</span></span>
<span data-ttu-id="e279e-103">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e279e-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="e279e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e279e-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e279e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e279e-105">DESCRIPTION</span></span>
<span data-ttu-id="e279e-106">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e279e-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="e279e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e279e-107">EXAMPLES</span></span>

### <span data-ttu-id="e279e-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="e279e-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="e279e-109">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e279e-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="e279e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e279e-110">PARAMETERS</span></span>

### <span data-ttu-id="e279e-111">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="e279e-111">-Filter</span></span>
<span data-ttu-id="e279e-112">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="e279e-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e279e-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e279e-113">-OrderBy</span></span>
<span data-ttu-id="e279e-114">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="e279e-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e279e-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="e279e-115">-Skip</span></span>
<span data-ttu-id="e279e-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e279e-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e279e-117">-Top</span><span class="sxs-lookup"><span data-stu-id="e279e-117">-Top</span></span>
<span data-ttu-id="e279e-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="e279e-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e279e-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="e279e-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e279e-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="e279e-120">-InlineCount</span></span>
<span data-ttu-id="e279e-121">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="e279e-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e279e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e279e-122">CommonParameters</span></span>
<span data-ttu-id="e279e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e279e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e279e-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e279e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e279e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e279e-125">INPUTS</span></span>

## <span data-ttu-id="e279e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e279e-126">OUTPUTS</span></span>

### <span data-ttu-id="e279e-127">Microsoft. AzureStack. Management. Network. admin. models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e279e-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="e279e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e279e-128">NOTES</span></span>

## <span data-ttu-id="e279e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e279e-129">RELATED LINKS</span></span>
