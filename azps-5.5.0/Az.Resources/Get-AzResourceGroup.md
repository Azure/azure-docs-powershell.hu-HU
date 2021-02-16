---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153699"
---
# <span data-ttu-id="843ff-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="843ff-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="843ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="843ff-102">SYNOPSIS</span></span>
<span data-ttu-id="843ff-103">Erőforráscsoportokat kap.</span><span class="sxs-lookup"><span data-stu-id="843ff-103">Gets resource groups.</span></span>

## <span data-ttu-id="843ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="843ff-104">SYNTAX</span></span>

### <span data-ttu-id="843ff-105">GetByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="843ff-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="843ff-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="843ff-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="843ff-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="843ff-107">DESCRIPTION</span></span>
<span data-ttu-id="843ff-108">A **Get-AzResourceGroup** parancsmag azure-erőforráscsoportokat kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="843ff-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="843ff-109">Lekértheti az összes erőforráscsoportot, vagy megadhat egy erőforráscsoportot név vagy más tulajdonság alapján.</span><span class="sxs-lookup"><span data-stu-id="843ff-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="843ff-110">Ez a parancsmag alapértelmezés szerint az aktuális előfizetés összes erőforráscsoportját beveszi.</span><span class="sxs-lookup"><span data-stu-id="843ff-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="843ff-111">Az Azure-erőforrásokról és az Azure-erőforráscsoportokról a New-AzResourceGroup talál.</span><span class="sxs-lookup"><span data-stu-id="843ff-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="843ff-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="843ff-112">EXAMPLES</span></span>

### <span data-ttu-id="843ff-113">1. példa: Erőforráscsoport lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="843ff-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="843ff-114">Ez a parancs lekérte az Azure-erőforráscsoportot az előfizetésében a EngineerBlog névre.</span><span class="sxs-lookup"><span data-stu-id="843ff-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="843ff-115">2. példa: Erőforráscsoport összes címkéének be szerezze</span><span class="sxs-lookup"><span data-stu-id="843ff-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="843ff-116">Ez a parancs bemutatja a ContosoRG nevű erőforráscsoportot, és megjeleníti a csoporthoz társított címkéket.</span><span class="sxs-lookup"><span data-stu-id="843ff-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="843ff-117">3. példa: Erőforráscsoportok lekérte címkéje alapján</span><span class="sxs-lookup"><span data-stu-id="843ff-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="843ff-118">4. példa: Az erőforráscsoportok megjelenítése hely szerint</span><span class="sxs-lookup"><span data-stu-id="843ff-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="843ff-119">5. példa: Az erőforráscsoportok nevének megjelenítése egy adott helyen</span><span class="sxs-lookup"><span data-stu-id="843ff-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="843ff-120">6. példa: Azoknak az erőforráscsoportoknak a megjelenítése, amelyeknek a neve WebServer névvel kezdődik</span><span class="sxs-lookup"><span data-stu-id="843ff-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="843ff-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="843ff-121">PARAMETERS</span></span>

### <span data-ttu-id="843ff-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="843ff-122">-ApiVersion</span></span>
<span data-ttu-id="843ff-123">Az erőforrásszolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="843ff-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="843ff-124">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="843ff-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="843ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="843ff-125">-DefaultProfile</span></span>
<span data-ttu-id="843ff-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="843ff-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="843ff-127">-Id</span><span class="sxs-lookup"><span data-stu-id="843ff-127">-Id</span></span>
<span data-ttu-id="843ff-128">A lekért erőforráscsoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="843ff-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="843ff-129">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="843ff-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="843ff-130">-Location</span><span class="sxs-lookup"><span data-stu-id="843ff-130">-Location</span></span>
<span data-ttu-id="843ff-131">A lekért erőforráscsoport helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="843ff-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="843ff-132">-Name</span><span class="sxs-lookup"><span data-stu-id="843ff-132">-Name</span></span>
<span data-ttu-id="843ff-133">A lekért erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="843ff-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="843ff-134">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="843ff-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="843ff-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="843ff-135">-Pre</span></span>
<span data-ttu-id="843ff-136">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="843ff-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="843ff-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="843ff-137">-Tag</span></span>
<span data-ttu-id="843ff-138">Az erőforráscsoportok szűréséhez szükséges címke-kivonat.</span><span class="sxs-lookup"><span data-stu-id="843ff-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="843ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843ff-139">CommonParameters</span></span>
<span data-ttu-id="843ff-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="843ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843ff-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="843ff-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843ff-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="843ff-142">INPUTS</span></span>

### <span data-ttu-id="843ff-143">System.String</span><span class="sxs-lookup"><span data-stu-id="843ff-143">System.String</span></span>

### <span data-ttu-id="843ff-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="843ff-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="843ff-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="843ff-145">OUTPUTS</span></span>

### <span data-ttu-id="843ff-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="843ff-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="843ff-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="843ff-147">NOTES</span></span>

## <span data-ttu-id="843ff-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="843ff-148">RELATED LINKS</span></span>

[<span data-ttu-id="843ff-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="843ff-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="843ff-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="843ff-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="843ff-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="843ff-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

