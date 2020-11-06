---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 6042b62bb7c641cef335834645f29d73b3d4c53a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505092"
---
# <span data-ttu-id="d6ca5-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="d6ca5-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="d6ca5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ca5-103">Információt kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6ca5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6ca5-104">SYNTAX</span></span>

### <span data-ttu-id="d6ca5-105">ByFactoryNameByRunId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6ca5-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String>
```

### <span data-ttu-id="d6ca5-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="d6ca5-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
```

### <span data-ttu-id="d6ca5-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="d6ca5-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

### <span data-ttu-id="d6ca5-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="d6ca5-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
```

## <span data-ttu-id="d6ca5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6ca5-109">DESCRIPTION</span></span>
<span data-ttu-id="d6ca5-110">A **Get-AzureRmDataFactoryV2PipelineRun** parancs a megadott csővezetéken futó futásokra vonatkozó információkat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="d6ca5-111">Ha a PipelineRunId meg van adva, az adott AZONOSÍTÓval végzett Futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="d6ca5-112">Ha a PipelineRunId nem adja meg, akkor az a LastUpdatedAfter és a LastUpdatedBefore értékek között megjelenő adott csővezetékre vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="d6ca5-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d6ca5-113">EXAMPLES</span></span>

### <span data-ttu-id="d6ca5-114">1. példa: pipline-futtatási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="d6ca5-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :

```

<span data-ttu-id="d6ca5-115">Ez a parancs részletesen ismerteti az "61eb095a-FE23-4591-8a97-fade6c65ca72" AZONOSÍTÓJÚ pipeline-kapcsolat adatait.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>


## <span data-ttu-id="d6ca5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6ca5-116">PARAMETERS</span></span>

### <span data-ttu-id="d6ca5-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6ca5-117">-DataFactory</span></span>
<span data-ttu-id="d6ca5-118">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ca5-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d6ca5-119">-DataFactoryName</span></span>
<span data-ttu-id="d6ca5-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ca5-121">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="d6ca5-121">-LastUpdatedAfter</span></span>
<span data-ttu-id="d6ca5-122">Az az időpont, amikor a csővezeték-futtatást ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-122">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ca5-123">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="d6ca5-123">-LastUpdatedBefore</span></span>
<span data-ttu-id="d6ca5-124">Az az időpont, amikor a csővezeték futását ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-124">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ca5-125">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d6ca5-125">-PipelineName</span></span>
<span data-ttu-id="d6ca5-126">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-126">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ca5-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d6ca5-127">-PipelineRunId</span></span>
<span data-ttu-id="d6ca5-128">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-128">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByRunId, ByFactoryNameByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ca5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ca5-129">-ResourceGroupName</span></span>
<span data-ttu-id="d6ca5-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6ca5-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d6ca5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ca5-131">INPUTS</span></span>

### <span data-ttu-id="d6ca5-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d6ca5-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="d6ca5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ca5-133">System.String</span></span>


## <span data-ttu-id="d6ca5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ca5-134">OUTPUTS</span></span>

### <span data-ttu-id="d6ca5-135">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d6ca5-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d6ca5-136">Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="d6ca5-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>


## <span data-ttu-id="d6ca5-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6ca5-137">NOTES</span></span>

## <span data-ttu-id="d6ca5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6ca5-138">RELATED LINKS</span></span>
[<span data-ttu-id="d6ca5-139">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d6ca5-139">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d6ca5-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="d6ca5-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

