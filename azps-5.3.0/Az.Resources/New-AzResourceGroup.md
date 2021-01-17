---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466449"
---
# <span data-ttu-id="5411e-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5411e-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="5411e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5411e-102">SYNOPSIS</span></span>
<span data-ttu-id="5411e-103">Létrehoz egy Azure-erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="5411e-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="5411e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5411e-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5411e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5411e-105">DESCRIPTION</span></span>
<span data-ttu-id="5411e-106">A **New-AzResourceGroup** parancsmag létrehoz egy Azure-erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="5411e-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="5411e-107">Létrehozhat egy erőforráscsoportot úgy, hogy csak egy nevet és egy helyet használ, majd a New-AzResource parancsmagot használva erőforrásokat hozhat létre az erőforráscsoporthoz való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="5411e-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="5411e-108">Ha egy meglévő erőforráscsoporthoz szeretne központi telepítést hozzáadni, használja a New-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5411e-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="5411e-109">Ha erőforrást szeretne hozzáadni egy meglévő erőforráscsoporthoz, használja a **New-AzResource** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5411e-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="5411e-110">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="5411e-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="5411e-111">Az Azure-erőforráscsoportok egy egységként üzembe helyezett Azure-erőforrások gyűjteményei.</span><span class="sxs-lookup"><span data-stu-id="5411e-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="5411e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5411e-112">EXAMPLES</span></span>

### <span data-ttu-id="5411e-113">1. példa: Üres erőforráscsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="5411e-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="5411e-114">Ez a parancs olyan erőforráscsoportot hoz létre, amely nem rendelkezik erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="5411e-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="5411e-115">A **New-AzResource** vagy **a New-AzResourceGroupDeployment** parancsmagokkal erőforrásokat és telepítéseket adhat ehhez az erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5411e-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="5411e-116">2. példa: Üres erőforráscsoport létrehozása pozícióparaméterek használatával</span><span class="sxs-lookup"><span data-stu-id="5411e-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="5411e-117">Ez a parancs olyan erőforráscsoportot hoz létre, amely nem rendelkezik erőforrásokkal.</span><span class="sxs-lookup"><span data-stu-id="5411e-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="5411e-118">3. példa: Erőforráscsoport létrehozása címkékkel</span><span class="sxs-lookup"><span data-stu-id="5411e-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="5411e-119">Ez a parancs egy üres erőforráscsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5411e-119">This command creates an empty resource group.</span></span> <span data-ttu-id="5411e-120">Ez a parancs ugyanaz, mint az 1. példa parancsa, azzal a kivételvel, hogy címkéket rendel az erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5411e-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="5411e-121">Az első üres címke segítségével azonosíthatók az erőforrásokkal nem kapcsolatos erőforráscsoportok.</span><span class="sxs-lookup"><span data-stu-id="5411e-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="5411e-122">A második címke neve Részleg, értéke Marketing.</span><span class="sxs-lookup"><span data-stu-id="5411e-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="5411e-123">Az ehhez hasonló címkék segítségével kategorizálhatja az erőforráscsoportokat felügyelet vagy költségvetés-elosztás érdekében.</span><span class="sxs-lookup"><span data-stu-id="5411e-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="5411e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5411e-124">PARAMETERS</span></span>

### <span data-ttu-id="5411e-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5411e-125">-ApiVersion</span></span>
<span data-ttu-id="5411e-126">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5411e-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5411e-127">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="5411e-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5411e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5411e-128">-DefaultProfile</span></span>
<span data-ttu-id="5411e-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5411e-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5411e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5411e-130">-Force</span></span>
<span data-ttu-id="5411e-131">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5411e-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5411e-132">-Location</span><span class="sxs-lookup"><span data-stu-id="5411e-132">-Location</span></span>
<span data-ttu-id="5411e-133">Az erőforráscsoport helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5411e-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="5411e-134">Adja meg az Azure-adatközpont helyét, például Nyugat-Egyesült Államok vagy Délkelet-Ázsia.</span><span class="sxs-lookup"><span data-stu-id="5411e-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="5411e-135">Az erőforráscsoportokat bármilyen helyen el lehet helyezése.</span><span class="sxs-lookup"><span data-stu-id="5411e-135">You can place a resource group in any location.</span></span> <span data-ttu-id="5411e-136">Az erőforráscsoportnak nem kell az Azure-előfizetésével azonos helyen lennie, és nem is kell ugyanazon a helyen lennie, mint az erőforrásainak.</span><span class="sxs-lookup"><span data-stu-id="5411e-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="5411e-137">Ha meg szeretné állapítani, hogy melyik hely támogatja az egyes erőforrástípusokat, használja a Get-AzResourceProvider parancsmagot *a ProviderNamespace* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="5411e-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5411e-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5411e-138">-Name</span></span>
<span data-ttu-id="5411e-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5411e-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="5411e-140">Az erőforrás nevének egyedinek kell lennie az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5411e-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="5411e-141">Ha már létezik ilyen nevű erőforráscsoport, a parancs megerősítést kér, mielőtt lecseréli a meglévő erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="5411e-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5411e-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="5411e-142">-Pre</span></span>
<span data-ttu-id="5411e-143">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="5411e-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5411e-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="5411e-144">-Tag</span></span>
<span data-ttu-id="5411e-145">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="5411e-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5411e-146">Például: @{key0="érték0";key1=$null;key2="érték2"} Címke hozzáadásához vagy cseréjéhez le kell cserélnie az erőforráscsoport címkéinek gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="5411e-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="5411e-147">Miután címkéket hozzárendelt az erőforrásokhoz  és a csoportokhoz, a Get-AzResource és a Get-AzResourceGroup címke paraméterével kereshet erőforrásokat és csoportokat címkenév, illetve név és érték szerint.</span><span class="sxs-lookup"><span data-stu-id="5411e-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="5411e-148">Címkékkel kategorizálhatja az erőforrásokat, például részlegek vagy költségközpontok szerint, illetve nyomon követheti az erőforrásokkal kapcsolatos jegyzeteket vagy megjegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="5411e-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="5411e-149">Az előre definiált címkéket a Get-AzTag használhatja.</span><span class="sxs-lookup"><span data-stu-id="5411e-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="5411e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5411e-150">-Confirm</span></span>
<span data-ttu-id="5411e-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5411e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5411e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5411e-152">-WhatIf</span></span>
<span data-ttu-id="5411e-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5411e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5411e-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5411e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5411e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5411e-155">CommonParameters</span></span>
<span data-ttu-id="5411e-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5411e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5411e-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5411e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5411e-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5411e-158">INPUTS</span></span>

### <span data-ttu-id="5411e-159">System.String</span><span class="sxs-lookup"><span data-stu-id="5411e-159">System.String</span></span>

### <span data-ttu-id="5411e-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5411e-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5411e-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5411e-161">OUTPUTS</span></span>

### <span data-ttu-id="5411e-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5411e-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="5411e-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5411e-163">NOTES</span></span>

## <span data-ttu-id="5411e-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5411e-164">RELATED LINKS</span></span>

[<span data-ttu-id="5411e-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5411e-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="5411e-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5411e-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="5411e-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="5411e-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="5411e-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5411e-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="5411e-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5411e-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="5411e-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5411e-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
