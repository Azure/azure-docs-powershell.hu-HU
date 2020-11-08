---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184600"
---
# <span data-ttu-id="96db5-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="96db5-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="96db5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96db5-102">SYNOPSIS</span></span>
<span data-ttu-id="96db5-103">Az egyéni erőforrás-szolgáltató létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="96db5-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="96db5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96db5-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96db5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96db5-105">DESCRIPTION</span></span>
<span data-ttu-id="96db5-106">Az egyéni erőforrás-szolgáltató létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="96db5-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="96db5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96db5-107">EXAMPLES</span></span>

### <span data-ttu-id="96db5-108">Példa 1: egyéni szolgáltató létrehozása</span><span class="sxs-lookup"><span data-stu-id="96db5-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="96db5-109">Egyéni erőforrás-szolgáltató létrehozása</span><span class="sxs-lookup"><span data-stu-id="96db5-109">Create a custom resource provider</span></span>

### <span data-ttu-id="96db5-110">2. példa: egyéni szolgáltató létrehozása társításokkal</span><span class="sxs-lookup"><span data-stu-id="96db5-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="96db5-111">Egyéni szolgáltató létrehozása az egyéni szolgáltatói társítások útvonalával.</span><span class="sxs-lookup"><span data-stu-id="96db5-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="96db5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96db5-112">PARAMETERS</span></span>

### <span data-ttu-id="96db5-113">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="96db5-113">-Action</span></span>
<span data-ttu-id="96db5-114">Az egyéni erőforrás-szolgáltató által megvalósított műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="96db5-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="96db5-115">A kivitelezéshez lásd a megjegyzések szakaszt a műveletek tulajdonságaihoz, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="96db5-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96db5-116">-AsJob</span></span>
<span data-ttu-id="96db5-117">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="96db5-117">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96db5-118">-DefaultProfile</span></span>
<span data-ttu-id="96db5-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96db5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96db5-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="96db5-120">-Location</span></span>
<span data-ttu-id="96db5-121">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="96db5-121">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96db5-122">-Name</span></span>
<span data-ttu-id="96db5-123">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="96db5-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="96db5-124">-NoWait</span></span>
<span data-ttu-id="96db5-125">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="96db5-125">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96db5-126">-ResourceGroupName</span></span>
<span data-ttu-id="96db5-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="96db5-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="96db5-128">-ResourceType</span></span>
<span data-ttu-id="96db5-129">Az egyéni erőforrás-szolgáltató által megvalósított erőforrástípusok listája.</span><span class="sxs-lookup"><span data-stu-id="96db5-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="96db5-130">A kivitelezéshez tekintse meg a RESOURCETYPE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="96db5-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96db5-131">-SubscriptionId</span></span>
<span data-ttu-id="96db5-132">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="96db5-132">The Azure subscription ID.</span></span>
<span data-ttu-id="96db5-133">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="96db5-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="96db5-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="96db5-134">-Tag</span></span>
<span data-ttu-id="96db5-135">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="96db5-135">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-136">– Érvényesítés</span><span class="sxs-lookup"><span data-stu-id="96db5-136">-Validation</span></span>
<span data-ttu-id="96db5-137">Az egyéni erőforrás-szolgáltató kérésein futtatandó érvényes érvényesítések listája.</span><span class="sxs-lookup"><span data-stu-id="96db5-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="96db5-138">A kivitelezéshez tekintse meg az ÉRVÉNYESÍTÉSi tulajdonságok megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="96db5-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96db5-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96db5-139">-Confirm</span></span>
<span data-ttu-id="96db5-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96db5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96db5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96db5-141">-WhatIf</span></span>
<span data-ttu-id="96db5-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96db5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96db5-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96db5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96db5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96db5-144">CommonParameters</span></span>
<span data-ttu-id="96db5-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96db5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96db5-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96db5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96db5-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96db5-147">INPUTS</span></span>

## <span data-ttu-id="96db5-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96db5-148">OUTPUTS</span></span>

### <span data-ttu-id="96db5-149">Microsoft. Azure. PowerShell. parancsmagok. CustomProviders. modellek. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="96db5-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="96db5-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96db5-150">NOTES</span></span>

<span data-ttu-id="96db5-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="96db5-151">ALIASES</span></span>

<span data-ttu-id="96db5-152">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="96db5-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96db5-153">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="96db5-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96db5-154">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="96db5-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96db5-155">MŰVELET <ICustomRpActionRouteDefinition [] >: az egyéni erőforrás-szolgáltató által megvalósított műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="96db5-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="96db5-156">`Endpoint <String>`: Az útvonal-definíciós végpontok URI-ja, amelyet az egyéni erőforrás-szolgáltató meghatalmazotti a kérésekre.</span><span class="sxs-lookup"><span data-stu-id="96db5-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="96db5-157">Ez lehet egy sima URI (például ' ' https://testendpoint/ ), vagy az útvonalon keresztüli útvonal (például ' https://testendpoint/{requestPath} ') formájában.</span><span class="sxs-lookup"><span data-stu-id="96db5-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="96db5-158">`Name <String>`: Az útvonal-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="96db5-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="96db5-159">Ez lesz a kar kiterjesztésének neve (például "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="96db5-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="96db5-160">`[RoutingType <ActionRouting?>]`: A műveleti kérések által támogatott műveletterv-típusok.</span><span class="sxs-lookup"><span data-stu-id="96db5-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="96db5-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: az egyéni erőforrás-szolgáltató által megvalósított erőforrástípusok listája.</span><span class="sxs-lookup"><span data-stu-id="96db5-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="96db5-162">`Endpoint <String>`: Az útvonal-definíciós végpontok URI-ja, amelyet az egyéni erőforrás-szolgáltató meghatalmazotti a kérésekre.</span><span class="sxs-lookup"><span data-stu-id="96db5-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="96db5-163">Ez lehet egy sima URI (például ' ' https://testendpoint/ ), vagy az útvonalon keresztüli útvonal (például ' https://testendpoint/{requestPath} ') formájában.</span><span class="sxs-lookup"><span data-stu-id="96db5-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="96db5-164">`Name <String>`: Az útvonal-definíció neve.</span><span class="sxs-lookup"><span data-stu-id="96db5-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="96db5-165">Ez lesz a kar kiterjesztésének neve (például "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="96db5-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="96db5-166">`[RoutingType <ResourceTypeRouting?>]`: Az erőforrás-kérelmekben támogatott műveletterv-típusok.</span><span class="sxs-lookup"><span data-stu-id="96db5-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="96db5-167">VALIDATion <ICustomRpValidations [] >: az egyéni erőforrás-szolgáltató kérésein futtatandó érvényes érvényesítések listája.</span><span class="sxs-lookup"><span data-stu-id="96db5-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="96db5-168">`Specification <String>`: Az érvényesítési specifikációra mutató hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="96db5-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="96db5-169">A specifikációnak a raw.githubusercontent.com-on kell lennie.</span><span class="sxs-lookup"><span data-stu-id="96db5-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="96db5-170">`[ValidationType <ValidationType?>]`: Az érvényesítés típusa a megfelelő kéréshez képest.</span><span class="sxs-lookup"><span data-stu-id="96db5-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="96db5-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96db5-171">RELATED LINKS</span></span>

