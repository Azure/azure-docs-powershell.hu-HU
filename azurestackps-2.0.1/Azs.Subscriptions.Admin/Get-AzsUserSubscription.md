---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015339"
---
# <span data-ttu-id="e34cd-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e34cd-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="e34cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e34cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e34cd-103">A megadott előfizetés beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e34cd-103">Get a specified subscription.</span></span>

## <span data-ttu-id="e34cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e34cd-104">SYNTAX</span></span>

### <span data-ttu-id="e34cd-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e34cd-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e34cd-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e34cd-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e34cd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e34cd-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e34cd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e34cd-108">DESCRIPTION</span></span>
<span data-ttu-id="e34cd-109">A megadott előfizetés beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e34cd-109">Get a specified subscription.</span></span>

## <span data-ttu-id="e34cd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e34cd-110">EXAMPLES</span></span>

### <span data-ttu-id="e34cd-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e34cd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="e34cd-112">A felhasználói előfizetések listájának beszerzése operátorként.</span><span class="sxs-lookup"><span data-stu-id="e34cd-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="e34cd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e34cd-113">PARAMETERS</span></span>

### <span data-ttu-id="e34cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e34cd-114">-DefaultProfile</span></span>
<span data-ttu-id="e34cd-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e34cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e34cd-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="e34cd-116">-Filter</span></span>
<span data-ttu-id="e34cd-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="e34cd-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e34cd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e34cd-118">-InputObject</span></span>
<span data-ttu-id="e34cd-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e34cd-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e34cd-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e34cd-120">-SubscriptionId</span></span>
<span data-ttu-id="e34cd-121">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e34cd-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e34cd-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e34cd-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="e34cd-123">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="e34cd-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="e34cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e34cd-124">CommonParameters</span></span>
<span data-ttu-id="e34cd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e34cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e34cd-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e34cd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e34cd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e34cd-127">INPUTS</span></span>

### <span data-ttu-id="e34cd-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e34cd-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e34cd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e34cd-129">OUTPUTS</span></span>

### <span data-ttu-id="e34cd-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="e34cd-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="e34cd-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e34cd-131">ALIASES</span></span>

## <span data-ttu-id="e34cd-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e34cd-132">NOTES</span></span>

<span data-ttu-id="e34cd-133">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e34cd-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e34cd-134">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e34cd-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e34cd-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e34cd-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e34cd-136">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e34cd-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e34cd-137">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="e34cd-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e34cd-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e34cd-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e34cd-139">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="e34cd-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e34cd-140">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="e34cd-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e34cd-141">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="e34cd-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e34cd-142">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="e34cd-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e34cd-143">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="e34cd-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e34cd-144">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="e34cd-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e34cd-145">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="e34cd-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e34cd-146">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="e34cd-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e34cd-147">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="e34cd-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e34cd-148">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e34cd-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e34cd-149">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="e34cd-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e34cd-150">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="e34cd-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e34cd-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e34cd-151">RELATED LINKS</span></span>

