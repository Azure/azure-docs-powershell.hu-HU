---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840970"
---
# <span data-ttu-id="fc7a0-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="fc7a0-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="fc7a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7a0-103">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="fc7a0-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="fc7a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc7a0-104">SYNTAX</span></span>

### <span data-ttu-id="fc7a0-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc7a0-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fc7a0-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="fc7a0-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fc7a0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc7a0-107">DESCRIPTION</span></span>
<span data-ttu-id="fc7a0-108">Előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="fc7a0-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="fc7a0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fc7a0-109">EXAMPLES</span></span>

### <span data-ttu-id="fc7a0-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc7a0-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="fc7a0-111">Előfizetést frissít.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-111">Updates a subscription.</span></span>

## <span data-ttu-id="fc7a0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc7a0-112">PARAMETERS</span></span>

### <span data-ttu-id="fc7a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7a0-113">-DefaultProfile</span></span>
<span data-ttu-id="fc7a0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc7a0-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fc7a0-115">-DisplayName</span></span>
<span data-ttu-id="fc7a0-116">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="fc7a0-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fc7a0-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="fc7a0-117">-Id</span></span>
<span data-ttu-id="fc7a0-118">Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fc7a0-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="fc7a0-119">-OfferId</span></span>
<span data-ttu-id="fc7a0-120">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fc7a0-121">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="fc7a0-121">-State</span></span>
<span data-ttu-id="fc7a0-122">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="fc7a0-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fc7a0-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="fc7a0-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="fc7a0-124">A támogatott műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-124">List of supported operations.</span></span>
<span data-ttu-id="fc7a0-125">A kivitelezéshez tekintse meg a SUBSCRIPTIONDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fc7a0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc7a0-126">-SubscriptionId</span></span>
<span data-ttu-id="fc7a0-127">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fc7a0-128">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="fc7a0-128">-TenantId</span></span>
<span data-ttu-id="fc7a0-129">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="fc7a0-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fc7a0-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc7a0-130">-Confirm</span></span>
<span data-ttu-id="fc7a0-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc7a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7a0-132">-WhatIf</span></span>
<span data-ttu-id="fc7a0-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7a0-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc7a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7a0-135">CommonParameters</span></span>
<span data-ttu-id="fc7a0-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc7a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7a0-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7a0-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc7a0-138">INPUTS</span></span>

### <span data-ttu-id="fc7a0-139">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="fc7a0-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="fc7a0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc7a0-140">OUTPUTS</span></span>

### <span data-ttu-id="fc7a0-141">Microsoft. Azure. PowerShell. parancsmagok. előfizetés. models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="fc7a0-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="fc7a0-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc7a0-142">NOTES</span></span>

<span data-ttu-id="fc7a0-143">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc7a0-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fc7a0-145">SUBSCRIPTIONDEFINITION <ISubscription> : a támogatott műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="fc7a0-146">`[DisplayName <String>]`: Előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="fc7a0-147">`[Id <String>]`: Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="fc7a0-148">`[OfferId <String>]`: Az ajánlat azonosítója egy delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="fc7a0-149">`[State <SubscriptionState?>]`: Előfizetés állapota.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="fc7a0-150">`[SubscriptionId <String>]`: Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="fc7a0-151">`[TenantId <String>]`: Címtár-bérlői azonosító.</span><span class="sxs-lookup"><span data-stu-id="fc7a0-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="fc7a0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc7a0-152">RELATED LINKS</span></span>

