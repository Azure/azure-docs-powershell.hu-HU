---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016926"
---
# <span data-ttu-id="213f3-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="213f3-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="213f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="213f3-102">SYNOPSIS</span></span>
<span data-ttu-id="213f3-103">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="213f3-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="213f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="213f3-104">SYNTAX</span></span>

### <span data-ttu-id="213f3-105">UnlinkExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="213f3-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="213f3-106">Szétválasztása</span><span class="sxs-lookup"><span data-stu-id="213f3-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="213f3-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="213f3-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="213f3-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="213f3-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="213f3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="213f3-109">DESCRIPTION</span></span>
<span data-ttu-id="213f3-110">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="213f3-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="213f3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="213f3-111">EXAMPLES</span></span>

### <span data-ttu-id="213f3-112">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="213f3-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="213f3-113">Terv leválasztása egy ajánlatból.</span><span class="sxs-lookup"><span data-stu-id="213f3-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="213f3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="213f3-114">PARAMETERS</span></span>

### <span data-ttu-id="213f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213f3-115">-DefaultProfile</span></span>
<span data-ttu-id="213f3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="213f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="213f3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="213f3-117">-InputObject</span></span>
<span data-ttu-id="213f3-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="213f3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="213f3-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="213f3-120">A beszerzések maximális száma az előfizetőktől</span><span class="sxs-lookup"><span data-stu-id="213f3-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-121">-OfferName</span><span class="sxs-lookup"><span data-stu-id="213f3-121">-OfferName</span></span>
<span data-ttu-id="213f3-122">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="213f3-123">-PlanLink</span></span>
<span data-ttu-id="213f3-124">A csomagok ajánlatokra való hivatkozásának és leválasztásának definíciója.</span><span class="sxs-lookup"><span data-stu-id="213f3-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="213f3-125">A kivitelezéshez tekintse meg a PLANLINK tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="213f3-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="213f3-126">-PlanLinkType</span></span>
<span data-ttu-id="213f3-127">A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="213f3-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="213f3-128">-PlanName</span></span>
<span data-ttu-id="213f3-129">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="213f3-131">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="213f3-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="213f3-132">-SubscriptionId</span></span>
<span data-ttu-id="213f3-133">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="213f3-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="213f3-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="213f3-134">-Confirm</span></span>
<span data-ttu-id="213f3-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="213f3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="213f3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="213f3-136">-WhatIf</span></span>
<span data-ttu-id="213f3-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="213f3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="213f3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="213f3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="213f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213f3-139">CommonParameters</span></span>
<span data-ttu-id="213f3-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="213f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213f3-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="213f3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213f3-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="213f3-142">INPUTS</span></span>

### <span data-ttu-id="213f3-143">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="213f3-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="213f3-144">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="213f3-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="213f3-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="213f3-145">OUTPUTS</span></span>

### <span data-ttu-id="213f3-146">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="213f3-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="213f3-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="213f3-147">ALIASES</span></span>

## <span data-ttu-id="213f3-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="213f3-148">NOTES</span></span>

<span data-ttu-id="213f3-149">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="213f3-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="213f3-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="213f3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="213f3-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="213f3-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="213f3-152">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="213f3-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="213f3-153">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="213f3-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="213f3-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="213f3-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="213f3-155">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="213f3-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="213f3-156">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="213f3-157">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="213f3-158">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="213f3-159">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="213f3-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="213f3-160">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="213f3-161">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="213f3-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="213f3-162">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="213f3-163">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="213f3-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="213f3-164">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="213f3-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="213f3-165">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="213f3-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="213f3-166">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="213f3-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="213f3-167">PLANLINK <IPlanLinkDefinition> : definíció a csomagok ajánlatokra való összekapcsolásához és leválasztásához.</span><span class="sxs-lookup"><span data-stu-id="213f3-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="213f3-168">`[MaxAcquisitionCount <Int32?>]`: A részesedésszerzések maximális száma az előfizetők szerint</span><span class="sxs-lookup"><span data-stu-id="213f3-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="213f3-169">`[PlanLinkType <PlanLinkType?>]`: A terv hivatkozásának típusa.</span><span class="sxs-lookup"><span data-stu-id="213f3-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="213f3-170">`[PlanName <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="213f3-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="213f3-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="213f3-171">RELATED LINKS</span></span>

