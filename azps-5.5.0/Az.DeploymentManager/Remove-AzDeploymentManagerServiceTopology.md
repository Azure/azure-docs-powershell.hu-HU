---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204287"
---
# <span data-ttu-id="7aac1-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="7aac1-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="7aac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aac1-102">SYNOPSIS</span></span>
<span data-ttu-id="7aac1-103">Törli a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="7aac1-103">Deletes the service topology.</span></span> <span data-ttu-id="7aac1-104">A szolgáltatás topológiája alapján létrehozott összes szolgáltatást törölni kell a szolgáltatás topológiája törlése előtt.</span><span class="sxs-lookup"><span data-stu-id="7aac1-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="7aac1-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7aac1-105">SYNTAX</span></span>

### <span data-ttu-id="7aac1-106">Interaktív (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7aac1-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aac1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7aac1-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aac1-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="7aac1-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aac1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7aac1-109">DESCRIPTION</span></span>
<span data-ttu-id="7aac1-110">A **Remove-AzDeploymentManagerServiceTopology** parancsmag törli a szolgáltatás topológiáját.</span><span class="sxs-lookup"><span data-stu-id="7aac1-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="7aac1-111">Adja meg a szolgáltatás topológiáját a neve és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="7aac1-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="7aac1-112">Másik módon meg is használhatja a ServiceTopology objektumot vagy az ResourceId objektumot.</span><span class="sxs-lookup"><span data-stu-id="7aac1-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="7aac1-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7aac1-113">EXAMPLES</span></span>

### <span data-ttu-id="7aac1-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="7aac1-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="7aac1-115">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatás topológiát a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="7aac1-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7aac1-116">2. példa: Szolgáltatás-topológia törlése az erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="7aac1-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="7aac1-117">Ez a parancs törli a ContosoServiceTopology nevű szolgáltatás topológiát a ContosoResourceGroup csoportban.</span><span class="sxs-lookup"><span data-stu-id="7aac1-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7aac1-118">3. példa: Szolgáltatás-topológia törlése a szolgáltatás topológia objektumával.</span><span class="sxs-lookup"><span data-stu-id="7aac1-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="7aac1-119">Ez a parancs törli a szolgáltatás topológiáját, amelynek neve és ResourceGroup tulajdonsága megegyezik a $serviceTopologyObject ResourceGroupName tulajdonságaival.</span><span class="sxs-lookup"><span data-stu-id="7aac1-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="7aac1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7aac1-120">PARAMETERS</span></span>

### <span data-ttu-id="7aac1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aac1-121">-DefaultProfile</span></span>
<span data-ttu-id="7aac1-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7aac1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aac1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7aac1-123">-InputObject</span></span>
<span data-ttu-id="7aac1-124">Az eltávolítható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="7aac1-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="7aac1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7aac1-125">-Name</span></span>
<span data-ttu-id="7aac1-126">A szolgáltatás-topológia neve.</span><span class="sxs-lookup"><span data-stu-id="7aac1-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="7aac1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7aac1-127">-PassThru</span></span>
<span data-ttu-id="7aac1-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7aac1-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7aac1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aac1-129">-ResourceGroupName</span></span>
<span data-ttu-id="7aac1-130">Az erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="7aac1-130">The resource group.</span></span>

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

### <span data-ttu-id="7aac1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7aac1-131">-ResourceId</span></span>
<span data-ttu-id="7aac1-132">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7aac1-132">The resource identifier.</span></span>

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

### <span data-ttu-id="7aac1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7aac1-133">-Confirm</span></span>
<span data-ttu-id="7aac1-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7aac1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aac1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aac1-135">-WhatIf</span></span>
<span data-ttu-id="7aac1-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7aac1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aac1-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7aac1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aac1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aac1-138">CommonParameters</span></span>
<span data-ttu-id="7aac1-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aac1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aac1-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7aac1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aac1-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7aac1-141">INPUTS</span></span>

### <span data-ttu-id="7aac1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7aac1-142">System.String</span></span>

### <span data-ttu-id="7aac1-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="7aac1-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="7aac1-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aac1-144">OUTPUTS</span></span>

### <span data-ttu-id="7aac1-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7aac1-145">System.Boolean</span></span>

## <span data-ttu-id="7aac1-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7aac1-146">NOTES</span></span>

## <span data-ttu-id="7aac1-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aac1-147">RELATED LINKS</span></span>
