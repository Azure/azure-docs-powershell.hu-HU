---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/move-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 51ad63ef1531e7494b3929b8508e88e988155081
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016828"
---
# <span data-ttu-id="472fa-101">Move-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="472fa-101">Move-AzsUserSubscription</span></span>

## <span data-ttu-id="472fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="472fa-102">SYNOPSIS</span></span>
<span data-ttu-id="472fa-103">Előfizetések áthelyezése a meghatalmazott szolgáltató által kínált ajánlatok között</span><span class="sxs-lookup"><span data-stu-id="472fa-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="472fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="472fa-104">SYNTAX</span></span>

### <span data-ttu-id="472fa-105">MoveExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="472fa-105">MoveExpanded (Default)</span></span>
```
Move-AzsUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="472fa-106">Áthelyezése</span><span class="sxs-lookup"><span data-stu-id="472fa-106">Move</span></span>
```
Move-AzsUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="472fa-107">MoveViaIdentity</span><span class="sxs-lookup"><span data-stu-id="472fa-107">MoveViaIdentity</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="472fa-108">MoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="472fa-108">MoveViaIdentityExpanded</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="472fa-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="472fa-109">DESCRIPTION</span></span>
<span data-ttu-id="472fa-110">Előfizetések áthelyezése a meghatalmazott szolgáltató által kínált ajánlatok között</span><span class="sxs-lookup"><span data-stu-id="472fa-110">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="472fa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="472fa-111">EXAMPLES</span></span>

### <span data-ttu-id="472fa-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="472fa-112">Example 1</span></span>
```powershell
PS C:\> Move-AzsSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

{{ Add output here }}
```

<span data-ttu-id="472fa-113">Felhasználói előfizetések áthelyezése delegált szolgáltatói ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="472fa-113">Move user subscriptions to a delegated provider offer.</span></span>

### <span data-ttu-id="472fa-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="472fa-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id
Move-AzsSubscription -ResourceId $resourceIds

{{ Add output here }}
```

<span data-ttu-id="472fa-115">Felhasználói előfizetések áthelyezése egy delegált szolgáltatótól az alapértelmezett szolgáltatóig</span><span class="sxs-lookup"><span data-stu-id="472fa-115">Move user subscriptions from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="472fa-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="472fa-116">PARAMETERS</span></span>

### <span data-ttu-id="472fa-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="472fa-117">-AsJob</span></span>
<span data-ttu-id="472fa-118">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="472fa-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472fa-119">-DefaultProfile</span></span>
<span data-ttu-id="472fa-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="472fa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="472fa-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="472fa-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="472fa-122">A delegált szolgáltató azonosítója (rendszergazdai környezetből), amelyre az előfizetéseket át kell helyezni.</span><span class="sxs-lookup"><span data-stu-id="472fa-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="472fa-123">-InputObject</span></span>
<span data-ttu-id="472fa-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="472fa-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: MoveViaIdentity, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="472fa-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="472fa-126">Az előfizetések áthelyezése a következőre: létrehozás, a MOVESUBSCRIPTIONSDEFINITION tulajdonságainak megjegyzések szakasza és a kivonatoló táblázat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="472fa-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Move, MoveViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="472fa-127">-NoWait</span></span>
<span data-ttu-id="472fa-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="472fa-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="472fa-129">-PassThru</span></span>
<span data-ttu-id="472fa-130">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="472fa-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="472fa-131">-ResourceId</span></span>
<span data-ttu-id="472fa-132">Az előfizetések gyűjteménye a delegált szolgáltató által kínált ajánlatra való ugráshoz.</span><span class="sxs-lookup"><span data-stu-id="472fa-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="472fa-133">-SubscriptionId</span></span>
<span data-ttu-id="472fa-134">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="472fa-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Move, MoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="472fa-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="472fa-135">-Confirm</span></span>
<span data-ttu-id="472fa-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="472fa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="472fa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="472fa-137">-WhatIf</span></span>
<span data-ttu-id="472fa-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="472fa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="472fa-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="472fa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="472fa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472fa-140">CommonParameters</span></span>
<span data-ttu-id="472fa-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="472fa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472fa-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="472fa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472fa-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="472fa-143">INPUTS</span></span>

### <span data-ttu-id="472fa-144">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="472fa-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="472fa-145">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="472fa-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="472fa-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="472fa-146">OUTPUTS</span></span>

### <span data-ttu-id="472fa-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="472fa-147">System.Boolean</span></span>

<span data-ttu-id="472fa-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="472fa-148">ALIASES</span></span>

## <span data-ttu-id="472fa-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="472fa-149">NOTES</span></span>

<span data-ttu-id="472fa-150">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="472fa-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="472fa-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="472fa-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="472fa-152">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="472fa-152">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="472fa-153">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="472fa-153">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="472fa-154">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="472fa-154">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="472fa-155">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="472fa-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="472fa-156">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="472fa-156">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="472fa-157">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="472fa-157">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="472fa-158">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="472fa-158">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="472fa-159">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="472fa-159">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="472fa-160">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="472fa-160">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="472fa-161">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="472fa-161">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="472fa-162">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="472fa-162">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="472fa-163">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="472fa-163">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="472fa-164">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="472fa-164">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="472fa-165">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="472fa-165">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="472fa-166">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="472fa-166">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="472fa-167">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="472fa-167">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="472fa-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : az előfizetések áthelyezése műveletek definíciója</span><span class="sxs-lookup"><span data-stu-id="472fa-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="472fa-169">`Resources <String[]>`: Az előfizetések gyűjteménye a delegált szolgáltató által kínált ajánlatra való ugráshoz.</span><span class="sxs-lookup"><span data-stu-id="472fa-169">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="472fa-170">`[TargetDelegatedProviderOffer <String>]`: A delegált szolgáltató az előfizetések áthelyezni kívánt azonosítóját (rendszergazdai környezetből) adja meg.</span><span class="sxs-lookup"><span data-stu-id="472fa-170">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="472fa-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="472fa-171">RELATED LINKS</span></span>

