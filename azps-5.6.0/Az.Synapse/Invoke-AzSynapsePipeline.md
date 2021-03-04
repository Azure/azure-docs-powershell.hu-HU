---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: 756db1072eec6546f6e495b3ec2115ca77389a73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934617"
---
# <span data-ttu-id="069dd-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="069dd-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="069dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="069dd-102">SYNOPSIS</span></span>
<span data-ttu-id="069dd-103">Elindít egy folyamatot, hogy elindítsa a futtatásot.</span><span class="sxs-lookup"><span data-stu-id="069dd-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="069dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="069dd-104">SYNTAX</span></span>

### <span data-ttu-id="069dd-105">NewByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="069dd-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="069dd-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="069dd-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="069dd-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="069dd-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="069dd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="069dd-108">DESCRIPTION</span></span>
<span data-ttu-id="069dd-109">Az **Invoke-AzSynapsePipeline** parancs elindít egy futtatást a megadott folyamaton, és a futtatás azonosítóját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="069dd-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="069dd-110">Ez a GUID-azonosító a **Get-AzSynapsePipelineRun** vagy **a Get-AzSynapseActivityRun** számára is átadható, hogy további részleteket szerezzen a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="069dd-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="069dd-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="069dd-111">EXAMPLES</span></span>

### <span data-ttu-id="069dd-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="069dd-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="069dd-113">Ez a parancs elindítja a ContosoPipeline nevű folyamat futtatását a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="069dd-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="069dd-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="069dd-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="069dd-115">Ez a parancs elindítja a ContosoPipeline nevű prognózis futtatását a Munkaterület ContosoWorkspace-en keresztüli folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="069dd-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="069dd-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="069dd-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="069dd-117">Ez a parancs elindítja a ContosoPipeline nevű prognózis futtatását a Munkaterület ContosoWorkspace-en keresztüli folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="069dd-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="069dd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="069dd-118">PARAMETERS</span></span>

### <span data-ttu-id="069dd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="069dd-119">-AsJob</span></span>
<span data-ttu-id="069dd-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="069dd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="069dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="069dd-121">-DefaultProfile</span></span>
<span data-ttu-id="069dd-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="069dd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="069dd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="069dd-123">-InputObject</span></span>
<span data-ttu-id="069dd-124">A folyamatra vonatkozó információk.</span><span class="sxs-lookup"><span data-stu-id="069dd-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="069dd-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="069dd-125">-IsRecovery</span></span>
<span data-ttu-id="069dd-126">Helyreállítási mód jelzője.</span><span class="sxs-lookup"><span data-stu-id="069dd-126">Recovery mode flag.</span></span>
<span data-ttu-id="069dd-127">Ha a helyreállítási mód igazra van állítva, a megadott hivatkozott folyamat fut, és az új futtatás ugyanazon groupId csoportban lesz csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="069dd-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="069dd-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="069dd-128">-Parameter</span></span>
<span data-ttu-id="069dd-129">A folyamat futtatásának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="069dd-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="069dd-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="069dd-130">-ParameterFile</span></span>
<span data-ttu-id="069dd-131">A fájl neve a folyamat futtatásához szükséges paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="069dd-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="069dd-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="069dd-132">-PipelineName</span></span>
<span data-ttu-id="069dd-133">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="069dd-133">The pipeline name.</span></span>

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

### <span data-ttu-id="069dd-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="069dd-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="069dd-135">A pipeline run ID for rerun.</span><span class="sxs-lookup"><span data-stu-id="069dd-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="069dd-136">Ha a futtatásazonosító meg van adva, a megadott futtatás paramétereit használja a rendszer új futtatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="069dd-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="069dd-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="069dd-137">-StartActivityName</span></span>
<span data-ttu-id="069dd-138">Helyreállítási módban az újrafuttatás ebből a tevékenységből indul ki.</span><span class="sxs-lookup"><span data-stu-id="069dd-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="069dd-139">Ha nincs megadva, az összes tevékenység futni fog.</span><span class="sxs-lookup"><span data-stu-id="069dd-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="069dd-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="069dd-140">-WorkspaceName</span></span>
<span data-ttu-id="069dd-141">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="069dd-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="069dd-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="069dd-142">-WorkspaceObject</span></span>
<span data-ttu-id="069dd-143">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="069dd-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="069dd-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="069dd-144">-Confirm</span></span>
<span data-ttu-id="069dd-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="069dd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="069dd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="069dd-146">-WhatIf</span></span>
<span data-ttu-id="069dd-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="069dd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="069dd-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="069dd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="069dd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="069dd-149">CommonParameters</span></span>
<span data-ttu-id="069dd-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="069dd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="069dd-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="069dd-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="069dd-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="069dd-152">INPUTS</span></span>

### <span data-ttu-id="069dd-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="069dd-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="069dd-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="069dd-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="069dd-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="069dd-155">OUTPUTS</span></span>

### <span data-ttu-id="069dd-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="069dd-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="069dd-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="069dd-157">NOTES</span></span>

## <span data-ttu-id="069dd-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="069dd-158">RELATED LINKS</span></span>
