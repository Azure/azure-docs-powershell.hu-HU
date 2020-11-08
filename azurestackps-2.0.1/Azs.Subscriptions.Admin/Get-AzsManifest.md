---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsmanifest
schema: 2.0.0
ms.openlocfilehash: 4e5ccedc67af31c19d35e5a91fad62ba46535ed7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015374"
---
# <span data-ttu-id="94ea1-101">Get-AzsManifest</span><span class="sxs-lookup"><span data-stu-id="94ea1-101">Get-AzsManifest</span></span>

## <span data-ttu-id="94ea1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="94ea1-103">A megadott jegyzékfájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="94ea1-103">Get the specified manifest.</span></span>

## <span data-ttu-id="94ea1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94ea1-104">SYNTAX</span></span>

### <span data-ttu-id="94ea1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94ea1-105">List (Default)</span></span>
```
Get-AzsManifest [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94ea1-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="94ea1-106">Get</span></span>
```
Get-AzsManifest -ManifestName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="94ea1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94ea1-107">GetViaIdentity</span></span>
```
Get-AzsManifest -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="94ea1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="94ea1-108">DESCRIPTION</span></span>
<span data-ttu-id="94ea1-109">A megadott jegyzékfájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="94ea1-109">Get the specified manifest.</span></span>

## <span data-ttu-id="94ea1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="94ea1-110">EXAMPLES</span></span>

### <span data-ttu-id="94ea1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94ea1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsManifest

Name     : Microsoft-Authorization-Admin--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata

Name     : Microsoft-Authorization--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata
```

<span data-ttu-id="94ea1-112">Felsorolja a jelenlegi előfizetés alatti összes jegyzékfájlt.</span><span class="sxs-lookup"><span data-stu-id="94ea1-112">Lists all the manifests under the current subscription.</span></span>

## <span data-ttu-id="94ea1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94ea1-113">PARAMETERS</span></span>

### <span data-ttu-id="94ea1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ea1-114">-DefaultProfile</span></span>
<span data-ttu-id="94ea1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94ea1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94ea1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94ea1-116">-InputObject</span></span>
<span data-ttu-id="94ea1-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94ea1-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94ea1-118">-ManifestName</span><span class="sxs-lookup"><span data-stu-id="94ea1-118">-ManifestName</span></span>
<span data-ttu-id="94ea1-119">A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="94ea1-119">The manifest name.</span></span>

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

### <span data-ttu-id="94ea1-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94ea1-120">-SubscriptionId</span></span>
<span data-ttu-id="94ea1-121">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94ea1-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94ea1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ea1-122">CommonParameters</span></span>
<span data-ttu-id="94ea1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94ea1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ea1-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94ea1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ea1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94ea1-125">INPUTS</span></span>

### <span data-ttu-id="94ea1-126">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="94ea1-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="94ea1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94ea1-127">OUTPUTS</span></span>

### <span data-ttu-id="94ea1-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IManifest</span><span class="sxs-lookup"><span data-stu-id="94ea1-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IManifest</span></span>

<span data-ttu-id="94ea1-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="94ea1-129">ALIASES</span></span>

## <span data-ttu-id="94ea1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94ea1-130">NOTES</span></span>

<span data-ttu-id="94ea1-131">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="94ea1-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94ea1-132">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="94ea1-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="94ea1-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="94ea1-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94ea1-134">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="94ea1-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="94ea1-135">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="94ea1-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="94ea1-136">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="94ea1-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94ea1-137">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="94ea1-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="94ea1-138">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="94ea1-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="94ea1-139">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="94ea1-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="94ea1-140">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="94ea1-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="94ea1-141">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="94ea1-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="94ea1-142">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="94ea1-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="94ea1-143">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="94ea1-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="94ea1-144">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="94ea1-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="94ea1-145">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="94ea1-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="94ea1-146">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="94ea1-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="94ea1-147">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="94ea1-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="94ea1-148">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="94ea1-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="94ea1-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94ea1-149">RELATED LINKS</span></span>

