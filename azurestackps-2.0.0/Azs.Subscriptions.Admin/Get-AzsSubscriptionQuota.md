---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015087"
---
# <span data-ttu-id="b4e4f-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="b4e4f-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="b4e4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e4f-103">A kvótát név szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-103">Gets a quota by name.</span></span>

## <span data-ttu-id="b4e4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4e4f-104">SYNTAX</span></span>

### <span data-ttu-id="b4e4f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4e4f-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e4f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b4e4f-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b4e4f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b4e4f-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4e4f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4e4f-108">DESCRIPTION</span></span>
<span data-ttu-id="b4e4f-109">A kvótát név szerint kapja.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-109">Gets a quota by name.</span></span>

## <span data-ttu-id="b4e4f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b4e4f-110">EXAMPLES</span></span>

### <span data-ttu-id="b4e4f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4e4f-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="b4e4f-112">Az előfizetéses erőforrás-szolgáltatói kvóták listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b4e4f-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="b4e4f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4e4f-113">PARAMETERS</span></span>

### <span data-ttu-id="b4e4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e4f-114">-DefaultProfile</span></span>
<span data-ttu-id="b4e4f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e4f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4e4f-116">-InputObject</span></span>
<span data-ttu-id="b4e4f-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4e4f-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="b4e4f-118">-Location</span></span>
<span data-ttu-id="b4e4f-119">A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b4e4f-120">-Kvóta</span><span class="sxs-lookup"><span data-stu-id="b4e4f-120">-Quota</span></span>
<span data-ttu-id="b4e4f-121">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-121">Name of the quota.</span></span>

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

### <span data-ttu-id="b4e4f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4e4f-122">-SubscriptionId</span></span>
<span data-ttu-id="b4e4f-123">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b4e4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e4f-124">CommonParameters</span></span>
<span data-ttu-id="b4e4f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4e4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e4f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e4f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4e4f-127">INPUTS</span></span>

### <span data-ttu-id="b4e4f-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b4e4f-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b4e4f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4e4f-129">OUTPUTS</span></span>

### <span data-ttu-id="b4e4f-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IQuota</span><span class="sxs-lookup"><span data-stu-id="b4e4f-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="b4e4f-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b4e4f-131">ALIASES</span></span>

<span data-ttu-id="b4e4f-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="b4e4f-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="b4e4f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4e4f-133">NOTES</span></span>

<span data-ttu-id="b4e4f-134">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4e4f-135">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b4e4f-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b4e4f-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4e4f-137">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b4e4f-138">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b4e4f-139">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b4e4f-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4e4f-140">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b4e4f-141">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b4e4f-142">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b4e4f-143">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b4e4f-144">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b4e4f-145">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b4e4f-146">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="b4e4f-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b4e4f-147">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b4e4f-148">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b4e4f-149">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b4e4f-150">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b4e4f-151">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="b4e4f-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b4e4f-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4e4f-152">RELATED LINKS</span></span>

