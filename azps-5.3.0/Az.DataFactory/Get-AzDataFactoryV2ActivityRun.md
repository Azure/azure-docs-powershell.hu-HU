---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477173"
---
# <span data-ttu-id="f4c46-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="f4c46-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="f4c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4c46-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c46-103">Információkat kap a folyamatok futtatásához futtatott tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="f4c46-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="f4c46-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4c46-104">SYNTAX</span></span>

### <span data-ttu-id="f4c46-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4c46-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4c46-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f4c46-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4c46-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4c46-107">DESCRIPTION</span></span>
<span data-ttu-id="f4c46-108">A **Get-AzDataFactoryV2ActivityRun** parancsmag információt kap az Azure Data Factoryban a megadott, a megadott időkereten belül lefutott folyamat futtatásáról.</span><span class="sxs-lookup"><span data-stu-id="f4c46-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="f4c46-109">Emellett megadhat szűrőket a tevékenységnévhez, a futtatás végrehajtása során hivatkozott szolgáltatásnévhez és a futtatás állapotához.</span><span class="sxs-lookup"><span data-stu-id="f4c46-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="f4c46-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4c46-110">EXAMPLES</span></span>

### <span data-ttu-id="f4c46-111">1. példa: Az összes tevékenység futtatása egy folyamat futtatásához</span><span class="sxs-lookup"><span data-stu-id="f4c46-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="f4c46-112">Ez a parancs részletes információkat kap az "f288712d-fb08-4cb8-96ef-82d3b9b30621" azonosítóval futtatott folyamatban futó összes olyan tevékenységről, amely a "2017-09-01" és a "2017-09-30" azonosító között történt.</span><span class="sxs-lookup"><span data-stu-id="f4c46-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="f4c46-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4c46-113">PARAMETERS</span></span>

### <span data-ttu-id="f4c46-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="f4c46-114">-ActivityName</span></span>
<span data-ttu-id="f4c46-115">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="f4c46-115">The name of the activity.</span></span>

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

### <span data-ttu-id="f4c46-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4c46-116">-DataFactory</span></span>
<span data-ttu-id="f4c46-117">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="f4c46-117">The data factory object.</span></span>

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

### <span data-ttu-id="f4c46-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f4c46-118">-DataFactoryName</span></span>
<span data-ttu-id="f4c46-119">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="f4c46-119">The data factory name.</span></span>

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

### <span data-ttu-id="f4c46-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c46-120">-DefaultProfile</span></span>
<span data-ttu-id="f4c46-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4c46-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4c46-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="f4c46-122">-PipelineRunId</span></span>
<span data-ttu-id="f4c46-123">A folyamat futtatásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4c46-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="f4c46-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c46-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4c46-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4c46-125">The resource group name.</span></span>

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

### <span data-ttu-id="f4c46-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="f4c46-126">-RunStartedAfter</span></span>
<span data-ttu-id="f4c46-127">Az az időpont, amikor vagy azt követően elindul a folyamat végrehajtása.</span><span class="sxs-lookup"><span data-stu-id="f4c46-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="f4c46-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="f4c46-128">-RunStartedBefore</span></span>
<span data-ttu-id="f4c46-129">Az az időpont, amikor vagy amely előtt a folyamat elindul.</span><span class="sxs-lookup"><span data-stu-id="f4c46-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="f4c46-130">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f4c46-130">-Status</span></span>
<span data-ttu-id="f4c46-131">A folyamat állapota fut.</span><span class="sxs-lookup"><span data-stu-id="f4c46-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="f4c46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c46-132">CommonParameters</span></span>
<span data-ttu-id="f4c46-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c46-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c46-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c46-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4c46-135">INPUTS</span></span>

### <span data-ttu-id="f4c46-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f4c46-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="f4c46-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f4c46-137">System.String</span></span>

## <span data-ttu-id="f4c46-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4c46-138">OUTPUTS</span></span>

### <span data-ttu-id="f4c46-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="f4c46-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="f4c46-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4c46-140">NOTES</span></span>

## <span data-ttu-id="f4c46-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4c46-141">RELATED LINKS</span></span>

[<span data-ttu-id="f4c46-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f4c46-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f4c46-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f4c46-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

