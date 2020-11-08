---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017144"
---
# <span data-ttu-id="d3ce5-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d3ce5-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="d3ce5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ce5-103">Az előfizetések listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3ce5-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="d3ce5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3ce5-104">SYNTAX</span></span>

### <span data-ttu-id="d3ce5-105">CheckExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3ce5-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3ce5-106">Jelölőnégyzetet</span><span class="sxs-lookup"><span data-stu-id="d3ce5-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3ce5-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3ce5-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3ce5-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d3ce5-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3ce5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3ce5-109">DESCRIPTION</span></span>
<span data-ttu-id="d3ce5-110">Az előfizetések listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d3ce5-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="d3ce5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d3ce5-111">EXAMPLES</span></span>

### <span data-ttu-id="d3ce5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3ce5-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="d3ce5-113">A megadott erőforrás-típus és-név elérhetőségét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="d3ce5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3ce5-114">PARAMETERS</span></span>

### <span data-ttu-id="d3ce5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ce5-115">-DefaultProfile</span></span>
<span data-ttu-id="d3ce5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3ce5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3ce5-117">-InputObject</span></span>
<span data-ttu-id="d3ce5-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d3ce5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3ce5-119">-Name</span></span>
<span data-ttu-id="d3ce5-120">A hitelesíteni kívánt erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3ce5-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="d3ce5-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="d3ce5-122">A név elérhetősége műveletek definíciójának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="d3ce5-122">The check name availability action definition.</span></span>
<span data-ttu-id="d3ce5-123">A kivitelezéshez tekintse meg a NAMEAVAILABILITYDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d3ce5-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d3ce5-124">-ResourceType</span></span>
<span data-ttu-id="d3ce5-125">Az ellenőrizni kívánt erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3ce5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3ce5-126">-SubscriptionId</span></span>
<span data-ttu-id="d3ce5-127">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3ce5-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3ce5-128">-Confirm</span></span>
<span data-ttu-id="d3ce5-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3ce5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ce5-130">-WhatIf</span></span>
<span data-ttu-id="d3ce5-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3ce5-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3ce5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ce5-133">CommonParameters</span></span>
<span data-ttu-id="d3ce5-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3ce5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ce5-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ce5-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3ce5-136">INPUTS</span></span>

### <span data-ttu-id="d3ce5-137">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="d3ce5-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="d3ce5-138">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d3ce5-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d3ce5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3ce5-139">OUTPUTS</span></span>

### <span data-ttu-id="d3ce5-140">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d3ce5-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="d3ce5-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d3ce5-141">ALIASES</span></span>

## <span data-ttu-id="d3ce5-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3ce5-142">NOTES</span></span>

<span data-ttu-id="d3ce5-143">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3ce5-144">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d3ce5-145">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d3ce5-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3ce5-146">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d3ce5-147">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d3ce5-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d3ce5-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3ce5-149">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d3ce5-150">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d3ce5-151">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d3ce5-152">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d3ce5-153">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d3ce5-154">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d3ce5-155">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="d3ce5-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d3ce5-156">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d3ce5-157">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d3ce5-158">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d3ce5-159">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d3ce5-160">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="d3ce5-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : a név elérhetősége tevékenység definíciójának ellenőrzése.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="d3ce5-162">`[Name <String>]`: Ellenőrizze az erőforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="d3ce5-163">`[ResourceType <String>]`: Az ellenőrizni kívánt erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="d3ce5-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="d3ce5-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3ce5-164">RELATED LINKS</span></span>

