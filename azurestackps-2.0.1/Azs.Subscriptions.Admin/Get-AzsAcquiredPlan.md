---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015157"
---
# <span data-ttu-id="3a6c0-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="3a6c0-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="3a6c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6c0-103">Az ajánlat előfizetése által elfogyasztott előfizetéssel szerzi be a megadott csomagot.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="3a6c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a6c0-104">SYNTAX</span></span>

### <span data-ttu-id="3a6c0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a6c0-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a6c0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="3a6c0-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a6c0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a6c0-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a6c0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a6c0-108">DESCRIPTION</span></span>
<span data-ttu-id="3a6c0-109">Az ajánlat előfizetése által elfogyasztott előfizetéssel szerzi be a megadott csomagot.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="3a6c0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3a6c0-110">EXAMPLES</span></span>

### <span data-ttu-id="3a6c0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3a6c0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="3a6c0-112">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="3a6c0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a6c0-113">PARAMETERS</span></span>

### <span data-ttu-id="3a6c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6c0-114">-DefaultProfile</span></span>
<span data-ttu-id="3a6c0-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6c0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a6c0-116">-InputObject</span></span>
<span data-ttu-id="3a6c0-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a6c0-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="3a6c0-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="3a6c0-119">A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="3a6c0-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="3a6c0-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a6c0-120">-SubscriptionId</span></span>
<span data-ttu-id="3a6c0-121">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a6c0-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a6c0-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="3a6c0-123">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="3a6c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6c0-124">CommonParameters</span></span>
<span data-ttu-id="3a6c0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a6c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6c0-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6c0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a6c0-127">INPUTS</span></span>

### <span data-ttu-id="3a6c0-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3a6c0-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3a6c0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a6c0-129">OUTPUTS</span></span>

### <span data-ttu-id="3a6c0-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="3a6c0-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="3a6c0-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3a6c0-131">ALIASES</span></span>

<span data-ttu-id="3a6c0-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="3a6c0-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="3a6c0-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a6c0-133">NOTES</span></span>

<span data-ttu-id="3a6c0-134">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a6c0-135">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3a6c0-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3a6c0-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a6c0-137">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3a6c0-138">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3a6c0-139">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3a6c0-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a6c0-140">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3a6c0-141">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3a6c0-142">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3a6c0-143">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3a6c0-144">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3a6c0-145">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3a6c0-146">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="3a6c0-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3a6c0-147">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3a6c0-148">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3a6c0-149">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3a6c0-150">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3a6c0-151">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="3a6c0-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="3a6c0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a6c0-152">RELATED LINKS</span></span>

