---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181233"
---
# <span data-ttu-id="770de-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="770de-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="770de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="770de-102">SYNOPSIS</span></span>
<span data-ttu-id="770de-103">A tevékenységekről szóló információkat a csővezeték-futás során futtatja.</span><span class="sxs-lookup"><span data-stu-id="770de-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="770de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="770de-104">SYNTAX</span></span>

### <span data-ttu-id="770de-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="770de-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770de-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="770de-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770de-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="770de-107">DESCRIPTION</span></span>
<span data-ttu-id="770de-108">A **Get-AzSynapseActivityRun** parancsmag a megadott időkeretben megjelenő, a munkaterületen futtatott folyamatokról tartalmaz információkat.</span><span class="sxs-lookup"><span data-stu-id="770de-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="770de-109">Ezenkívül megadhat szűrőket a tevékenység nevéhez és a futás állapotát.</span><span class="sxs-lookup"><span data-stu-id="770de-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="770de-110">Példák</span><span class="sxs-lookup"><span data-stu-id="770de-110">EXAMPLES</span></span>

### <span data-ttu-id="770de-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="770de-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="770de-112">Ez a parancs részletesen ismerteti az összes tevékenységről a "f288712d-fb08-4cb8-96ef-82d3b9b30621" nevű ContosoPipeline-as verzióval, a "2018-09-01T21:00" és a "2018-09-30T21:00" AZONOSÍTÓJÚ adatcsatornán.</span><span class="sxs-lookup"><span data-stu-id="770de-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="770de-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="770de-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="770de-114">Ez a parancs részletesen ismerteti az összes tevékenységről az "f288712d-fb08-4cb8-96ef-82d3b9b30621" nevű ContosoPipeline-as verzióban a "2018-09-01T21:00" és a "2018-09-30T21:00" közötti távolságot a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="770de-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="770de-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="770de-115">PARAMETERS</span></span>

### <span data-ttu-id="770de-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="770de-116">-ActivityName</span></span>
<span data-ttu-id="770de-117">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="770de-117">The name of the activity.</span></span>

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

### <span data-ttu-id="770de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770de-118">-DefaultProfile</span></span>
<span data-ttu-id="770de-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="770de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770de-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="770de-120">-PipelineName</span></span>
<span data-ttu-id="770de-121">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="770de-121">The pipeline name.</span></span>

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

### <span data-ttu-id="770de-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="770de-122">-PipelineRunId</span></span>
<span data-ttu-id="770de-123">A pipeline-Run azonosító.</span><span class="sxs-lookup"><span data-stu-id="770de-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="770de-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="770de-124">-RunStartedAfter</span></span>
<span data-ttu-id="770de-125">A futási esemény "ISO 8601" formátumban való frissítésének időpontja.</span><span class="sxs-lookup"><span data-stu-id="770de-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="770de-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="770de-126">-RunStartedBefore</span></span>
<span data-ttu-id="770de-127">A futási esemény "ISO 8601" formátumban való frissítésének időpontja.</span><span class="sxs-lookup"><span data-stu-id="770de-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="770de-128">-Állapot</span><span class="sxs-lookup"><span data-stu-id="770de-128">-Status</span></span>
<span data-ttu-id="770de-129">A csővezeték-futás állapota.</span><span class="sxs-lookup"><span data-stu-id="770de-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="770de-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="770de-130">-WorkspaceName</span></span>
<span data-ttu-id="770de-131">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="770de-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="770de-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="770de-132">-WorkspaceObject</span></span>
<span data-ttu-id="770de-133">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="770de-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="770de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770de-134">CommonParameters</span></span>
<span data-ttu-id="770de-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="770de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770de-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="770de-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770de-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="770de-137">INPUTS</span></span>

### <span data-ttu-id="770de-138">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="770de-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="770de-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="770de-139">OUTPUTS</span></span>

### <span data-ttu-id="770de-140">Microsoft. Azure. commands. szinapszis. models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="770de-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="770de-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="770de-141">NOTES</span></span>

## <span data-ttu-id="770de-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="770de-142">RELATED LINKS</span></span>
