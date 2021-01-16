---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339282"
---
# <span data-ttu-id="78c59-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="78c59-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="78c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78c59-102">SYNOPSIS</span></span>
<span data-ttu-id="78c59-103">Információkat kap a folyamatok futtatásához futtatott tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="78c59-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="78c59-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78c59-104">SYNTAX</span></span>

### <span data-ttu-id="78c59-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78c59-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c59-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="78c59-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c59-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78c59-107">DESCRIPTION</span></span>
<span data-ttu-id="78c59-108">A **Get-AzSynapseActivityRun** parancsmag információt kap a munkaterületen való futtatásról a megadott időkereten belül lefutott folyamathoz.</span><span class="sxs-lookup"><span data-stu-id="78c59-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="78c59-109">Emellett szűrőket is megadhat a tevékenység nevéhez és a futtatás állapotához.</span><span class="sxs-lookup"><span data-stu-id="78c59-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="78c59-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78c59-110">EXAMPLES</span></span>

### <span data-ttu-id="78c59-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="78c59-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="78c59-112">Ez a parancs részletes információkat kap a ContosoPipeline run nevű folyamatban futó összes olyan tevékenységről, amely "f288712d-fb08-4cb8-96ef-82d3b9b30621" azonosítóval fut, amely a "2018-09-09-01T21:00" és a "2018-09-30T21:00" között történt.</span><span class="sxs-lookup"><span data-stu-id="78c59-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="78c59-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="78c59-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="78c59-114">Ez a parancs részletes információkat kap az "f288712d-fb08-4cb8-96ef-82d3b9b306" azonosítójú ContosoPipeline-futtatás folyamatában futó összes tevékenységről. "21", amely a "2018-09-09-01T21:00" és a "2018-09-30T21:00" között történt a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="78c59-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="78c59-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78c59-115">PARAMETERS</span></span>

### <span data-ttu-id="78c59-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="78c59-116">-ActivityName</span></span>
<span data-ttu-id="78c59-117">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="78c59-117">The name of the activity.</span></span>

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

### <span data-ttu-id="78c59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c59-118">-DefaultProfile</span></span>
<span data-ttu-id="78c59-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78c59-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78c59-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="78c59-120">-PipelineName</span></span>
<span data-ttu-id="78c59-121">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="78c59-121">The pipeline name.</span></span>

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

### <span data-ttu-id="78c59-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="78c59-122">-PipelineRunId</span></span>
<span data-ttu-id="78c59-123">A folyamat futtatásának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="78c59-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="78c59-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="78c59-124">-RunStartedAfter</span></span>
<span data-ttu-id="78c59-125">Az az időpont, amikor vagy amely után a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="78c59-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c59-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="78c59-126">-RunStartedBefore</span></span>
<span data-ttu-id="78c59-127">Az az időpont, amikor vagy amely előtt a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="78c59-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c59-128">-Állapot</span><span class="sxs-lookup"><span data-stu-id="78c59-128">-Status</span></span>
<span data-ttu-id="78c59-129">A folyamat állapota fut.</span><span class="sxs-lookup"><span data-stu-id="78c59-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="78c59-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78c59-130">-WorkspaceName</span></span>
<span data-ttu-id="78c59-131">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="78c59-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c59-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="78c59-132">-WorkspaceObject</span></span>
<span data-ttu-id="78c59-133">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="78c59-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78c59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c59-134">CommonParameters</span></span>
<span data-ttu-id="78c59-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c59-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78c59-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c59-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78c59-137">INPUTS</span></span>

### <span data-ttu-id="78c59-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78c59-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="78c59-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78c59-139">OUTPUTS</span></span>

### <span data-ttu-id="78c59-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="78c59-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="78c59-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78c59-141">NOTES</span></span>

## <span data-ttu-id="78c59-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78c59-142">RELATED LINKS</span></span>
