---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: e6f6be148757bb2f30ac0f09575907669ddc195b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838936"
---
# <span data-ttu-id="62e28-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62e28-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="62e28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62e28-102">SYNOPSIS</span></span>
<span data-ttu-id="62e28-103">Beilleszti a telepített erőforrásokat egy erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="62e28-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="62e28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62e28-104">SYNTAX</span></span>

### <span data-ttu-id="62e28-105">GetByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62e28-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62e28-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="62e28-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e28-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="62e28-107">DESCRIPTION</span></span>
<span data-ttu-id="62e28-108">A **Get-AzResourceGroupDeployment** parancsmag a telepített példányokat egy Azure-erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62e28-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="62e28-109">Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="62e28-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="62e28-110">Alapértelmezés szerint a **Get-AzResourceGroupDeployment beolvassa** a megadott erőforráscsoport összes telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="62e28-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="62e28-111">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="62e28-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="62e28-112">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="62e28-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="62e28-113">A telepítés az a művelet, amely az erőforráscsoport számára elérhetővé teszi az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="62e28-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="62e28-114">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="62e28-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="62e28-115">Ezt a parancsmagot a nyomkövetéshez használhatja.</span><span class="sxs-lookup"><span data-stu-id="62e28-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="62e28-116">Hibakereséshez használja ezt a parancsmagot a Get-AzLog parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="62e28-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="62e28-117">Példák</span><span class="sxs-lookup"><span data-stu-id="62e28-117">EXAMPLES</span></span>

### <span data-ttu-id="62e28-118">Példa 1: erőforráscsoport minden telepített példányának beszerzése</span><span class="sxs-lookup"><span data-stu-id="62e28-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="62e28-119">Ez a parancs beilleszti a ContosoLabsRG-erőforráscsoport összes telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="62e28-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="62e28-120">A kimenet a gyűjteményt jeleníti meg egy olyan WordPress bloghoz, amely a gyűjtemény sablonját használta.</span><span class="sxs-lookup"><span data-stu-id="62e28-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="62e28-121">2. példa: a központi felügyelet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="62e28-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="62e28-122">Ez a parancs a ContosoLabsRG-erőforráscsoport DeployWebsite01 telepítését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62e28-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="62e28-123">Az **új AzResourceGroup** vagy a **New-AzResourceGroupDeployment** parancsmagok segítségével létrehozhat egy nevet a központi telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="62e28-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="62e28-124">Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.</span><span class="sxs-lookup"><span data-stu-id="62e28-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="62e28-125">3. példa: a minden erőforráscsoport telepített példányának beszerzése</span><span class="sxs-lookup"><span data-stu-id="62e28-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="62e28-126">Ez a parancs a Get-AzResourceGroup parancsmag használatával beilleszti az előfizetéshez tartozó összes erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="62e28-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="62e28-127">A parancs a pipeline operátor segítségével átadja az erőforráscsoportok az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="62e28-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="62e28-128">A jelenlegi parancsmag beilleszti az előfizetésben szereplő összes erőforráscsoport telepített példányait, és az eredményeket átadja az Format-Table parancsmagnak a **ResourceGroupName** , a **DeploymentName** és a **ProvisioningState** tulajdonság értékeinek megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="62e28-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="62e28-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62e28-129">PARAMETERS</span></span>

### <span data-ttu-id="62e28-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="62e28-130">-ApiVersion</span></span>
<span data-ttu-id="62e28-131">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="62e28-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="62e28-132">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="62e28-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="62e28-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e28-133">-DefaultProfile</span></span>
<span data-ttu-id="62e28-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62e28-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62e28-135">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="62e28-135">-Id</span></span>
<span data-ttu-id="62e28-136">A beolvasott erőforráscsoport-telepítő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="62e28-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="62e28-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62e28-137">-Name</span></span>
<span data-ttu-id="62e28-138">A beolvasott példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62e28-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="62e28-139">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="62e28-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="62e28-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="62e28-140">-Pre</span></span>
<span data-ttu-id="62e28-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="62e28-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="62e28-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e28-142">-ResourceGroupName</span></span>
<span data-ttu-id="62e28-143">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62e28-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="62e28-144">A parancsmag a paraméter által megadott erőforráscsoport telepített példányait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62e28-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="62e28-145">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="62e28-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="62e28-146">Ez a paraméter szükséges, és a parancsokban csak egy erőforráscsoport lehet megadható.</span><span class="sxs-lookup"><span data-stu-id="62e28-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="62e28-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e28-147">CommonParameters</span></span>
<span data-ttu-id="62e28-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62e28-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e28-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e28-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e28-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e28-150">INPUTS</span></span>

### <span data-ttu-id="62e28-151">System. String</span><span class="sxs-lookup"><span data-stu-id="62e28-151">System.String</span></span>

## <span data-ttu-id="62e28-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e28-152">OUTPUTS</span></span>

### <span data-ttu-id="62e28-153">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62e28-153">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="62e28-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62e28-154">NOTES</span></span>

## <span data-ttu-id="62e28-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62e28-155">RELATED LINKS</span></span>

[<span data-ttu-id="62e28-156">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62e28-156">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="62e28-157">Új – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62e28-157">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="62e28-158">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62e28-158">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="62e28-159">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62e28-159">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="62e28-160">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62e28-160">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="62e28-161">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="62e28-161">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


