---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494373"
---
# <span data-ttu-id="0e914-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0e914-101">New-AzureRmResource</span></span>

## <span data-ttu-id="0e914-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e914-102">SYNOPSIS</span></span>
<span data-ttu-id="0e914-103">Létrehoz egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="0e914-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e914-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e914-104">SYNTAX</span></span>

### <span data-ttu-id="0e914-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e914-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e914-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0e914-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e914-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0e914-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e914-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e914-108">DESCRIPTION</span></span>
<span data-ttu-id="0e914-109">A **New-AzureRmResource** parancsmag Azure-erőforrást hoz létre, például egy webhelyet, az Azure SQL-adatbázis kiszolgálóját vagy az Azure SQL-adatbázist egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="0e914-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="0e914-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0e914-110">EXAMPLES</span></span>

### <span data-ttu-id="0e914-111">Példa 1: erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="0e914-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="0e914-112">Ez a parancs olyan erőforrást hoz létre, amely a ResourceGroup11 webhelye.</span><span class="sxs-lookup"><span data-stu-id="0e914-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="0e914-113">2. példa: erőforrás létrehozása a splatting használatával</span><span class="sxs-lookup"><span data-stu-id="0e914-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="0e914-114">Ez a parancs olyan erőforrást hoz létre, amely a ResourceGroup11 webhelye.</span><span class="sxs-lookup"><span data-stu-id="0e914-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="0e914-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e914-115">PARAMETERS</span></span>

### <span data-ttu-id="0e914-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0e914-116">-ApiVersion</span></span>
<span data-ttu-id="0e914-117">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="0e914-118">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0e914-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e914-119">-AsJob</span></span>
<span data-ttu-id="0e914-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0e914-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e914-121">-DefaultProfile</span></span>
<span data-ttu-id="0e914-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e914-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0e914-123">-ExtensionResourceName</span></span>
<span data-ttu-id="0e914-124">Az erőforráshoz tartozó mellék-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="0e914-125">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="0e914-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="0e914-126">kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="0e914-126">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0e914-127">-ExtensionResourceType</span></span>
<span data-ttu-id="0e914-128">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="0e914-129">Ha például a bővítmény erőforrása adatbázis, adja meg az alábbi típust:</span><span class="sxs-lookup"><span data-stu-id="0e914-129">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0e914-130">-Force</span></span>
<span data-ttu-id="0e914-131">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0e914-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-132">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="0e914-132">-IsFullObject</span></span>
<span data-ttu-id="0e914-133">Azt jelzi, hogy a *Tulajdonságok* paramétert megadó objektum a teljes objektum.</span><span class="sxs-lookup"><span data-stu-id="0e914-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-134">-Kind</span><span class="sxs-lookup"><span data-stu-id="0e914-134">-Kind</span></span>
<span data-ttu-id="0e914-135">Az erőforráshoz tartozó erőforrás-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-135">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="0e914-136">-Location</span></span>
<span data-ttu-id="0e914-137">Az erőforrás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="0e914-138">Adja meg az adatközpont helyét (például Közép-amerikai vagy Délkelet-ázsiai).</span><span class="sxs-lookup"><span data-stu-id="0e914-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="0e914-139">Az erőforrást tetszőleges helyre helyezheti, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="0e914-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="0e914-140">Az erőforráscsoportok különböző helyekről származó erőforrásokat tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="0e914-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="0e914-141">Ha meg szeretné állapítani, hogy mely helyek támogatják az egyes erőforrás-típusokat, használja az Get-AzureLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0e914-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0e914-142">-ODataQuery</span></span>
<span data-ttu-id="0e914-143">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="0e914-144">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="0e914-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-145">-Terv</span><span class="sxs-lookup"><span data-stu-id="0e914-145">-Plan</span></span>
<span data-ttu-id="0e914-146">Az erőforrásterv tulajdonságait jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="0e914-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="0e914-147">-Pre</span></span>
<span data-ttu-id="0e914-148">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0e914-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-149">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="0e914-149">-Properties</span></span>
<span data-ttu-id="0e914-150">Az erőforrás erőforrás-tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="0e914-151">Ezzel a paraméterrel megadhatja az erőforrás típusára jellemző tulajdonságok értékét.</span><span class="sxs-lookup"><span data-stu-id="0e914-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e914-152">-ResourceGroupName</span></span>
<span data-ttu-id="0e914-153">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag létrehozta az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="0e914-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e914-154">-ResourceId</span></span>
<span data-ttu-id="0e914-155">A teljesen minősített erőforrás-azonosítót adja meg, az előfizetéssel együtt, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="0e914-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="0e914-156">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0e914-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0e914-157">-ResourceName</span></span>
<span data-ttu-id="0e914-158">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-158">Specifies the name of the resource.</span></span> <span data-ttu-id="0e914-159">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="0e914-159">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0e914-160">-ResourceType</span></span>
<span data-ttu-id="0e914-161">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e914-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="0e914-162">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="0e914-162">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="0e914-163">-Sku</span></span>
<span data-ttu-id="0e914-164">Egy olyan kivonatoló táblázat, amely a SKU tulajdonságát képviseli.</span><span class="sxs-lookup"><span data-stu-id="0e914-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-165">-Címke</span><span class="sxs-lookup"><span data-stu-id="0e914-165">-Tag</span></span>
<span data-ttu-id="0e914-166">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0e914-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e914-167">Példa:</span><span class="sxs-lookup"><span data-stu-id="0e914-167">For example:</span></span>

<span data-ttu-id="0e914-168">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0e914-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0e914-169">-TenantLevel</span></span>
<span data-ttu-id="0e914-170">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="0e914-170">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e914-171">-Confirm</span></span>
<span data-ttu-id="0e914-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e914-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e914-173">-WhatIf</span></span>
<span data-ttu-id="0e914-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e914-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e914-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e914-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e914-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e914-176">CommonParameters</span></span>
<span data-ttu-id="0e914-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e914-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e914-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e914-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e914-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e914-179">INPUTS</span></span>

### <span data-ttu-id="0e914-180">Nincs</span><span class="sxs-lookup"><span data-stu-id="0e914-180">None</span></span>
<span data-ttu-id="0e914-181">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0e914-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e914-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e914-182">OUTPUTS</span></span>

### <span data-ttu-id="0e914-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0e914-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0e914-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e914-184">NOTES</span></span>

## <span data-ttu-id="0e914-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e914-185">RELATED LINKS</span></span>

[<span data-ttu-id="0e914-186">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0e914-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="0e914-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0e914-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="0e914-188">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0e914-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="0e914-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0e914-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="0e914-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0e914-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
