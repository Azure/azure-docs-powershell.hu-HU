---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186600"
---
# <span data-ttu-id="04d07-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="04d07-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="04d07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04d07-102">SYNOPSIS</span></span>
<span data-ttu-id="04d07-103">Egy munkaterületen futó csővezeték leállítása</span><span class="sxs-lookup"><span data-stu-id="04d07-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="04d07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04d07-104">SYNTAX</span></span>

### <span data-ttu-id="04d07-105">RemoveByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04d07-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04d07-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="04d07-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04d07-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="04d07-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d07-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="04d07-108">DESCRIPTION</span></span>
<span data-ttu-id="04d07-109">A **stop-AzSynapsePipelineRun** parancsmag a PIPELINE Run azonosítóval megadott munkaterületen leáll.</span><span class="sxs-lookup"><span data-stu-id="04d07-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="04d07-110">Példák</span><span class="sxs-lookup"><span data-stu-id="04d07-110">EXAMPLES</span></span>

### <span data-ttu-id="04d07-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="04d07-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="04d07-112">Ez a parancs leállítja a munkafolyamatot az azonosító b9730a13-AA12-4926-a8b3-8e3a974ab0bd a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="04d07-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="04d07-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="04d07-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="04d07-114">Ez a parancs a munkafolyamatot a munkaterület ContosoWorkspace a csővezetéken keresztül futtatja a b9730a13-AA12-4926-a8b3-8e3a974ab0bd.</span><span class="sxs-lookup"><span data-stu-id="04d07-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="04d07-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="04d07-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="04d07-116">Ez a parancs a munkafolyamatot a munkaterület ContosoWorkspace a csővezetéken keresztül futtatja a b9730a13-AA12-4926-a8b3-8e3a974ab0bd.</span><span class="sxs-lookup"><span data-stu-id="04d07-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="04d07-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04d07-117">PARAMETERS</span></span>

### <span data-ttu-id="04d07-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04d07-118">-AsJob</span></span>
<span data-ttu-id="04d07-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="04d07-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04d07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d07-120">-DefaultProfile</span></span>
<span data-ttu-id="04d07-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04d07-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04d07-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04d07-122">-InputObject</span></span>
<span data-ttu-id="04d07-123">A csővezeték-futtatással kapcsolatos információk.</span><span class="sxs-lookup"><span data-stu-id="04d07-123">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="04d07-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04d07-124">-PassThru</span></span>
<span data-ttu-id="04d07-125">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="04d07-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="04d07-126">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="04d07-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="04d07-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="04d07-127">-PipelineRunId</span></span>
<span data-ttu-id="04d07-128">A pipeline-Run azonosító.</span><span class="sxs-lookup"><span data-stu-id="04d07-128">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="04d07-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="04d07-129">-WorkspaceName</span></span>
<span data-ttu-id="04d07-130">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="04d07-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="04d07-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="04d07-131">-WorkspaceObject</span></span>
<span data-ttu-id="04d07-132">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="04d07-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="04d07-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04d07-133">-Confirm</span></span>
<span data-ttu-id="04d07-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04d07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d07-135">-WhatIf</span></span>
<span data-ttu-id="04d07-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04d07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d07-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04d07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d07-138">CommonParameters</span></span>
<span data-ttu-id="04d07-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04d07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d07-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="04d07-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d07-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04d07-141">INPUTS</span></span>

### <span data-ttu-id="04d07-142">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="04d07-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="04d07-143">Microsoft. Azure. commands. szinapszis. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="04d07-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="04d07-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04d07-144">OUTPUTS</span></span>

### <span data-ttu-id="04d07-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04d07-145">System.Boolean</span></span>

## <span data-ttu-id="04d07-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04d07-146">NOTES</span></span>

## <span data-ttu-id="04d07-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04d07-147">RELATED LINKS</span></span>
