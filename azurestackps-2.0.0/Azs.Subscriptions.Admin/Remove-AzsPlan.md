---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015111"
---
# <span data-ttu-id="d1654-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="d1654-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="d1654-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1654-102">SYNOPSIS</span></span>
<span data-ttu-id="d1654-103">A megadott csomag törlése</span><span class="sxs-lookup"><span data-stu-id="d1654-103">Delete the specified plan.</span></span>

## <span data-ttu-id="d1654-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1654-104">SYNTAX</span></span>

### <span data-ttu-id="d1654-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1654-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1654-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1654-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1654-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1654-107">DESCRIPTION</span></span>
<span data-ttu-id="d1654-108">A megadott csomag törlése</span><span class="sxs-lookup"><span data-stu-id="d1654-108">Delete the specified plan.</span></span>

## <span data-ttu-id="d1654-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d1654-109">EXAMPLES</span></span>

### <span data-ttu-id="d1654-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d1654-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

<span data-ttu-id="d1654-111">A megadott csomag törlése</span><span class="sxs-lookup"><span data-stu-id="d1654-111">Delete the specified plan</span></span>

## <span data-ttu-id="d1654-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1654-112">PARAMETERS</span></span>

### <span data-ttu-id="d1654-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1654-113">-DefaultProfile</span></span>
<span data-ttu-id="d1654-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1654-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1654-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1654-115">-InputObject</span></span>
<span data-ttu-id="d1654-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d1654-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1654-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1654-117">-Name</span></span>
<span data-ttu-id="d1654-118">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="d1654-118">Name of the plan.</span></span>

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

### <span data-ttu-id="d1654-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1654-119">-PassThru</span></span>
<span data-ttu-id="d1654-120">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="d1654-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d1654-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1654-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1654-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="d1654-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d1654-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1654-123">-SubscriptionId</span></span>
<span data-ttu-id="d1654-124">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d1654-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d1654-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1654-125">-Confirm</span></span>
<span data-ttu-id="d1654-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1654-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1654-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1654-127">-WhatIf</span></span>
<span data-ttu-id="d1654-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1654-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1654-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1654-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1654-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1654-130">CommonParameters</span></span>
<span data-ttu-id="d1654-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1654-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1654-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d1654-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1654-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1654-133">INPUTS</span></span>

### <span data-ttu-id="d1654-134">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d1654-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d1654-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1654-135">OUTPUTS</span></span>

### <span data-ttu-id="d1654-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1654-136">System.Boolean</span></span>

<span data-ttu-id="d1654-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d1654-137">ALIASES</span></span>

## <span data-ttu-id="d1654-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1654-138">NOTES</span></span>

<span data-ttu-id="d1654-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d1654-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1654-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d1654-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d1654-141">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d1654-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1654-142">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d1654-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d1654-143">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d1654-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d1654-144">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d1654-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1654-145">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="d1654-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d1654-146">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="d1654-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d1654-147">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="d1654-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d1654-148">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="d1654-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d1654-149">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="d1654-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d1654-150">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="d1654-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d1654-151">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="d1654-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d1654-152">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="d1654-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d1654-153">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="d1654-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d1654-154">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d1654-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d1654-155">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d1654-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d1654-156">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="d1654-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="d1654-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1654-157">RELATED LINKS</span></span>

