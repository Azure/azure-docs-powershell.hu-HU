---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015287"
---
# <span data-ttu-id="95dfb-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="95dfb-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="95dfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="95dfb-103">A megadott ajánlat delegációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="95dfb-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="95dfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95dfb-104">SYNTAX</span></span>

### <span data-ttu-id="95dfb-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95dfb-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="95dfb-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="95dfb-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="95dfb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="95dfb-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="95dfb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="95dfb-108">DESCRIPTION</span></span>
<span data-ttu-id="95dfb-109">A megadott ajánlat delegációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="95dfb-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="95dfb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="95dfb-110">EXAMPLES</span></span>

### <span data-ttu-id="95dfb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="95dfb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="95dfb-112">A delegált ajánlatok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="95dfb-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="95dfb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95dfb-113">PARAMETERS</span></span>

### <span data-ttu-id="95dfb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95dfb-114">-DefaultProfile</span></span>
<span data-ttu-id="95dfb-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95dfb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95dfb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95dfb-116">-InputObject</span></span>
<span data-ttu-id="95dfb-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="95dfb-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="95dfb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95dfb-118">-Name</span></span>
<span data-ttu-id="95dfb-119">Az ajánlat delegációjának neve</span><span class="sxs-lookup"><span data-stu-id="95dfb-119">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95dfb-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="95dfb-120">-OfferName</span></span>
<span data-ttu-id="95dfb-121">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="95dfb-121">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95dfb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95dfb-122">-ResourceGroupName</span></span>
<span data-ttu-id="95dfb-123">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="95dfb-123">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95dfb-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95dfb-124">-SubscriptionId</span></span>
<span data-ttu-id="95dfb-125">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="95dfb-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="95dfb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95dfb-126">CommonParameters</span></span>
<span data-ttu-id="95dfb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95dfb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95dfb-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="95dfb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95dfb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95dfb-129">INPUTS</span></span>

### <span data-ttu-id="95dfb-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="95dfb-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="95dfb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95dfb-131">OUTPUTS</span></span>

### <span data-ttu-id="95dfb-132">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="95dfb-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="95dfb-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="95dfb-133">ALIASES</span></span>

## <span data-ttu-id="95dfb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95dfb-134">NOTES</span></span>

<span data-ttu-id="95dfb-135">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="95dfb-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95dfb-136">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="95dfb-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="95dfb-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="95dfb-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95dfb-138">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="95dfb-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="95dfb-139">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="95dfb-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="95dfb-140">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="95dfb-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95dfb-141">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="95dfb-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="95dfb-142">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="95dfb-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="95dfb-143">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="95dfb-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="95dfb-144">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="95dfb-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="95dfb-145">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="95dfb-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="95dfb-146">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="95dfb-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="95dfb-147">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="95dfb-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="95dfb-148">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="95dfb-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="95dfb-149">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="95dfb-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="95dfb-150">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="95dfb-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="95dfb-151">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="95dfb-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="95dfb-152">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="95dfb-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="95dfb-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95dfb-153">RELATED LINKS</span></span>

