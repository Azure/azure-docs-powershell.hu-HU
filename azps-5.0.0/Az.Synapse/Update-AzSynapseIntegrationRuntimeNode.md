---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185147"
---
# <span data-ttu-id="1d303-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1d303-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="1d303-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d303-102">SYNOPSIS</span></span>
<span data-ttu-id="1d303-103">Frissítheti az önkiszolgáló integrációs futásidejű csomópontot.</span><span class="sxs-lookup"><span data-stu-id="1d303-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="1d303-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d303-104">SYNTAX</span></span>

### <span data-ttu-id="1d303-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d303-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d303-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d303-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d303-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d303-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d303-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d303-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d303-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d303-109">DESCRIPTION</span></span>
<span data-ttu-id="1d303-110">Az **Update-AzSynapseIntegrationRuntimeNode** parancsmag frissíti a munkaterületen az önálló integrációs futásidejű csomópontok tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1d303-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="1d303-111">Jelenleg csak az "ConcurrentJobsLimit" frissítését támogatja.</span><span class="sxs-lookup"><span data-stu-id="1d303-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="1d303-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1d303-112">EXAMPLES</span></span>

### <span data-ttu-id="1d303-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d303-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="1d303-114">A parancsmag a "ConcurrentJobsLimit" Node_1 és a "selfhost-IR"-es "</span><span class="sxs-lookup"><span data-stu-id="1d303-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="1d303-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d303-115">PARAMETERS</span></span>

### <span data-ttu-id="1d303-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="1d303-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="1d303-117">Az egyidejű munkafolyamatok száma az integrációs futtatókörnyezet-csomóponton.</span><span class="sxs-lookup"><span data-stu-id="1d303-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="1d303-118">Az 1 és a maxConcurrentJobs közötti értékek engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="1d303-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="1d303-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d303-119">-DefaultProfile</span></span>
<span data-ttu-id="1d303-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d303-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d303-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d303-121">-InputObject</span></span>
<span data-ttu-id="1d303-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="1d303-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="1d303-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1d303-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="1d303-124">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="1d303-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="1d303-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d303-125">-Name</span></span>
<span data-ttu-id="1d303-126">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="1d303-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="1d303-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d303-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d303-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1d303-128">Resource group name.</span></span>

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

### <span data-ttu-id="1d303-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d303-129">-ResourceId</span></span>
<span data-ttu-id="1d303-130">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d303-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="1d303-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1d303-131">-WorkspaceName</span></span>
<span data-ttu-id="1d303-132">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="1d303-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1d303-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1d303-133">-WorkspaceObject</span></span>
<span data-ttu-id="1d303-134">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="1d303-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1d303-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d303-135">-Confirm</span></span>
<span data-ttu-id="1d303-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d303-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d303-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d303-137">-WhatIf</span></span>
<span data-ttu-id="1d303-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d303-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d303-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d303-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d303-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d303-140">CommonParameters</span></span>
<span data-ttu-id="1d303-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d303-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d303-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d303-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d303-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d303-143">INPUTS</span></span>

### <span data-ttu-id="1d303-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d303-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1d303-145">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1d303-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1d303-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d303-146">OUTPUTS</span></span>

### <span data-ttu-id="1d303-147">Microsoft. Azure. commands. szinapszis. models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="1d303-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="1d303-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d303-148">NOTES</span></span>

## <span data-ttu-id="1d303-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d303-149">RELATED LINKS</span></span>
