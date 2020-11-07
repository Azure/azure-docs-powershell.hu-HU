---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: ee0f1f855f4f24e3672606bfedc000452ce6040d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670986"
---
# <span data-ttu-id="7cd37-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="7cd37-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="7cd37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cd37-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd37-103">A szolgáltatás törlése..</span><span class="sxs-lookup"><span data-stu-id="7cd37-103">Deletes the service..</span></span> <span data-ttu-id="7cd37-104">A szolgáltatás törlése előtt minden, a szolgáltatás alatt létrehozott szolgáltatási egységet törölni kell.</span><span class="sxs-lookup"><span data-stu-id="7cd37-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="7cd37-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cd37-105">SYNTAX</span></span>

### <span data-ttu-id="7cd37-106">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cd37-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7cd37-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="7cd37-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd37-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd37-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd37-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd37-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd37-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd37-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd37-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cd37-111">DESCRIPTION</span></span>
<span data-ttu-id="7cd37-112">A **Remove-AzDeploymentManagerService** parancsmag a szolgáltatás topológiája alatt töröl egy szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7cd37-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="7cd37-113">Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével.</span><span class="sxs-lookup"><span data-stu-id="7cd37-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="7cd37-114">Másik lehetőségként megadhatja a szolgáltatás objektumát vagy a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7cd37-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="7cd37-115">Példák</span><span class="sxs-lookup"><span data-stu-id="7cd37-115">EXAMPLES</span></span>

### <span data-ttu-id="7cd37-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7cd37-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="7cd37-117">Ez a parancs törli a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="7cd37-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7cd37-118">2. példa: szolgáltatás törlése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="7cd37-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="7cd37-119">Ez a parancs törli a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában.</span><span class="sxs-lookup"><span data-stu-id="7cd37-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7cd37-120">Példa 3: szolgáltatás törlése a Service objektummal.</span><span class="sxs-lookup"><span data-stu-id="7cd37-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="7cd37-121">Ez a parancs törli azt a szolgáltatást, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="7cd37-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="7cd37-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cd37-122">PARAMETERS</span></span>

### <span data-ttu-id="7cd37-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd37-123">-DefaultProfile</span></span>
<span data-ttu-id="7cd37-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cd37-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd37-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd37-125">-InputObject</span></span>
<span data-ttu-id="7cd37-126">Service objektum.</span><span class="sxs-lookup"><span data-stu-id="7cd37-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cd37-127">-Name</span></span>
<span data-ttu-id="7cd37-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7cd37-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cd37-129">-PassThru</span></span>
<span data-ttu-id="7cd37-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7cd37-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7cd37-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd37-131">-ResourceGroupName</span></span>
<span data-ttu-id="7cd37-132">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="7cd37-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd37-133">-ResourceId</span></span>
<span data-ttu-id="7cd37-134">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7cd37-134">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="7cd37-135">-ServiceTopologyName</span></span>
<span data-ttu-id="7cd37-136">A szolgáltatás topológiájának neve.</span><span class="sxs-lookup"><span data-stu-id="7cd37-136">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="7cd37-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="7cd37-138">A szolgáltatás topológiájának objektuma, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7cd37-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd37-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="7cd37-140">A szolgáltatás topológiája erőforrás-azonosító, amelyben a szolgáltatást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7cd37-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cd37-141">-Confirm</span></span>
<span data-ttu-id="7cd37-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cd37-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd37-143">-WhatIf</span></span>
<span data-ttu-id="7cd37-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cd37-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd37-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cd37-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd37-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd37-146">CommonParameters</span></span>
<span data-ttu-id="7cd37-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cd37-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd37-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd37-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd37-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cd37-149">INPUTS</span></span>

### <span data-ttu-id="7cd37-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd37-150">System.String</span></span>

### <span data-ttu-id="7cd37-151">Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="7cd37-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="7cd37-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cd37-152">OUTPUTS</span></span>

### <span data-ttu-id="7cd37-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cd37-153">System.Boolean</span></span>

## <span data-ttu-id="7cd37-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cd37-154">NOTES</span></span>

## <span data-ttu-id="7cd37-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cd37-155">RELATED LINKS</span></span>
