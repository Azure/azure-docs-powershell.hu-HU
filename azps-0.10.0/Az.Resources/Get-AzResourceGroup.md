---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: d09031270e61be80228003ae2a9ae47a5ce5ac74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843417"
---
# <span data-ttu-id="52bfc-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52bfc-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="52bfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="52bfc-103">Erőforrás-csoportok beolvasása</span><span class="sxs-lookup"><span data-stu-id="52bfc-103">Gets resource groups.</span></span>

## <span data-ttu-id="52bfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52bfc-104">SYNTAX</span></span>

### <span data-ttu-id="52bfc-105">GetByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52bfc-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52bfc-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="52bfc-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52bfc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="52bfc-107">DESCRIPTION</span></span>
<span data-ttu-id="52bfc-108">A **Get-AzResourceGroup** parancsmag Azure-erőforráscsoportokat kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="52bfc-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="52bfc-109">Az összes erőforráscsoport beolvasható, vagy megadhat egy erőforráscsoportot név vagy egyéb tulajdonság alapján.</span><span class="sxs-lookup"><span data-stu-id="52bfc-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="52bfc-110">Alapértelmezés szerint ez a parancsmag a jelenlegi előfizetésben az összes erőforráscsoport számára elérhető lesz.</span><span class="sxs-lookup"><span data-stu-id="52bfc-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="52bfc-111">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="52bfc-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="52bfc-112">Példák</span><span class="sxs-lookup"><span data-stu-id="52bfc-112">EXAMPLES</span></span>

### <span data-ttu-id="52bfc-113">Példa 1: erőforráscsoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="52bfc-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="52bfc-114">Ez a parancs a EngineerBlog nevű előfizetésben az Azure Resource Group nevet kapja.</span><span class="sxs-lookup"><span data-stu-id="52bfc-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="52bfc-115">2. példa: erőforráscsoport összes címkéjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="52bfc-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="52bfc-116">Ez a parancs beolvassa a ContosoRG nevű erőforráscsoportot, és megjeleníti a csoporthoz társított címkéket.</span><span class="sxs-lookup"><span data-stu-id="52bfc-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="52bfc-117">3. példa: erőforráscsoportok megjelenítése hely szerint</span><span class="sxs-lookup"><span data-stu-id="52bfc-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="52bfc-118">Példa 4: egy adott helyen található összes erőforráscsoport nevének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="52bfc-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="52bfc-119">Példa 5: azoknak az erőforrás-csoportoknak a megjelenítése, amelyek nevei a webkiszolgálóval kezdődnek</span><span class="sxs-lookup"><span data-stu-id="52bfc-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="52bfc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52bfc-120">PARAMETERS</span></span>

### <span data-ttu-id="52bfc-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="52bfc-121">-ApiVersion</span></span>
<span data-ttu-id="52bfc-122">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="52bfc-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="52bfc-123">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="52bfc-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="52bfc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bfc-124">-DefaultProfile</span></span>
<span data-ttu-id="52bfc-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="52bfc-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bfc-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="52bfc-126">-Id</span></span>
<span data-ttu-id="52bfc-127">A beolvasott erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="52bfc-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="52bfc-128">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="52bfc-128">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="52bfc-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="52bfc-129">-Location</span></span>
<span data-ttu-id="52bfc-130">A beolvasott erőforráscsoport helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52bfc-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52bfc-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52bfc-131">-Name</span></span>
<span data-ttu-id="52bfc-132">A beolvasott erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52bfc-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="52bfc-133">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="52bfc-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52bfc-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="52bfc-134">-Pre</span></span>
<span data-ttu-id="52bfc-135">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="52bfc-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="52bfc-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="52bfc-136">-Tag</span></span>
<span data-ttu-id="52bfc-137">A címke Hashtable az erőforráscsoportok szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="52bfc-137">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="52bfc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bfc-138">CommonParameters</span></span>
<span data-ttu-id="52bfc-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52bfc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bfc-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52bfc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bfc-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52bfc-141">INPUTS</span></span>

### <span data-ttu-id="52bfc-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="52bfc-142">None</span></span>

## <span data-ttu-id="52bfc-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52bfc-143">OUTPUTS</span></span>

### <span data-ttu-id="52bfc-144">Microsoft. Azure. Command. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52bfc-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="52bfc-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52bfc-145">NOTES</span></span>

## <span data-ttu-id="52bfc-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52bfc-146">RELATED LINKS</span></span>

[<span data-ttu-id="52bfc-147">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52bfc-147">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="52bfc-148">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52bfc-148">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="52bfc-149">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52bfc-149">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


