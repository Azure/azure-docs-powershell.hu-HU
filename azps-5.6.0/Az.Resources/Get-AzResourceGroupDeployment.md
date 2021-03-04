---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937409"
---
# <span data-ttu-id="25815-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25815-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="25815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25815-102">SYNOPSIS</span></span>
<span data-ttu-id="25815-103">Beveszi a telepítéseket egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="25815-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="25815-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25815-104">SYNTAX</span></span>

### <span data-ttu-id="25815-105">GetByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25815-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25815-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="25815-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25815-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25815-107">DESCRIPTION</span></span>
<span data-ttu-id="25815-108">A **Get-AzResourceGroupDeployment** parancsmag egy Azure-erőforráscsoportban kapja meg a telepítéseket.</span><span class="sxs-lookup"><span data-stu-id="25815-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="25815-109">Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="25815-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="25815-110">Alapértelmezés szerint a **Get-AzResourceGroupDeployment** egy adott erőforráscsoport összes telepítését megkapja.</span><span class="sxs-lookup"><span data-stu-id="25815-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="25815-111">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="25815-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="25815-112">Az Azure-erőforráscsoportok egy egységként üzembe helyezett Azure-erőforrások gyűjteményei.</span><span class="sxs-lookup"><span data-stu-id="25815-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="25815-113">A telepítés az a művelet, amely az erőforráscsoport erőforrásait használatra elérhetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="25815-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="25815-114">Az Azure-erőforrásokról és az Azure-erőforráscsoportokról a New-AzResourceGroup talál.</span><span class="sxs-lookup"><span data-stu-id="25815-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="25815-115">Ezt a parancsmagot nyomon követésre használhatja.</span><span class="sxs-lookup"><span data-stu-id="25815-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="25815-116">Hibakereséshez használja ezt a parancsmagot a Get-AzLog parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="25815-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="25815-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25815-117">EXAMPLES</span></span>

### <span data-ttu-id="25815-118">1. példa: Erőforráscsoport összes telepítésének letelepítése</span><span class="sxs-lookup"><span data-stu-id="25815-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="25815-119">Ez a parancs a ContosoLabsRG erőforráscsoport összes központi telepítését beveszi.</span><span class="sxs-lookup"><span data-stu-id="25815-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="25815-120">A kimenet egy gyűjteménysablont használt WordPress-blog központi telepítését mutatja.</span><span class="sxs-lookup"><span data-stu-id="25815-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="25815-121">2. példa: Telepítés lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="25815-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="25815-122">Ez a parancs a ContosoLabsRG erőforráscsoport DeployWebsite01 telepítését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="25815-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="25815-123">A **New-AzResourceGroup** vagy a **New-AzResourceGroupDeployment** parancsmagok használatával nevet rendelhet a telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="25815-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="25815-124">Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.</span><span class="sxs-lookup"><span data-stu-id="25815-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="25815-125">3. példa: Az összes erőforráscsoport telepítésének lekérte</span><span class="sxs-lookup"><span data-stu-id="25815-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="25815-126">Ez a parancs az előfizetés összes erőforráscsoportját begyakorlja a Get-AzResourceGroup parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="25815-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="25815-127">A parancs a folyamat műveleti operátorával átadja az erőforráscsoportokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="25815-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="25815-128">Az aktuális parancsmag begyűszi az előfizetés összes erőforráscsoportját, és átadja az eredményeket a Format-Table-parancsmagnak, hogy megjelenítse a **ResourceGroupName,** **a DeploymentName** és a **ProvisioningState** tulajdonságértékeket.</span><span class="sxs-lookup"><span data-stu-id="25815-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="25815-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25815-129">PARAMETERS</span></span>

### <span data-ttu-id="25815-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25815-130">-DefaultProfile</span></span>
<span data-ttu-id="25815-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="25815-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25815-132">-Id</span><span class="sxs-lookup"><span data-stu-id="25815-132">-Id</span></span>
<span data-ttu-id="25815-133">A lekért erőforráscsoport-telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="25815-133">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25815-134">-Name</span><span class="sxs-lookup"><span data-stu-id="25815-134">-Name</span></span>
<span data-ttu-id="25815-135">A lekért központi telepítés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25815-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="25815-136">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="25815-136">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25815-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="25815-137">-Pre</span></span>
<span data-ttu-id="25815-138">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="25815-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="25815-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25815-139">-ResourceGroupName</span></span>
<span data-ttu-id="25815-140">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25815-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="25815-141">A parancsmag beállítja a paraméter által megadott erőforráscsoport üzembe helyezését.</span><span class="sxs-lookup"><span data-stu-id="25815-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="25815-142">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="25815-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="25815-143">Ez a paraméter kötelező, és minden parancsban csak egy erőforráscsoport adható meg.</span><span class="sxs-lookup"><span data-stu-id="25815-143">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25815-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25815-144">CommonParameters</span></span>
<span data-ttu-id="25815-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25815-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25815-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25815-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25815-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25815-147">INPUTS</span></span>

### <span data-ttu-id="25815-148">System.String</span><span class="sxs-lookup"><span data-stu-id="25815-148">System.String</span></span>

## <span data-ttu-id="25815-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25815-149">OUTPUTS</span></span>

### <span data-ttu-id="25815-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25815-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="25815-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25815-151">NOTES</span></span>

## <span data-ttu-id="25815-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25815-152">RELATED LINKS</span></span>

[<span data-ttu-id="25815-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25815-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="25815-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25815-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="25815-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25815-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="25815-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25815-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="25815-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25815-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="25815-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25815-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


