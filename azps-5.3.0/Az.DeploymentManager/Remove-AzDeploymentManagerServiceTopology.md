---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467926"
---
# <span data-ttu-id="07b39-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="07b39-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="07b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b39-102">SYNOPSIS</span></span>
<span data-ttu-id="07b39-103">Törli a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="07b39-103">Deletes the service topology.</span></span> <span data-ttu-id="07b39-104">A szolgáltatás topológiája alapján létrehozott összes szolgáltatást törölni kell a szolgáltatás topológiája törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="07b39-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="07b39-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07b39-105">SYNTAX</span></span>

### <span data-ttu-id="07b39-106">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07b39-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07b39-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="07b39-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07b39-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="07b39-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07b39-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07b39-109">DESCRIPTION</span></span>
<span data-ttu-id="07b39-110">A **Remove-AzDeploymentManagerServiceTopology** parancsmag törli a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="07b39-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="07b39-111">Adja meg a szolgáltatás topológiáját a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="07b39-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="07b39-112">Másik módon meg is használhatja a ServiceTopology objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="07b39-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="07b39-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07b39-113">EXAMPLES</span></span>

### <span data-ttu-id="07b39-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="07b39-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="07b39-115">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatás topológiát a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="07b39-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="07b39-116">2. példa: Szolgáltatás topológiájának törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="07b39-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="07b39-117">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatás topológiát a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="07b39-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="07b39-118">3. példa: Szolgáltatás-topológia törlése a szolgáltatás topológia objektumával.</span><span class="sxs-lookup"><span data-stu-id="07b39-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="07b39-119">Ez a parancs törli a szolgáltatás topológiáját, amelynek neve és ResourceGroup tulajdonsága megegyezik a $serviceTopologyObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="07b39-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="07b39-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07b39-120">PARAMETERS</span></span>

### <span data-ttu-id="07b39-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b39-121">-DefaultProfile</span></span>
<span data-ttu-id="07b39-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07b39-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b39-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07b39-123">-InputObject</span></span>
<span data-ttu-id="07b39-124">Az eltávolítható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="07b39-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07b39-125">-Name</span><span class="sxs-lookup"><span data-stu-id="07b39-125">-Name</span></span>
<span data-ttu-id="07b39-126">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="07b39-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="07b39-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07b39-127">-PassThru</span></span>
<span data-ttu-id="07b39-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="07b39-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="07b39-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b39-129">-ResourceGroupName</span></span>
<span data-ttu-id="07b39-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="07b39-130">The resource group.</span></span>

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

### <span data-ttu-id="07b39-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07b39-131">-ResourceId</span></span>
<span data-ttu-id="07b39-132">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="07b39-132">The resource identifier.</span></span>

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

### <span data-ttu-id="07b39-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07b39-133">-Confirm</span></span>
<span data-ttu-id="07b39-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07b39-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b39-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b39-135">-WhatIf</span></span>
<span data-ttu-id="07b39-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07b39-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b39-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07b39-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b39-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b39-138">CommonParameters</span></span>
<span data-ttu-id="07b39-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07b39-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b39-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07b39-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b39-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07b39-141">INPUTS</span></span>

### <span data-ttu-id="07b39-142">System.String</span><span class="sxs-lookup"><span data-stu-id="07b39-142">System.String</span></span>

### <span data-ttu-id="07b39-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="07b39-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="07b39-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07b39-144">OUTPUTS</span></span>

### <span data-ttu-id="07b39-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07b39-145">System.Boolean</span></span>

## <span data-ttu-id="07b39-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07b39-146">NOTES</span></span>

## <span data-ttu-id="07b39-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07b39-147">RELATED LINKS</span></span>
