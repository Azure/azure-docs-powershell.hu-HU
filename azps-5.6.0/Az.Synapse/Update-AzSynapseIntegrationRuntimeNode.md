---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5c2d7c8aa81cb45b6b49898c95b27256aa504b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924330"
---
# <span data-ttu-id="f29c7-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f29c7-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f29c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f29c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f29c7-103">Frissíti az önkiszolgáló integrációs futásidejű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="f29c7-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="f29c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f29c7-104">SYNTAX</span></span>

### <span data-ttu-id="f29c7-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f29c7-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f29c7-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f29c7-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f29c7-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f29c7-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f29c7-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f29c7-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f29c7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f29c7-109">DESCRIPTION</span></span>
<span data-ttu-id="f29c7-110">Az **Update-AzSynapseIntegrationRuntimeNode** parancsmag frissíti a munkaterület önkiszolgáló integrációs futásidejű csomópontjának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f29c7-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="f29c7-111">Jelenleg csak az "ConcurrentJobsLimit" frissítését támogatja.</span><span class="sxs-lookup"><span data-stu-id="f29c7-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="f29c7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f29c7-112">EXAMPLES</span></span>

### <span data-ttu-id="f29c7-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="f29c7-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="f29c7-114">A parancsmag frissíti a "ConcurrentCmsLimit" 3-asra a "Node_1" csomópontot az önkiszolgáló integrációs futásidejű "test-selfhost-ir" környezetben.</span><span class="sxs-lookup"><span data-stu-id="f29c7-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f29c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f29c7-115">PARAMETERS</span></span>

### <span data-ttu-id="f29c7-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="f29c7-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="f29c7-117">Az integrációs futásidejű csomóponton futtatható párhuzamos feladatok száma.</span><span class="sxs-lookup"><span data-stu-id="f29c7-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="f29c7-118">Az 1 és a maxConcurrentÚts közötti értékek megengedettek.</span><span class="sxs-lookup"><span data-stu-id="f29c7-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29c7-119">-DefaultProfile</span></span>
<span data-ttu-id="f29c7-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f29c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f29c7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f29c7-121">-InputObject</span></span>
<span data-ttu-id="f29c7-122">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="f29c7-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f29c7-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f29c7-124">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="f29c7-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f29c7-125">-Name</span></span>
<span data-ttu-id="f29c7-126">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="f29c7-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f29c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="f29c7-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f29c7-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f29c7-129">-ResourceId</span></span>
<span data-ttu-id="f29c7-130">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f29c7-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f29c7-131">-WorkspaceName</span></span>
<span data-ttu-id="f29c7-132">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f29c7-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f29c7-133">-WorkspaceObject</span></span>
<span data-ttu-id="f29c7-134">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="f29c7-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f29c7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f29c7-135">-Confirm</span></span>
<span data-ttu-id="f29c7-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f29c7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f29c7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f29c7-137">-WhatIf</span></span>
<span data-ttu-id="f29c7-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f29c7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f29c7-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f29c7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f29c7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29c7-140">CommonParameters</span></span>
<span data-ttu-id="f29c7-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29c7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29c7-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f29c7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29c7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f29c7-143">INPUTS</span></span>

### <span data-ttu-id="f29c7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f29c7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f29c7-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f29c7-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f29c7-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f29c7-146">OUTPUTS</span></span>

### <span data-ttu-id="f29c7-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="f29c7-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="f29c7-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f29c7-148">NOTES</span></span>

## <span data-ttu-id="f29c7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f29c7-149">RELATED LINKS</span></span>
