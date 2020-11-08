---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015281"
---
# <span data-ttu-id="f77bd-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="f77bd-101">Set-AzsOffer</span></span>

## <span data-ttu-id="f77bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f77bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f77bd-103">Az ajánlat létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="f77bd-103">Create or update the offer.</span></span>

## <span data-ttu-id="f77bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f77bd-104">SYNTAX</span></span>

### <span data-ttu-id="f77bd-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f77bd-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f77bd-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="f77bd-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f77bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f77bd-107">DESCRIPTION</span></span>
<span data-ttu-id="f77bd-108">Az ajánlat létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="f77bd-108">Create or update the offer.</span></span>

## <span data-ttu-id="f77bd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f77bd-109">EXAMPLES</span></span>

### <span data-ttu-id="f77bd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f77bd-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="f77bd-111">Frissítheti az ajánlatot.</span><span class="sxs-lookup"><span data-stu-id="f77bd-111">Update an offer.</span></span>

## <span data-ttu-id="f77bd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f77bd-112">PARAMETERS</span></span>

### <span data-ttu-id="f77bd-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="f77bd-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="f77bd-114">Azon bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként tetszés szerint tud beszerezni.</span><span class="sxs-lookup"><span data-stu-id="f77bd-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="f77bd-115">A kivitelezéshez tekintse meg a ADDONPLANDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f77bd-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="f77bd-116">-BasePlanIds</span></span>
<span data-ttu-id="f77bd-117">Azoknak az alapterveknek az azonosítói, amelyek azonnal elérhetővé válnak a bérlői webhelyre, amikor a bérlő előfizet az ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="f77bd-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77bd-118">-DefaultProfile</span></span>
<span data-ttu-id="f77bd-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f77bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f77bd-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f77bd-120">-Description</span></span>
<span data-ttu-id="f77bd-121">Az ajánlat leírása.</span><span class="sxs-lookup"><span data-stu-id="f77bd-121">Description of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f77bd-122">-DisplayName</span></span>
<span data-ttu-id="f77bd-123">Az ajánlat megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="f77bd-123">Display name of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f77bd-124">-ExternalReferenceId</span></span>
<span data-ttu-id="f77bd-125">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="f77bd-125">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="f77bd-126">-Location</span></span>
<span data-ttu-id="f77bd-127">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="f77bd-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="f77bd-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="f77bd-129">Fiók maximális előfizetése.</span><span class="sxs-lookup"><span data-stu-id="f77bd-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f77bd-130">-Name</span></span>
<span data-ttu-id="f77bd-131">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f77bd-131">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="f77bd-132">-OfferDefinition</span></span>
<span data-ttu-id="f77bd-133">Azoknak a szolgáltatásoknak a felajánlását jelenti, amelyekhez előfizetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="f77bd-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="f77bd-134">A kivitelezéshez tekintse meg a OFFERDEFINITION tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f77bd-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-135">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="f77bd-135">-PropertiesName</span></span>
<span data-ttu-id="f77bd-136">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f77bd-136">Name of the Offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77bd-137">-ResourceGroupName</span></span>
<span data-ttu-id="f77bd-138">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="f77bd-138">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-139">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="f77bd-139">-State</span></span>
<span data-ttu-id="f77bd-140">Kisegítő lehetőségek állapota</span><span class="sxs-lookup"><span data-stu-id="f77bd-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="f77bd-141">-SubscriptionCount</span></span>
<span data-ttu-id="f77bd-142">Aktuális előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="f77bd-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f77bd-143">-SubscriptionId</span></span>
<span data-ttu-id="f77bd-144">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f77bd-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f77bd-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f77bd-145">-Confirm</span></span>
<span data-ttu-id="f77bd-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f77bd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f77bd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f77bd-147">-WhatIf</span></span>
<span data-ttu-id="f77bd-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f77bd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f77bd-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f77bd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f77bd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77bd-150">CommonParameters</span></span>
<span data-ttu-id="f77bd-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f77bd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77bd-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f77bd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77bd-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f77bd-153">INPUTS</span></span>

### <span data-ttu-id="f77bd-154">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="f77bd-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="f77bd-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f77bd-155">OUTPUTS</span></span>

### <span data-ttu-id="f77bd-156">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="f77bd-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="f77bd-157">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f77bd-157">ALIASES</span></span>

## <span data-ttu-id="f77bd-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f77bd-158">NOTES</span></span>

<span data-ttu-id="f77bd-159">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f77bd-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f77bd-160">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f77bd-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f77bd-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: olyan bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="f77bd-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="f77bd-162">`[MaxAcquisitionCount <Int32?>]`: Egyetlen előfizetés által megszerezhető példányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="f77bd-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="f77bd-163">Ha nincs megadva, a feltételezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="f77bd-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="f77bd-164">`[PlanId <String>]`: Csomag-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f77bd-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="f77bd-165">OFFERDEFINITION <IOffer> : olyan szolgáltatások felajánlását jelenti, amelyekkel előfizetést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="f77bd-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="f77bd-166">`[Location <String>]`: Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="f77bd-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="f77bd-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként tetszés szerint igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="f77bd-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="f77bd-168">`[MaxAcquisitionCount <Int32?>]`: Egyetlen előfizetés által megszerezhető példányok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="f77bd-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="f77bd-169">Ha nincs megadva, a feltételezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="f77bd-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="f77bd-170">`[PlanId <String>]`: Csomag-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f77bd-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="f77bd-171">`[BasePlanIds <String[]>]`: Az alaptervek azonosítói, amelyek azonnal elérhetővé válnak a bérlői webhelyre, amikor a bérlő előfizet az ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="f77bd-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="f77bd-172">`[Description <String>]`: Az ajánlat leírása.</span><span class="sxs-lookup"><span data-stu-id="f77bd-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="f77bd-173">`[DisplayName <String>]`: Az ajánlat megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="f77bd-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="f77bd-174">`[ExternalReferenceId <String>]`: Külső hivatkozási azonosító.</span><span class="sxs-lookup"><span data-stu-id="f77bd-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="f77bd-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Egy fiók maximális előfizetése.</span><span class="sxs-lookup"><span data-stu-id="f77bd-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="f77bd-176">`[PropertiesName <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f77bd-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="f77bd-177">`[State <AccessibilityState?>]`: Ajánlati kisegítő lehetőségek</span><span class="sxs-lookup"><span data-stu-id="f77bd-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="f77bd-178">`[SubscriptionCount <Int32?>]`: Aktuális előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="f77bd-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="f77bd-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f77bd-179">RELATED LINKS</span></span>

