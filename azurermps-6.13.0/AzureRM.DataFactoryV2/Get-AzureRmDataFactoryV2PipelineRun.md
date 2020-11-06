---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: ac5735d66a7b44c7183a9af3a32c01445f2b3486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499620"
---
# <span data-ttu-id="2f7ae-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2f7ae-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="2f7ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7ae-103">Információt kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f7ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f7ae-104">SYNTAX</span></span>

### <span data-ttu-id="2f7ae-105">ByFactoryNameByRunId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f7ae-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f7ae-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="2f7ae-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f7ae-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="2f7ae-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f7ae-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="2f7ae-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f7ae-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f7ae-109">DESCRIPTION</span></span>
<span data-ttu-id="2f7ae-110">A **Get-AzureRmDataFactoryV2PipelineRun** parancs a megadott csővezetéken futó futásokra vonatkozó információkat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="2f7ae-111">Ha a PipelineRunId meg van adva, az adott AZONOSÍTÓval végzett Futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="2f7ae-112">Ha a PipelineRunId nem adja meg, akkor az a LastUpdatedAfter és a LastUpdatedBefore értékek között megjelenő adott csővezetékre vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="2f7ae-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2f7ae-113">EXAMPLES</span></span>

### <span data-ttu-id="2f7ae-114">1. példa: pipline-futtatási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f7ae-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="2f7ae-115">Ez a parancs részletesen ismerteti az "61eb095a-FE23-4591-8a97-fade6c65ca72" AZONOSÍTÓJÚ pipeline-kapcsolat adatait.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="2f7ae-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f7ae-116">PARAMETERS</span></span>

### <span data-ttu-id="2f7ae-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2f7ae-117">-DataFactory</span></span>
<span data-ttu-id="2f7ae-118">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-118">The data factory object.</span></span>

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

### <span data-ttu-id="2f7ae-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2f7ae-119">-DataFactoryName</span></span>
<span data-ttu-id="2f7ae-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-120">The data factory name.</span></span>

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

### <span data-ttu-id="2f7ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7ae-121">-DefaultProfile</span></span>
<span data-ttu-id="2f7ae-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7ae-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="2f7ae-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="2f7ae-124">Az az időpont, amikor a csővezeték-futtatást ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="2f7ae-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="2f7ae-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="2f7ae-126">Az az időpont, amikor a csővezeték futását ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="2f7ae-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="2f7ae-127">-PipelineName</span></span>
<span data-ttu-id="2f7ae-128">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-128">The pipeline name.</span></span>

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

### <span data-ttu-id="2f7ae-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="2f7ae-129">-PipelineRunId</span></span>
<span data-ttu-id="2f7ae-130">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="2f7ae-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f7ae-131">-ResourceGroupName</span></span>
<span data-ttu-id="2f7ae-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2f7ae-132">The resource group name.</span></span>

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

### <span data-ttu-id="2f7ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7ae-133">CommonParameters</span></span>
<span data-ttu-id="2f7ae-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f7ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7ae-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f7ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7ae-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f7ae-136">INPUTS</span></span>

### <span data-ttu-id="2f7ae-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2f7ae-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="2f7ae-138">Paraméterek: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f7ae-138">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="2f7ae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2f7ae-139">System.String</span></span>

## <span data-ttu-id="2f7ae-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f7ae-140">OUTPUTS</span></span>

### <span data-ttu-id="2f7ae-141">Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="2f7ae-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="2f7ae-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f7ae-142">NOTES</span></span>

## <span data-ttu-id="2f7ae-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f7ae-143">RELATED LINKS</span></span>

[<span data-ttu-id="2f7ae-144">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="2f7ae-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="2f7ae-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="2f7ae-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

