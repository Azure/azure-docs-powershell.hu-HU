---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87966f8ac96ab70f7617f857d9f1d83945b5e639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491360"
---
# <span data-ttu-id="3d358-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d358-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="3d358-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d358-102">SYNOPSIS</span></span>
<span data-ttu-id="3d358-103">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3d358-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="3d358-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d358-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="3d358-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d358-105">DESCRIPTION</span></span>
<span data-ttu-id="3d358-106">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3d358-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="3d358-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3d358-107">EXAMPLES</span></span>

### <span data-ttu-id="3d358-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3d358-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="3d358-109">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3d358-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="3d358-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d358-110">PARAMETERS</span></span>

### <span data-ttu-id="3d358-111">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="3d358-111">-Filter</span></span>
<span data-ttu-id="3d358-112">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="3d358-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="3d358-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="3d358-113">-InlineCount</span></span>
<span data-ttu-id="3d358-114">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="3d358-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="3d358-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="3d358-115">-OrderBy</span></span>
<span data-ttu-id="3d358-116">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="3d358-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="3d358-117">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="3d358-117">-Skip</span></span>
<span data-ttu-id="3d358-118">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="3d358-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3d358-119">-Top</span><span class="sxs-lookup"><span data-stu-id="3d358-119">-Top</span></span>
<span data-ttu-id="3d358-120">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="3d358-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3d358-121">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="3d358-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3d358-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d358-122">CommonParameters</span></span>
<span data-ttu-id="3d358-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d358-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d358-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d358-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d358-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d358-125">INPUTS</span></span>

## <span data-ttu-id="3d358-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d358-126">OUTPUTS</span></span>

### <span data-ttu-id="3d358-127">Microsoft. AzureStack. Management. Network. admin. models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d358-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="3d358-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d358-128">NOTES</span></span>

## <span data-ttu-id="3d358-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d358-129">RELATED LINKS</span></span>

