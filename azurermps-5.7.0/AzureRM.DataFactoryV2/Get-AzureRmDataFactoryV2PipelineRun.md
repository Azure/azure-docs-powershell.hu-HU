---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503800"
---
# <span data-ttu-id="3ecfb-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="3ecfb-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="3ecfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ecfb-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecfb-103">Információt kap a csővezetékről.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ecfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ecfb-104">SYNTAX</span></span>

### <span data-ttu-id="3ecfb-105">ByFactoryNameByRunId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ecfb-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ecfb-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="3ecfb-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ecfb-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="3ecfb-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ecfb-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="3ecfb-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ecfb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ecfb-109">DESCRIPTION</span></span>
<span data-ttu-id="3ecfb-110">A **Get-AzureRmDataFactoryV2PipelineRun** parancs a megadott csővezetéken futó futásokra vonatkozó információkat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="3ecfb-111">Ha a PipelineRunId meg van adva, az adott AZONOSÍTÓval végzett Futtatás részleteit jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="3ecfb-112">Ha a PipelineRunId nem adja meg, akkor az a LastUpdatedAfter és a LastUpdatedBefore értékek között megjelenő adott csővezetékre vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="3ecfb-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3ecfb-113">EXAMPLES</span></span>

### <span data-ttu-id="3ecfb-114">1. példa: pipline-futtatási adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ecfb-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="3ecfb-115">Ez a parancs részletesen ismerteti az "61eb095a-FE23-4591-8a97-fade6c65ca72" AZONOSÍTÓJÚ pipeline-kapcsolat adatait.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="3ecfb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ecfb-116">PARAMETERS</span></span>

### <span data-ttu-id="3ecfb-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ecfb-117">-DataFactory</span></span>
<span data-ttu-id="3ecfb-118">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-118">The data factory object.</span></span>

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

### <span data-ttu-id="3ecfb-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3ecfb-119">-DataFactoryName</span></span>
<span data-ttu-id="3ecfb-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-120">The data factory name.</span></span>

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

### <span data-ttu-id="3ecfb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecfb-121">-DefaultProfile</span></span>
<span data-ttu-id="3ecfb-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecfb-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="3ecfb-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="3ecfb-124">Az az időpont, amikor a csővezeték-futtatást ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="3ecfb-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="3ecfb-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="3ecfb-126">Az az időpont, amikor a csővezeték futását ISO8601 formátumban frissítették.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="3ecfb-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="3ecfb-127">-PipelineName</span></span>
<span data-ttu-id="3ecfb-128">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-128">The pipeline name.</span></span>

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

### <span data-ttu-id="3ecfb-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="3ecfb-129">-PipelineRunId</span></span>
<span data-ttu-id="3ecfb-130">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ecfb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ecfb-131">-ResourceGroupName</span></span>
<span data-ttu-id="3ecfb-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ecfb-132">The resource group name.</span></span>

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

### <span data-ttu-id="3ecfb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecfb-133">CommonParameters</span></span>
<span data-ttu-id="3ecfb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ecfb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecfb-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecfb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecfb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ecfb-136">INPUTS</span></span>

### <span data-ttu-id="3ecfb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3ecfb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="3ecfb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3ecfb-138">System.String</span></span>

## <span data-ttu-id="3ecfb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ecfb-139">OUTPUTS</span></span>

### <span data-ttu-id="3ecfb-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3ecfb-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="3ecfb-141">Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="3ecfb-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="3ecfb-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ecfb-142">NOTES</span></span>

## <span data-ttu-id="3ecfb-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ecfb-143">RELATED LINKS</span></span>

[<span data-ttu-id="3ecfb-144">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="3ecfb-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="3ecfb-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="3ecfb-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

