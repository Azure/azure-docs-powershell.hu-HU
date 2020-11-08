---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: bf01232939881feb5a60420cde76e0e809cbcb3d
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017429"
---
# <span data-ttu-id="814fd-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="814fd-101">Set-AzResource</span></span>

## <span data-ttu-id="814fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="814fd-102">SYNOPSIS</span></span>
<span data-ttu-id="814fd-103">Módosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="814fd-103">Modifies a resource.</span></span>

## <span data-ttu-id="814fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="814fd-104">SYNTAX</span></span>

### <span data-ttu-id="814fd-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="814fd-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="814fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="814fd-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="814fd-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="814fd-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="814fd-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="814fd-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="814fd-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="814fd-109">DESCRIPTION</span></span>
<span data-ttu-id="814fd-110">A **set-AzResource** parancsmag egy meglévő Azure-erőforrást módosít.</span><span class="sxs-lookup"><span data-stu-id="814fd-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="814fd-111">Adjon meg egy olyan erőforrást, amelyet név és típus vagy azonosító szerint szeretne módosítani.</span><span class="sxs-lookup"><span data-stu-id="814fd-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="814fd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="814fd-112">EXAMPLES</span></span>

### <span data-ttu-id="814fd-113">Példa 1: erőforrás módosítása</span><span class="sxs-lookup"><span data-stu-id="814fd-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="814fd-114">Az első parancs a ContosoSite nevű erőforrást a Get-AzResource parancsmag használatával kapja, majd a $Resource változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="814fd-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="814fd-115">A második parancs módosítja a $Resource tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="814fd-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="814fd-116">A végleges parancs frissíti az erőforrást, hogy egyezzen $Resource.</span><span class="sxs-lookup"><span data-stu-id="814fd-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="814fd-117">2. példa: egy adott erőforráscsoport összes erőforrásának módosítása</span><span class="sxs-lookup"><span data-stu-id="814fd-117">Example 2: Modify all resources in a given resource group</span></span>
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

<span data-ttu-id="814fd-118">Az első parancs a testrg erőforrás csoportban kapja az erőforrásokat, majd a $Resource változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="814fd-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="814fd-119">A második parancs megismétli az erőforrás csoport minden erőforrását, és új címkét ad hozzájuk.</span><span class="sxs-lookup"><span data-stu-id="814fd-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="814fd-120">A végleges parancs frissíti ezeket az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="814fd-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="814fd-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="814fd-121">PARAMETERS</span></span>

### <span data-ttu-id="814fd-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="814fd-122">-ApiVersion</span></span>
<span data-ttu-id="814fd-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="814fd-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="814fd-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="814fd-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="814fd-125">-AsJob</span></span>
<span data-ttu-id="814fd-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="814fd-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="814fd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814fd-127">-DefaultProfile</span></span>
<span data-ttu-id="814fd-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="814fd-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="814fd-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="814fd-129">-ExtensionResourceName</span></span>
<span data-ttu-id="814fd-130">Az erőforráshoz tartozó mellék-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="814fd-131">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="814fd-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="814fd-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="814fd-132">-ExtensionResourceType</span></span>
<span data-ttu-id="814fd-133">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="814fd-134">Ha a bővítmény erőforrása például egy adatbázis, a következőket adja meg: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="814fd-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="814fd-135">-Force</span><span class="sxs-lookup"><span data-stu-id="814fd-135">-Force</span></span>
<span data-ttu-id="814fd-136">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="814fd-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="814fd-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="814fd-137">-InputObject</span></span>
<span data-ttu-id="814fd-138">A frissítendő erőforrás objektum-ábrázolása.</span><span class="sxs-lookup"><span data-stu-id="814fd-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="814fd-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="814fd-139">-Kind</span></span>
<span data-ttu-id="814fd-140">Az erőforráshoz tartozó erőforrás-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="814fd-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="814fd-141">-ODataQuery</span></span>
<span data-ttu-id="814fd-142">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="814fd-143">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="814fd-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="814fd-144">-Terv</span><span class="sxs-lookup"><span data-stu-id="814fd-144">-Plan</span></span>
<span data-ttu-id="814fd-145">Az erőforrásterv tulajdonságait adja meg ujjlenyomat-táblázatként az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="814fd-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="814fd-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="814fd-146">-Pre</span></span>
<span data-ttu-id="814fd-147">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="814fd-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="814fd-148">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="814fd-148">-Properties</span></span>
<span data-ttu-id="814fd-149">Az erőforrás erőforrás-tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="814fd-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="814fd-150">-ResourceGroupName</span></span>
<span data-ttu-id="814fd-151">Annak az erőforráscsoport a nevét adja meg, ahol a parancsmag módosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="814fd-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="814fd-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="814fd-152">-ResourceId</span></span>
<span data-ttu-id="814fd-153">A teljes értékű erőforrás-azonosítót adja meg, az előfizetéssel együtt, ahogy az alábbi példában: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="814fd-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="814fd-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="814fd-154">-ResourceName</span></span>
<span data-ttu-id="814fd-155">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="814fd-156">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="814fd-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="814fd-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="814fd-157">-ResourceType</span></span>
<span data-ttu-id="814fd-158">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="814fd-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="814fd-159">Adatbázis esetén például az erőforrás típusa az alábbi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="814fd-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="814fd-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="814fd-160">-Sku</span></span>
<span data-ttu-id="814fd-161">Az erőforrás SKU-objektumát adja meg kivonatoló táblázatként.</span><span class="sxs-lookup"><span data-stu-id="814fd-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="814fd-162">-Címke</span><span class="sxs-lookup"><span data-stu-id="814fd-162">-Tag</span></span>
<span data-ttu-id="814fd-163">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="814fd-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="814fd-164">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="814fd-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="814fd-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="814fd-165">-TenantLevel</span></span>
<span data-ttu-id="814fd-166">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="814fd-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="814fd-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="814fd-167">-UsePatchSemantics</span></span>
<span data-ttu-id="814fd-168">Azt jelzi, hogy ez a parancsmag HTTP-hiba helyett HTTP-javítást használ az objektum frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="814fd-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="814fd-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="814fd-169">-Confirm</span></span>
<span data-ttu-id="814fd-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="814fd-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="814fd-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="814fd-171">-WhatIf</span></span>
<span data-ttu-id="814fd-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="814fd-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="814fd-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="814fd-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="814fd-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814fd-174">CommonParameters</span></span>
<span data-ttu-id="814fd-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="814fd-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814fd-176">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="814fd-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814fd-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="814fd-177">INPUTS</span></span>

### <span data-ttu-id="814fd-178">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="814fd-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="814fd-179">System. String</span><span class="sxs-lookup"><span data-stu-id="814fd-179">System.String</span></span>

### <span data-ttu-id="814fd-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="814fd-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="814fd-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="814fd-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="814fd-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="814fd-182">OUTPUTS</span></span>

### <span data-ttu-id="814fd-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="814fd-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="814fd-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="814fd-184">NOTES</span></span>

## <span data-ttu-id="814fd-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="814fd-185">RELATED LINKS</span></span>

[<span data-ttu-id="814fd-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="814fd-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="814fd-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="814fd-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="814fd-188">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="814fd-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="814fd-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="814fd-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
