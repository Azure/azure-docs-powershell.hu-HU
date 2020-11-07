---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: ede228aef26cf7e4729acf3a6acc0faae3902f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849494"
---
# <span data-ttu-id="8a374-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a374-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="8a374-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a374-102">SYNOPSIS</span></span>
<span data-ttu-id="8a374-103">Erőforrás-csoportok beolvasása</span><span class="sxs-lookup"><span data-stu-id="8a374-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a374-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a374-104">SYNTAX</span></span>

### <span data-ttu-id="8a374-105">GetByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a374-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a374-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8a374-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a374-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a374-107">DESCRIPTION</span></span>
<span data-ttu-id="8a374-108">A **Get-AzureRmResourceGroup** parancsmag Azure-erőforráscsoportokat kap az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="8a374-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="8a374-109">Az összes erőforráscsoport beolvasható, vagy megadhat egy erőforráscsoportot név vagy egyéb tulajdonság alapján.</span><span class="sxs-lookup"><span data-stu-id="8a374-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="8a374-110">Alapértelmezés szerint ez a parancsmag a jelenlegi előfizetésben az összes erőforráscsoport számára elérhető lesz.</span><span class="sxs-lookup"><span data-stu-id="8a374-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="8a374-111">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzureRmResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="8a374-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="8a374-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8a374-112">EXAMPLES</span></span>

### <span data-ttu-id="8a374-113">Példa 1: erőforráscsoport beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="8a374-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="8a374-114">Ez a parancs a EngineerBlog nevű előfizetésben az Azure Resource Group nevet kapja.</span><span class="sxs-lookup"><span data-stu-id="8a374-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="8a374-115">2. példa: erőforráscsoport összes címkéjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="8a374-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="8a374-116">Ez a parancs beolvassa a ContosoRG nevű erőforráscsoportot, és megjeleníti a csoporthoz társított címkéket.</span><span class="sxs-lookup"><span data-stu-id="8a374-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="8a374-117">3. példa: erőforráscsoportok megjelenítése hely szerint</span><span class="sxs-lookup"><span data-stu-id="8a374-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="8a374-118">Példa 4: egy adott helyen található összes erőforráscsoport nevének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="8a374-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="8a374-119">Példa 5: azoknak az erőforrás-csoportoknak a megjelenítése, amelyek nevei a webkiszolgálóval kezdődnek</span><span class="sxs-lookup"><span data-stu-id="8a374-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="8a374-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a374-120">PARAMETERS</span></span>

### <span data-ttu-id="8a374-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a374-121">-ApiVersion</span></span>
<span data-ttu-id="8a374-122">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a374-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8a374-123">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="8a374-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8a374-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a374-124">-DefaultProfile</span></span>
<span data-ttu-id="8a374-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8a374-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a374-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8a374-126">-Id</span></span>
<span data-ttu-id="8a374-127">A beolvasott erőforráscsoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a374-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="8a374-128">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="8a374-128">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="8a374-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="8a374-129">-Location</span></span>
<span data-ttu-id="8a374-130">A beolvasott erőforráscsoport helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a374-130">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="8a374-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a374-131">-Name</span></span>
<span data-ttu-id="8a374-132">A beolvasott erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a374-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="8a374-133">Ez a paraméter a karakterlánc elején és/vagy végén támogatja a helyettesítő karaktereket.</span><span class="sxs-lookup"><span data-stu-id="8a374-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="8a374-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="8a374-134">-Pre</span></span>
<span data-ttu-id="8a374-135">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8a374-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8a374-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="8a374-136">-Tag</span></span>
<span data-ttu-id="8a374-137">A címke Hashtable az erőforráscsoportok szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="8a374-137">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="8a374-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a374-138">CommonParameters</span></span>
<span data-ttu-id="8a374-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a374-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a374-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a374-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a374-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a374-141">INPUTS</span></span>

### <span data-ttu-id="8a374-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a374-142">None</span></span>

## <span data-ttu-id="8a374-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a374-143">OUTPUTS</span></span>

### <span data-ttu-id="8a374-144">Microsoft. Azure. Command. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a374-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="8a374-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a374-145">NOTES</span></span>

## <span data-ttu-id="8a374-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a374-146">RELATED LINKS</span></span>

[<span data-ttu-id="8a374-147">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a374-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="8a374-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a374-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="8a374-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a374-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


