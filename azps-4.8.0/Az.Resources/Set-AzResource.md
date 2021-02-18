---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 82e06a4736a613111efac452eb1fced2713dc470
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415750"
---
# <span data-ttu-id="e5fe1-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="e5fe1-101">Set-AzResource</span></span>

## <span data-ttu-id="e5fe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fe1-103">Módosít egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-103">Modifies a resource.</span></span>

## <span data-ttu-id="e5fe1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5fe1-104">SYNTAX</span></span>

### <span data-ttu-id="e5fe1-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5fe1-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5fe1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5fe1-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5fe1-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e5fe1-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5fe1-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e5fe1-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5fe1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5fe1-109">DESCRIPTION</span></span>
<span data-ttu-id="e5fe1-110">A **Set-AzResource** parancsmag módosít egy meglévő Azure-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="e5fe1-111">Adjon meg egy nevet és típust, illetve azonosító szerint módosítani kívánt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="e5fe1-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5fe1-112">EXAMPLES</span></span>

### <span data-ttu-id="e5fe1-113">1. példa: Erőforrás módosítása</span><span class="sxs-lookup"><span data-stu-id="e5fe1-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="e5fe1-114">Az első parancs a ContosoSite nevű erőforrást a Get-AzResource parancsmag használatával kapja meg, majd a $Resource tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="e5fe1-115">A második parancs módosítja a $Resource.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="e5fe1-116">Az utolsó parancs frissíti az erőforrást a $Resource.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="e5fe1-117">2. példa: Egy adott erőforráscsoport összes erőforrásának módosítása</span><span class="sxs-lookup"><span data-stu-id="e5fe1-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="e5fe1-118">Az első parancs a testrg erőforráscsoportban található erőforrásokat kapja meg, majd tárolja őket a $Resource változóban.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="e5fe1-119">A második parancs az erőforráscsoportban az erőforrások mindegyikét átveszi, és felvesz hozzájuk egy új címkét.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="e5fe1-120">A végleges parancs frissíti ezeket az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="e5fe1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5fe1-121">PARAMETERS</span></span>

### <span data-ttu-id="e5fe1-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5fe1-122">-ApiVersion</span></span>
<span data-ttu-id="e5fe1-123">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5fe1-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e5fe1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5fe1-125">-AsJob</span></span>
<span data-ttu-id="e5fe1-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e5fe1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5fe1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fe1-127">-DefaultProfile</span></span>
<span data-ttu-id="e5fe1-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5fe1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5fe1-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e5fe1-129">-ExtensionResourceName</span></span>
<span data-ttu-id="e5fe1-130">Az erőforrás bővítményerőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="e5fe1-131">Adatbázis megadásához például használja a következő formátumot: kiszolgálónév `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="e5fe1-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="e5fe1-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e5fe1-132">-ExtensionResourceType</span></span>
<span data-ttu-id="e5fe1-133">Egy bővítményerőforrás erőforrástípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e5fe1-134">Ha például a bővítményerőforrás egy adatbázis, adja meg az alábbiakat: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e5fe1-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e5fe1-135">-Force</span><span class="sxs-lookup"><span data-stu-id="e5fe1-135">-Force</span></span>
<span data-ttu-id="e5fe1-136">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5fe1-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5fe1-137">-InputObject</span></span>
<span data-ttu-id="e5fe1-138">A frissítenie kell az erőforrás objektum reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe1-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="e5fe1-139">-Kind</span></span>
<span data-ttu-id="e5fe1-140">Az erőforrás erőforrástípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe1-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e5fe1-141">-ODataQuery</span></span>
<span data-ttu-id="e5fe1-142">OData-stílusszűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="e5fe1-143">Ez a parancsmag minden más szűrő mellett hozzáfűzi ezt az értéket a kérelemhez.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e5fe1-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="e5fe1-144">-Plan</span></span>
<span data-ttu-id="e5fe1-145">Az erőforrás erőforrásterv-tulajdonságait adja meg kivonattáblaként az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe1-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5fe1-146">-Pre</span></span>
<span data-ttu-id="e5fe1-147">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5fe1-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="e5fe1-148">-Properties</span></span>
<span data-ttu-id="e5fe1-149">Megadja az erőforrás erőforrás-tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fe1-150">-ResourceGroupName</span></span>
<span data-ttu-id="e5fe1-151">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag módosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="e5fe1-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5fe1-152">-ResourceId</span></span>
<span data-ttu-id="e5fe1-153">A teljes erőforrás-azonosítót adja meg az előfizetéssel együtt, az alábbi `/subscriptions/` példának megfelelően: előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e5fe1-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e5fe1-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e5fe1-154">-ResourceName</span></span>
<span data-ttu-id="e5fe1-155">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="e5fe1-156">Adatbázis megadásához például használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e5fe1-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e5fe1-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e5fe1-157">-ResourceType</span></span>
<span data-ttu-id="e5fe1-158">Az erőforrás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="e5fe1-159">Adatbázis például az alábbi erőforrástípust követi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e5fe1-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e5fe1-160">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="e5fe1-160">-Sku</span></span>
<span data-ttu-id="e5fe1-161">Az erőforrás termékváltozat-objektumát adja meg kivonattáblaként.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe1-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5fe1-162">-Tag</span></span>
<span data-ttu-id="e5fe1-163">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5fe1-164">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="e5fe1-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe1-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e5fe1-165">-TenantLevel</span></span>
<span data-ttu-id="e5fe1-166">Azt jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e5fe1-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="e5fe1-167">-UsePatchSemantics</span></span>
<span data-ttu-id="e5fe1-168">Azt jelzi, hogy ez a parancsmag HTTP-javítást használ az objektum frissítéséhez HTTP PUT helyett.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="e5fe1-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5fe1-169">-Confirm</span></span>
<span data-ttu-id="e5fe1-170">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fe1-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fe1-171">-WhatIf</span></span>
<span data-ttu-id="e5fe1-172">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5fe1-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fe1-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fe1-174">CommonParameters</span></span>
<span data-ttu-id="e5fe1-175">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fe1-176">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5fe1-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fe1-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5fe1-177">INPUTS</span></span>

### <span data-ttu-id="e5fe1-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="e5fe1-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="e5fe1-179">System.String</span><span class="sxs-lookup"><span data-stu-id="e5fe1-179">System.String</span></span>

### <span data-ttu-id="e5fe1-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e5fe1-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="e5fe1-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5fe1-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5fe1-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5fe1-182">OUTPUTS</span></span>

### <span data-ttu-id="e5fe1-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e5fe1-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5fe1-184">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5fe1-184">NOTES</span></span>

## <span data-ttu-id="e5fe1-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5fe1-185">RELATED LINKS</span></span>


[<span data-ttu-id="e5fe1-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e5fe1-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="e5fe1-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="e5fe1-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="e5fe1-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="e5fe1-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="e5fe1-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="e5fe1-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
