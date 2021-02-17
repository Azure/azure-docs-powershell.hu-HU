---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: eea8d72285e478f9eecb0a34f80cae5787ecec83
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405295"
---
# <span data-ttu-id="a1f9d-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="a1f9d-101">New-AzResource</span></span>

## <span data-ttu-id="a1f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f9d-103">Létrehoz egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-103">Creates a resource.</span></span>

## <span data-ttu-id="a1f9d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1f9d-104">SYNTAX</span></span>

### <span data-ttu-id="a1f9d-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1f9d-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1f9d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a1f9d-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f9d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a1f9d-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1f9d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1f9d-108">DESCRIPTION</span></span>
<span data-ttu-id="a1f9d-109">A **New-AzResource** parancsmag létrehoz egy Azure-erőforrást, például egy webhelyet, egy Azure SQL-adatbázis-kiszolgálót vagy egy Azure SQL-adatbázist egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="a1f9d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1f9d-110">EXAMPLES</span></span>

### <span data-ttu-id="a1f9d-111">1. példa: Erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="a1f9d-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="a1f9d-112">Ez a parancs olyan erőforrást hoz létre, amely egy webhely az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="a1f9d-113">2. példa: Erőforrás létrehozása splatting használatával</span><span class="sxs-lookup"><span data-stu-id="a1f9d-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="a1f9d-114">Ez a parancs olyan erőforrást hoz létre, amely egy webhely az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="a1f9d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1f9d-115">PARAMETERS</span></span>

### <span data-ttu-id="a1f9d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a1f9d-116">-ApiVersion</span></span>
<span data-ttu-id="a1f9d-117">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="a1f9d-118">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a1f9d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1f9d-119">-AsJob</span></span>
<span data-ttu-id="a1f9d-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a1f9d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1f9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f9d-121">-DefaultProfile</span></span>
<span data-ttu-id="a1f9d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a1f9d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1f9d-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a1f9d-123">-ExtensionResourceName</span></span>
<span data-ttu-id="a1f9d-124">Az erőforrás bővítményerőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="a1f9d-125">Adatbázis megadásához például használja a következő formátumot: kiszolgálónév `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="a1f9d-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="a1f9d-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a1f9d-126">-ExtensionResourceType</span></span>
<span data-ttu-id="a1f9d-127">Egy bővítményerőforrás erőforrástípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a1f9d-128">Ha például a bővítményerőforrás egy adatbázis, adja meg a következő típust: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a1f9d-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a1f9d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a1f9d-129">-Force</span></span>
<span data-ttu-id="a1f9d-130">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1f9d-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="a1f9d-131">-IsFullObject</span></span>
<span data-ttu-id="a1f9d-132">Azt jelzi, hogy a *Properties* paraméterben megadott objektum a teljes objektum.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="a1f9d-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="a1f9d-133">-Kind</span></span>
<span data-ttu-id="a1f9d-134">Az erőforrás erőforrástípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="a1f9d-135">-Location</span><span class="sxs-lookup"><span data-stu-id="a1f9d-135">-Location</span></span>
<span data-ttu-id="a1f9d-136">Az erőforrás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="a1f9d-137">Adja meg az adatközpont helyét, például Közép-Egyesült Államok vagy Délkelet-Ázsia.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="a1f9d-138">Az erőforrásokat bármely olyan helyen el lehet helyezése, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="a1f9d-139">Az erőforráscsoportok különböző helyekről tartalmazhatnak erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="a1f9d-140">Ha meg szeretné állapítani, hogy mely helyek támogatják az egyes erőforrástípusokat, használja a Get-AzLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="a1f9d-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a1f9d-141">-ODataQuery</span></span>
<span data-ttu-id="a1f9d-142">OData-stílusszűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="a1f9d-143">Ez a parancsmag minden más szűrő mellett hozzáfűzi ezt az értéket a kérelemhez.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a1f9d-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="a1f9d-144">-Plan</span></span>
<span data-ttu-id="a1f9d-145">Az erőforrásterv tulajdonságait képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f9d-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="a1f9d-146">-Pre</span></span>
<span data-ttu-id="a1f9d-147">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1f9d-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="a1f9d-148">-Properties</span></span>
<span data-ttu-id="a1f9d-149">Megadja az erőforrás erőforrás-tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="a1f9d-150">Ezzel a paraméterrel megadhatja az erőforrástípusra jellemző tulajdonságok értékeit.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f9d-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f9d-151">-ResourceGroupName</span></span>
<span data-ttu-id="a1f9d-152">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag létrehozza az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="a1f9d-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1f9d-153">-ResourceId</span></span>
<span data-ttu-id="a1f9d-154">A teljes erőforrás-azonosítót adja meg az előfizetéssel együtt, az alábbi `/subscriptions/` példának megfelelően: előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a1f9d-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a1f9d-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a1f9d-155">-ResourceName</span></span>
<span data-ttu-id="a1f9d-156">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-156">Specifies the name of the resource.</span></span> <span data-ttu-id="a1f9d-157">Adatbázis megadásához például használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a1f9d-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a1f9d-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a1f9d-158">-ResourceType</span></span>
<span data-ttu-id="a1f9d-159">Az erőforrás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="a1f9d-160">Adatbázis például az alábbi erőforrástípust követi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a1f9d-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a1f9d-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="a1f9d-161">-Sku</span></span>
<span data-ttu-id="a1f9d-162">A termékváltozat tulajdonságait képviselő kivonattábla.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="a1f9d-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1f9d-163">-Tag</span></span>
<span data-ttu-id="a1f9d-164">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a1f9d-165">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="a1f9d-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f9d-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a1f9d-166">-TenantLevel</span></span>
<span data-ttu-id="a1f9d-167">Azt jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a1f9d-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1f9d-168">-Confirm</span></span>
<span data-ttu-id="a1f9d-169">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f9d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f9d-170">-WhatIf</span></span>
<span data-ttu-id="a1f9d-171">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1f9d-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f9d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f9d-173">CommonParameters</span></span>
<span data-ttu-id="a1f9d-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f9d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f9d-175">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1f9d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f9d-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1f9d-176">INPUTS</span></span>

### <span data-ttu-id="a1f9d-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1f9d-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a1f9d-178">System.String</span><span class="sxs-lookup"><span data-stu-id="a1f9d-178">System.String</span></span>

## <span data-ttu-id="a1f9d-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1f9d-179">OUTPUTS</span></span>

### <span data-ttu-id="a1f9d-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a1f9d-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a1f9d-181">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1f9d-181">NOTES</span></span>

## <span data-ttu-id="a1f9d-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1f9d-182">RELATED LINKS</span></span>


[<span data-ttu-id="a1f9d-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a1f9d-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="a1f9d-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="a1f9d-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="a1f9d-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="a1f9d-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="a1f9d-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="a1f9d-186">Set-AzResource</span></span>](./Set-AzResource.md)
