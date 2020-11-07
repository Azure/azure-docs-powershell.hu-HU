---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: 7264733055322c3d5886ff57f50d22e23f932a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672288"
---
# <span data-ttu-id="89f6a-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89f6a-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="89f6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="89f6a-103">Azure-erőforráscsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89f6a-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89f6a-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f6a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="89f6a-106">A **New-AzureRmResourceGroup** parancsmag létrehoz egy Azure erőforrás-csoportot.</span><span class="sxs-lookup"><span data-stu-id="89f6a-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="89f6a-107">Erőforráscsoport létrehozásához csak egy nevet és egy helyet kell használnia, majd az New-AzureRmResource parancsmaggal hozhat létre erőforrásokat az erőforráscsoport hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="89f6a-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="89f6a-108">Ha egy meglévő erőforrás-csoporthoz szeretne bevezetést hozzáadni, használja az New-AzureRmResourceGroupDeployment parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89f6a-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="89f6a-109">Ha egy erőforrást meglévő erőforráscsoporthoz szeretne hozzáadni, használja a **New-AzureRmResource** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89f6a-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="89f6a-110">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="89f6a-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="89f6a-111">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="89f6a-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="89f6a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="89f6a-112">EXAMPLES</span></span>

### <span data-ttu-id="89f6a-113">Példa 1: üres erőforráscsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="89f6a-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="89f6a-114">Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai.</span><span class="sxs-lookup"><span data-stu-id="89f6a-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="89f6a-115">A **New-AzureRmResource** és a **New-AzureRmResourceGroupDeployment** parancsmagok segítségével erőforrásokat és üzembe helyezheti az erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="89f6a-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="89f6a-116">2. példa: üres erőforráscsoport létrehozása a pozicionális paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="89f6a-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="89f6a-117">Ez a parancs olyan erőforráscsoportot hoz létre, amelynek nincs erőforrásai.</span><span class="sxs-lookup"><span data-stu-id="89f6a-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="89f6a-118">3. példa: erőforráscsoport létrehozása címkékkel</span><span class="sxs-lookup"><span data-stu-id="89f6a-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="89f6a-119">A parancs üres erőforráscsoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89f6a-119">This command creates an empty resource group.</span></span> <span data-ttu-id="89f6a-120">Ez a parancs ugyanaz, mint az 1-es parancs, kivéve, hogy címkéket rendel az erőforrás csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="89f6a-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="89f6a-121">Az első címkét, az üres nevet használja, az erőforrás-csoportok meghatározására használható.</span><span class="sxs-lookup"><span data-stu-id="89f6a-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="89f6a-122">A második címke a "részleg" nevű osztály, és a marketing értéke.</span><span class="sxs-lookup"><span data-stu-id="89f6a-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="89f6a-123">A felügyelethez vagy a költségvetéshez használhat olyan címkét is, mint például az ez az erőforrás-csoportok kategorizálásához.</span><span class="sxs-lookup"><span data-stu-id="89f6a-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="89f6a-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89f6a-124">PARAMETERS</span></span>

### <span data-ttu-id="89f6a-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="89f6a-125">-ApiVersion</span></span>
<span data-ttu-id="89f6a-126">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="89f6a-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="89f6a-127">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="89f6a-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="89f6a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f6a-128">-DefaultProfile</span></span>
<span data-ttu-id="89f6a-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="89f6a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89f6a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="89f6a-130">-Force</span></span>
<span data-ttu-id="89f6a-131">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="89f6a-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89f6a-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="89f6a-132">-Location</span></span>
<span data-ttu-id="89f6a-133">Az erőforráscsoport helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89f6a-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="89f6a-134">Adjon meg egy Azure Data Center helyet, például Nyugat-amerikai vagy Délkelet-ázsiai.</span><span class="sxs-lookup"><span data-stu-id="89f6a-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="89f6a-135">Az erőforráscsoportok tetszőleges helyre helyezhetők.</span><span class="sxs-lookup"><span data-stu-id="89f6a-135">You can place a resource group in any location.</span></span> <span data-ttu-id="89f6a-136">Az erőforráscsoport nem kell ugyanazon a helyen lennie az Azure-előfizetésben vagy ugyanazon a helyen, mint az erőforrás.</span><span class="sxs-lookup"><span data-stu-id="89f6a-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="89f6a-137">Ha meg szeretné állapítani, hogy melyik hely támogatja az egyes erőforrás-típusokat, használja az Get-AzureRmResourceProvider parancsmagot a *ProviderNamespace* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="89f6a-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f6a-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89f6a-138">-Name</span></span>
<span data-ttu-id="89f6a-139">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="89f6a-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="89f6a-140">Az erőforrás nevének egyedinek kell lennie az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="89f6a-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="89f6a-141">Ha az adott nevű erőforráscsoport már létezik, a parancs a meglévő erőforráscsoport cseréje előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89f6a-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f6a-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="89f6a-142">-Pre</span></span>
<span data-ttu-id="89f6a-143">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="89f6a-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="89f6a-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="89f6a-144">-Tag</span></span>
<span data-ttu-id="89f6a-145">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="89f6a-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="89f6a-146">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"} a címke hozzáadásához vagy módosításához az erőforráscsoport címkéjének gyűjteményét kell lecserélnie.</span><span class="sxs-lookup"><span data-stu-id="89f6a-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="89f6a-147">Miután címkéket rendelt az erőforrásokhoz és csoportokhoz, a *címke* paramétert használhatja Get-AzureRmResource és az Get-AzureRmResourceGroup az erőforrások és a csoportok megkereséséhez a címke neve vagy név és érték alapján.</span><span class="sxs-lookup"><span data-stu-id="89f6a-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="89f6a-148">Címkéket használhat az erőforrások (például részleg vagy költséghely) kategorizálásához, illetve az erőforrásokkal kapcsolatos megjegyzések és megjegyzések nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="89f6a-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="89f6a-149">Az előre definiált címkék megtekintéséhez használja az Get-AzureRMTag parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89f6a-149">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="89f6a-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89f6a-150">-Confirm</span></span>
<span data-ttu-id="89f6a-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89f6a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f6a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f6a-152">-WhatIf</span></span>
<span data-ttu-id="89f6a-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89f6a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f6a-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89f6a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f6a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f6a-155">CommonParameters</span></span>
<span data-ttu-id="89f6a-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89f6a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f6a-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f6a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f6a-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89f6a-158">INPUTS</span></span>

### <span data-ttu-id="89f6a-159">Nincs</span><span class="sxs-lookup"><span data-stu-id="89f6a-159">None</span></span>

## <span data-ttu-id="89f6a-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89f6a-160">OUTPUTS</span></span>

### <span data-ttu-id="89f6a-161">Microsoft. Azure. Command. ResourceManagement. models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89f6a-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="89f6a-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89f6a-162">NOTES</span></span>

## <span data-ttu-id="89f6a-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89f6a-163">RELATED LINKS</span></span>

[<span data-ttu-id="89f6a-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="89f6a-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="89f6a-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89f6a-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="89f6a-166">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="89f6a-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="89f6a-167">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="89f6a-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="89f6a-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89f6a-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="89f6a-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89f6a-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
