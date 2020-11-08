---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017092"
---
# <span data-ttu-id="3cb8a-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="3cb8a-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="3cb8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3cb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb8a-103">A megadott ajánlat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-103">Get the specified offer.</span></span>

## <span data-ttu-id="3cb8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3cb8a-104">SYNTAX</span></span>

### <span data-ttu-id="3cb8a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3cb8a-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3cb8a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="3cb8a-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3cb8a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3cb8a-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3cb8a-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="3cb8a-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cb8a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3cb8a-109">DESCRIPTION</span></span>
<span data-ttu-id="3cb8a-110">A megadott ajánlat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-110">Get the specified offer.</span></span>

## <span data-ttu-id="3cb8a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3cb8a-111">EXAMPLES</span></span>

### <span data-ttu-id="3cb8a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3cb8a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="3cb8a-113">Ajánlat kérése névvel és ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb8a-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="3cb8a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3cb8a-114">PARAMETERS</span></span>

### <span data-ttu-id="3cb8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb8a-115">-DefaultProfile</span></span>
<span data-ttu-id="3cb8a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cb8a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cb8a-117">-InputObject</span></span>
<span data-ttu-id="3cb8a-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3cb8a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3cb8a-119">-Name</span></span>
<span data-ttu-id="3cb8a-120">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-120">Name of an offer.</span></span>

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

### <span data-ttu-id="3cb8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cb8a-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3cb8a-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cb8a-123">-SubscriptionId</span></span>
<span data-ttu-id="3cb8a-124">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3cb8a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb8a-125">CommonParameters</span></span>
<span data-ttu-id="3cb8a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3cb8a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb8a-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb8a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cb8a-128">INPUTS</span></span>

### <span data-ttu-id="3cb8a-129">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3cb8a-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3cb8a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cb8a-130">OUTPUTS</span></span>

### <span data-ttu-id="3cb8a-131">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="3cb8a-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="3cb8a-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3cb8a-132">ALIASES</span></span>

<span data-ttu-id="3cb8a-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="3cb8a-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="3cb8a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3cb8a-134">NOTES</span></span>

<span data-ttu-id="3cb8a-135">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3cb8a-136">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3cb8a-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3cb8a-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3cb8a-138">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3cb8a-139">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3cb8a-140">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3cb8a-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3cb8a-141">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3cb8a-142">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3cb8a-143">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3cb8a-144">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3cb8a-145">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3cb8a-146">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3cb8a-147">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="3cb8a-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3cb8a-148">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3cb8a-149">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3cb8a-150">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3cb8a-151">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3cb8a-152">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="3cb8a-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="3cb8a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cb8a-153">RELATED LINKS</span></span>

