---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149995"
---
# <span data-ttu-id="a75ce-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="a75ce-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="a75ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a75ce-103">Elindít egy folyamatot, hogy elindítsa a futtatásot.</span><span class="sxs-lookup"><span data-stu-id="a75ce-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="a75ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a75ce-104">SYNTAX</span></span>

### <span data-ttu-id="a75ce-105">NewByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a75ce-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a75ce-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="a75ce-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a75ce-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="a75ce-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a75ce-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a75ce-108">DESCRIPTION</span></span>
<span data-ttu-id="a75ce-109">Az **Invoke-AzSynapsePipeline** parancs elindít egy futtatást a megadott folyamaton, és a futtatás azonosítóját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a75ce-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="a75ce-110">Ez a GUID-azonosító a **Get-AzSynapsePipelineRun** vagy **a Get-AzSynapseActivityRun** számára is átadható, hogy további részleteket szerezzen a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="a75ce-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="a75ce-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a75ce-111">EXAMPLES</span></span>

### <span data-ttu-id="a75ce-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a75ce-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="a75ce-113">Ez a parancs elindítja a ContosoPipeline nevű folyamat futtatását a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="a75ce-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a75ce-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a75ce-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="a75ce-115">Ez a parancs elindítja a ContosoPipeline nevű prognózis futtatását a Munkaterület ContosoWorkspace-en keresztüli folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="a75ce-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a75ce-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a75ce-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="a75ce-117">Ez a parancs elindítja a ContosoPipeline nevű folyamat futtatását a Munkaterület ContosoWorkspace-en keresztüli folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="a75ce-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a75ce-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a75ce-118">PARAMETERS</span></span>

### <span data-ttu-id="a75ce-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a75ce-119">-AsJob</span></span>
<span data-ttu-id="a75ce-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a75ce-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a75ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75ce-121">-DefaultProfile</span></span>
<span data-ttu-id="a75ce-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a75ce-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a75ce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a75ce-123">-InputObject</span></span>
<span data-ttu-id="a75ce-124">A folyamatra vonatkozó információk.</span><span class="sxs-lookup"><span data-stu-id="a75ce-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="a75ce-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="a75ce-125">-IsRecovery</span></span>
<span data-ttu-id="a75ce-126">Helyreállítási mód jelzője.</span><span class="sxs-lookup"><span data-stu-id="a75ce-126">Recovery mode flag.</span></span>
<span data-ttu-id="a75ce-127">Ha a helyreállítási mód igazra van állítva, a megadott hivatkozott folyamat fut, és az új futtatás ugyanazon groupId csoportban lesz csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="a75ce-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="a75ce-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a75ce-128">-Parameter</span></span>
<span data-ttu-id="a75ce-129">A folyamat futtatásának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="a75ce-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="a75ce-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="a75ce-130">-ParameterFile</span></span>
<span data-ttu-id="a75ce-131">A fájl neve a folyamat futtatásához szükséges paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="a75ce-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="a75ce-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a75ce-132">-PipelineName</span></span>
<span data-ttu-id="a75ce-133">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="a75ce-133">The pipeline name.</span></span>

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

### <span data-ttu-id="a75ce-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a75ce-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="a75ce-135">A pipeline run ID for rerun.</span><span class="sxs-lookup"><span data-stu-id="a75ce-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="a75ce-136">Ha a futtatásazonosító meg van adva, a megadott futtatás paramétereit használja a rendszer új futtatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="a75ce-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="a75ce-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="a75ce-137">-StartActivityName</span></span>
<span data-ttu-id="a75ce-138">Helyreállítási módban az újrafuttatás ebből a tevékenységből indul ki.</span><span class="sxs-lookup"><span data-stu-id="a75ce-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="a75ce-139">Ha nincs megadva, az összes tevékenység futni fog.</span><span class="sxs-lookup"><span data-stu-id="a75ce-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="a75ce-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a75ce-140">-WorkspaceName</span></span>
<span data-ttu-id="a75ce-141">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="a75ce-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a75ce-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a75ce-142">-WorkspaceObject</span></span>
<span data-ttu-id="a75ce-143">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="a75ce-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a75ce-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a75ce-144">-Confirm</span></span>
<span data-ttu-id="a75ce-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a75ce-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a75ce-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a75ce-146">-WhatIf</span></span>
<span data-ttu-id="a75ce-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a75ce-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a75ce-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a75ce-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a75ce-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75ce-149">CommonParameters</span></span>
<span data-ttu-id="a75ce-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a75ce-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75ce-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a75ce-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75ce-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a75ce-152">INPUTS</span></span>

### <span data-ttu-id="a75ce-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="a75ce-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="a75ce-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a75ce-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a75ce-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a75ce-155">OUTPUTS</span></span>

### <span data-ttu-id="a75ce-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="a75ce-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="a75ce-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a75ce-157">NOTES</span></span>

## <span data-ttu-id="a75ce-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a75ce-158">RELATED LINKS</span></span>
