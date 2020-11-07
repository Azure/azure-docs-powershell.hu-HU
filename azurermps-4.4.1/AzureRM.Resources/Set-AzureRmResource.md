---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679944"
---
# <span data-ttu-id="6e08b-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6e08b-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="6e08b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e08b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e08b-103">Módosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6e08b-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e08b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e08b-104">SYNTAX</span></span>

### <span data-ttu-id="6e08b-105">Az erőforrás azonosítója. (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e08b-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e08b-106">Az előfizetési szinten található erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6e08b-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e08b-107">A bérlői szinten lakóhellyel rendelkező erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6e08b-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e08b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e08b-108">DESCRIPTION</span></span>
<span data-ttu-id="6e08b-109">A **set-AzureRmResource** parancsmag egy meglévő Azure-erőforrást módosít.</span><span class="sxs-lookup"><span data-stu-id="6e08b-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="6e08b-110">Adjon meg egy olyan erőforrást, amelyet név és típus vagy azonosító szerint szeretne módosítani.</span><span class="sxs-lookup"><span data-stu-id="6e08b-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="6e08b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6e08b-111">EXAMPLES</span></span>

### <span data-ttu-id="6e08b-112">Példa 1: erőforrás módosítása</span><span class="sxs-lookup"><span data-stu-id="6e08b-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="6e08b-113">Az első parancs a ContosoSite nevű erőforrást a Get-AzureRmResource parancsmag használatával kapja, majd a $Resource változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6e08b-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="6e08b-114">A második parancs módosítja a $Resource tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="6e08b-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="6e08b-115">A végleges parancs frissíti az erőforrást, hogy egyezzen $Resource.</span><span class="sxs-lookup"><span data-stu-id="6e08b-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="6e08b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e08b-116">PARAMETERS</span></span>

### <span data-ttu-id="6e08b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6e08b-117">-ApiVersion</span></span>
<span data-ttu-id="6e08b-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6e08b-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6e08b-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6e08b-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6e08b-120">-ExtensionResourceName</span></span>
<span data-ttu-id="6e08b-121">Az erőforráshoz tartozó mellék-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="6e08b-122">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="6e08b-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="6e08b-123">kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="6e08b-123">server name`/`database name</span></span>

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

### <span data-ttu-id="6e08b-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6e08b-124">-ExtensionResourceType</span></span>
<span data-ttu-id="6e08b-125">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="6e08b-126">Ha a bővítmény erőforrása például egy adatbázis, a következőket adja meg:</span><span class="sxs-lookup"><span data-stu-id="6e08b-126">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="6e08b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="6e08b-127">-Force</span></span>
<span data-ttu-id="6e08b-128">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6e08b-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e08b-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="6e08b-129">-Kind</span></span>
<span data-ttu-id="6e08b-130">Az erőforráshoz tartozó erőforrás-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="6e08b-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6e08b-131">-ODataQuery</span></span>
<span data-ttu-id="6e08b-132">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="6e08b-133">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="6e08b-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6e08b-134">-Terv</span><span class="sxs-lookup"><span data-stu-id="6e08b-134">-Plan</span></span>
<span data-ttu-id="6e08b-135">Az erőforrásterv tulajdonságait adja meg ujjlenyomat-táblázatként az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="6e08b-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="6e08b-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e08b-136">-Pre</span></span>
<span data-ttu-id="6e08b-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6e08b-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6e08b-138">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="6e08b-138">-Properties</span></span>
<span data-ttu-id="6e08b-139">Az erőforrás erőforrás-tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="6e08b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e08b-140">-ResourceGroupName</span></span>
<span data-ttu-id="6e08b-141">Annak az erőforráscsoport a nevét adja meg, ahol a parancsmag módosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6e08b-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="6e08b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e08b-142">-ResourceId</span></span>
<span data-ttu-id="6e08b-143">A teljesen minősített erőforrás-azonosítót adja meg, az előfizetéssel együtt, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="6e08b-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="6e08b-144">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6e08b-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6e08b-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6e08b-145">-ResourceName</span></span>
<span data-ttu-id="6e08b-146">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="6e08b-147">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="6e08b-147">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="6e08b-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6e08b-148">-ResourceType</span></span>
<span data-ttu-id="6e08b-149">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e08b-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="6e08b-150">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="6e08b-150">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="6e08b-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="6e08b-151">-Sku</span></span>
<span data-ttu-id="6e08b-152">Az erőforrás SKU-objektumát adja meg kivonatoló táblázatként.</span><span class="sxs-lookup"><span data-stu-id="6e08b-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="6e08b-153">-Címke</span><span class="sxs-lookup"><span data-stu-id="6e08b-153">-Tag</span></span>
<span data-ttu-id="6e08b-154">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="6e08b-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6e08b-155">Példa:</span><span class="sxs-lookup"><span data-stu-id="6e08b-155">For example:</span></span>

<span data-ttu-id="6e08b-156">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="6e08b-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6e08b-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6e08b-157">-TenantLevel</span></span>
<span data-ttu-id="6e08b-158">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="6e08b-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6e08b-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="6e08b-159">-UsePatchSemantics</span></span>
<span data-ttu-id="6e08b-160">Azt jelzi, hogy ez a parancsmag HTTP-hiba helyett HTTP-javítást használ az objektum frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="6e08b-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="6e08b-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e08b-161">-Confirm</span></span>
<span data-ttu-id="6e08b-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e08b-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e08b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e08b-163">-WhatIf</span></span>
<span data-ttu-id="6e08b-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e08b-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e08b-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e08b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e08b-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e08b-166">-DefaultProfile</span></span>
<span data-ttu-id="6e08b-167">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e08b-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e08b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e08b-168">CommonParameters</span></span>
<span data-ttu-id="6e08b-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e08b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e08b-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e08b-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e08b-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e08b-171">INPUTS</span></span>

## <span data-ttu-id="6e08b-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e08b-172">OUTPUTS</span></span>

### <span data-ttu-id="6e08b-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6e08b-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6e08b-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e08b-174">NOTES</span></span>

## <span data-ttu-id="6e08b-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e08b-175">RELATED LINKS</span></span>

[<span data-ttu-id="6e08b-176">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6e08b-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="6e08b-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6e08b-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="6e08b-178">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6e08b-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="6e08b-179">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6e08b-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="6e08b-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6e08b-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
