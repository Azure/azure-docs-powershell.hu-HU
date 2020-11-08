---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015236"
---
# <span data-ttu-id="620d3-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="620d3-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="620d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="620d3-102">SYNOPSIS</span></span>
<span data-ttu-id="620d3-103">Az identitás állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="620d3-103">Checks the identity health</span></span>

## <span data-ttu-id="620d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="620d3-104">SYNTAX</span></span>

### <span data-ttu-id="620d3-105">Ellenőrzés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="620d3-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="620d3-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="620d3-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="620d3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="620d3-107">DESCRIPTION</span></span>
<span data-ttu-id="620d3-108">Az identitás állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="620d3-108">Checks the identity health</span></span>

## <span data-ttu-id="620d3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="620d3-109">EXAMPLES</span></span>

### <span data-ttu-id="620d3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="620d3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="620d3-111">Ismerje meg az identitás állapotát.</span><span class="sxs-lookup"><span data-stu-id="620d3-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="620d3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="620d3-112">PARAMETERS</span></span>

### <span data-ttu-id="620d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620d3-113">-DefaultProfile</span></span>
<span data-ttu-id="620d3-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="620d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="620d3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="620d3-115">-InputObject</span></span>
<span data-ttu-id="620d3-116">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="620d3-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="620d3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="620d3-117">-SubscriptionId</span></span>
<span data-ttu-id="620d3-118">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="620d3-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="620d3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="620d3-119">-Confirm</span></span>
<span data-ttu-id="620d3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="620d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="620d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="620d3-121">-WhatIf</span></span>
<span data-ttu-id="620d3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="620d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="620d3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="620d3-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="620d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620d3-124">CommonParameters</span></span>
<span data-ttu-id="620d3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="620d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620d3-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="620d3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620d3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="620d3-127">INPUTS</span></span>

### <span data-ttu-id="620d3-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="620d3-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="620d3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="620d3-129">OUTPUTS</span></span>

### <span data-ttu-id="620d3-130">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IIdentityHealthCheckReportDefinition</span><span class="sxs-lookup"><span data-stu-id="620d3-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="620d3-131">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="620d3-131">ALIASES</span></span>

## <span data-ttu-id="620d3-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="620d3-132">NOTES</span></span>

<span data-ttu-id="620d3-133">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="620d3-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="620d3-134">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="620d3-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="620d3-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="620d3-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="620d3-136">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="620d3-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="620d3-137">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="620d3-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="620d3-138">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="620d3-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="620d3-139">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="620d3-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="620d3-140">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="620d3-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="620d3-141">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="620d3-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="620d3-142">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="620d3-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="620d3-143">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="620d3-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="620d3-144">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="620d3-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="620d3-145">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="620d3-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="620d3-146">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="620d3-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="620d3-147">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="620d3-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="620d3-148">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="620d3-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="620d3-149">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="620d3-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="620d3-150">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="620d3-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="620d3-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="620d3-151">RELATED LINKS</span></span>

