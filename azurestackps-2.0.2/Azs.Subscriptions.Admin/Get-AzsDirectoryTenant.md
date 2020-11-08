---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016874"
---
# <span data-ttu-id="05e8a-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="05e8a-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="05e8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="05e8a-103">Címtár-bérlői fiók kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="05e8a-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="05e8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05e8a-104">SYNTAX</span></span>

### <span data-ttu-id="05e8a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05e8a-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="05e8a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="05e8a-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05e8a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05e8a-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="05e8a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="05e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="05e8a-109">Címtár-bérlői fiók kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="05e8a-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="05e8a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="05e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="05e8a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="05e8a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="05e8a-112">Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="05e8a-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="05e8a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05e8a-113">PARAMETERS</span></span>

### <span data-ttu-id="05e8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e8a-114">-DefaultProfile</span></span>
<span data-ttu-id="05e8a-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05e8a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05e8a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05e8a-116">-InputObject</span></span>
<span data-ttu-id="05e8a-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05e8a-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05e8a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05e8a-118">-Name</span></span>
<span data-ttu-id="05e8a-119">Címtár-bérlő neve</span><span class="sxs-lookup"><span data-stu-id="05e8a-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="05e8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="05e8a-121">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="05e8a-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="05e8a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05e8a-122">-SubscriptionId</span></span>
<span data-ttu-id="05e8a-123">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="05e8a-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="05e8a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e8a-124">CommonParameters</span></span>
<span data-ttu-id="05e8a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05e8a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e8a-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05e8a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e8a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05e8a-127">INPUTS</span></span>

### <span data-ttu-id="05e8a-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="05e8a-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="05e8a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05e8a-129">OUTPUTS</span></span>

### <span data-ttu-id="05e8a-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="05e8a-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="05e8a-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="05e8a-131">ALIASES</span></span>

## <span data-ttu-id="05e8a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05e8a-132">NOTES</span></span>

<span data-ttu-id="05e8a-133">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="05e8a-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05e8a-134">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="05e8a-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="05e8a-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="05e8a-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05e8a-136">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="05e8a-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="05e8a-137">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="05e8a-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="05e8a-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="05e8a-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05e8a-139">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="05e8a-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="05e8a-140">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="05e8a-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="05e8a-141">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="05e8a-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="05e8a-142">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="05e8a-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="05e8a-143">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="05e8a-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="05e8a-144">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="05e8a-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="05e8a-145">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="05e8a-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="05e8a-146">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="05e8a-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="05e8a-147">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="05e8a-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="05e8a-148">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="05e8a-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="05e8a-149">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="05e8a-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="05e8a-150">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="05e8a-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="05e8a-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05e8a-151">RELATED LINKS</span></span>

