---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840502"
---
# <span data-ttu-id="e87cd-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e87cd-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="e87cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e87cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e87cd-103">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="e87cd-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="e87cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e87cd-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e87cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e87cd-105">DESCRIPTION</span></span>
<span data-ttu-id="e87cd-106">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="e87cd-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="e87cd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e87cd-107">EXAMPLES</span></span>

### <span data-ttu-id="e87cd-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e87cd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e87cd-109">Hozzon létre egy új ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="e87cd-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="e87cd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e87cd-110">PARAMETERS</span></span>

### <span data-ttu-id="e87cd-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="e87cd-111">-Location</span></span>
<span data-ttu-id="e87cd-112">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e87cd-112">Location of the resource.</span></span>

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

### <span data-ttu-id="e87cd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e87cd-113">-Name</span></span>
<span data-ttu-id="e87cd-114">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="e87cd-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="e87cd-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="e87cd-115">-OfferName</span></span>
<span data-ttu-id="e87cd-116">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="e87cd-116">Name of an offer.</span></span>

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

### <span data-ttu-id="e87cd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e87cd-117">-ResourceGroupName</span></span>
<span data-ttu-id="e87cd-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="e87cd-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e87cd-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e87cd-119">-SubscriptionId</span></span>
<span data-ttu-id="e87cd-120">A delegált ajánlatot kapó előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e87cd-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="e87cd-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e87cd-121">-Confirm</span></span>
<span data-ttu-id="e87cd-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e87cd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e87cd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e87cd-123">-WhatIf</span></span>
<span data-ttu-id="e87cd-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e87cd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e87cd-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e87cd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e87cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87cd-126">CommonParameters</span></span>
<span data-ttu-id="e87cd-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e87cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87cd-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e87cd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87cd-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e87cd-129">INPUTS</span></span>

## <span data-ttu-id="e87cd-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e87cd-130">OUTPUTS</span></span>

### <span data-ttu-id="e87cd-131">Microsoft. AzureStack. Management. Subscriptions. admin. models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e87cd-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="e87cd-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e87cd-132">NOTES</span></span>

## <span data-ttu-id="e87cd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e87cd-133">RELATED LINKS</span></span>

