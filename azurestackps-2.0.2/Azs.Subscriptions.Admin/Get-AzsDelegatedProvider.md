---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017121"
---
# <span data-ttu-id="d37e5-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="d37e5-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="d37e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d37e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d37e5-103">A megadott delegált szolgáltató beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d37e5-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="d37e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d37e5-104">SYNTAX</span></span>

### <span data-ttu-id="d37e5-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d37e5-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d37e5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d37e5-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d37e5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d37e5-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d37e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d37e5-108">DESCRIPTION</span></span>
<span data-ttu-id="d37e5-109">A megadott delegált szolgáltató beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d37e5-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="d37e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d37e5-110">EXAMPLES</span></span>

### <span data-ttu-id="d37e5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d37e5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="d37e5-112">Adott delegált szolgáltató beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d37e5-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="d37e5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d37e5-113">PARAMETERS</span></span>

### <span data-ttu-id="d37e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37e5-114">-DefaultProfile</span></span>
<span data-ttu-id="d37e5-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d37e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37e5-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="d37e5-116">-DelegatedProviderId</span></span>
<span data-ttu-id="d37e5-117">DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d37e5-117">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="d37e5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d37e5-118">-InputObject</span></span>
<span data-ttu-id="d37e5-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d37e5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d37e5-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d37e5-120">-SubscriptionId</span></span>
<span data-ttu-id="d37e5-121">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d37e5-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d37e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37e5-122">CommonParameters</span></span>
<span data-ttu-id="d37e5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d37e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37e5-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d37e5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37e5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37e5-125">INPUTS</span></span>

### <span data-ttu-id="d37e5-126">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d37e5-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d37e5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37e5-127">OUTPUTS</span></span>

### <span data-ttu-id="d37e5-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="d37e5-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="d37e5-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d37e5-129">ALIASES</span></span>

## <span data-ttu-id="d37e5-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d37e5-130">NOTES</span></span>

<span data-ttu-id="d37e5-131">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d37e5-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d37e5-132">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d37e5-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d37e5-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d37e5-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d37e5-134">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d37e5-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d37e5-135">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d37e5-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d37e5-136">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d37e5-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d37e5-137">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="d37e5-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d37e5-138">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="d37e5-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d37e5-139">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="d37e5-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d37e5-140">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="d37e5-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d37e5-141">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="d37e5-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d37e5-142">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="d37e5-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d37e5-143">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="d37e5-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d37e5-144">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="d37e5-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d37e5-145">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="d37e5-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d37e5-146">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d37e5-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d37e5-147">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="d37e5-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d37e5-148">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="d37e5-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="d37e5-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d37e5-149">RELATED LINKS</span></span>

