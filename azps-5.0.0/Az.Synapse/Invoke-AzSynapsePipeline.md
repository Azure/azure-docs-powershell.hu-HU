---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186499"
---
# <span data-ttu-id="74b8c-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="74b8c-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="74b8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="74b8c-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="74b8c-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="74b8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74b8c-104">SYNTAX</span></span>

### <span data-ttu-id="74b8c-105">NewByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74b8c-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b8c-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="74b8c-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b8c-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="74b8c-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74b8c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="74b8c-108">DESCRIPTION</span></span>
<span data-ttu-id="74b8c-109">Az **AzSynapsePipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="74b8c-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="74b8c-110">Ezt a GUID-ot átadhatja a **Get-AzSynapsePipelineRun** vagy a **Get-AzSynapseActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="74b8c-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="74b8c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="74b8c-111">EXAMPLES</span></span>

### <span data-ttu-id="74b8c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74b8c-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="74b8c-113">Ez a parancs elindítja a ContosoPipeline nevű pipeline-futást a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="74b8c-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="74b8c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="74b8c-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="74b8c-115">Ez a parancs elindítja a ContosoPipeline nevű pipeline-futást a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="74b8c-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="74b8c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="74b8c-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="74b8c-117">Ez a parancs elindítja a ContosoPipeline nevű pipeline-futást a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="74b8c-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="74b8c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74b8c-118">PARAMETERS</span></span>

### <span data-ttu-id="74b8c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74b8c-119">-AsJob</span></span>
<span data-ttu-id="74b8c-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="74b8c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74b8c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b8c-121">-DefaultProfile</span></span>
<span data-ttu-id="74b8c-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74b8c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b8c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74b8c-123">-InputObject</span></span>
<span data-ttu-id="74b8c-124">A csővezeték-futtatással kapcsolatos információk.</span><span class="sxs-lookup"><span data-stu-id="74b8c-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74b8c-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="74b8c-125">-IsRecovery</span></span>
<span data-ttu-id="74b8c-126">Helyreállítási mód jelölője</span><span class="sxs-lookup"><span data-stu-id="74b8c-126">Recovery mode flag.</span></span>
<span data-ttu-id="74b8c-127">Ha a helyreállítási mód True értékre van állítva, akkor a megadott hivatkozott csővezeték fut, és az új Futtatás ugyanabba a groupId lesz csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="74b8c-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="74b8c-128">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="74b8c-128">-Parameter</span></span>
<span data-ttu-id="74b8c-129">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="74b8c-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b8c-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="74b8c-130">-ParameterFile</span></span>
<span data-ttu-id="74b8c-131">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="74b8c-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="74b8c-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="74b8c-132">-PipelineName</span></span>
<span data-ttu-id="74b8c-133">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="74b8c-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b8c-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="74b8c-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="74b8c-135">Az újraindításhoz használt pipeline-azonosító.</span><span class="sxs-lookup"><span data-stu-id="74b8c-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="74b8c-136">Ha meg van adva a futtatási azonosító, a program a megadott Futtatás paramétereit fogja használni az új Futtatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="74b8c-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="74b8c-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="74b8c-137">-StartActivityName</span></span>
<span data-ttu-id="74b8c-138">Helyreállítási módban a program az ismétlést ebből a tevékenységből kezdi.</span><span class="sxs-lookup"><span data-stu-id="74b8c-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="74b8c-139">Ha nincs megadva, a program minden tevékenységet futtat.</span><span class="sxs-lookup"><span data-stu-id="74b8c-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="74b8c-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74b8c-140">-WorkspaceName</span></span>
<span data-ttu-id="74b8c-141">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="74b8c-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b8c-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="74b8c-142">-WorkspaceObject</span></span>
<span data-ttu-id="74b8c-143">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="74b8c-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74b8c-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74b8c-144">-Confirm</span></span>
<span data-ttu-id="74b8c-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74b8c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b8c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b8c-146">-WhatIf</span></span>
<span data-ttu-id="74b8c-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74b8c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b8c-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74b8c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b8c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b8c-149">CommonParameters</span></span>
<span data-ttu-id="74b8c-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74b8c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b8c-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="74b8c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b8c-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74b8c-152">INPUTS</span></span>

### <span data-ttu-id="74b8c-153">Microsoft. Azure. commands. szinapszis. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="74b8c-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="74b8c-154">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="74b8c-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="74b8c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74b8c-155">OUTPUTS</span></span>

### <span data-ttu-id="74b8c-156">Microsoft. Azure. commands. szinapszis. models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="74b8c-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="74b8c-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74b8c-157">NOTES</span></span>

## <span data-ttu-id="74b8c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74b8c-158">RELATED LINKS</span></span>
