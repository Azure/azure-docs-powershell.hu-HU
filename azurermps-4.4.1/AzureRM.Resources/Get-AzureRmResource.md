---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500771"
---
# <span data-ttu-id="dd047-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd047-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="dd047-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd047-102">SYNOPSIS</span></span>
<span data-ttu-id="dd047-103">Erőforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="dd047-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd047-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd047-104">SYNTAX</span></span>

### <span data-ttu-id="dd047-105">A lista minden erőforrás-paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="dd047-105">The list all resources parameter set.</span></span> <span data-ttu-id="dd047-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="dd047-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd047-107">Egyetlen erőforrás beszerzése az azonosítóval</span><span class="sxs-lookup"><span data-stu-id="dd047-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd047-108">Egyetlen erőforrás beszerzése a bérlői szinten</span><span class="sxs-lookup"><span data-stu-id="dd047-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd047-109">Felsorolja az erőforrásokat a bérlői szinten megadott hatókör alapján.</span><span class="sxs-lookup"><span data-stu-id="dd047-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd047-110">Erőforrás beolvasása név és csoport szerint</span><span class="sxs-lookup"><span data-stu-id="dd047-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd047-111">Erőforrás beszerzése név és típus szerint</span><span class="sxs-lookup"><span data-stu-id="dd047-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd047-112">Az erőforrás beolvasása név, csoport és típus szerint</span><span class="sxs-lookup"><span data-stu-id="dd047-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd047-113">Erőforrás-gyűjtemény beszerzése</span><span class="sxs-lookup"><span data-stu-id="dd047-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd047-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd047-114">DESCRIPTION</span></span>
<span data-ttu-id="dd047-115">A **Get-AzureRmResource** parancsmag Azure-erőforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="dd047-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="dd047-116">Példák</span><span class="sxs-lookup"><span data-stu-id="dd047-116">EXAMPLES</span></span>

### <span data-ttu-id="dd047-117">Példa 1: erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="dd047-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="dd047-118">Ez a parancs a Microsoft. Web/Sites nevű erőforrást kapja meg, a ContosoWebsite nevű ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dd047-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="dd047-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd047-119">PARAMETERS</span></span>

### <span data-ttu-id="dd047-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dd047-120">-ApiVersion</span></span>
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

### <span data-ttu-id="dd047-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="dd047-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="dd047-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="dd047-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="dd047-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="dd047-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="dd047-125">-ODataQuery</span></span>
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

### <span data-ttu-id="dd047-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="dd047-126">-Pre</span></span>
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

### <span data-ttu-id="dd047-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd047-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd047-128">-ResourceId</span></span>
<span data-ttu-id="dd047-129">A teljesen minősített erőforrás-azonosítót adja meg, az előfizetéssel együtt, az alábbi példában látható módon:</span><span class="sxs-lookup"><span data-stu-id="dd047-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="dd047-130">`/subscriptions/`előfizetés azonosítója`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="dd047-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="dd047-131">Ez a parancsmag az azonosítót tartalmazó erőforrást kapja.</span><span class="sxs-lookup"><span data-stu-id="dd047-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dd047-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dd047-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="dd047-134">-TenantLevel</span></span>
<span data-ttu-id="dd047-135">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="dd047-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-136">-Top</span><span class="sxs-lookup"><span data-stu-id="dd047-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd047-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd047-137">-DefaultProfile</span></span>
<span data-ttu-id="dd047-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd047-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd047-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd047-139">CommonParameters</span></span>
<span data-ttu-id="dd047-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd047-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd047-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd047-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd047-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd047-142">INPUTS</span></span>

## <span data-ttu-id="dd047-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd047-143">OUTPUTS</span></span>

### <span data-ttu-id="dd047-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="dd047-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dd047-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd047-145">NOTES</span></span>

## <span data-ttu-id="dd047-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd047-146">RELATED LINKS</span></span>

[<span data-ttu-id="dd047-147">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd047-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="dd047-148">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd047-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="dd047-149">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd047-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="dd047-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd047-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="dd047-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dd047-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


