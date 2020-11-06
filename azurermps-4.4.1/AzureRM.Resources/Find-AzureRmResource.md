---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494706"
---
# <span data-ttu-id="2deba-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2deba-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="2deba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2deba-102">SYNOPSIS</span></span>
<span data-ttu-id="2deba-103">Erőforrások keresése megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="2deba-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2deba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2deba-104">SYNTAX</span></span>

### <span data-ttu-id="2deba-105">Felsorolja az erőforrásokat a megadott hatókör alapján.</span><span class="sxs-lookup"><span data-stu-id="2deba-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="2deba-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="2deba-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2deba-107">Felsorolja az erőforrásokat a bérlői szinten megadott hatókör alapján.</span><span class="sxs-lookup"><span data-stu-id="2deba-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2deba-108">Források beszerzése több előfizetéses lekérdezéssel.</span><span class="sxs-lookup"><span data-stu-id="2deba-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2deba-109">A hashset megadott címke-objektum által létrehozott erőforrásokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2deba-110">Az erőforrásokat az egyedi név és érték paraméterként megadott címke szerint sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="2deba-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2deba-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="2deba-111">DESCRIPTION</span></span>
<span data-ttu-id="2deba-112">A **Find-AzureRmResource** parancsmag meghatározott paraméterek alapján keres erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="2deba-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="2deba-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2deba-113">EXAMPLES</span></span>

### <span data-ttu-id="2deba-114">1. példa: erőforrások keresése típus szerinti kereséssel és erőforrás csoport nevével</span><span class="sxs-lookup"><span data-stu-id="2deba-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="2deba-115">Ez a parancs a Microsoft. Web/webhelyek kategóriába tartozó erőforrásokat keres a karakterlánc ResourceGroup megfelelő nevekkel.</span><span class="sxs-lookup"><span data-stu-id="2deba-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="2deba-116">2. példa: erőforrások keresése típus és erőforrás neve szerint</span><span class="sxs-lookup"><span data-stu-id="2deba-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="2deba-117">Ez a parancs a Microsoft. Web/webhelyek nevű olyan erőforrást keresi meg, amely megfelel a karakterlánc-tesztnek.</span><span class="sxs-lookup"><span data-stu-id="2deba-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="2deba-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2deba-118">PARAMETERS</span></span>

### <span data-ttu-id="2deba-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2deba-119">-ApiVersion</span></span>
<span data-ttu-id="2deba-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2deba-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2deba-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2deba-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="2deba-122">-ExpandProperties</span></span>
<span data-ttu-id="2deba-123">Azt jelzi, hogy ez a parancsmag kibővíti az erőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="2deba-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="2deba-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="2deba-124">-ExtensionResourceType</span></span>
<span data-ttu-id="2deba-125">Annak az erőforrásnak a bővítmény-típusát adja meg, amelyhez a parancsmag keres.</span><span class="sxs-lookup"><span data-stu-id="2deba-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="2deba-126">Például:</span><span class="sxs-lookup"><span data-stu-id="2deba-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2deba-127">-InformationAction</span></span>
<span data-ttu-id="2deba-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="2deba-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2deba-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2deba-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2deba-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="2deba-130">Continue</span></span>
- <span data-ttu-id="2deba-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="2deba-131">Ignore</span></span>
- <span data-ttu-id="2deba-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="2deba-132">Inquire</span></span>
- <span data-ttu-id="2deba-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2deba-133">SilentlyContinue</span></span>
- <span data-ttu-id="2deba-134">állj</span><span class="sxs-lookup"><span data-stu-id="2deba-134">Stop</span></span>
- <span data-ttu-id="2deba-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="2deba-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2deba-136">-InformationVariable</span></span>
<span data-ttu-id="2deba-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="2deba-138">-ODataQuery</span></span>
<span data-ttu-id="2deba-139">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="2deba-140">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="2deba-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="2deba-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="2deba-141">-Pre</span></span>
<span data-ttu-id="2deba-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2deba-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2deba-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="2deba-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="2deba-144">Egy erőforráscsoport részleges nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="2deba-145">Ez a parancsmag olyan erőforrás-csoportokat tartalmaz, amelyeknek az értéke egy karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="2deba-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="2deba-146">A parancsmag erőforrásokat keres az erőforrás-csoportokban.</span><span class="sxs-lookup"><span data-stu-id="2deba-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="2deba-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="2deba-148">Az erőforráscsoport neve a teljes egyezéshez.</span><span class="sxs-lookup"><span data-stu-id="2deba-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="2deba-149">-ResourceNameContains</span></span>
<span data-ttu-id="2deba-150">Egy erőforrás részleges nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="2deba-151">A parancsmag olyan erőforrásokat keres, amelyek az értéket alkarakterláncként tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="2deba-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="2deba-152">-ResourceNameEquals</span></span>
<span data-ttu-id="2deba-153">Az erőforrás neve a teljes egyezéshez.</span><span class="sxs-lookup"><span data-stu-id="2deba-153">The resource name for a full match.</span></span> <span data-ttu-id="2deba-154">például ha az erőforrás neve testResource, megadhatja a testResource.</span><span class="sxs-lookup"><span data-stu-id="2deba-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2deba-155">-ResourceType</span></span>
<span data-ttu-id="2deba-156">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="2deba-157">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="2deba-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="2deba-158">Ez a parancsmag a megadott típusú erőforrásokat keresi meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-159">-Címke</span><span class="sxs-lookup"><span data-stu-id="2deba-159">-Tag</span></span>
<span data-ttu-id="2deba-160">A OData lekérdezéshez tartozó címke szűrője</span><span class="sxs-lookup"><span data-stu-id="2deba-160">The tag filter for the OData query.</span></span> <span data-ttu-id="2deba-161">A várható formátum: @ {tagName = $null} vagy @ {tagName = "tagValue"}.</span><span class="sxs-lookup"><span data-stu-id="2deba-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="2deba-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="2deba-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="2deba-164">-TenantLevel</span></span>
<span data-ttu-id="2deba-165">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="2deba-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-166">-Top</span><span class="sxs-lookup"><span data-stu-id="2deba-166">-Top</span></span>
<span data-ttu-id="2deba-167">A lekérdezni kívánt erőforrások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2deba-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deba-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2deba-168">-DefaultProfile</span></span>
<span data-ttu-id="2deba-169">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2deba-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2deba-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2deba-170">CommonParameters</span></span>
<span data-ttu-id="2deba-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2deba-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2deba-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2deba-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2deba-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2deba-173">INPUTS</span></span>

## <span data-ttu-id="2deba-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2deba-174">OUTPUTS</span></span>

### <span data-ttu-id="2deba-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2deba-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2deba-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2deba-176">NOTES</span></span>

## <span data-ttu-id="2deba-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2deba-177">RELATED LINKS</span></span>

[<span data-ttu-id="2deba-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2deba-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="2deba-179">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2deba-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="2deba-180">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2deba-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="2deba-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2deba-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="2deba-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="2deba-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
