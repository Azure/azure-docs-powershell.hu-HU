---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: b8e74a0c349ea058d05ef044648e836fddc1f7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181946"
---
# <span data-ttu-id="5b08e-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b08e-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="5b08e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b08e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b08e-103">Erőforrás-csoportok beolvasása</span><span class="sxs-lookup"><span data-stu-id="5b08e-103">Gets resource groups.</span></span>

## <span data-ttu-id="5b08e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b08e-104">SYNTAX</span></span>

### <span data-ttu-id="5b08e-105">GetByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b08e-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b08e-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5b08e-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b08e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b08e-107">DESCRIPTION</span></span>
<span data-ttu-id="5b08e-108">A **Get-AzResourceGroup** parancsmag Azure-erőforráscsoportokat kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5b08e-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="5b08e-109">Az összes erőforráscsoport beolvasható, vagy megadhat egy erőforráscsoportot név vagy egyéb tulajdonság alapján.</span><span class="sxs-lookup"><span data-stu-id="5b08e-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="5b08e-110">Alapértelmezés szerint ez a parancsmag a jelenlegi előfizetésben az összes erőforráscsoport számára elérhető lesz.</span><span class="sxs-lookup"><span data-stu-id="5b08e-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="5b08e-111">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="5b08e-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="5b08e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="5b08e-112">EXAMPLES</span></span>

### <span data-ttu-id="5b08e-113">Példa 1: erőforráscsoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="5b08e-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="5b08e-114">Ez a parancs a EngineerBlog nevű előfizetésben az Azure Resource Group nevet kapja.</span><span class="sxs-lookup"><span data-stu-id="5b08e-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="5b08e-115">2. példa: erőforráscsoport összes címkéjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="5b08e-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="5b08e-116">Ez a parancs beolvassa a ContosoRG nevű erőforráscsoportot, és megjeleníti a csoporthoz társított címkéket.</span><span class="sxs-lookup"><span data-stu-id="5b08e-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="5b08e-117">3. példa: erőforráscsoportok beolvasása címke alapján</span><span class="sxs-lookup"><span data-stu-id="5b08e-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="5b08e-118">Példa 4: erőforráscsoportok megjelenítése hely szerint</span><span class="sxs-lookup"><span data-stu-id="5b08e-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="5b08e-119">Példa 5: az összes erőforráscsoport nevének megjelenítése adott helyen</span><span class="sxs-lookup"><span data-stu-id="5b08e-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="5b08e-120">Példa 6: azon erőforráscsoportok megjelenítése, amelyek nevei a webkiszolgálóval kezdődnek</span><span class="sxs-lookup"><span data-stu-id="5b08e-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="5b08e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b08e-121">PARAMETERS</span></span>

### <span data-ttu-id="5b08e-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5b08e-122">-ApiVersion</span></span>
<span data-ttu-id="5b08e-123">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b08e-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5b08e-124">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="5b08e-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5b08e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b08e-125">-DefaultProfile</span></span>
<span data-ttu-id="5b08e-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5b08e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b08e-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="5b08e-127">-Id</span></span>
<span data-ttu-id="5b08e-128">A beolvasott erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b08e-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="5b08e-129">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="5b08e-129">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="5b08e-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="5b08e-130">-Location</span></span>
<span data-ttu-id="5b08e-131">A beolvasott erőforráscsoport helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b08e-131">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="5b08e-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b08e-132">-Name</span></span>
<span data-ttu-id="5b08e-133">A beolvasott erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b08e-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="5b08e-134">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="5b08e-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="5b08e-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="5b08e-135">-Pre</span></span>
<span data-ttu-id="5b08e-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="5b08e-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5b08e-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="5b08e-137">-Tag</span></span>
<span data-ttu-id="5b08e-138">A címke Hashtable az erőforráscsoportok szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="5b08e-138">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="5b08e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b08e-139">CommonParameters</span></span>
<span data-ttu-id="5b08e-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b08e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b08e-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5b08e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b08e-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b08e-142">INPUTS</span></span>

### <span data-ttu-id="5b08e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5b08e-143">System.String</span></span>

### <span data-ttu-id="5b08e-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5b08e-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5b08e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b08e-145">OUTPUTS</span></span>

### <span data-ttu-id="5b08e-146">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b08e-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="5b08e-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b08e-147">NOTES</span></span>

## <span data-ttu-id="5b08e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b08e-148">RELATED LINKS</span></span>

[<span data-ttu-id="5b08e-149">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b08e-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="5b08e-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b08e-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="5b08e-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b08e-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


