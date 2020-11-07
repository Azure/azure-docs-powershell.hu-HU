---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: f61fda6c67f0abdee1c136ec6a5fee8b31952d81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838914"
---
# <span data-ttu-id="e0f5c-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0f5c-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="e0f5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f5c-103">Azure-erőforráscsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="e0f5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0f5c-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0f5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="e0f5c-106">A **New-AzResourceGroup** parancsmag létrehoz egy Azure erőforrás-csoportot.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="e0f5c-107">Erőforráscsoport létrehozásához csak egy nevet és egy helyet kell használnia, majd az New-AzResource parancsmaggal hozhat létre erőforrásokat az erőforráscsoport hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="e0f5c-108">Ha egy meglévő erőforrás-csoporthoz szeretne bevezetést hozzáadni, használja az New-AzResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="e0f5c-109">Ha egy erőforrást meglévő erőforráscsoporthoz szeretne hozzáadni, használja a **New-AzResource** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="e0f5c-110">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="e0f5c-111">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="e0f5c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e0f5c-112">EXAMPLES</span></span>

### <span data-ttu-id="e0f5c-113">Példa 1: üres erőforráscsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="e0f5c-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="e0f5c-114">Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="e0f5c-115">A **New-AzResource** és a **New-AzResourceGroupDeployment** parancsmagok segítségével erőforrásokat és üzembe helyezheti az erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="e0f5c-116">2. példa: üres erőforráscsoport létrehozása a pozicionális paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="e0f5c-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="e0f5c-117">Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="e0f5c-118">3. példa: erőforráscsoport létrehozása címkékkel</span><span class="sxs-lookup"><span data-stu-id="e0f5c-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="e0f5c-119">A parancs üres erőforráscsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-119">This command creates an empty resource group.</span></span> <span data-ttu-id="e0f5c-120">Ez a parancs ugyanaz, mint az 1-es parancs, kivéve, hogy címkéket rendel az erőforrás csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="e0f5c-121">Az első címkét, az üres nevet használja, az erőforrás-csoportok meghatározására használható.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="e0f5c-122">A második címke a "részleg" nevű osztály, és a marketing értéke.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="e0f5c-123">A felügyelethez vagy a költségvetéshez használhat olyan címkét is, mint például az ez az erőforrás-csoportok kategorizálásához.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="e0f5c-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0f5c-124">PARAMETERS</span></span>

### <span data-ttu-id="e0f5c-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e0f5c-125">-ApiVersion</span></span>
<span data-ttu-id="e0f5c-126">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e0f5c-127">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e0f5c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f5c-128">-DefaultProfile</span></span>
<span data-ttu-id="e0f5c-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0f5c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0f5c-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e0f5c-130">-Force</span></span>
<span data-ttu-id="e0f5c-131">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0f5c-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="e0f5c-132">-Location</span></span>
<span data-ttu-id="e0f5c-133">Az erőforráscsoport helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="e0f5c-134">Adjon meg egy Azure Data Center helyet, például Nyugat-amerikai vagy Délkelet-ázsiai.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="e0f5c-135">Az erőforráscsoportok tetszőleges helyre helyezhetők.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-135">You can place a resource group in any location.</span></span> <span data-ttu-id="e0f5c-136">Az erőforráscsoport nem kell ugyanazon a helyen lennie az Azure-előfizetésben vagy ugyanazon a helyen, mint az erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="e0f5c-137">Ha meg szeretné állapítani, hogy melyik hely támogatja az egyes erőforrás-típusokat, használja az Get-AzResourceProvider parancsmagot a *ProviderNamespace* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="e0f5c-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0f5c-138">-Name</span></span>
<span data-ttu-id="e0f5c-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="e0f5c-140">Az erőforrás nevének egyedinek kell lennie az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="e0f5c-141">Ha az adott nevű erőforráscsoport már létezik, a parancs a meglévő erőforráscsoport cseréje előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="e0f5c-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="e0f5c-142">-Pre</span></span>
<span data-ttu-id="e0f5c-143">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e0f5c-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="e0f5c-144">-Tag</span></span>
<span data-ttu-id="e0f5c-145">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e0f5c-146">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"} a címke hozzáadásához vagy módosításához az erőforráscsoport címkéjének gyűjteményét kell lecserélnie.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="e0f5c-147">Miután címkéket rendelt az erőforrásokhoz és csoportokhoz, a *címke* paramétert használhatja Get-AzResource és az Get-AzResourceGroup az erőforrások és a csoportok megkereséséhez a címke neve vagy név és érték alapján.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="e0f5c-148">Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="e0f5c-149">Az előre definiált címkék megtekintéséhez használja az Get-AzTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="e0f5c-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0f5c-150">-Confirm</span></span>
<span data-ttu-id="e0f5c-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f5c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f5c-152">-WhatIf</span></span>
<span data-ttu-id="e0f5c-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0f5c-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0f5c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f5c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f5c-155">CommonParameters</span></span>
<span data-ttu-id="e0f5c-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0f5c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f5c-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f5c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f5c-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0f5c-158">INPUTS</span></span>

### <span data-ttu-id="e0f5c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="e0f5c-159">System.String</span></span>

### <span data-ttu-id="e0f5c-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0f5c-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0f5c-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0f5c-161">OUTPUTS</span></span>

### <span data-ttu-id="e0f5c-162">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0f5c-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="e0f5c-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0f5c-163">NOTES</span></span>

## <span data-ttu-id="e0f5c-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0f5c-164">RELATED LINKS</span></span>

[<span data-ttu-id="e0f5c-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e0f5c-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="e0f5c-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0f5c-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="e0f5c-167">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="e0f5c-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="e0f5c-168">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e0f5c-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e0f5c-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0f5c-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="e0f5c-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0f5c-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
