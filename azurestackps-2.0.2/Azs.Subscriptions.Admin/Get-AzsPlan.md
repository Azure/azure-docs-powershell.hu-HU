---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016996"
---
# <span data-ttu-id="ccfc5-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="ccfc5-101">Get-AzsPlan</span></span>

## <span data-ttu-id="ccfc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfc5-103">A megadott csomag beszerzése</span><span class="sxs-lookup"><span data-stu-id="ccfc5-103">Get the specified plan.</span></span>

## <span data-ttu-id="ccfc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccfc5-104">SYNTAX</span></span>

### <span data-ttu-id="ccfc5-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccfc5-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ccfc5-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="ccfc5-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ccfc5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ccfc5-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ccfc5-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="ccfc5-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccfc5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccfc5-109">DESCRIPTION</span></span>
<span data-ttu-id="ccfc5-110">A megadott csomag beszerzése</span><span class="sxs-lookup"><span data-stu-id="ccfc5-110">Get the specified plan.</span></span>

## <span data-ttu-id="ccfc5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ccfc5-111">EXAMPLES</span></span>

### <span data-ttu-id="ccfc5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccfc5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="ccfc5-113">Konkrét-terv beszerzése az előfizetések csoportban</span><span class="sxs-lookup"><span data-stu-id="ccfc5-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="ccfc5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccfc5-114">PARAMETERS</span></span>

### <span data-ttu-id="ccfc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccfc5-115">-DefaultProfile</span></span>
<span data-ttu-id="ccfc5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccfc5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccfc5-117">-InputObject</span></span>
<span data-ttu-id="ccfc5-118">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ccfc5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ccfc5-119">-Name</span></span>
<span data-ttu-id="ccfc5-120">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-120">Name of the plan.</span></span>

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

### <span data-ttu-id="ccfc5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccfc5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccfc5-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ccfc5-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccfc5-123">-SubscriptionId</span></span>
<span data-ttu-id="ccfc5-124">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ccfc5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfc5-125">CommonParameters</span></span>
<span data-ttu-id="ccfc5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccfc5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfc5-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfc5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccfc5-128">INPUTS</span></span>

### <span data-ttu-id="ccfc5-129">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ccfc5-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="ccfc5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccfc5-130">OUTPUTS</span></span>

### <span data-ttu-id="ccfc5-131">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="ccfc5-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="ccfc5-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ccfc5-132">ALIASES</span></span>

## <span data-ttu-id="ccfc5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccfc5-133">NOTES</span></span>

<span data-ttu-id="ccfc5-134">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ccfc5-135">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ccfc5-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="ccfc5-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ccfc5-137">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="ccfc5-138">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="ccfc5-139">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="ccfc5-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ccfc5-140">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="ccfc5-141">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="ccfc5-142">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="ccfc5-143">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="ccfc5-144">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="ccfc5-145">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="ccfc5-146">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="ccfc5-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="ccfc5-147">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="ccfc5-148">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="ccfc5-149">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ccfc5-150">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="ccfc5-151">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="ccfc5-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="ccfc5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccfc5-152">RELATED LINKS</span></span>

