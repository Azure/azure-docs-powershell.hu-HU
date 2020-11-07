---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 81a4780fb4b4b2249c135104ab3d939d71a93684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669426"
---
# <span data-ttu-id="50844-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50844-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="50844-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50844-102">SYNOPSIS</span></span>
<span data-ttu-id="50844-103">Erőforrás-csoportok beolvasása</span><span class="sxs-lookup"><span data-stu-id="50844-103">Gets resource groups.</span></span>

## <span data-ttu-id="50844-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50844-104">SYNTAX</span></span>

### <span data-ttu-id="50844-105">GetByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50844-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50844-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="50844-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50844-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="50844-107">DESCRIPTION</span></span>
<span data-ttu-id="50844-108">A **Get-AzResourceGroup** parancsmag Azure-erőforráscsoportokat kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="50844-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="50844-109">Az összes erőforráscsoport beolvasható, vagy megadhat egy erőforráscsoportot név vagy egyéb tulajdonság alapján.</span><span class="sxs-lookup"><span data-stu-id="50844-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="50844-110">Alapértelmezés szerint ez a parancsmag a jelenlegi előfizetésben az összes erőforráscsoport számára elérhető lesz.</span><span class="sxs-lookup"><span data-stu-id="50844-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="50844-111">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="50844-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="50844-112">Példák</span><span class="sxs-lookup"><span data-stu-id="50844-112">EXAMPLES</span></span>

### <span data-ttu-id="50844-113">Példa 1: erőforráscsoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="50844-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="50844-114">Ez a parancs a EngineerBlog nevű előfizetésben az Azure Resource Group nevet kapja.</span><span class="sxs-lookup"><span data-stu-id="50844-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="50844-115">2. példa: erőforráscsoport összes címkéjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="50844-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="50844-116">Ez a parancs beolvassa a ContosoRG nevű erőforráscsoportot, és megjeleníti a csoporthoz társított címkéket.</span><span class="sxs-lookup"><span data-stu-id="50844-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="50844-117">3. példa: erőforráscsoportok megjelenítése hely szerint</span><span class="sxs-lookup"><span data-stu-id="50844-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="50844-118">Példa 4: egy adott helyen található összes erőforráscsoport nevének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="50844-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="50844-119">Példa 5: azoknak az erőforrás-csoportoknak a megjelenítése, amelyek nevei a webkiszolgálóval kezdődnek</span><span class="sxs-lookup"><span data-stu-id="50844-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="50844-120">Példa 6: erőforráscsoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="50844-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="50844-121">Ez a parancs a "EngineerBlog" kezdetű Azure Resource Group-előfizetést kapja meg.</span><span class="sxs-lookup"><span data-stu-id="50844-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="50844-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50844-122">PARAMETERS</span></span>

### <span data-ttu-id="50844-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50844-123">-ApiVersion</span></span>
<span data-ttu-id="50844-124">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="50844-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="50844-125">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="50844-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="50844-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50844-126">-DefaultProfile</span></span>
<span data-ttu-id="50844-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="50844-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50844-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="50844-128">-Id</span></span>
<span data-ttu-id="50844-129">A beolvasott erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="50844-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="50844-130">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="50844-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="50844-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="50844-131">-Location</span></span>
<span data-ttu-id="50844-132">A beolvasott erőforráscsoport helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50844-132">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="50844-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50844-133">-Name</span></span>
<span data-ttu-id="50844-134">A beolvasott erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50844-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="50844-135">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="50844-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="50844-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="50844-136">-Pre</span></span>
<span data-ttu-id="50844-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="50844-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="50844-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="50844-138">-Tag</span></span>
<span data-ttu-id="50844-139">A címke Hashtable az erőforráscsoportok szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="50844-139">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="50844-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50844-140">CommonParameters</span></span>
<span data-ttu-id="50844-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50844-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50844-142">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="50844-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50844-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50844-143">INPUTS</span></span>

### <span data-ttu-id="50844-144">System. String</span><span class="sxs-lookup"><span data-stu-id="50844-144">System.String</span></span>

### <span data-ttu-id="50844-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50844-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="50844-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50844-146">OUTPUTS</span></span>

### <span data-ttu-id="50844-147">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50844-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="50844-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50844-148">NOTES</span></span>

## <span data-ttu-id="50844-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50844-149">RELATED LINKS</span></span>

[<span data-ttu-id="50844-150">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50844-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="50844-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50844-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="50844-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50844-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


