---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 4bfebac1d37dbdc0cac2bc8262993a6c81b0c9ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496272"
---
# <span data-ttu-id="3071a-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="3071a-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="3071a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3071a-102">SYNOPSIS</span></span>
<span data-ttu-id="3071a-103">A tevékenységekről szóló információkat a csővezeték-futás során futtatja.</span><span class="sxs-lookup"><span data-stu-id="3071a-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3071a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3071a-104">SYNTAX</span></span>

### <span data-ttu-id="3071a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3071a-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3071a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3071a-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3071a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3071a-107">DESCRIPTION</span></span>
<span data-ttu-id="3071a-108">A **Get-AzureRmDataFactoryV2ActivityRun** parancsmag információkat kap az Azure Data Factory alkalmazásban az adott időkeretben történt futásról.</span><span class="sxs-lookup"><span data-stu-id="3071a-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="3071a-109">Ezenkívül megadhat szűrőket a tevékenység nevéhez, a futtatott szolgáltatás nevéhez, valamint a futás állapotát.</span><span class="sxs-lookup"><span data-stu-id="3071a-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="3071a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3071a-110">EXAMPLES</span></span>

### <span data-ttu-id="3071a-111">Példa 1: az összes tevékenység futása folyamatban</span><span class="sxs-lookup"><span data-stu-id="3071a-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="3071a-112">Ez a parancs a "2017-09-01" és a "2017-09-30" között megjelenő "f288712d-fb08-4cb8-96ef-82d3b9b30621" azonosítójú "" azonosítójú folyamaton futó minden tevékenységről részletes információt kap.</span><span class="sxs-lookup"><span data-stu-id="3071a-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="3071a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3071a-113">PARAMETERS</span></span>

### <span data-ttu-id="3071a-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="3071a-114">-ActivityName</span></span>
<span data-ttu-id="3071a-115">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="3071a-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3071a-116">-DataFactory</span></span>
<span data-ttu-id="3071a-117">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="3071a-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3071a-118">-DataFactoryName</span></span>
<span data-ttu-id="3071a-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="3071a-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3071a-120">-DefaultProfile</span></span>
<span data-ttu-id="3071a-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3071a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3071a-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="3071a-122">-LinkedServiceName</span></span>
<span data-ttu-id="3071a-123">A kapcsolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3071a-123">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="3071a-124">-PipelineRunId</span></span>
<span data-ttu-id="3071a-125">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3071a-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3071a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3071a-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3071a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="3071a-128">-RunStartedAfter</span></span>
<span data-ttu-id="3071a-129">Az az időpont, amikor a pipeline futása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="3071a-129">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="3071a-130">-RunStartedBefore</span></span>
<span data-ttu-id="3071a-131">Az az időpont, amikor a csővezeték futása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="3071a-131">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-132">-Állapot</span><span class="sxs-lookup"><span data-stu-id="3071a-132">-Status</span></span>
<span data-ttu-id="3071a-133">A csővezeték-futás állapota.</span><span class="sxs-lookup"><span data-stu-id="3071a-133">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3071a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3071a-134">CommonParameters</span></span>
<span data-ttu-id="3071a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3071a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3071a-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3071a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3071a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3071a-137">INPUTS</span></span>

### <span data-ttu-id="3071a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3071a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="3071a-139">Paraméterek: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3071a-139">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="3071a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3071a-140">System.String</span></span>

## <span data-ttu-id="3071a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3071a-141">OUTPUTS</span></span>

### <span data-ttu-id="3071a-142">Microsoft. Azure. Command. DataFactoryV2. models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="3071a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="3071a-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3071a-143">NOTES</span></span>

## <span data-ttu-id="3071a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3071a-144">RELATED LINKS</span></span>

[<span data-ttu-id="3071a-145">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="3071a-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="3071a-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="3071a-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

