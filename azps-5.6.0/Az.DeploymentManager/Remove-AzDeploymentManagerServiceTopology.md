---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: d3716d18bc883d5407ee4acf3fa43960b63e7cd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932954"
---
# <span data-ttu-id="31ba2-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="31ba2-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="31ba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="31ba2-103">Törli a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="31ba2-103">Deletes the service topology.</span></span> <span data-ttu-id="31ba2-104">A szolgáltatás topológiája alapján létrehozott összes szolgáltatást törölni kell a szolgáltatás topológiája törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="31ba2-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="31ba2-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31ba2-105">SYNTAX</span></span>

### <span data-ttu-id="31ba2-106">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31ba2-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ba2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="31ba2-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31ba2-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="31ba2-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ba2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31ba2-109">DESCRIPTION</span></span>
<span data-ttu-id="31ba2-110">A **Remove-AzDeploymentManagerServiceTopology** parancsmag törli a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="31ba2-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="31ba2-111">Adja meg a szolgáltatás topológiáját a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="31ba2-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="31ba2-112">Másik módon meg is használhatja a ServiceTopology objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="31ba2-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="31ba2-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31ba2-113">EXAMPLES</span></span>

### <span data-ttu-id="31ba2-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="31ba2-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="31ba2-115">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatás topológiát a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="31ba2-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="31ba2-116">2. példa: Szolgáltatás topológiájának törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="31ba2-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="31ba2-117">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatás topológiát a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="31ba2-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="31ba2-118">3. példa: Szolgáltatás-topológia törlése a szolgáltatás topológia objektumával.</span><span class="sxs-lookup"><span data-stu-id="31ba2-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="31ba2-119">Ez a parancs törli a szolgáltatás topológiáját, amelynek neve és ResourceGroup tulajdonsága megegyezik a $serviceTopologyObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="31ba2-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="31ba2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31ba2-120">PARAMETERS</span></span>

### <span data-ttu-id="31ba2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ba2-121">-DefaultProfile</span></span>
<span data-ttu-id="31ba2-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31ba2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31ba2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31ba2-123">-InputObject</span></span>
<span data-ttu-id="31ba2-124">Az eltávolítható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="31ba2-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="31ba2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="31ba2-125">-Name</span></span>
<span data-ttu-id="31ba2-126">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="31ba2-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="31ba2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31ba2-127">-PassThru</span></span>
<span data-ttu-id="31ba2-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="31ba2-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="31ba2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ba2-129">-ResourceGroupName</span></span>
<span data-ttu-id="31ba2-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="31ba2-130">The resource group.</span></span>

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

### <span data-ttu-id="31ba2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31ba2-131">-ResourceId</span></span>
<span data-ttu-id="31ba2-132">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="31ba2-132">The resource identifier.</span></span>

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

### <span data-ttu-id="31ba2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31ba2-133">-Confirm</span></span>
<span data-ttu-id="31ba2-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="31ba2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ba2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ba2-135">-WhatIf</span></span>
<span data-ttu-id="31ba2-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="31ba2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31ba2-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31ba2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ba2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ba2-138">CommonParameters</span></span>
<span data-ttu-id="31ba2-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ba2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ba2-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31ba2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ba2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31ba2-141">INPUTS</span></span>

### <span data-ttu-id="31ba2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="31ba2-142">System.String</span></span>

### <span data-ttu-id="31ba2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="31ba2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="31ba2-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31ba2-144">OUTPUTS</span></span>

### <span data-ttu-id="31ba2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31ba2-145">System.Boolean</span></span>

## <span data-ttu-id="31ba2-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31ba2-146">NOTES</span></span>

## <span data-ttu-id="31ba2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31ba2-147">RELATED LINKS</span></span>
