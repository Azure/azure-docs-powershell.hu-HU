---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016930"
---
# <span data-ttu-id="9c2a4-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="9c2a4-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="9c2a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2a4-103">Törölje a megadott ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="9c2a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c2a4-104">SYNTAX</span></span>

### <span data-ttu-id="9c2a4-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c2a4-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9c2a4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9c2a4-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c2a4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c2a4-107">DESCRIPTION</span></span>
<span data-ttu-id="9c2a4-108">Törölje a megadott ajánlat-delegálást.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="9c2a4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9c2a4-109">EXAMPLES</span></span>

### <span data-ttu-id="9c2a4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c2a4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="9c2a4-111">Az ajánlat-delegálás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9c2a4-111">Removes the offer delegation</span></span>

## <span data-ttu-id="9c2a4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c2a4-112">PARAMETERS</span></span>

### <span data-ttu-id="9c2a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2a4-113">-DefaultProfile</span></span>
<span data-ttu-id="9c2a4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c2a4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c2a4-115">-InputObject</span></span>
<span data-ttu-id="9c2a4-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9c2a4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c2a4-117">-Name</span></span>
<span data-ttu-id="9c2a4-118">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="9c2a4-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2a4-119">-OfferName</span><span class="sxs-lookup"><span data-stu-id="9c2a4-119">-OfferName</span></span>
<span data-ttu-id="9c2a4-120">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2a4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c2a4-121">-PassThru</span></span>
<span data-ttu-id="9c2a4-122">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="9c2a4-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9c2a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c2a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c2a4-124">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-124">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2a4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c2a4-125">-SubscriptionId</span></span>
<span data-ttu-id="9c2a4-126">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2a4-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c2a4-127">-Confirm</span></span>
<span data-ttu-id="9c2a4-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c2a4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2a4-129">-WhatIf</span></span>
<span data-ttu-id="9c2a4-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c2a4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c2a4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2a4-132">CommonParameters</span></span>
<span data-ttu-id="9c2a4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c2a4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2a4-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2a4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c2a4-135">INPUTS</span></span>

### <span data-ttu-id="9c2a4-136">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9c2a4-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9c2a4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c2a4-137">OUTPUTS</span></span>

### <span data-ttu-id="9c2a4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c2a4-138">System.Boolean</span></span>

<span data-ttu-id="9c2a4-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9c2a4-139">ALIASES</span></span>

## <span data-ttu-id="9c2a4-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c2a4-140">NOTES</span></span>

<span data-ttu-id="9c2a4-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c2a4-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9c2a4-143">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="9c2a4-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c2a4-144">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9c2a4-145">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9c2a4-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="9c2a4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c2a4-147">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9c2a4-148">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9c2a4-149">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9c2a4-150">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9c2a4-151">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9c2a4-152">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9c2a4-153">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="9c2a4-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9c2a4-154">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9c2a4-155">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9c2a4-156">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9c2a4-157">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9c2a4-158">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="9c2a4-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="9c2a4-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c2a4-159">RELATED LINKS</span></span>

