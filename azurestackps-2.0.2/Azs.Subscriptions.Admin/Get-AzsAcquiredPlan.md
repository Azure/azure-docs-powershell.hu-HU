---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017156"
---
# <span data-ttu-id="10fe8-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="10fe8-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="10fe8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="10fe8-103">Az ajánlat előfizetése által elfogyasztott előfizetéssel szerzi be a megadott csomagot.</span><span class="sxs-lookup"><span data-stu-id="10fe8-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="10fe8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10fe8-104">SYNTAX</span></span>

### <span data-ttu-id="10fe8-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10fe8-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="10fe8-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="10fe8-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="10fe8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="10fe8-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="10fe8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="10fe8-108">DESCRIPTION</span></span>
<span data-ttu-id="10fe8-109">Az ajánlat előfizetése által elfogyasztott előfizetéssel szerzi be a megadott csomagot.</span><span class="sxs-lookup"><span data-stu-id="10fe8-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="10fe8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="10fe8-110">EXAMPLES</span></span>

### <span data-ttu-id="10fe8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="10fe8-111">Example 1</span></span>
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

<span data-ttu-id="10fe8-112">Szerezzen be minden megvásárolt csomagot, amelyre az előfizetés hozzáfér.</span><span class="sxs-lookup"><span data-stu-id="10fe8-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="10fe8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10fe8-113">PARAMETERS</span></span>

### <span data-ttu-id="10fe8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10fe8-114">-DefaultProfile</span></span>
<span data-ttu-id="10fe8-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10fe8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10fe8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10fe8-116">-InputObject</span></span>
<span data-ttu-id="10fe8-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10fe8-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="10fe8-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="10fe8-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="10fe8-119">A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="10fe8-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="10fe8-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10fe8-120">-SubscriptionId</span></span>
<span data-ttu-id="10fe8-121">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="10fe8-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="10fe8-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10fe8-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="10fe8-123">A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="10fe8-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="10fe8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fe8-124">CommonParameters</span></span>
<span data-ttu-id="10fe8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10fe8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fe8-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10fe8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fe8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10fe8-127">INPUTS</span></span>

### <span data-ttu-id="10fe8-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="10fe8-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="10fe8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10fe8-129">OUTPUTS</span></span>

### <span data-ttu-id="10fe8-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="10fe8-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="10fe8-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="10fe8-131">ALIASES</span></span>

<span data-ttu-id="10fe8-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="10fe8-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="10fe8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10fe8-133">NOTES</span></span>

<span data-ttu-id="10fe8-134">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="10fe8-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10fe8-135">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="10fe8-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="10fe8-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="10fe8-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="10fe8-137">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="10fe8-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="10fe8-138">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="10fe8-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="10fe8-139">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="10fe8-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10fe8-140">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="10fe8-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="10fe8-141">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="10fe8-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="10fe8-142">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="10fe8-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="10fe8-143">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="10fe8-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="10fe8-144">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="10fe8-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="10fe8-145">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="10fe8-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="10fe8-146">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="10fe8-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="10fe8-147">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="10fe8-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="10fe8-148">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="10fe8-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="10fe8-149">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="10fe8-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="10fe8-150">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="10fe8-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="10fe8-151">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="10fe8-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="10fe8-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10fe8-152">RELATED LINKS</span></span>

