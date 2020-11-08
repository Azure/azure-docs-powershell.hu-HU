---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015113"
---
# <span data-ttu-id="b6581-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="b6581-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="b6581-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6581-102">SYNOPSIS</span></span>
<span data-ttu-id="b6581-103">Megvásárolt csomag törlése</span><span class="sxs-lookup"><span data-stu-id="b6581-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="b6581-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6581-104">SYNTAX</span></span>

### <span data-ttu-id="b6581-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6581-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6581-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6581-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6581-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6581-107">DESCRIPTION</span></span>
<span data-ttu-id="b6581-108">Megvásárolt csomag törlése</span><span class="sxs-lookup"><span data-stu-id="b6581-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="b6581-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b6581-109">EXAMPLES</span></span>

### <span data-ttu-id="b6581-110">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="b6581-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="b6581-111">A megvásárolt csomag törlése</span><span class="sxs-lookup"><span data-stu-id="b6581-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="b6581-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6581-112">PARAMETERS</span></span>

### <span data-ttu-id="b6581-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6581-113">-DefaultProfile</span></span>
<span data-ttu-id="b6581-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6581-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6581-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6581-115">-InputObject</span></span>
<span data-ttu-id="b6581-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6581-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6581-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6581-117">-PassThru</span></span>
<span data-ttu-id="b6581-118">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="b6581-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b6581-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="b6581-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="b6581-120">A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="b6581-120">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="b6581-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6581-121">-SubscriptionId</span></span>
<span data-ttu-id="b6581-122">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b6581-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b6581-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6581-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="b6581-124">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b6581-124">The target subscription ID.</span></span>

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

### <span data-ttu-id="b6581-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6581-125">-Confirm</span></span>
<span data-ttu-id="b6581-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6581-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6581-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6581-127">-WhatIf</span></span>
<span data-ttu-id="b6581-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6581-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6581-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6581-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6581-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6581-130">CommonParameters</span></span>
<span data-ttu-id="b6581-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6581-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6581-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6581-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6581-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6581-133">INPUTS</span></span>

### <span data-ttu-id="b6581-134">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b6581-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b6581-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6581-135">OUTPUTS</span></span>

### <span data-ttu-id="b6581-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6581-136">System.Boolean</span></span>

<span data-ttu-id="b6581-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b6581-137">ALIASES</span></span>

### <span data-ttu-id="b6581-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="b6581-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="b6581-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6581-139">NOTES</span></span>

<span data-ttu-id="b6581-140">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b6581-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6581-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b6581-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b6581-142">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b6581-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6581-143">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b6581-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b6581-144">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b6581-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b6581-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b6581-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6581-146">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="b6581-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b6581-147">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="b6581-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b6581-148">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="b6581-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b6581-149">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="b6581-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b6581-150">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="b6581-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b6581-151">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="b6581-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b6581-152">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="b6581-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b6581-153">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="b6581-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b6581-154">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="b6581-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b6581-155">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b6581-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b6581-156">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b6581-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b6581-157">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="b6581-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b6581-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6581-158">RELATED LINKS</span></span>

