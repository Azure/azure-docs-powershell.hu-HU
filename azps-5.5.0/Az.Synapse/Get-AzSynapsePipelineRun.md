---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164610"
---
# <span data-ttu-id="83a05-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="83a05-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="83a05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83a05-102">SYNOPSIS</span></span>
<span data-ttu-id="83a05-103">Információkat kap a folyamat futásának folyamatról.</span><span class="sxs-lookup"><span data-stu-id="83a05-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="83a05-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83a05-104">SYNTAX</span></span>

### <span data-ttu-id="83a05-105">GetByNameAndId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83a05-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83a05-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="83a05-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83a05-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="83a05-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83a05-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="83a05-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83a05-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83a05-109">DESCRIPTION</span></span>
<span data-ttu-id="83a05-110">A **Get-AzSynapsePipelineRun parancs** információkat ad vissza a megadott folyamat futási adatairól.</span><span class="sxs-lookup"><span data-stu-id="83a05-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="83a05-111">Ha a PipelineRunId érték meg van adva, akkor az adott azonosítóval futtatott futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="83a05-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="83a05-112">Ha a PipelineRunId nincs megadva, akkor a RunStartedAfter és a RunStartedBefore érték között lefutó folyamatok összes futásának adatait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="83a05-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="83a05-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83a05-113">EXAMPLES</span></span>

### <span data-ttu-id="83a05-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="83a05-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="83a05-115">Ez a parancs részletes információkat kap a "61eb095a-fe23-4591-8a97-fade6c65ca72" azonosítóval futtatott folyamatról.</span><span class="sxs-lookup"><span data-stu-id="83a05-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="83a05-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83a05-116">PARAMETERS</span></span>

### <span data-ttu-id="83a05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a05-117">-DefaultProfile</span></span>
<span data-ttu-id="83a05-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83a05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83a05-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="83a05-119">-PipelineName</span></span>
<span data-ttu-id="83a05-120">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="83a05-120">The pipeline name.</span></span>

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

### <span data-ttu-id="83a05-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="83a05-121">-PipelineRunId</span></span>
<span data-ttu-id="83a05-122">A folyamat futtatásának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="83a05-122">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="83a05-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="83a05-123">-RunStartedAfter</span></span>
<span data-ttu-id="83a05-124">Az az időpont, amikor vagy amely után a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="83a05-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="83a05-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="83a05-125">-RunStartedBefore</span></span>
<span data-ttu-id="83a05-126">Az az időpont, amikor vagy amely előtt a futtatás eseménye "ISO 8601" formátumban frissült.</span><span class="sxs-lookup"><span data-stu-id="83a05-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="83a05-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="83a05-127">-WorkspaceName</span></span>
<span data-ttu-id="83a05-128">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="83a05-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="83a05-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="83a05-129">-WorkspaceObject</span></span>
<span data-ttu-id="83a05-130">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="83a05-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="83a05-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a05-131">CommonParameters</span></span>
<span data-ttu-id="83a05-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83a05-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a05-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83a05-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a05-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83a05-134">INPUTS</span></span>

### <span data-ttu-id="83a05-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="83a05-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="83a05-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83a05-136">OUTPUTS</span></span>

### <span data-ttu-id="83a05-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="83a05-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="83a05-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83a05-138">NOTES</span></span>

## <span data-ttu-id="83a05-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83a05-139">RELATED LINKS</span></span>
