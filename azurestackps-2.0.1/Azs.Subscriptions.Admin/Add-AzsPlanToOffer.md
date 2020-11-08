---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/add-azsplantooffer
schema: 2.0.0
ms.openlocfilehash: 65691116ea8e73e8f03e8cc7dc97f38c61ecebdb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015240"
---
# <span data-ttu-id="14a3e-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="14a3e-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="14a3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="14a3e-103">Összekapcsolja a csomagot az ajánlattal.</span><span class="sxs-lookup"><span data-stu-id="14a3e-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="14a3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14a3e-104">SYNTAX</span></span>

### <span data-ttu-id="14a3e-105">LinkExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14a3e-105">LinkExpanded (Default)</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14a3e-106">Hivatkozás</span><span class="sxs-lookup"><span data-stu-id="14a3e-106">Link</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14a3e-107">LinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14a3e-107">LinkViaIdentity</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14a3e-108">LinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="14a3e-108">LinkViaIdentityExpanded</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="14a3e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="14a3e-109">DESCRIPTION</span></span>
<span data-ttu-id="14a3e-110">Összekapcsolja a csomagot az ajánlattal.</span><span class="sxs-lookup"><span data-stu-id="14a3e-110">Links a plan to an offer.</span></span>

## <span data-ttu-id="14a3e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="14a3e-111">EXAMPLES</span></span>

### <span data-ttu-id="14a3e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="14a3e-112">Example 1</span></span>
```powershell
PS C:\> Add-AzsPlanToOffer -PlanName "addonplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg" -MaxAcquisitionCount 18

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="14a3e-113">Összekapcsolja a csomagot az ajánlattal.</span><span class="sxs-lookup"><span data-stu-id="14a3e-113">Links a plan to an offer.</span></span>

## <span data-ttu-id="14a3e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14a3e-114">PARAMETERS</span></span>

### <span data-ttu-id="14a3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a3e-115">-DefaultProfile</span></span>
<span data-ttu-id="14a3e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14a3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a3e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a3e-117">-InputObject</span></span>
<span data-ttu-id="14a3e-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14a3e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: LinkViaIdentity, LinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="14a3e-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="14a3e-120">A beszerzések maximális száma az előfizetőktől</span><span class="sxs-lookup"><span data-stu-id="14a3e-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-121">-OfferName</span><span class="sxs-lookup"><span data-stu-id="14a3e-121">-OfferName</span></span>
<span data-ttu-id="14a3e-122">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="14a3e-123">-PlanLink</span></span>
<span data-ttu-id="14a3e-124">A csomagok ajánlatokra való hivatkozásának és leválasztásának definíciója.</span><span class="sxs-lookup"><span data-stu-id="14a3e-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="14a3e-125">A kivitelezéshez tekintse meg a PLANLINK tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="14a3e-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Link, LinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="14a3e-126">-PlanLinkType</span></span>
<span data-ttu-id="14a3e-127">A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="14a3e-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="14a3e-128">-PlanName</span></span>
<span data-ttu-id="14a3e-129">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a3e-130">-ResourceGroupName</span></span>
<span data-ttu-id="14a3e-131">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="14a3e-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14a3e-132">-SubscriptionId</span></span>
<span data-ttu-id="14a3e-133">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="14a3e-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="14a3e-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14a3e-134">-Confirm</span></span>
<span data-ttu-id="14a3e-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14a3e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a3e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a3e-136">-WhatIf</span></span>
<span data-ttu-id="14a3e-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14a3e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a3e-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14a3e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a3e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a3e-139">CommonParameters</span></span>
<span data-ttu-id="14a3e-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14a3e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a3e-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14a3e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a3e-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14a3e-142">INPUTS</span></span>

### <span data-ttu-id="14a3e-143">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="14a3e-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="14a3e-144">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="14a3e-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="14a3e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14a3e-145">OUTPUTS</span></span>

### <span data-ttu-id="14a3e-146">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="14a3e-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="14a3e-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="14a3e-147">ALIASES</span></span>

## <span data-ttu-id="14a3e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14a3e-148">NOTES</span></span>

<span data-ttu-id="14a3e-149">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="14a3e-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14a3e-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="14a3e-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="14a3e-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="14a3e-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14a3e-152">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="14a3e-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="14a3e-153">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="14a3e-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="14a3e-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="14a3e-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14a3e-155">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="14a3e-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="14a3e-156">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="14a3e-157">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="14a3e-158">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="14a3e-159">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="14a3e-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="14a3e-160">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="14a3e-161">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="14a3e-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="14a3e-162">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="14a3e-163">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="14a3e-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="14a3e-164">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="14a3e-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="14a3e-165">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="14a3e-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="14a3e-166">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="14a3e-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="14a3e-167">PLANLINK <IPlanLinkDefinition> : definíció a csomagok ajánlatokra való összekapcsolásához és leválasztásához.</span><span class="sxs-lookup"><span data-stu-id="14a3e-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="14a3e-168">`[MaxAcquisitionCount <Int32?>]`: A részesedésszerzések maximális száma az előfizetők szerint</span><span class="sxs-lookup"><span data-stu-id="14a3e-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="14a3e-169">`[PlanLinkType <PlanLinkType?>]`: A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="14a3e-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="14a3e-170">`[PlanName <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="14a3e-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="14a3e-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14a3e-171">RELATED LINKS</span></span>

