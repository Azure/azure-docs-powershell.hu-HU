---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501639"
---
# <span data-ttu-id="9e83c-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e83c-101">New-AzureRmResource</span></span>

## <span data-ttu-id="9e83c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e83c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e83c-103">Létrehoz egy erőforrást.</span><span class="sxs-lookup"><span data-stu-id="9e83c-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e83c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e83c-104">SYNTAX</span></span>

### <span data-ttu-id="9e83c-105">Az erőforrás azonosítója. (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e83c-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e83c-106">Az előfizetési szinten található erőforrás.</span><span class="sxs-lookup"><span data-stu-id="9e83c-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e83c-107">A bérlői szinten lakóhellyel rendelkező erőforrás.</span><span class="sxs-lookup"><span data-stu-id="9e83c-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e83c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e83c-108">DESCRIPTION</span></span>
<span data-ttu-id="9e83c-109">A **New-AzureRmResource** parancsmag Azure-erőforrást hoz létre, például egy webhelyet, az Azure SQL-adatbázis kiszolgálóját vagy az Azure SQL-adatbázist egy erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="9e83c-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="9e83c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9e83c-110">EXAMPLES</span></span>

### <span data-ttu-id="9e83c-111">Példa 1: erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e83c-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="9e83c-112">Ez a parancs olyan erőforrást hoz létre, amely a ResourceGroup11 webhelye.</span><span class="sxs-lookup"><span data-stu-id="9e83c-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="9e83c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e83c-113">PARAMETERS</span></span>

### <span data-ttu-id="9e83c-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9e83c-114">-ApiVersion</span></span>
<span data-ttu-id="9e83c-115">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="9e83c-116">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9e83c-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9e83c-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9e83c-117">-ExtensionResourceName</span></span>
<span data-ttu-id="9e83c-118">Az erőforráshoz tartozó mellék-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="9e83c-119">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="9e83c-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="9e83c-120">kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="9e83c-120">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e83c-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9e83c-121">-ExtensionResourceType</span></span>
<span data-ttu-id="9e83c-122">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="9e83c-123">Ha például a bővítmény erőforrása adatbázis, adja meg az alábbi típust:</span><span class="sxs-lookup"><span data-stu-id="9e83c-123">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e83c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9e83c-124">-Force</span></span>
<span data-ttu-id="9e83c-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9e83c-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e83c-126">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="9e83c-126">-IsFullObject</span></span>
<span data-ttu-id="9e83c-127">Azt jelzi, hogy a *Tulajdonságok* paramétert megadó objektum a teljes objektum.</span><span class="sxs-lookup"><span data-stu-id="9e83c-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="9e83c-128">-Kind</span><span class="sxs-lookup"><span data-stu-id="9e83c-128">-Kind</span></span>
<span data-ttu-id="9e83c-129">Az erőforráshoz tartozó erőforrás-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="9e83c-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="9e83c-130">-Location</span></span>
<span data-ttu-id="9e83c-131">Az erőforrás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="9e83c-132">Adja meg az adatközpont helyét (például Közép-amerikai vagy Délkelet-ázsiai).</span><span class="sxs-lookup"><span data-stu-id="9e83c-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="9e83c-133">Az erőforrást tetszőleges helyre helyezheti, amely támogatja az adott típusú erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="9e83c-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="9e83c-134">Az erőforráscsoportok különböző helyekről származó erőforrásokat tartalmazhatnak.</span><span class="sxs-lookup"><span data-stu-id="9e83c-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="9e83c-135">Ha meg szeretné állapítani, hogy mely helyek támogatják az egyes erőforrás-típusokat, használja az Get-AzureLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9e83c-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="9e83c-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9e83c-136">-ODataQuery</span></span>
<span data-ttu-id="9e83c-137">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="9e83c-138">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="9e83c-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="9e83c-139">-Terv</span><span class="sxs-lookup"><span data-stu-id="9e83c-139">-Plan</span></span>
<span data-ttu-id="9e83c-140">Az erőforrásterv tulajdonságait jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="9e83c-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="9e83c-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="9e83c-141">-Pre</span></span>
<span data-ttu-id="9e83c-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="9e83c-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9e83c-143">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="9e83c-143">-Properties</span></span>
<span data-ttu-id="9e83c-144">Az erőforrás erőforrás-tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="9e83c-145">Ezzel a paraméterrel megadhatja az erőforrás típusára jellemző tulajdonságok értékét.</span><span class="sxs-lookup"><span data-stu-id="9e83c-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="9e83c-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e83c-146">-ResourceGroupName</span></span>
<span data-ttu-id="9e83c-147">Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag létrehozta az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="9e83c-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e83c-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e83c-148">-ResourceId</span></span>
<span data-ttu-id="9e83c-149">A teljesen minősített erőforrás-azonosítót adja meg, az előfizetéssel együtt, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="9e83c-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="9e83c-150">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9e83c-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e83c-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9e83c-151">-ResourceName</span></span>
<span data-ttu-id="9e83c-152">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-152">Specifies the name of the resource.</span></span> <span data-ttu-id="9e83c-153">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="9e83c-153">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e83c-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9e83c-154">-ResourceType</span></span>
<span data-ttu-id="9e83c-155">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e83c-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="9e83c-156">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="9e83c-156">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e83c-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e83c-157">-Sku</span></span>
<span data-ttu-id="9e83c-158">Egy olyan kivonatoló táblázat, amely a SKU tulajdonságát képviseli.</span><span class="sxs-lookup"><span data-stu-id="9e83c-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="9e83c-159">-Címke</span><span class="sxs-lookup"><span data-stu-id="9e83c-159">-Tag</span></span>
<span data-ttu-id="9e83c-160">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="9e83c-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e83c-161">Példa:</span><span class="sxs-lookup"><span data-stu-id="9e83c-161">For example:</span></span>

<span data-ttu-id="9e83c-162">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="9e83c-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9e83c-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9e83c-163">-TenantLevel</span></span>
<span data-ttu-id="9e83c-164">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="9e83c-164">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e83c-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e83c-165">-Confirm</span></span>
<span data-ttu-id="9e83c-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e83c-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e83c-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e83c-167">-WhatIf</span></span>
<span data-ttu-id="9e83c-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e83c-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e83c-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e83c-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e83c-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e83c-170">-DefaultProfile</span></span>
<span data-ttu-id="9e83c-171">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e83c-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e83c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e83c-172">CommonParameters</span></span>
<span data-ttu-id="9e83c-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e83c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e83c-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e83c-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e83c-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e83c-175">INPUTS</span></span>

## <span data-ttu-id="9e83c-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e83c-176">OUTPUTS</span></span>

### <span data-ttu-id="9e83c-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9e83c-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9e83c-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e83c-178">NOTES</span></span>

## <span data-ttu-id="9e83c-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e83c-179">RELATED LINKS</span></span>

[<span data-ttu-id="9e83c-180">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e83c-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="9e83c-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e83c-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="9e83c-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e83c-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="9e83c-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e83c-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="9e83c-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9e83c-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
