---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016923"
---
# <span data-ttu-id="d8d6c-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="d8d6c-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="d8d6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8d6c-102">SYNOPSIS</span></span>


## <span data-ttu-id="d8d6c-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8d6c-103">SYNTAX</span></span>

### <span data-ttu-id="d8d6c-104">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8d6c-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8d6c-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8d6c-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8d6c-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8d6c-106">DESCRIPTION</span></span>


## <span data-ttu-id="d8d6c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d8d6c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d6c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d8d6c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="d8d6c-109">Törölje a megadott bérlői előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="d8d6c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8d6c-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d6c-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="d8d6c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d8d6c-112">-Force</span></span>


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

### <span data-ttu-id="d8d6c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8d6c-113">-InputObject</span></span>
<span data-ttu-id="d8d6c-114">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8d6c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8d6c-115">-PassThru</span></span>


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

### <span data-ttu-id="d8d6c-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8d6c-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="d8d6c-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8d6c-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="d8d6c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8d6c-118">-Confirm</span></span>
<span data-ttu-id="d8d6c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d6c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d6c-120">-WhatIf</span></span>
<span data-ttu-id="d8d6c-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d6c-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d6c-123">CommonParameters</span></span>
<span data-ttu-id="d8d6c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8d6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d6c-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d6c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8d6c-126">INPUTS</span></span>

### <span data-ttu-id="d8d6c-127">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d8d6c-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d8d6c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8d6c-128">OUTPUTS</span></span>

### <span data-ttu-id="d8d6c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8d6c-129">System.Boolean</span></span>

<span data-ttu-id="d8d6c-130">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d8d6c-130">ALIASES</span></span>

## <span data-ttu-id="d8d6c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8d6c-131">NOTES</span></span>

<span data-ttu-id="d8d6c-132">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8d6c-133">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d8d6c-134">INPUTOBJECT <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="d8d6c-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="d8d6c-135">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d8d6c-136">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d8d6c-137">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d8d6c-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8d6c-138">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d8d6c-139">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d8d6c-140">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d8d6c-141">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d8d6c-142">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d8d6c-143">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d8d6c-144">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="d8d6c-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d8d6c-145">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d8d6c-146">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d8d6c-147">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d8d6c-148">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d8d6c-149">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="d8d6c-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="d8d6c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8d6c-150">RELATED LINKS</span></span>

