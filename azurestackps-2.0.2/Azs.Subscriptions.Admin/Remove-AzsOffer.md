---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsoffer
schema: 2.0.0
ms.openlocfilehash: d38c7493e49888fe638cae4fbb5cb937ec41ccba
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016604"
---
# <span data-ttu-id="f3b3f-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="f3b3f-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="f3b3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b3f-103">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="f3b3f-103">Delete the specified offer.</span></span>

## <span data-ttu-id="f3b3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3b3f-104">SYNTAX</span></span>

### <span data-ttu-id="f3b3f-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3b3f-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3b3f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3b3f-106">DeleteViaIdentity</span></span>
```
Remove-AzsOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3b3f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3b3f-107">DESCRIPTION</span></span>
<span data-ttu-id="f3b3f-108">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="f3b3f-108">Delete the specified offer.</span></span>

## <span data-ttu-id="f3b3f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f3b3f-109">EXAMPLES</span></span>

### <span data-ttu-id="f3b3f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f3b3f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOffer -Name "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="f3b3f-111">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="f3b3f-111">Delete the specified offer.</span></span>

## <span data-ttu-id="f3b3f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3b3f-112">PARAMETERS</span></span>

### <span data-ttu-id="f3b3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b3f-113">-DefaultProfile</span></span>
<span data-ttu-id="f3b3f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3b3f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3b3f-115">-InputObject</span></span>
<span data-ttu-id="f3b3f-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3b3f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3b3f-117">-Name</span></span>
<span data-ttu-id="f3b3f-118">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-118">Name of an offer.</span></span>

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

### <span data-ttu-id="f3b3f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3b3f-119">-PassThru</span></span>
<span data-ttu-id="f3b3f-120">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="f3b3f-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3b3f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b3f-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3b3f-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f3b3f-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3b3f-123">-SubscriptionId</span></span>
<span data-ttu-id="f3b3f-124">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f3b3f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3b3f-125">-Confirm</span></span>
<span data-ttu-id="f3b3f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b3f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b3f-127">-WhatIf</span></span>
<span data-ttu-id="f3b3f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3b3f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b3f-130">CommonParameters</span></span>
<span data-ttu-id="f3b3f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3b3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b3f-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b3f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3b3f-133">INPUTS</span></span>

### <span data-ttu-id="f3b3f-134">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f3b3f-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="f3b3f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3b3f-135">OUTPUTS</span></span>

### <span data-ttu-id="f3b3f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b3f-136">System.Boolean</span></span>

<span data-ttu-id="f3b3f-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f3b3f-137">ALIASES</span></span>

## <span data-ttu-id="f3b3f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3b3f-138">NOTES</span></span>

<span data-ttu-id="f3b3f-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3b3f-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f3b3f-141">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f3b3f-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3b3f-142">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="f3b3f-143">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="f3b3f-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f3b3f-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3b3f-145">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="f3b3f-146">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="f3b3f-147">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="f3b3f-148">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="f3b3f-149">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="f3b3f-150">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="f3b3f-151">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="f3b3f-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="f3b3f-152">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f3b3f-153">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="f3b3f-154">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f3b3f-155">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="f3b3f-156">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="f3b3f-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="f3b3f-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3b3f-157">RELATED LINKS</span></span>

