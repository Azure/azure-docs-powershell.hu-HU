---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498872"
---
# <span data-ttu-id="858e4-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="858e4-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="858e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="858e4-102">SYNOPSIS</span></span>
<span data-ttu-id="858e4-103">Erőforrások keresése megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="858e4-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="858e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="858e4-104">SYNTAX</span></span>

### <span data-ttu-id="858e4-105">GetBySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="858e4-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="858e4-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="858e4-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="858e4-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="858e4-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="858e4-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="858e4-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="858e4-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="858e4-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="858e4-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="858e4-110">DESCRIPTION</span></span>
<span data-ttu-id="858e4-111">A **Find-AzureRmResource** parancsmag meghatározott paraméterek alapján keres erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="858e4-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="858e4-112">Példák</span><span class="sxs-lookup"><span data-stu-id="858e4-112">EXAMPLES</span></span>

### <span data-ttu-id="858e4-113">1. példa: erőforrások keresése típus szerinti kereséssel és erőforrás csoport nevével</span><span class="sxs-lookup"><span data-stu-id="858e4-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="858e4-114">Ez a parancs a Microsoft. Web/webhelyek kategóriába tartozó erőforrásokat keres a karakterlánc ResourceGroup megfelelő nevekkel.</span><span class="sxs-lookup"><span data-stu-id="858e4-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="858e4-115">2. példa: erőforrások keresése típus és erőforrás neve szerint</span><span class="sxs-lookup"><span data-stu-id="858e4-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="858e4-116">Ez a parancs a Microsoft. Web/webhelyek nevű olyan erőforrást keresi meg, amely megfelel a karakterlánc-tesztnek.</span><span class="sxs-lookup"><span data-stu-id="858e4-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="858e4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="858e4-117">PARAMETERS</span></span>

### <span data-ttu-id="858e4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="858e4-118">-ApiVersion</span></span>
<span data-ttu-id="858e4-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="858e4-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="858e4-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="858e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858e4-121">-DefaultProfile</span></span>
<span data-ttu-id="858e4-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="858e4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="858e4-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="858e4-123">-ExpandProperties</span></span>
<span data-ttu-id="858e4-124">Azt jelzi, hogy ez a parancsmag kibővíti az erőforrás tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="858e4-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="858e4-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="858e4-125">-ExtensionResourceType</span></span>
<span data-ttu-id="858e4-126">Annak az erőforrásnak a bővítmény-típusát adja meg, amelyhez a parancsmag keres.</span><span class="sxs-lookup"><span data-stu-id="858e4-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="858e4-127">Például:</span><span class="sxs-lookup"><span data-stu-id="858e4-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="858e4-128">-InformationAction</span></span>
<span data-ttu-id="858e4-129">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="858e4-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="858e4-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="858e4-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="858e4-131">Folytassa</span><span class="sxs-lookup"><span data-stu-id="858e4-131">Continue</span></span>
- <span data-ttu-id="858e4-132">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="858e4-132">Ignore</span></span>
- <span data-ttu-id="858e4-133">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="858e4-133">Inquire</span></span>
- <span data-ttu-id="858e4-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="858e4-134">SilentlyContinue</span></span>
- <span data-ttu-id="858e4-135">állj</span><span class="sxs-lookup"><span data-stu-id="858e4-135">Stop</span></span>
- <span data-ttu-id="858e4-136">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="858e4-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="858e4-137">-InformationVariable</span></span>
<span data-ttu-id="858e4-138">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="858e4-139">-ODataQuery</span></span>
<span data-ttu-id="858e4-140">Egy Open Data Protocol (OData) stílusú szűrőt ad meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="858e4-141">Ez a parancsmag minden más szűrőn kívül hozzáfűzi ezt az értéket a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="858e4-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="858e4-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="858e4-142">-Pre</span></span>
<span data-ttu-id="858e4-143">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="858e4-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="858e4-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="858e4-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="858e4-145">Egy erőforráscsoport részleges nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="858e4-146">Ez a parancsmag olyan erőforrás-csoportokat tartalmaz, amelyeknek az értéke egy karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="858e4-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="858e4-147">A parancsmag erőforrásokat keres az erőforrás-csoportokban.</span><span class="sxs-lookup"><span data-stu-id="858e4-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="858e4-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="858e4-149">Az erőforráscsoport neve a teljes egyezéshez.</span><span class="sxs-lookup"><span data-stu-id="858e4-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="858e4-150">-ResourceNameContains</span></span>
<span data-ttu-id="858e4-151">Egy erőforrás részleges nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="858e4-152">A parancsmag olyan erőforrásokat keres, amelyek az értéket alkarakterláncként tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="858e4-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="858e4-153">-ResourceNameEquals</span></span>
<span data-ttu-id="858e4-154">Az erőforrás neve a teljes egyezéshez.</span><span class="sxs-lookup"><span data-stu-id="858e4-154">The resource name for a full match.</span></span> <span data-ttu-id="858e4-155">például ha az erőforrás neve testResource, megadhatja a testResource.</span><span class="sxs-lookup"><span data-stu-id="858e4-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="858e4-156">-ResourceType</span></span>
<span data-ttu-id="858e4-157">Az erőforrás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="858e4-158">Adatbázis esetén például az erőforrás típusa az alábbi:</span><span class="sxs-lookup"><span data-stu-id="858e4-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="858e4-159">Ez a parancsmag a megadott típusú erőforrásokat keresi meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-160">-Címke</span><span class="sxs-lookup"><span data-stu-id="858e4-160">-Tag</span></span>
<span data-ttu-id="858e4-161">A OData lekérdezéshez tartozó címke szűrője</span><span class="sxs-lookup"><span data-stu-id="858e4-161">The tag filter for the OData query.</span></span> <span data-ttu-id="858e4-162">A várható formátum: @ {tagName = $null} vagy @ {tagName = "tagValue"}.</span><span class="sxs-lookup"><span data-stu-id="858e4-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="858e4-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="858e4-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="858e4-165">-TenantLevel</span></span>
<span data-ttu-id="858e4-166">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="858e4-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-167">-Top</span><span class="sxs-lookup"><span data-stu-id="858e4-167">-Top</span></span>
<span data-ttu-id="858e4-168">A lekérdezni kívánt erőforrások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="858e4-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858e4-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858e4-169">CommonParameters</span></span>
<span data-ttu-id="858e4-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="858e4-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858e4-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858e4-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858e4-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="858e4-172">INPUTS</span></span>

### <span data-ttu-id="858e4-173">Nincs</span><span class="sxs-lookup"><span data-stu-id="858e4-173">None</span></span>
<span data-ttu-id="858e4-174">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="858e4-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="858e4-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="858e4-175">OUTPUTS</span></span>

### <span data-ttu-id="858e4-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="858e4-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="858e4-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="858e4-177">NOTES</span></span>

## <span data-ttu-id="858e4-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="858e4-178">RELATED LINKS</span></span>

[<span data-ttu-id="858e4-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="858e4-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="858e4-180">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="858e4-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="858e4-181">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="858e4-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="858e4-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="858e4-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="858e4-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="858e4-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
