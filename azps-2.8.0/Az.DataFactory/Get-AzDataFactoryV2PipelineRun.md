---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 2acfb9a0ebbbaef2fee92ef521d10c1c17fa5e48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667048"
---
# <span data-ttu-id="87c16-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="87c16-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="87c16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87c16-102">SYNOPSIS</span></span>
<span data-ttu-id="87c16-103">Információt kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="87c16-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="87c16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87c16-104">SYNTAX</span></span>

### <span data-ttu-id="87c16-105">ByFactoryNameByRunId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87c16-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87c16-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="87c16-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87c16-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="87c16-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87c16-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="87c16-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87c16-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="87c16-109">DESCRIPTION</span></span>
<span data-ttu-id="87c16-110">A **Get-AzDataFactoryV2PipelineRun** parancs a megadott csővezetéken futó futásokra vonatkozó információkat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="87c16-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="87c16-111">Ha a PipelineRunId meg van adva, az adott AZONOSÍTÓval végzett Futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="87c16-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="87c16-112">Ha a PipelineRunId nem adja meg, akkor a LastUpdatedAfter és a LastUpdatedBefore értékek közötti csővezetékek esetén az összes futóról szóló információt jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="87c16-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="87c16-113">Példák</span><span class="sxs-lookup"><span data-stu-id="87c16-113">EXAMPLES</span></span>

### <span data-ttu-id="87c16-114">1. példa: adatok beszerzése csővezeték-futáshoz</span><span class="sxs-lookup"><span data-stu-id="87c16-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="87c16-115">Ez a parancs részletesen ismerteti az "61eb095a-FE23-4591-8a97-fade6c65ca72" AZONOSÍTÓJÚ pipeline-kapcsolat adatait.</span><span class="sxs-lookup"><span data-stu-id="87c16-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="87c16-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87c16-116">PARAMETERS</span></span>

### <span data-ttu-id="87c16-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="87c16-117">-DataFactory</span></span>
<span data-ttu-id="87c16-118">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="87c16-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87c16-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="87c16-119">-DataFactoryName</span></span>
<span data-ttu-id="87c16-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="87c16-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c16-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c16-121">-DefaultProfile</span></span>
<span data-ttu-id="87c16-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87c16-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c16-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="87c16-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="87c16-124">Az az időpont, amikor a csővezeték-futtatást ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="87c16-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c16-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="87c16-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="87c16-126">Az az időpont, amikor a csővezeték futását ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="87c16-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c16-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="87c16-127">-PipelineName</span></span>
<span data-ttu-id="87c16-128">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="87c16-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c16-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="87c16-129">-PipelineRunId</span></span>
<span data-ttu-id="87c16-130">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87c16-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c16-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c16-131">-ResourceGroupName</span></span>
<span data-ttu-id="87c16-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="87c16-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c16-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c16-133">CommonParameters</span></span>
<span data-ttu-id="87c16-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87c16-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c16-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c16-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c16-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87c16-136">INPUTS</span></span>

### <span data-ttu-id="87c16-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="87c16-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="87c16-138">System. String</span><span class="sxs-lookup"><span data-stu-id="87c16-138">System.String</span></span>

## <span data-ttu-id="87c16-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87c16-139">OUTPUTS</span></span>

### <span data-ttu-id="87c16-140">Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="87c16-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="87c16-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87c16-141">NOTES</span></span>

## <span data-ttu-id="87c16-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87c16-142">RELATED LINKS</span></span>

[<span data-ttu-id="87c16-143">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="87c16-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="87c16-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="87c16-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

