---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490980"
---
# <span data-ttu-id="eb190-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="eb190-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="eb190-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb190-102">SYNOPSIS</span></span>
<span data-ttu-id="eb190-103">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="eb190-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="eb190-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb190-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb190-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb190-105">DESCRIPTION</span></span>
<span data-ttu-id="eb190-106">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="eb190-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="eb190-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eb190-107">EXAMPLES</span></span>

### <span data-ttu-id="eb190-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb190-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="eb190-109">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="eb190-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="eb190-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb190-110">PARAMETERS</span></span>

### <span data-ttu-id="eb190-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="eb190-111">-Location</span></span>
<span data-ttu-id="eb190-112">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="eb190-112">Location of the resource.</span></span>

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

### <span data-ttu-id="eb190-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb190-113">-Name</span></span>
<span data-ttu-id="eb190-114">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="eb190-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="eb190-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="eb190-115">-OfferName</span></span>
<span data-ttu-id="eb190-116">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="eb190-116">Name of an offer.</span></span>

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

### <span data-ttu-id="eb190-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb190-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb190-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="eb190-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb190-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb190-119">-SubscriptionId</span></span>
<span data-ttu-id="eb190-120">A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb190-120">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb190-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb190-121">-Confirm</span></span>
<span data-ttu-id="eb190-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb190-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb190-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb190-123">-WhatIf</span></span>
<span data-ttu-id="eb190-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb190-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb190-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb190-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb190-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb190-126">CommonParameters</span></span>
<span data-ttu-id="eb190-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb190-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb190-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb190-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb190-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb190-129">INPUTS</span></span>

## <span data-ttu-id="eb190-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb190-130">OUTPUTS</span></span>

### <span data-ttu-id="eb190-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="eb190-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="eb190-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb190-132">NOTES</span></span>

## <span data-ttu-id="eb190-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb190-133">RELATED LINKS</span></span>

