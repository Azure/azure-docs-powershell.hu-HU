---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017157"
---
# <span data-ttu-id="bb79b-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="bb79b-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="bb79b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb79b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb79b-103">A megadott előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="bb79b-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="bb79b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb79b-104">SYNTAX</span></span>

### <span data-ttu-id="bb79b-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bb79b-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb79b-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="bb79b-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb79b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb79b-107">DESCRIPTION</span></span>
<span data-ttu-id="bb79b-108">A megadott előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="bb79b-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="bb79b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bb79b-109">EXAMPLES</span></span>

### <span data-ttu-id="bb79b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb79b-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="bb79b-111">Előfizetés frissítése</span><span class="sxs-lookup"><span data-stu-id="bb79b-111">Updates a subscription</span></span>

## <span data-ttu-id="bb79b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb79b-112">PARAMETERS</span></span>

### <span data-ttu-id="bb79b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb79b-113">-DefaultProfile</span></span>
<span data-ttu-id="bb79b-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb79b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb79b-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb79b-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="bb79b-116">Fölérendelt DelegatedProvider-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="bb79b-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="bb79b-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bb79b-117">-DisplayName</span></span>
<span data-ttu-id="bb79b-118">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="bb79b-118">Subscription name.</span></span>

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

### <span data-ttu-id="bb79b-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="bb79b-119">-ExternalReferenceId</span></span>
<span data-ttu-id="bb79b-120">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="bb79b-120">External reference identifier.</span></span>

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

### <span data-ttu-id="bb79b-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bb79b-121">-Id</span></span>
<span data-ttu-id="bb79b-122">Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="bb79b-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="bb79b-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="bb79b-123">-OfferId</span></span>
<span data-ttu-id="bb79b-124">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="bb79b-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="bb79b-125">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="bb79b-125">-Owner</span></span>
<span data-ttu-id="bb79b-126">Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="bb79b-126">Subscription owner.</span></span>

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

### <span data-ttu-id="bb79b-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="bb79b-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="bb79b-128">Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="bb79b-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb79b-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="bb79b-129">-State</span></span>
<span data-ttu-id="bb79b-130">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="bb79b-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb79b-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="bb79b-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="bb79b-132">Az előfizetés objektum tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="bb79b-132">Subscription object properties.</span></span>
<span data-ttu-id="bb79b-133">A kivitelezéshez tekintse meg a SUBSCRIPTIONDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="bb79b-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bb79b-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb79b-134">-SubscriptionId</span></span>
<span data-ttu-id="bb79b-135">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="bb79b-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bb79b-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="bb79b-136">-SubscriptionId1</span></span>
<span data-ttu-id="bb79b-137">Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bb79b-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="bb79b-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb79b-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="bb79b-139">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="bb79b-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="bb79b-140">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="bb79b-140">-TenantId</span></span>
<span data-ttu-id="bb79b-141">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="bb79b-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="bb79b-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb79b-142">-Confirm</span></span>
<span data-ttu-id="bb79b-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb79b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb79b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb79b-144">-WhatIf</span></span>
<span data-ttu-id="bb79b-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb79b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb79b-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb79b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb79b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb79b-147">CommonParameters</span></span>
<span data-ttu-id="bb79b-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb79b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb79b-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bb79b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb79b-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb79b-150">INPUTS</span></span>

### <span data-ttu-id="bb79b-151">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="bb79b-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="bb79b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb79b-152">OUTPUTS</span></span>

### <span data-ttu-id="bb79b-153">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="bb79b-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="bb79b-154">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="bb79b-154">ALIASES</span></span>

## <span data-ttu-id="bb79b-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb79b-155">NOTES</span></span>

<span data-ttu-id="bb79b-156">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="bb79b-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb79b-157">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="bb79b-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bb79b-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : előfizetés objektum tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="bb79b-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="bb79b-159">`[DelegatedProviderSubscriptionId <String>]`: Szülő DelegatedProvider-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bb79b-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="bb79b-160">`[DisplayName <String>]`: Előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="bb79b-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="bb79b-161">`[ExternalReferenceId <String>]`: Külső hivatkozási azonosító.</span><span class="sxs-lookup"><span data-stu-id="bb79b-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="bb79b-162">`[Id <String>]`: Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="bb79b-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="bb79b-163">`[OfferId <String>]`: Az ajánlat azonosítója egy delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="bb79b-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="bb79b-164">`[Owner <String>]`: Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="bb79b-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="bb79b-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="bb79b-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="bb79b-166">`[State <SubscriptionState?>]`: Előfizetés állapota.</span><span class="sxs-lookup"><span data-stu-id="bb79b-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="bb79b-167">`[SubscriptionId <String>]`: Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bb79b-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="bb79b-168">`[TenantId <String>]`: Címtár-bérlői azonosító.</span><span class="sxs-lookup"><span data-stu-id="bb79b-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="bb79b-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb79b-169">RELATED LINKS</span></span>

