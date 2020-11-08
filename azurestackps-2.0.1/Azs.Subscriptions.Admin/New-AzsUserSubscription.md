---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015179"
---
# <span data-ttu-id="80bd4-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="80bd4-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="80bd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="80bd4-103">A megadott előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="80bd4-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="80bd4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80bd4-104">SYNTAX</span></span>

### <span data-ttu-id="80bd4-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80bd4-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80bd4-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="80bd4-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80bd4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="80bd4-107">DESCRIPTION</span></span>
<span data-ttu-id="80bd4-108">A megadott előfizetés létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="80bd4-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="80bd4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="80bd4-109">EXAMPLES</span></span>

### <span data-ttu-id="80bd4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="80bd4-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="80bd4-111">Új felhasználói előfizetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="80bd4-111">Creates a new user subscription</span></span>

## <span data-ttu-id="80bd4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80bd4-112">PARAMETERS</span></span>

### <span data-ttu-id="80bd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bd4-113">-DefaultProfile</span></span>
<span data-ttu-id="80bd4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80bd4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80bd4-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80bd4-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="80bd4-116">Fölérendelt DelegatedProvider-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="80bd4-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="80bd4-117">-DisplayName</span></span>
<span data-ttu-id="80bd4-118">Előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="80bd4-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="80bd4-119">-ExternalReferenceId</span></span>
<span data-ttu-id="80bd4-120">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="80bd4-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="80bd4-121">-Id</span></span>
<span data-ttu-id="80bd4-122">Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="80bd4-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="80bd4-123">-OfferId</span></span>
<span data-ttu-id="80bd4-124">Az ajánlat azonosítója a delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="80bd4-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-125">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="80bd4-125">-Owner</span></span>
<span data-ttu-id="80bd4-126">Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="80bd4-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="80bd4-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="80bd4-128">Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="80bd4-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="80bd4-129">-State</span></span>
<span data-ttu-id="80bd4-130">Előfizetés állapota</span><span class="sxs-lookup"><span data-stu-id="80bd4-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="80bd4-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="80bd4-132">Az előfizetés objektum tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="80bd4-132">Subscription object properties.</span></span>
<span data-ttu-id="80bd4-133">A kivitelezéshez tekintse meg a SUBSCRIPTIONDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="80bd4-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80bd4-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="80bd4-135">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="80bd4-135">The target subscription ID.</span></span>

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

### <span data-ttu-id="80bd4-136">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="80bd4-136">-TenantId</span></span>
<span data-ttu-id="80bd4-137">Címtár-bérlői azonosító</span><span class="sxs-lookup"><span data-stu-id="80bd4-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80bd4-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="80bd4-138">-Confirm</span></span>
<span data-ttu-id="80bd4-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="80bd4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80bd4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80bd4-140">-WhatIf</span></span>
<span data-ttu-id="80bd4-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="80bd4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80bd4-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80bd4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80bd4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bd4-143">CommonParameters</span></span>
<span data-ttu-id="80bd4-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80bd4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bd4-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="80bd4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bd4-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80bd4-146">INPUTS</span></span>

### <span data-ttu-id="80bd4-147">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="80bd4-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="80bd4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80bd4-148">OUTPUTS</span></span>

### <span data-ttu-id="80bd4-149">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="80bd4-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="80bd4-150">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="80bd4-150">ALIASES</span></span>

## <span data-ttu-id="80bd4-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80bd4-151">NOTES</span></span>

<span data-ttu-id="80bd4-152">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="80bd4-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80bd4-153">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="80bd4-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="80bd4-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : előfizetés objektum tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="80bd4-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="80bd4-155">`[DelegatedProviderSubscriptionId <String>]`: Szülő DelegatedProvider-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="80bd4-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="80bd4-156">`[DisplayName <String>]`: Előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="80bd4-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="80bd4-157">`[ExternalReferenceId <String>]`: Külső hivatkozási azonosító.</span><span class="sxs-lookup"><span data-stu-id="80bd4-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="80bd4-158">`[Id <String>]`: Teljesen minősített azonosító.</span><span class="sxs-lookup"><span data-stu-id="80bd4-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="80bd4-159">`[OfferId <String>]`: Az ajánlat azonosítója egy delegált szolgáltató hatóköre alatt.</span><span class="sxs-lookup"><span data-stu-id="80bd4-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="80bd4-160">`[Owner <String>]`: Előfizetés tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="80bd4-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="80bd4-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Útválasztási erőforrás-kezelő típusa</span><span class="sxs-lookup"><span data-stu-id="80bd4-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="80bd4-162">`[State <SubscriptionState?>]`: Előfizetés állapota.</span><span class="sxs-lookup"><span data-stu-id="80bd4-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="80bd4-163">`[SubscriptionId <String>]`: Előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="80bd4-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="80bd4-164">`[TenantId <String>]`: Címtár-bérlői azonosító.</span><span class="sxs-lookup"><span data-stu-id="80bd4-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="80bd4-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80bd4-165">RELATED LINKS</span></span>

