---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 300aad37f2dede64a4adebc4f1a9d9eb9cc43743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493151"
---
# <span data-ttu-id="c4a97-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="c4a97-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="c4a97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4a97-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a97-103">A tevékenységekről szóló információkat a csővezeték-futás során futtatja.</span><span class="sxs-lookup"><span data-stu-id="c4a97-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4a97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4a97-104">SYNTAX</span></span>

### <span data-ttu-id="c4a97-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4a97-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4a97-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c4a97-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4a97-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4a97-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a97-108">A **Get-AzureRmDataFactoryV2ActivityRun** parancsmag információkat kap az Azure Data Factory alkalmazásban az adott időkeretben történt futásról.</span><span class="sxs-lookup"><span data-stu-id="c4a97-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="c4a97-109">Ezenkívül megadhat szűrőket a tevékenység nevéhez, a futtatott szolgáltatás nevéhez, valamint a futás állapotát.</span><span class="sxs-lookup"><span data-stu-id="c4a97-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="c4a97-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c4a97-110">EXAMPLES</span></span>

### <span data-ttu-id="c4a97-111">Példa 1: az összes tevékenység futása folyamatban</span><span class="sxs-lookup"><span data-stu-id="c4a97-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="c4a97-112">Ez a parancs a "2017-09-01" és a "2017-09-30" között megjelenő "f288712d-fb08-4cb8-96ef-82d3b9b30621" azonosítójú "" azonosítójú folyamaton futó minden tevékenységről részletes információt kap.</span><span class="sxs-lookup"><span data-stu-id="c4a97-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="c4a97-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4a97-113">PARAMETERS</span></span>

### <span data-ttu-id="c4a97-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="c4a97-114">-ActivityName</span></span>
<span data-ttu-id="c4a97-115">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="c4a97-115">The name of the activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c4a97-116">-DataFactory</span></span>
<span data-ttu-id="c4a97-117">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="c4a97-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c4a97-118">-DataFactoryName</span></span>
<span data-ttu-id="c4a97-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c4a97-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a97-120">-DefaultProfile</span></span>
<span data-ttu-id="c4a97-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4a97-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4a97-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c4a97-122">-LinkedServiceName</span></span>
<span data-ttu-id="c4a97-123">A kapcsolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="c4a97-123">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c4a97-124">-PipelineRunId</span></span>
<span data-ttu-id="c4a97-125">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4a97-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a97-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4a97-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4a97-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c4a97-128">-RunStartedAfter</span></span>
<span data-ttu-id="c4a97-129">Az az időpont, amikor a pipeline futása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="c4a97-129">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c4a97-130">-RunStartedBefore</span></span>
<span data-ttu-id="c4a97-131">Az az időpont, amikor a csővezeték futása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="c4a97-131">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-132">-Állapot</span><span class="sxs-lookup"><span data-stu-id="c4a97-132">-Status</span></span>
<span data-ttu-id="c4a97-133">A csővezeték-futás állapota.</span><span class="sxs-lookup"><span data-stu-id="c4a97-133">The status of the pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a97-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a97-134">CommonParameters</span></span>
<span data-ttu-id="c4a97-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4a97-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a97-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a97-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a97-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4a97-137">INPUTS</span></span>

### <span data-ttu-id="c4a97-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c4a97-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="c4a97-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4a97-139">System.String</span></span>

## <span data-ttu-id="c4a97-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4a97-140">OUTPUTS</span></span>

### <span data-ttu-id="c4a97-141">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSActivityRun, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c4a97-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c4a97-142">Microsoft. Azure. Command. DataFactoryV2. models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="c4a97-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="c4a97-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4a97-143">NOTES</span></span>

## <span data-ttu-id="c4a97-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4a97-144">RELATED LINKS</span></span>

[<span data-ttu-id="c4a97-145">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c4a97-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c4a97-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="c4a97-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

