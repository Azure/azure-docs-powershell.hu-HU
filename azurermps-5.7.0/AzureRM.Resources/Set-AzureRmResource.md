---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679710"
---
# <span data-ttu-id="06edc-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="06edc-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="06edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06edc-102">SYNOPSIS</span></span>
<span data-ttu-id="06edc-103">Módosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="06edc-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06edc-104">SYNTAX</span></span>

### <span data-ttu-id="06edc-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06edc-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06edc-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="06edc-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06edc-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="06edc-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06edc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="06edc-108">DESCRIPTION</span></span>
<span data-ttu-id="06edc-109">A **set-AzureRmResource** parancsmag egy meglévő Azure-erőforrást módosít.</span><span class="sxs-lookup"><span data-stu-id="06edc-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="06edc-110">Adjon meg egy olyan erőforrást, amelyet név és típus vagy azonosító szerint szeretne módosítani.</span><span class="sxs-lookup"><span data-stu-id="06edc-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="06edc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="06edc-111">EXAMPLES</span></span>

### <span data-ttu-id="06edc-112">Példa 1: erőforrás módosítása</span><span class="sxs-lookup"><span data-stu-id="06edc-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="06edc-113">Az első parancs a ContosoSite nevű erőforrást a Get-AzureRmResource parancsmag használatával kapja, majd a $Resource változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="06edc-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="06edc-114">A második parancs módosítja a $Resource tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="06edc-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="06edc-115">A végleges parancs frissíti az erőforrást, hogy egyezzen $Resource.</span><span class="sxs-lookup"><span data-stu-id="06edc-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="06edc-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06edc-116">PARAMETERS</span></span>

### <span data-ttu-id="06edc-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="06edc-117">-ApiVersion</span></span>
<span data-ttu-id="06edc-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="06edc-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="06edc-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="06edc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06edc-120">-AsJob</span></span>
<span data-ttu-id="06edc-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="06edc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06edc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06edc-122">-DefaultProfile</span></span>
<span data-ttu-id="06edc-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="06edc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06edc-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="06edc-124">-ExtensionResourceName</span></span>
<span data-ttu-id="06edc-125">Az erőforráshoz tartozó mellék-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="06edc-126">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="06edc-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="06edc-127">kiszolgálónév- `/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="06edc-127">server name`/`database name</span></span>

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

### <span data-ttu-id="06edc-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="06edc-128">-ExtensionResourceType</span></span>
<span data-ttu-id="06edc-129">A bővítmény-erőforrás erőforrás-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="06edc-130">Ha a bővítmény erőforrása például egy adatbázis, a következőket adja meg:</span><span class="sxs-lookup"><span data-stu-id="06edc-130">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="06edc-131">-Force</span><span class="sxs-lookup"><span data-stu-id="06edc-131">-Force</span></span>
<span data-ttu-id="06edc-132">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="06edc-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06edc-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="06edc-133">-Kind</span></span>
<span data-ttu-id="06edc-134">Az erőforráshoz tartozó erőforrás-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06edc-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="06edc-135">-ODataQuery</span></span>
<span data-ttu-id="06edc-136">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="06edc-137">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="06edc-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="06edc-138">-Terv</span><span class="sxs-lookup"><span data-stu-id="06edc-138">-Plan</span></span>
<span data-ttu-id="06edc-139">Az erőforrásterv tulajdonságait adja meg ujjlenyomat-táblázatként az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="06edc-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06edc-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="06edc-140">-Pre</span></span>
<span data-ttu-id="06edc-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="06edc-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="06edc-142">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="06edc-142">-Properties</span></span>
<span data-ttu-id="06edc-143">Az erőforrás erőforrás-tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06edc-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06edc-144">-ResourceGroupName</span></span>
<span data-ttu-id="06edc-145">Annak az erőforráscsoport a nevét adja meg, ahol a parancsmag módosítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="06edc-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="06edc-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06edc-146">-ResourceId</span></span>
<span data-ttu-id="06edc-147">A teljesen minősített erőforrás-azonosítót adja meg, az előfizetéssel együtt, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="06edc-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="06edc-148">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="06edc-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="06edc-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="06edc-149">-ResourceName</span></span>
<span data-ttu-id="06edc-150">Az erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="06edc-151">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="06edc-151">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="06edc-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="06edc-152">-ResourceType</span></span>
<span data-ttu-id="06edc-153">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="06edc-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="06edc-154">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="06edc-154">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="06edc-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="06edc-155">-Sku</span></span>
<span data-ttu-id="06edc-156">Az erőforrás SKU-objektumát adja meg kivonatoló táblázatként.</span><span class="sxs-lookup"><span data-stu-id="06edc-156">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="06edc-157">-Címke</span><span class="sxs-lookup"><span data-stu-id="06edc-157">-Tag</span></span>
<span data-ttu-id="06edc-158">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="06edc-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="06edc-159">Példa:</span><span class="sxs-lookup"><span data-stu-id="06edc-159">For example:</span></span>

<span data-ttu-id="06edc-160">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="06edc-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06edc-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="06edc-161">-TenantLevel</span></span>
<span data-ttu-id="06edc-162">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="06edc-162">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="06edc-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="06edc-163">-UsePatchSemantics</span></span>
<span data-ttu-id="06edc-164">Azt jelzi, hogy ez a parancsmag HTTP-hiba helyett HTTP-javítást használ az objektum frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="06edc-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="06edc-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06edc-165">-Confirm</span></span>
<span data-ttu-id="06edc-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06edc-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06edc-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06edc-167">-WhatIf</span></span>
<span data-ttu-id="06edc-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06edc-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06edc-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06edc-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06edc-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06edc-170">CommonParameters</span></span>
<span data-ttu-id="06edc-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06edc-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06edc-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06edc-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06edc-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06edc-173">INPUTS</span></span>

### <span data-ttu-id="06edc-174">Nincs</span><span class="sxs-lookup"><span data-stu-id="06edc-174">None</span></span>
<span data-ttu-id="06edc-175">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="06edc-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06edc-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06edc-176">OUTPUTS</span></span>

### <span data-ttu-id="06edc-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="06edc-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="06edc-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06edc-178">NOTES</span></span>

## <span data-ttu-id="06edc-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06edc-179">RELATED LINKS</span></span>

[<span data-ttu-id="06edc-180">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="06edc-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="06edc-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="06edc-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="06edc-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="06edc-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="06edc-183">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="06edc-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="06edc-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="06edc-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
