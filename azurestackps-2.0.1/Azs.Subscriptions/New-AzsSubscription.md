---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015175"
---
# <span data-ttu-id="06eeb-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="06eeb-101">New-AzsSubscription</span></span>

## <span data-ttu-id="06eeb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="06eeb-103">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="06eeb-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="06eeb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06eeb-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="06eeb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="06eeb-106">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="06eeb-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="06eeb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="06eeb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06eeb-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="06eeb-109">Előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="06eeb-109">Create a subscription.</span></span>

## <span data-ttu-id="06eeb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06eeb-110">PARAMETERS</span></span>

### <span data-ttu-id="06eeb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06eeb-111">-DefaultProfile</span></span>
<span data-ttu-id="06eeb-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06eeb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="06eeb-113">-DisplayName</span></span>
<span data-ttu-id="06eeb-114">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="06eeb-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="06eeb-115">-Id</span></span>
<span data-ttu-id="06eeb-116">Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="06eeb-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="06eeb-117">-OfferId</span></span>
<span data-ttu-id="06eeb-118">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="06eeb-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-119">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="06eeb-119">-State</span></span>
<span data-ttu-id="06eeb-120">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="06eeb-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06eeb-121">-SubscriptionId</span></span>
<span data-ttu-id="06eeb-122">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="06eeb-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-123">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="06eeb-123">-TenantId</span></span>
<span data-ttu-id="06eeb-124">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="06eeb-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06eeb-125">-Confirm</span></span>
<span data-ttu-id="06eeb-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06eeb-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06eeb-127">-WhatIf</span></span>
<span data-ttu-id="06eeb-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06eeb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06eeb-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06eeb-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06eeb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06eeb-130">CommonParameters</span></span>
<span data-ttu-id="06eeb-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06eeb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06eeb-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="06eeb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06eeb-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06eeb-133">INPUTS</span></span>

## <span data-ttu-id="06eeb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06eeb-134">OUTPUTS</span></span>

### <span data-ttu-id="06eeb-135">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="06eeb-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="06eeb-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06eeb-136">NOTES</span></span>

## <span data-ttu-id="06eeb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06eeb-137">RELATED LINKS</span></span>

