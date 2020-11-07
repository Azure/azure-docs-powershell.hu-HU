---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: 5f6c56fac892e2c3e9c1546dac226c5d81ddb99e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667068"
---
# <span data-ttu-id="8b83f-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="8b83f-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="8b83f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b83f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b83f-103">A tevékenységekről szóló információkat a csővezeték-futás során futtatja.</span><span class="sxs-lookup"><span data-stu-id="8b83f-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="8b83f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b83f-104">SYNTAX</span></span>

### <span data-ttu-id="8b83f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b83f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b83f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8b83f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b83f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b83f-107">DESCRIPTION</span></span>
<span data-ttu-id="8b83f-108">A **Get-AzDataFactoryV2ActivityRun** parancsmag információkat kap az Azure Data Factory alkalmazásban az adott időkeretben történt futásról.</span><span class="sxs-lookup"><span data-stu-id="8b83f-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="8b83f-109">Ezenkívül megadhat szűrőket a tevékenység nevéhez, a futtatott szolgáltatás nevéhez, valamint a futás állapotát.</span><span class="sxs-lookup"><span data-stu-id="8b83f-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="8b83f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8b83f-110">EXAMPLES</span></span>

### <span data-ttu-id="8b83f-111">Példa 1: az összes tevékenység futása folyamatban</span><span class="sxs-lookup"><span data-stu-id="8b83f-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="8b83f-112">Ez a parancs a "2017-09-01" és a "2017-09-30" között megjelenő "f288712d-fb08-4cb8-96ef-82d3b9b30621" azonosítójú "" azonosítójú folyamaton futó minden tevékenységről részletes információt kap.</span><span class="sxs-lookup"><span data-stu-id="8b83f-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="8b83f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b83f-113">PARAMETERS</span></span>

### <span data-ttu-id="8b83f-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="8b83f-114">-ActivityName</span></span>
<span data-ttu-id="8b83f-115">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="8b83f-115">The name of the activity.</span></span>

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

### <span data-ttu-id="8b83f-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8b83f-116">-DataFactory</span></span>
<span data-ttu-id="8b83f-117">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="8b83f-117">The data factory object.</span></span>

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

### <span data-ttu-id="8b83f-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8b83f-118">-DataFactoryName</span></span>
<span data-ttu-id="8b83f-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="8b83f-119">The data factory name.</span></span>

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

### <span data-ttu-id="8b83f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b83f-120">-DefaultProfile</span></span>
<span data-ttu-id="8b83f-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b83f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b83f-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="8b83f-122">-PipelineRunId</span></span>
<span data-ttu-id="8b83f-123">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8b83f-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="8b83f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b83f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8b83f-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8b83f-125">The resource group name.</span></span>

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

### <span data-ttu-id="8b83f-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="8b83f-126">-RunStartedAfter</span></span>
<span data-ttu-id="8b83f-127">Az az időpont, amikor a pipeline futása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="8b83f-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="8b83f-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="8b83f-128">-RunStartedBefore</span></span>
<span data-ttu-id="8b83f-129">Az az időpont, amikor a csővezeték futása folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="8b83f-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="8b83f-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="8b83f-130">-Status</span></span>
<span data-ttu-id="8b83f-131">A csővezeték-futás állapota.</span><span class="sxs-lookup"><span data-stu-id="8b83f-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="8b83f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b83f-132">CommonParameters</span></span>
<span data-ttu-id="8b83f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b83f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b83f-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b83f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b83f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b83f-135">INPUTS</span></span>

### <span data-ttu-id="8b83f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8b83f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="8b83f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8b83f-137">System.String</span></span>

## <span data-ttu-id="8b83f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b83f-138">OUTPUTS</span></span>

### <span data-ttu-id="8b83f-139">Microsoft. Azure. Command. DataFactoryV2. models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="8b83f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="8b83f-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b83f-140">NOTES</span></span>

## <span data-ttu-id="8b83f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b83f-141">RELATED LINKS</span></span>

[<span data-ttu-id="8b83f-142">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b83f-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="8b83f-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8b83f-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

