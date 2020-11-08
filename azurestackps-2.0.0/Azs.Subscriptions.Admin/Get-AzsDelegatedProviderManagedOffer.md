---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015136"
---
# <span data-ttu-id="01f69-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="01f69-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="01f69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01f69-102">SYNOPSIS</span></span>
<span data-ttu-id="01f69-103">A megadott delegált szolgáltató ajánlatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="01f69-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="01f69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01f69-104">SYNTAX</span></span>

### <span data-ttu-id="01f69-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01f69-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="01f69-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="01f69-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="01f69-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01f69-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="01f69-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="01f69-108">DESCRIPTION</span></span>
<span data-ttu-id="01f69-109">A megadott delegált szolgáltató ajánlatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="01f69-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="01f69-110">Példák</span><span class="sxs-lookup"><span data-stu-id="01f69-110">EXAMPLES</span></span>

### <span data-ttu-id="01f69-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="01f69-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="01f69-112">A delegált szolgáltatói ajánlatok listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="01f69-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="01f69-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01f69-113">PARAMETERS</span></span>

### <span data-ttu-id="01f69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f69-114">-DefaultProfile</span></span>
<span data-ttu-id="01f69-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01f69-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01f69-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01f69-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="01f69-117">Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="01f69-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="01f69-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01f69-118">-InputObject</span></span>
<span data-ttu-id="01f69-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01f69-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="01f69-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="01f69-120">-Name</span></span>
<span data-ttu-id="01f69-121">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="01f69-121">Name of an offer.</span></span>

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

### <span data-ttu-id="01f69-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01f69-122">-SubscriptionId</span></span>
<span data-ttu-id="01f69-123">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="01f69-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="01f69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f69-124">CommonParameters</span></span>
<span data-ttu-id="01f69-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01f69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f69-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01f69-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f69-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01f69-127">INPUTS</span></span>

### <span data-ttu-id="01f69-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="01f69-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="01f69-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01f69-129">OUTPUTS</span></span>

### <span data-ttu-id="01f69-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="01f69-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="01f69-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="01f69-131">ALIASES</span></span>

## <span data-ttu-id="01f69-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01f69-132">NOTES</span></span>

<span data-ttu-id="01f69-133">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="01f69-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01f69-134">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="01f69-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="01f69-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="01f69-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01f69-136">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="01f69-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="01f69-137">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="01f69-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="01f69-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="01f69-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01f69-139">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="01f69-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="01f69-140">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="01f69-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="01f69-141">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="01f69-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="01f69-142">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="01f69-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="01f69-143">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="01f69-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="01f69-144">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="01f69-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="01f69-145">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="01f69-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="01f69-146">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="01f69-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="01f69-147">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="01f69-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="01f69-148">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="01f69-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="01f69-149">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="01f69-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="01f69-150">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="01f69-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="01f69-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01f69-151">RELATED LINKS</span></span>

