---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 98c0f5ed1dee4c5cd25c69a1a88e596a2f99a7c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938426"
---
# <span data-ttu-id="e1806-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="e1806-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="e1806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1806-102">SYNOPSIS</span></span>
<span data-ttu-id="e1806-103">Információkat kap a prognózis-futtatásról.</span><span class="sxs-lookup"><span data-stu-id="e1806-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="e1806-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1806-104">SYNTAX</span></span>

### <span data-ttu-id="e1806-105">GetByNameAndId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1806-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1806-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="e1806-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1806-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="e1806-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1806-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="e1806-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1806-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1806-109">DESCRIPTION</span></span>
<span data-ttu-id="e1806-110">A **Get-AzSynapsePipelineRun parancs** információkat ad vissza a megadott folyamat futási adatairól.</span><span class="sxs-lookup"><span data-stu-id="e1806-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="e1806-111">Ha a PipelineRunId érték meg van adva, akkor az adott azonosítóval futtatott futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="e1806-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="e1806-112">Ha a PipelineRunId nincs megadva, akkor a RunStartedAfter és a RunStartedBefore értékek között lefutó folyamatok összes futásának adatait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="e1806-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="e1806-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1806-113">EXAMPLES</span></span>

### <span data-ttu-id="e1806-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="e1806-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="e1806-115">Ez a parancs részletes információkat kap a "61eb095a-fe23-4591-8a97-fade6c65ca72" azonosítóval futtatott folyamatról.</span><span class="sxs-lookup"><span data-stu-id="e1806-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="e1806-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1806-116">PARAMETERS</span></span>

### <span data-ttu-id="e1806-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1806-117">-DefaultProfile</span></span>
<span data-ttu-id="e1806-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1806-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1806-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="e1806-119">-PipelineName</span></span>
<span data-ttu-id="e1806-120">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="e1806-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1806-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e1806-121">-PipelineRunId</span></span>
<span data-ttu-id="e1806-122">A folyamat futtatásának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e1806-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1806-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="e1806-123">-RunStartedAfter</span></span>
<span data-ttu-id="e1806-124">Az az időpont, amikor vagy amely után a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="e1806-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1806-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="e1806-125">-RunStartedBefore</span></span>
<span data-ttu-id="e1806-126">Az az időpont, amikor vagy amely előtt a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="e1806-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1806-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e1806-127">-WorkspaceName</span></span>
<span data-ttu-id="e1806-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e1806-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1806-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e1806-129">-WorkspaceObject</span></span>
<span data-ttu-id="e1806-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1806-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1806-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1806-131">CommonParameters</span></span>
<span data-ttu-id="e1806-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1806-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1806-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1806-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1806-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1806-134">INPUTS</span></span>

### <span data-ttu-id="e1806-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e1806-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e1806-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1806-136">OUTPUTS</span></span>

### <span data-ttu-id="e1806-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="e1806-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="e1806-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1806-138">NOTES</span></span>

## <span data-ttu-id="e1806-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1806-139">RELATED LINKS</span></span>
