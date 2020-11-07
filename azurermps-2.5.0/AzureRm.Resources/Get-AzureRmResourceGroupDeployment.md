---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848393"
---
# <span data-ttu-id="e2f67-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e2f67-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e2f67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2f67-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f67-103">Beilleszti a telepített erőforrásokat egy erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="e2f67-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2f67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2f67-104">SYNTAX</span></span>

### <span data-ttu-id="e2f67-105">GetByResourceGroupDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2f67-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2f67-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e2f67-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2f67-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2f67-107">DESCRIPTION</span></span>
<span data-ttu-id="e2f67-108">A **Get-AzureRmResourceGroupDeployment** parancsmag a telepített példányokat egy Azure-erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e2f67-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="e2f67-109">Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="e2f67-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="e2f67-110">Alapértelmezés szerint a **Get-AzureRmResourceGroupDeployment beolvassa** a megadott erőforráscsoport összes telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="e2f67-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="e2f67-111">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="e2f67-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="e2f67-112">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="e2f67-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="e2f67-113">A telepítés az a művelet, amely az erőforráscsoport számára elérhetővé teszi az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="e2f67-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="e2f67-114">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzureRmResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="e2f67-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="e2f67-115">Ezt a parancsmagot a nyomkövetéshez használhatja.</span><span class="sxs-lookup"><span data-stu-id="e2f67-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="e2f67-116">Hibakereséshez használja ezt a parancsmagot a Get-AzureRmLog parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="e2f67-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="e2f67-117">Példák</span><span class="sxs-lookup"><span data-stu-id="e2f67-117">EXAMPLES</span></span>

### <span data-ttu-id="e2f67-118">Példa 1: erőforráscsoport minden telepített példányának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e2f67-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="e2f67-119">Ez a parancs beilleszti a ContosoLabsRG-erőforráscsoport összes telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="e2f67-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="e2f67-120">A kimenet a gyűjteményt jeleníti meg egy olyan WordPress bloghoz, amely a gyűjtemény sablonját használta.</span><span class="sxs-lookup"><span data-stu-id="e2f67-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="e2f67-121">2. példa: a központi felügyelet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="e2f67-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="e2f67-122">Ez a parancs a ContosoLabsRG-erőforráscsoport DeployWebsite01 telepítését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e2f67-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="e2f67-123">Az **új AzureRmResourceGroup** vagy a **New-AzureRmResourceGroupDeployment** parancsmagok segítségével létrehozhat egy nevet a központi telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="e2f67-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="e2f67-124">Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.</span><span class="sxs-lookup"><span data-stu-id="e2f67-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="e2f67-125">3. példa: a minden erőforráscsoport telepített példányának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e2f67-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="e2f67-126">Ez a parancs a Get-AzureRmResourceGroup parancsmag használatával beilleszti az előfizetéshez tartozó összes erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="e2f67-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="e2f67-127">A parancs a pipeline operátor segítségével átadja az erőforráscsoportok az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e2f67-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e2f67-128">A jelenlegi parancsmag beilleszti az előfizetésben szereplő összes erőforráscsoport telepített példányait, és az eredményeket átadja az Format-Table parancsmagnak a **ResourceGroupName** , a **DeploymentName** és a **ProvisioningState** tulajdonság értékeinek megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e2f67-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="e2f67-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2f67-129">PARAMETERS</span></span>

### <span data-ttu-id="e2f67-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e2f67-130">-ApiVersion</span></span>
<span data-ttu-id="e2f67-131">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2f67-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e2f67-132">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="e2f67-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e2f67-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f67-133">-DefaultProfile</span></span>
<span data-ttu-id="e2f67-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e2f67-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2f67-135">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e2f67-135">-Id</span></span>
<span data-ttu-id="e2f67-136">A beolvasott erőforráscsoport-telepítő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2f67-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="e2f67-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2f67-137">-Name</span></span>
<span data-ttu-id="e2f67-138">A beolvasott példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2f67-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="e2f67-139">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="e2f67-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="e2f67-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="e2f67-140">-Pre</span></span>
<span data-ttu-id="e2f67-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="e2f67-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e2f67-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f67-142">-ResourceGroupName</span></span>
<span data-ttu-id="e2f67-143">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2f67-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e2f67-144">A parancsmag a paraméter által megadott erőforráscsoport telepített példányait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e2f67-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="e2f67-145">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="e2f67-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="e2f67-146">Ez a paraméter szükséges, és a parancsokban csak egy erőforráscsoport lehet megadható.</span><span class="sxs-lookup"><span data-stu-id="e2f67-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="e2f67-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f67-147">CommonParameters</span></span>
<span data-ttu-id="e2f67-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2f67-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f67-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f67-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f67-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2f67-150">INPUTS</span></span>

### <span data-ttu-id="e2f67-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2f67-151">None</span></span>

## <span data-ttu-id="e2f67-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2f67-152">OUTPUTS</span></span>

### <span data-ttu-id="e2f67-153">Microsoft. Azure. Command. ResourceManagement. models.</span><span class="sxs-lookup"><span data-stu-id="e2f67-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="e2f67-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e2f67-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="e2f67-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2f67-155">NOTES</span></span>

## <span data-ttu-id="e2f67-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2f67-156">RELATED LINKS</span></span>

[<span data-ttu-id="e2f67-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2f67-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="e2f67-158">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2f67-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e2f67-159">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e2f67-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e2f67-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e2f67-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e2f67-161">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e2f67-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e2f67-162">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e2f67-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


