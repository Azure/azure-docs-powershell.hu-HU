---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480503"
---
# <span data-ttu-id="dba7a-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="dba7a-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="dba7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dba7a-102">SYNOPSIS</span></span>
<span data-ttu-id="dba7a-103">Létrehozza vagy frissíti az egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="dba7a-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="dba7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dba7a-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dba7a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dba7a-105">DESCRIPTION</span></span>
<span data-ttu-id="dba7a-106">Létrehozza vagy frissíti az egyéni erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="dba7a-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="dba7a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dba7a-107">EXAMPLES</span></span>

### <span data-ttu-id="dba7a-108">1. példa: Egyéni szolgáltató létrehozása</span><span class="sxs-lookup"><span data-stu-id="dba7a-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="dba7a-109">Egyéni erőforrás-szolgáltató létrehozása</span><span class="sxs-lookup"><span data-stu-id="dba7a-109">Create a custom resource provider</span></span>

### <span data-ttu-id="dba7a-110">2. példa: Egyéni szolgáltató létrehozása társításokkal</span><span class="sxs-lookup"><span data-stu-id="dba7a-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="dba7a-111">Hozzon létre egy egyéni szolgáltatót az egyéni szolgáltatói társítások útvonalával.</span><span class="sxs-lookup"><span data-stu-id="dba7a-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="dba7a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dba7a-112">PARAMETERS</span></span>

### <span data-ttu-id="dba7a-113">-Művelet</span><span class="sxs-lookup"><span data-stu-id="dba7a-113">-Action</span></span>
<span data-ttu-id="dba7a-114">Az egyéni erőforrás-szolgáltató által implementálja a műveletek listáját.</span><span class="sxs-lookup"><span data-stu-id="dba7a-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="dba7a-115">Az ACTION tulajdonságokat és a kivonattáblát a MEGJEGYZÉSEK szakaszban hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="dba7a-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="dba7a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dba7a-116">-AsJob</span></span>
<span data-ttu-id="dba7a-117">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="dba7a-117">Run the command as a job</span></span>

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

### <span data-ttu-id="dba7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba7a-118">-DefaultProfile</span></span>
<span data-ttu-id="dba7a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dba7a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba7a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="dba7a-120">-Location</span></span>
<span data-ttu-id="dba7a-121">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="dba7a-121">Resource location</span></span>

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

### <span data-ttu-id="dba7a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dba7a-122">-Name</span></span>
<span data-ttu-id="dba7a-123">Az erőforrás-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="dba7a-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="dba7a-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dba7a-124">-NoWait</span></span>
<span data-ttu-id="dba7a-125">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="dba7a-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dba7a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba7a-126">-ResourceGroupName</span></span>
<span data-ttu-id="dba7a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dba7a-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="dba7a-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dba7a-128">-ResourceType</span></span>
<span data-ttu-id="dba7a-129">Az egyéni erőforrásszolgáltató által implementálja az erőforrástípusok listáját.</span><span class="sxs-lookup"><span data-stu-id="dba7a-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="dba7a-130">Az ERŐFORRÁSTÍPUS tulajdonságainak létrehozására és a kivonattáblák létrehozására vonatkozó MEGJEGYZÉSEK szakaszban talál további konstrukciót.</span><span class="sxs-lookup"><span data-stu-id="dba7a-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="dba7a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dba7a-131">-SubscriptionId</span></span>
<span data-ttu-id="dba7a-132">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dba7a-132">The Azure subscription ID.</span></span>
<span data-ttu-id="dba7a-133">Ez egy GUID formátumú karakterlánc (például 000000000-0000-0000-0000-0000000000000000000)</span><span class="sxs-lookup"><span data-stu-id="dba7a-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="dba7a-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="dba7a-134">-Tag</span></span>
<span data-ttu-id="dba7a-135">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="dba7a-135">Resource tags</span></span>

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

