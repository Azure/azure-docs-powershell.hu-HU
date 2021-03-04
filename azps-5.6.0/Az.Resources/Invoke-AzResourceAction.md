---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 14da2ddfdd94be5cd95d00eeeb742b9e4ac982e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929849"
---
# <span data-ttu-id="19670-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="19670-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="19670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19670-102">SYNOPSIS</span></span>
<span data-ttu-id="19670-103">Meghív egy műveletet egy erőforráson.</span><span class="sxs-lookup"><span data-stu-id="19670-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="19670-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19670-104">SYNTAX</span></span>

### <span data-ttu-id="19670-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19670-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19670-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="19670-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19670-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="19670-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19670-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19670-108">DESCRIPTION</span></span>
<span data-ttu-id="19670-109">Az **Invoke-AzResourceAction** parancsmag meghív egy műveletet egy megadott Azure-erőforráson.</span><span class="sxs-lookup"><span data-stu-id="19670-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="19670-110">A támogatott műveletek listájának lekértérte az Azure Resource Explorer eszközt.</span><span class="sxs-lookup"><span data-stu-id="19670-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="19670-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19670-111">EXAMPLES</span></span>

### <span data-ttu-id="19670-112">1. példa: Virtuális gép indítása a ResourceId-val</span><span class="sxs-lookup"><span data-stu-id="19670-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="19670-113">Ez a parancs elindítja a virtuális gépet a következővel: {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="19670-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="19670-114">2. példa: Virtuális gép erőforrás-hozzárendelésének meghívása a ResourceName névvel</span><span class="sxs-lookup"><span data-stu-id="19670-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="19670-115">Ez a parancs leállítja a virtuális gépet a következővel: {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="19670-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="19670-116">A parancs megadja a *Force* paramétert, ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19670-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="19670-117">3. példa: Erőforrásszolgáltató regisztrálásának meghívása az Erőforrásazonosító függe</span><span class="sxs-lookup"><span data-stu-id="19670-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="19670-118">Ez a parancs regisztrálja a "Microsoft.Network" erőforrás-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="19670-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="19670-119">A parancs megadja a *Force* paramétert, ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19670-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="19670-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19670-120">PARAMETERS</span></span>

### <span data-ttu-id="19670-121">-Művelet</span><span class="sxs-lookup"><span data-stu-id="19670-121">-Action</span></span>
<span data-ttu-id="19670-122">Az meghívni szükséges művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19670-122">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19670-123">-ApiVersion</span></span>
<span data-ttu-id="19670-124">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="19670-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="19670-125">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="19670-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19670-126">-DefaultProfile</span></span>
<span data-ttu-id="19670-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19670-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="19670-128">-ExtensionResourceName</span></span>
<span data-ttu-id="19670-129">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag műveletet meghív.</span><span class="sxs-lookup"><span data-stu-id="19670-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="19670-130">Adatbázis megadásához például használja a következő formátumot: kiszolgálónév `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="19670-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19670-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="19670-131">-ExtensionResourceType</span></span>
<span data-ttu-id="19670-132">A bővítményerőforrás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="19670-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="19670-133">Például: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="19670-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19670-134">-Force</span><span class="sxs-lookup"><span data-stu-id="19670-134">-Force</span></span>
<span data-ttu-id="19670-135">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="19670-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19670-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="19670-136">-ODataQuery</span></span>
<span data-ttu-id="19670-137">OData-stílusszűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="19670-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="19670-138">Ez a parancsmag minden más szűrő mellett hozzáfűzi ezt az értéket a kérelemhez.</span><span class="sxs-lookup"><span data-stu-id="19670-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="19670-139">-Parameters</span></span>
<span data-ttu-id="19670-140">A parancsmag által elindított művelet paramétereit adja meg kivonattáblaként.</span><span class="sxs-lookup"><span data-stu-id="19670-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="19670-141">-Pre</span></span>
<span data-ttu-id="19670-142">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="19670-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="19670-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19670-143">-ResourceGroupName</span></span>
<span data-ttu-id="19670-144">Annak az erőforráscsoportnak a nevét adja meg, amelyben a parancsmag egy műveletet meghív.</span><span class="sxs-lookup"><span data-stu-id="19670-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19670-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19670-145">-ResourceId</span></span>
<span data-ttu-id="19670-146">Annak az erőforrásnak a teljes erőforrás-azonosítója, amelyre a parancsmag műveletet meghív.</span><span class="sxs-lookup"><span data-stu-id="19670-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="19670-147">Az azonosító tartalmazza az előfizetést, ahogy az alábbi példában is: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="19670-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19670-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="19670-148">-ResourceName</span></span>
<span data-ttu-id="19670-149">Annak az erőforrásnak a nevét adja meg, amelyre a parancsmag műveletet meghív.</span><span class="sxs-lookup"><span data-stu-id="19670-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="19670-150">Adatbázis megadásához például használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="19670-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19670-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="19670-151">-ResourceType</span></span>
<span data-ttu-id="19670-152">Az erőforrás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="19670-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="19670-153">Adatbázis például az alábbi erőforrástípust követi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="19670-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19670-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="19670-154">-TenantLevel</span></span>
<span data-ttu-id="19670-155">Azt jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="19670-155">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19670-156">-Confirm</span></span>
<span data-ttu-id="19670-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="19670-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19670-158">-WhatIf</span></span>
<span data-ttu-id="19670-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="19670-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19670-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19670-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19670-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19670-161">CommonParameters</span></span>
<span data-ttu-id="19670-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19670-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19670-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19670-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19670-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19670-164">INPUTS</span></span>

### <span data-ttu-id="19670-165">System.String</span><span class="sxs-lookup"><span data-stu-id="19670-165">System.String</span></span>

## <span data-ttu-id="19670-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19670-166">OUTPUTS</span></span>

### <span data-ttu-id="19670-167">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="19670-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19670-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19670-168">NOTES</span></span>

## <span data-ttu-id="19670-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19670-169">RELATED LINKS</span></span>
