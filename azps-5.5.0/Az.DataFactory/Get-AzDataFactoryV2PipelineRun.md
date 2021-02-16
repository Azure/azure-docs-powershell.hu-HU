---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166098"
---
# <span data-ttu-id="0e645-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="0e645-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="0e645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e645-102">SYNOPSIS</span></span>
<span data-ttu-id="0e645-103">Információkat kap a prognózis-futtatásról.</span><span class="sxs-lookup"><span data-stu-id="0e645-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="0e645-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e645-104">SYNTAX</span></span>

### <span data-ttu-id="0e645-105">ByFactoryNameByRunId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e645-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e645-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="0e645-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e645-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="0e645-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e645-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="0e645-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e645-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e645-109">DESCRIPTION</span></span>
<span data-ttu-id="0e645-110">A **Get-AzDataFactoryV2PipelineRun** parancs információt ad a megadott folyamat futási adatairól.</span><span class="sxs-lookup"><span data-stu-id="0e645-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="0e645-111">Ha a PipelineRunId érték meg van adva, akkor az adott azonosítóval futtatott futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0e645-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="0e645-112">Ha a PipelineRunId nincs megadva, akkor a LastUpdatedAfter és az LastUpdatedBefore érték között lefutó folyamatok összes futásának adatait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="0e645-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="0e645-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e645-113">EXAMPLES</span></span>

### <span data-ttu-id="0e645-114">1. példa: Információ lekérte egy folyamat futtatásáról</span><span class="sxs-lookup"><span data-stu-id="0e645-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="0e645-115">Ez a parancs részletes információkat kap a "61eb095a-fe23-4591-8a97-fade6c65ca72" azonosítóval futtatott folyamatról.</span><span class="sxs-lookup"><span data-stu-id="0e645-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="0e645-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e645-116">PARAMETERS</span></span>

### <span data-ttu-id="0e645-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e645-117">-DataFactory</span></span>
<span data-ttu-id="0e645-118">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="0e645-118">The data factory object.</span></span>

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

### <span data-ttu-id="0e645-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0e645-119">-DataFactoryName</span></span>
<span data-ttu-id="0e645-120">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="0e645-120">The data factory name.</span></span>

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

### <span data-ttu-id="0e645-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e645-121">-DefaultProfile</span></span>
<span data-ttu-id="0e645-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e645-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e645-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="0e645-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="0e645-124">A folyamat futtatásának ideje ISO8601 formátumban frissítve.</span><span class="sxs-lookup"><span data-stu-id="0e645-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="0e645-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="0e645-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="0e645-126">A folyamat futtatásának ideje ISO8601 formátumban frissítve.</span><span class="sxs-lookup"><span data-stu-id="0e645-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="0e645-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="0e645-127">-PipelineName</span></span>
<span data-ttu-id="0e645-128">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="0e645-128">The pipeline name.</span></span>

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

### <span data-ttu-id="0e645-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="0e645-129">-PipelineRunId</span></span>
<span data-ttu-id="0e645-130">A folyamat futtatásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="0e645-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="0e645-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e645-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e645-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e645-132">The resource group name.</span></span>

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

### <span data-ttu-id="0e645-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e645-133">CommonParameters</span></span>
<span data-ttu-id="0e645-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e645-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e645-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e645-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e645-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e645-136">INPUTS</span></span>

### <span data-ttu-id="0e645-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0e645-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="0e645-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0e645-138">System.String</span></span>

## <span data-ttu-id="0e645-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e645-139">OUTPUTS</span></span>

### <span data-ttu-id="0e645-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="0e645-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="0e645-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e645-141">NOTES</span></span>

## <span data-ttu-id="0e645-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e645-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e645-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e645-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0e645-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="0e645-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

