---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 284e568e1748c8bf6da3c5d43c27acb046be6172
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932961"
---
# <span data-ttu-id="b0e6c-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b0e6c-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="b0e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e6c-103">Törli a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-103">Deletes the service..</span></span> <span data-ttu-id="b0e6c-104">A szolgáltatás törlése előtt a szolgáltatásban létrehozott összes szolgáltatási egységet törölni kell.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="b0e6c-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0e6c-105">SYNTAX</span></span>

### <span data-ttu-id="b0e6c-106">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0e6c-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e6c-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="b0e6c-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e6c-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e6c-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e6c-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e6c-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e6c-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0e6c-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e6c-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0e6c-111">DESCRIPTION</span></span>
<span data-ttu-id="b0e6c-112">A **Remove-AzDeploymentManagerService parancsmag** egy szolgáltatás topológiája alatt töröl egy szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="b0e6c-113">Adja meg a szolgáltatást a neve, a szolgáltatás topológiája és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="b0e6c-114">Másik módon meg is használhatja a Service objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="b0e6c-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0e6c-115">EXAMPLES</span></span>

### <span data-ttu-id="b0e6c-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="b0e6c-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="b0e6c-117">Ez a parancs törli a ContosoService1 nevű szolgáltatást a ContosoResourceGroup szolgáltatás topológiája szerint.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b0e6c-118">2. példa: Szolgáltatás törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="b0e6c-119">Ez a parancs törli a ContosoService1 nevű szolgáltatást a ContosoResourceGroup szolgáltatás topológiája szerint.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b0e6c-120">3. példa: Szolgáltatás törlése a szolgáltatásobjektum használatával.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="b0e6c-121">Ez a parancs törli azt a szolgáltatást, amelynek a neve, a szolgáltatás topológiája és az Erőforráscsoport neve megegyezik a $serviceObject, ServiceTopologyName és ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="b0e6c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0e6c-122">PARAMETERS</span></span>

### <span data-ttu-id="b0e6c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e6c-123">-DefaultProfile</span></span>
<span data-ttu-id="b0e6c-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e6c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0e6c-125">-InputObject</span></span>
<span data-ttu-id="b0e6c-126">Szolgáltatásobjektum.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-126">Service object.</span></span>

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

### <span data-ttu-id="b0e6c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b0e6c-127">-Name</span></span>
<span data-ttu-id="b0e6c-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-128">The name of the service.</span></span>

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

### <span data-ttu-id="b0e6c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0e6c-129">-PassThru</span></span>
<span data-ttu-id="b0e6c-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b0e6c-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b0e6c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e6c-131">-ResourceGroupName</span></span>
<span data-ttu-id="b0e6c-132">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-132">The resource group.</span></span>

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

### <span data-ttu-id="b0e6c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e6c-133">-ResourceId</span></span>
<span data-ttu-id="b0e6c-134">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-134">The resource identifier.</span></span>

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

### <span data-ttu-id="b0e6c-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="b0e6c-135">-ServiceTopologyName</span></span>
<span data-ttu-id="b0e6c-136">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="b0e6c-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="b0e6c-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="b0e6c-138">Az a szolgáltatás topológia objektum, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="b0e6c-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e6c-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="b0e6c-140">Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hozatni a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="b0e6c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0e6c-141">-Confirm</span></span>
<span data-ttu-id="b0e6c-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e6c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e6c-143">-WhatIf</span></span>
<span data-ttu-id="b0e6c-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e6c-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e6c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e6c-146">CommonParameters</span></span>
<span data-ttu-id="b0e6c-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e6c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e6c-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0e6c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e6c-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0e6c-149">INPUTS</span></span>

### <span data-ttu-id="b0e6c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b0e6c-150">System.String</span></span>

### <span data-ttu-id="b0e6c-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="b0e6c-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="b0e6c-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0e6c-152">OUTPUTS</span></span>

### <span data-ttu-id="b0e6c-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0e6c-153">System.Boolean</span></span>

## <span data-ttu-id="b0e6c-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0e6c-154">NOTES</span></span>

## <span data-ttu-id="b0e6c-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0e6c-155">RELATED LINKS</span></span>
