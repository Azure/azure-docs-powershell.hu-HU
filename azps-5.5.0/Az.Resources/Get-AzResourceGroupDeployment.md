---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153690"
---
# <span data-ttu-id="d8392-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8392-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="d8392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8392-102">SYNOPSIS</span></span>
<span data-ttu-id="d8392-103">Beveszi a telepítéseket egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d8392-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="d8392-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8392-104">SYNTAX</span></span>

### <span data-ttu-id="d8392-105">GetByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8392-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8392-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d8392-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8392-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8392-107">DESCRIPTION</span></span>
<span data-ttu-id="d8392-108">A **Get-AzResourceGroupDeployment** parancsmag egy Azure-erőforráscsoportban kapja meg a telepítéseket.</span><span class="sxs-lookup"><span data-stu-id="d8392-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="d8392-109">Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="d8392-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d8392-110">Alapértelmezés szerint a **Get-AzResourceGroupDeployment** egy adott erőforráscsoport összes telepítését megkapja.</span><span class="sxs-lookup"><span data-stu-id="d8392-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="d8392-111">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="d8392-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="d8392-112">Az Azure-erőforráscsoportok egy egységként üzembe helyezett Azure-erőforrások gyűjteményei.</span><span class="sxs-lookup"><span data-stu-id="d8392-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="d8392-113">A telepítés az a művelet, amely az erőforráscsoport erőforrásait használatra elérhetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="d8392-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="d8392-114">Az Azure-erőforrásokról és az Azure-erőforráscsoportokról a New-AzResourceGroup talál.</span><span class="sxs-lookup"><span data-stu-id="d8392-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="d8392-115">Ezt a parancsmagot nyomon követésre használhatja.</span><span class="sxs-lookup"><span data-stu-id="d8392-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="d8392-116">Hibakereséshez használja ezt a parancsmagot a Get-AzLog parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="d8392-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="d8392-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8392-117">EXAMPLES</span></span>

### <span data-ttu-id="d8392-118">1. példa: Erőforráscsoport összes telepítésének letelepítése</span><span class="sxs-lookup"><span data-stu-id="d8392-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="d8392-119">Ez a parancs a ContosoLabsRG erőforráscsoport összes telepítését begyabasza.</span><span class="sxs-lookup"><span data-stu-id="d8392-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="d8392-120">A kimenet egy wordPress-blog üzembe helyezését mutatja, amely egy gyűjteménysablont használt.</span><span class="sxs-lookup"><span data-stu-id="d8392-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="d8392-121">2. példa: Telepítés lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="d8392-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="d8392-122">Ez a parancs a ContosoLabsRG erőforráscsoport DeployWebsite01 telepítését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d8392-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="d8392-123">A **New-AzResourceGroup** vagy a **New-AzResourceGroupDeployment** parancsmagok használatával nevet rendelhet a telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="d8392-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="d8392-124">Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.</span><span class="sxs-lookup"><span data-stu-id="d8392-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="d8392-125">3. példa: Az összes erőforráscsoport telepítésének lekérte</span><span class="sxs-lookup"><span data-stu-id="d8392-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="d8392-126">Ez a parancs az előfizetés összes erőforráscsoportját begyakorlja a Get-AzResourceGroup parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d8392-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="d8392-127">A parancs a folyamat műveleti operátorával átadja az erőforráscsoportokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="d8392-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8392-128">Az aktuális parancsmag begyűszi az előfizetés összes erőforráscsoportját, és átadja az eredményeket a Format-Table-parancsmagnak, hogy megjelenítse a **ResourceGroupName,** **a DeploymentName** és a **ProvisioningState** tulajdonságértékeket.</span><span class="sxs-lookup"><span data-stu-id="d8392-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="d8392-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8392-129">PARAMETERS</span></span>

### <span data-ttu-id="d8392-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8392-130">-DefaultProfile</span></span>
<span data-ttu-id="d8392-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8392-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8392-132">-Id</span><span class="sxs-lookup"><span data-stu-id="d8392-132">-Id</span></span>
<span data-ttu-id="d8392-133">A lekért erőforráscsoport-telepítés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8392-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="d8392-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d8392-134">-Name</span></span>
<span data-ttu-id="d8392-135">A lekért központi telepítés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8392-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="d8392-136">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="d8392-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="d8392-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="d8392-137">-Pre</span></span>
<span data-ttu-id="d8392-138">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="d8392-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d8392-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8392-139">-ResourceGroupName</span></span>
<span data-ttu-id="d8392-140">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8392-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d8392-141">A parancsmag beállítja a paraméter által megadott erőforráscsoport üzembe helyezését.</span><span class="sxs-lookup"><span data-stu-id="d8392-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="d8392-142">A helyettesítő karakterek használata nem engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="d8392-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="d8392-143">Ez a paraméter kötelező, és minden parancsban csak egy erőforráscsoport adható meg.</span><span class="sxs-lookup"><span data-stu-id="d8392-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="d8392-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8392-144">CommonParameters</span></span>
<span data-ttu-id="d8392-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8392-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8392-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8392-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8392-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8392-147">INPUTS</span></span>

### <span data-ttu-id="d8392-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d8392-148">System.String</span></span>

## <span data-ttu-id="d8392-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8392-149">OUTPUTS</span></span>

### <span data-ttu-id="d8392-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8392-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="d8392-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8392-151">NOTES</span></span>

## <span data-ttu-id="d8392-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8392-152">RELATED LINKS</span></span>

[<span data-ttu-id="d8392-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8392-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="d8392-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8392-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="d8392-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8392-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="d8392-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8392-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="d8392-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8392-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="d8392-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8392-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