### <span data-ttu-id="dba7a-136">-Validation</span><span class="sxs-lookup"><span data-stu-id="dba7a-136">-Validation</span></span>
<span data-ttu-id="dba7a-137">Az egyéni erőforrás-szolgáltató kérései alapján futtatható érvényesítések listája.</span><span class="sxs-lookup"><span data-stu-id="dba7a-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="dba7a-138">Ennek létrehozásáról az ÉRVÉNYESÍTési tulajdonságokat és a kivonattáblát a JEGYZETEK szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="dba7a-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="dba7a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dba7a-139">-Confirm</span></span>
<span data-ttu-id="dba7a-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dba7a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba7a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba7a-141">-WhatIf</span></span>
<span data-ttu-id="dba7a-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dba7a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba7a-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dba7a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba7a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba7a-144">CommonParameters</span></span>
<span data-ttu-id="dba7a-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba7a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba7a-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dba7a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba7a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dba7a-147">INPUTS</span></span>

## <span data-ttu-id="dba7a-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dba7a-148">OUTPUTS</span></span>

### <span data-ttu-id="dba7a-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="dba7a-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="dba7a-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dba7a-150">NOTES</span></span>

<span data-ttu-id="dba7a-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dba7a-151">ALIASES</span></span>

<span data-ttu-id="dba7a-152">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="dba7a-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dba7a-153">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="dba7a-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dba7a-154">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dba7a-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dba7a-155">ACTION <ICustomRpActionRouteDefinition[]>: Az egyéni erőforrás-szolgáltató által implementálható műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="dba7a-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="dba7a-156">`Endpoint <String>`: Az az útvonaldefiníciós végpont URI, amelyről az egyéni erőforrás-szolgáltató proxyt kér.</span><span class="sxs-lookup"><span data-stu-id="dba7a-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="dba7a-157">Ez lehet egyszerű URI (például ' '), vagy megadhatja, hogy egy útvonalon (például ' ') keresztül kell útvonalat https://testendpoint/ https://testendpoint/{requestPath} haladni.</span><span class="sxs-lookup"><span data-stu-id="dba7a-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="dba7a-158">`Name <String>`: Az útvonaldefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="dba7a-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="dba7a-159">Ez lesz az ARM-bővítmény neve (pl. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="dba7a-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="dba7a-160">`[RoutingType <ActionRouting?>]`: A műveletkérések által támogatott útválasztási típusok.</span><span class="sxs-lookup"><span data-stu-id="dba7a-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="dba7a-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: Az egyéni erőforrásszolgáltató által implementálható erőforrástípusok listája.</span><span class="sxs-lookup"><span data-stu-id="dba7a-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="dba7a-162">`Endpoint <String>`: Az az útvonaldefiníciós végpont URI, amelyről az egyéni erőforrás-szolgáltató proxyt kér.</span><span class="sxs-lookup"><span data-stu-id="dba7a-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="dba7a-163">Ez lehet egyszerű URI (például ' '), vagy megadhatja, hogy egy útvonalon (például ' ') keresztül kell útvonalat https://testendpoint/ https://testendpoint/{requestPath} haladni.</span><span class="sxs-lookup"><span data-stu-id="dba7a-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="dba7a-164">`Name <String>`: Az útvonaldefiníció neve.</span><span class="sxs-lookup"><span data-stu-id="dba7a-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="dba7a-165">Ez lesz az ARM-bővítmény neve (pl. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="dba7a-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="dba7a-166">`[RoutingType <ResourceTypeRouting?>]`: Az erőforrás-kérelmekhez támogatott útválasztási típusok.</span><span class="sxs-lookup"><span data-stu-id="dba7a-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="dba7a-167">VALIDATION <ICustomRpValidations[]>: Az egyéni erőforrás-szolgáltató kérésén futtatható érvényesítések listája.</span><span class="sxs-lookup"><span data-stu-id="dba7a-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="dba7a-168">`Specification <String>`: Az érvényesítési specifikációra mutató hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="dba7a-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="dba7a-169">A specifikációt az adott raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="dba7a-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="dba7a-170">`[ValidationType <ValidationType?>]`: Az egyező kérésen futtatott érvényesítés típusa.</span><span class="sxs-lookup"><span data-stu-id="dba7a-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="dba7a-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dba7a-171">RELATED LINKS</span></span>

