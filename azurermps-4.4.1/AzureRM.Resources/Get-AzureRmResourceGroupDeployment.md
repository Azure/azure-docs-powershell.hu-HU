---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500756"
---
# <span data-ttu-id="41c7b-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="41c7b-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="41c7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="41c7b-103">Beilleszti a telepített erőforrásokat egy erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="41c7b-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41c7b-104">SYNTAX</span></span>

### <span data-ttu-id="41c7b-105">A telepítő név paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="41c7b-105">The deployment name parameter set.</span></span> <span data-ttu-id="41c7b-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="41c7b-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41c7b-107">A telepítő-azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="41c7b-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41c7b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="41c7b-108">DESCRIPTION</span></span>
<span data-ttu-id="41c7b-109">A **Get-AzureRmResourceGroupDeployment** parancsmag a telepített példányokat egy Azure-erőforráscsoport szerint kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41c7b-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="41c7b-110">Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.</span><span class="sxs-lookup"><span data-stu-id="41c7b-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="41c7b-111">Alapértelmezés szerint a **Get-AzureRmResourceGroupDeployment beolvassa** a megadott erőforráscsoport összes telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="41c7b-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="41c7b-112">Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.</span><span class="sxs-lookup"><span data-stu-id="41c7b-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="41c7b-113">Az Azure-erőforráscsoport olyan Azure-erőforrások gyűjteménye, amelyek egységként települnek.</span><span class="sxs-lookup"><span data-stu-id="41c7b-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="41c7b-114">A telepítés az a művelet, amely az erőforráscsoport számára elérhetővé teszi az erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="41c7b-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="41c7b-115">Az Azure-erőforrásokról és az Azure-erőforráscsoportok használatáról az New-AzureRmResourceGroup parancsmag című témakörben olvashat bővebben.</span><span class="sxs-lookup"><span data-stu-id="41c7b-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="41c7b-116">Ezt a parancsmagot a nyomkövetéshez használhatja.</span><span class="sxs-lookup"><span data-stu-id="41c7b-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="41c7b-117">Hibakereséshez használja ezt a parancsmagot a Get-AzureRmLog parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="41c7b-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="41c7b-118">Példák</span><span class="sxs-lookup"><span data-stu-id="41c7b-118">EXAMPLES</span></span>

### <span data-ttu-id="41c7b-119">Példa 1: erőforráscsoport minden telepített példányának beszerzése</span><span class="sxs-lookup"><span data-stu-id="41c7b-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="41c7b-120">Ez a parancs beilleszti a ContosoLabsRG-erőforráscsoport összes telepített példányát.</span><span class="sxs-lookup"><span data-stu-id="41c7b-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="41c7b-121">A kimenet a gyűjteményt jeleníti meg egy olyan WordPress bloghoz, amely a gyűjtemény sablonját használta.</span><span class="sxs-lookup"><span data-stu-id="41c7b-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="41c7b-122">2. példa: a központi felügyelet beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="41c7b-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="41c7b-123">Ez a parancs a ContosoLabsRG-erőforráscsoport DeployWebsite01 telepítését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41c7b-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="41c7b-124">Az **új AzureRmResourceGroup** vagy a **New-AzureRmResourceGroupDeployment** parancsmagok segítségével létrehozhat egy nevet a központi telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="41c7b-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="41c7b-125">Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.</span><span class="sxs-lookup"><span data-stu-id="41c7b-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="41c7b-126">3. példa: a minden erőforráscsoport telepített példányának beszerzése</span><span class="sxs-lookup"><span data-stu-id="41c7b-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="41c7b-127">Ez a parancs a Get-AzureRmResourceGroup parancsmag használatával beilleszti az előfizetéshez tartozó összes erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="41c7b-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="41c7b-128">A parancs a pipeline operátor segítségével átadja az erőforráscsoportok az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="41c7b-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="41c7b-129">A jelenlegi parancsmag beilleszti az előfizetésben szereplő összes erőforráscsoport telepített példányait, és az eredményeket átadja az Format-Table parancsmagnak a **ResourceGroupName** , a **DeploymentName** és a **ProvisioningState** tulajdonság értékeinek megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="41c7b-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="41c7b-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41c7b-130">PARAMETERS</span></span>

### <span data-ttu-id="41c7b-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="41c7b-131">-ApiVersion</span></span>
<span data-ttu-id="41c7b-132">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="41c7b-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="41c7b-133">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="41c7b-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="41c7b-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="41c7b-134">-Id</span></span>
<span data-ttu-id="41c7b-135">A beolvasott erőforráscsoport-telepítő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="41c7b-135">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c7b-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41c7b-136">-Name</span></span>
<span data-ttu-id="41c7b-137">A beolvasott példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41c7b-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="41c7b-138">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="41c7b-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c7b-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="41c7b-139">-Pre</span></span>
<span data-ttu-id="41c7b-140">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="41c7b-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="41c7b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c7b-141">-ResourceGroupName</span></span>
<span data-ttu-id="41c7b-142">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41c7b-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="41c7b-143">A parancsmag a paraméter által megadott erőforráscsoport telepített példányait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="41c7b-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="41c7b-144">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="41c7b-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="41c7b-145">Ez a paraméter szükséges, és a parancsokban csak egy erőforráscsoport lehet megadható.</span><span class="sxs-lookup"><span data-stu-id="41c7b-145">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c7b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c7b-146">-DefaultProfile</span></span>
<span data-ttu-id="41c7b-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41c7b-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41c7b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c7b-148">CommonParameters</span></span>
<span data-ttu-id="41c7b-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41c7b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c7b-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c7b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c7b-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41c7b-151">INPUTS</span></span>

### <span data-ttu-id="41c7b-152">Nincs</span><span class="sxs-lookup"><span data-stu-id="41c7b-152">None</span></span>

## <span data-ttu-id="41c7b-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41c7b-153">OUTPUTS</span></span>

### <span data-ttu-id="41c7b-154">Microsoft. Azure. Command. ResourceManagement. models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="41c7b-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="41c7b-155">A parancsmag az erőforráscsoport-bevezetéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="41c7b-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="41c7b-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41c7b-156">NOTES</span></span>

## <span data-ttu-id="41c7b-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41c7b-157">RELATED LINKS</span></span>

[<span data-ttu-id="41c7b-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="41c7b-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="41c7b-159">Új – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="41c7b-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="41c7b-160">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="41c7b-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="41c7b-161">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="41c7b-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="41c7b-162">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="41c7b-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="41c7b-163">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="41c7b-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


