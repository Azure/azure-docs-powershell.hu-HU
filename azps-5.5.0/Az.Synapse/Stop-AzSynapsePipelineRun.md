---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157810"
---
# <span data-ttu-id="c7a33-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="c7a33-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="c7a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a33-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a33-103">Leállítja a munkaterületen futó prognózist.</span><span class="sxs-lookup"><span data-stu-id="c7a33-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="c7a33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7a33-104">SYNTAX</span></span>

### <span data-ttu-id="c7a33-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7a33-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a33-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c7a33-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a33-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7a33-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7a33-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7a33-108">DESCRIPTION</span></span>
<span data-ttu-id="c7a33-109">A **Stop-AzSynapsePipelineRun parancsmag** leállítja a folyamat futtatását a folyamatazonosítóval megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="c7a33-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="c7a33-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7a33-110">EXAMPLES</span></span>

### <span data-ttu-id="c7a33-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c7a33-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="c7a33-112">Ez a parancs leállítja a folyamat futtatását a ContosoWorkspace munkaterület b9730a13-aa12-4926-a8b3-8e3a974ab0bd azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="c7a33-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c7a33-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c7a33-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="c7a33-114">Ez a parancs leállítja a folyamat futtatását a ContosoWorkspace munkaterületen a ContosoWorkspace-en keresztül a következő azonosítóval: b9730a13-aa12-4926-a8b3-8e3a974ab0bd.</span><span class="sxs-lookup"><span data-stu-id="c7a33-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="c7a33-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="c7a33-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="c7a33-116">Ez a parancs leállítja a folyamat futtatását a ContosoWorkspace munkaterületen a ContosoWorkspace-en keresztül a következő azonosítóval: b9730a13-aa12-4926-a8b3-8e3a974ab0bd.</span><span class="sxs-lookup"><span data-stu-id="c7a33-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c7a33-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7a33-117">PARAMETERS</span></span>

### <span data-ttu-id="c7a33-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7a33-118">-AsJob</span></span>
<span data-ttu-id="c7a33-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c7a33-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7a33-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a33-120">-DefaultProfile</span></span>
<span data-ttu-id="c7a33-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7a33-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a33-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7a33-122">-InputObject</span></span>
<span data-ttu-id="c7a33-123">A folyamatra vonatkozó információk.</span><span class="sxs-lookup"><span data-stu-id="c7a33-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a33-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7a33-124">-PassThru</span></span>
<span data-ttu-id="c7a33-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="c7a33-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c7a33-126">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="c7a33-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c7a33-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c7a33-127">-PipelineRunId</span></span>
<span data-ttu-id="c7a33-128">A folyamat futtatásának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7a33-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a33-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c7a33-129">-WorkspaceName</span></span>
<span data-ttu-id="c7a33-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="c7a33-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a33-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c7a33-131">-WorkspaceObject</span></span>
<span data-ttu-id="c7a33-132">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7a33-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a33-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7a33-133">-Confirm</span></span>
<span data-ttu-id="c7a33-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c7a33-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a33-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a33-135">-WhatIf</span></span>
<span data-ttu-id="c7a33-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c7a33-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a33-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7a33-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a33-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a33-138">CommonParameters</span></span>
<span data-ttu-id="c7a33-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a33-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a33-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7a33-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a33-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7a33-141">INPUTS</span></span>

### <span data-ttu-id="c7a33-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7a33-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c7a33-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="c7a33-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="c7a33-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7a33-144">OUTPUTS</span></span>

### <span data-ttu-id="c7a33-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c7a33-145">System.Boolean</span></span>

## <span data-ttu-id="c7a33-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7a33-146">NOTES</span></span>

## <span data-ttu-id="c7a33-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7a33-147">RELATED LINKS</span></span>
