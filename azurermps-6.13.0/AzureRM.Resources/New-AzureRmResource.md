---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: 57e4bd86ad3f5205749579e190960ea4f8e70588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672093"
---
# <span data-ttu-id="fdfcc-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fdfcc-101">New-AzureRmResource</span></span>

## <span data-ttu-id="fdfcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdfcc-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfcc-103">Létrehoz egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdfcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdfcc-104">SYNTAX</span></span>

### <span data-ttu-id="fdfcc-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdfcc-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdfcc-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="fdfcc-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfcc-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fdfcc-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdfcc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdfcc-108">DESCRIPTION</span></span>
<span data-ttu-id="fdfcc-109">A **New-AzureRmResource** parancsmag Azure-erőforrást hoz létre, például egy webhelyet, az Azure SQL-adatbázis kiszolgálóját vagy az Azure SQL-adatbázist egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="fdfcc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fdfcc-110">EXAMPLES</span></span>

### <span data-ttu-id="fdfcc-111">Példa 1: erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="fdfcc-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="fdfcc-112">Ez a parancs olyan erőforrást hoz létre, amely a ResourceGroup11 webhelye.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="fdfcc-113">2. példa: erőforrás létrehozása a splatting használatával</span><span class="sxs-lookup"><span data-stu-id="fdfcc-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="fdfcc-114">Ez a parancs olyan erőforrást hoz létre, amely a ResourceGroup11 webhelye.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="fdfcc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdfcc-115">PARAMETERS</span></span>

### <span data-ttu-id="fdfcc-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fdfcc-116">-ApiVersion</span></span>
<span data-ttu-id="fdfcc-117">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="fdfcc-118">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fdfcc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdfcc-119">-AsJob</span></span>
<span data-ttu-id="fdfcc-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fdfcc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdfcc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfcc-121">-DefaultProfile</span></span>
<span data-ttu-id="fdfcc-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fdfcc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdfcc-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="fdfcc-123">-ExtensionResourceName</span></span>
<span data-ttu-id="fdfcc-124">Az erőforráshoz tartozó mellék-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="fdfcc-125">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="fdfcc-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="fdfcc-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fdfcc-126">-ExtensionResourceType</span></span>
<span data-ttu-id="fdfcc-127">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="fdfcc-128">Ha például a bővítmény erőforrása adatbázis, adja meg az alábbi típust: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fdfcc-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="fdfcc-129">-Force</span><span class="sxs-lookup"><span data-stu-id="fdfcc-129">-Force</span></span>
<span data-ttu-id="fdfcc-130">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fdfcc-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="fdfcc-131">-IsFullObject</span></span>
<span data-ttu-id="fdfcc-132">Azt jelzi, hogy a *Tulajdonságok* paramétert megadó objektum a teljes objektum.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="fdfcc-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="fdfcc-133">-Kind</span></span>
<span data-ttu-id="fdfcc-134">Az erőforráshoz tartozó erőforrás-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="fdfcc-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="fdfcc-135">-Location</span></span>
<span data-ttu-id="fdfcc-136">Az erőforrás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="fdfcc-137">Adja meg az adatközpont helyét (például Közép-amerikai vagy Délkelet-ázsiai).</span><span class="sxs-lookup"><span data-stu-id="fdfcc-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="fdfcc-138">Az erőforrást tetszőleges helyre helyezheti, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="fdfcc-139">Az erőforráscsoportok különböző helyekről származó erőforrásokat tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="fdfcc-140">Ha meg szeretné állapítani, hogy mely helyek támogatják az egyes erőforrás-típusokat, használja az Get-AzureLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="fdfcc-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fdfcc-141">-ODataQuery</span></span>
<span data-ttu-id="fdfcc-142">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="fdfcc-143">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="fdfcc-144">-Terv</span><span class="sxs-lookup"><span data-stu-id="fdfcc-144">-Plan</span></span>
<span data-ttu-id="fdfcc-145">Az erőforrásterv tulajdonságait jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="fdfcc-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="fdfcc-146">-Pre</span></span>
<span data-ttu-id="fdfcc-147">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fdfcc-148">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="fdfcc-148">-Properties</span></span>
<span data-ttu-id="fdfcc-149">Az erőforrás erőforrás-tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="fdfcc-150">Ezzel a paraméterrel megadhatja az erőforrás típusára jellemző tulajdonságok értékét.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="fdfcc-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfcc-151">-ResourceGroupName</span></span>
<span data-ttu-id="fdfcc-152">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag létrehozta az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="fdfcc-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfcc-153">-ResourceId</span></span>
<span data-ttu-id="fdfcc-154">A teljes értékű erőforrás-azonosítót adja meg, az előfizetéssel együtt, ahogy az alábbi példában: `/subscriptions/` előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fdfcc-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="fdfcc-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fdfcc-155">-ResourceName</span></span>
<span data-ttu-id="fdfcc-156">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-156">Specifies the name of the resource.</span></span> <span data-ttu-id="fdfcc-157">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fdfcc-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="fdfcc-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fdfcc-158">-ResourceType</span></span>
<span data-ttu-id="fdfcc-159">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="fdfcc-160">Adatbázis esetén például az erőforrás típusa az alábbi: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fdfcc-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="fdfcc-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="fdfcc-161">-Sku</span></span>
<span data-ttu-id="fdfcc-162">Egy olyan kivonatoló táblázat, amely a SKU tulajdonságát képviseli.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="fdfcc-163">-Címke</span><span class="sxs-lookup"><span data-stu-id="fdfcc-163">-Tag</span></span>
<span data-ttu-id="fdfcc-164">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fdfcc-165">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fdfcc-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fdfcc-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fdfcc-166">-TenantLevel</span></span>
<span data-ttu-id="fdfcc-167">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="fdfcc-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fdfcc-168">-Confirm</span></span>
<span data-ttu-id="fdfcc-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdfcc-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfcc-170">-WhatIf</span></span>
<span data-ttu-id="fdfcc-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdfcc-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdfcc-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdfcc-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfcc-173">CommonParameters</span></span>
<span data-ttu-id="fdfcc-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdfcc-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfcc-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdfcc-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfcc-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdfcc-176">INPUTS</span></span>

### <span data-ttu-id="fdfcc-177">Nincs</span><span class="sxs-lookup"><span data-stu-id="fdfcc-177">None</span></span>

## <span data-ttu-id="fdfcc-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdfcc-178">OUTPUTS</span></span>

### <span data-ttu-id="fdfcc-179">Microsoft. Azure. Command. ResourceManagement. models. PSResource</span><span class="sxs-lookup"><span data-stu-id="fdfcc-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="fdfcc-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdfcc-180">NOTES</span></span>

## <span data-ttu-id="fdfcc-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdfcc-181">RELATED LINKS</span></span>

[<span data-ttu-id="fdfcc-182">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fdfcc-182">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="fdfcc-183">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fdfcc-183">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="fdfcc-184">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fdfcc-184">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="fdfcc-185">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fdfcc-185">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="fdfcc-186">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fdfcc-186">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
