---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: ba9ea38f5915f5a89326c806e11a055ec6aeed75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930177"
---
# <span data-ttu-id="58254-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="58254-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="58254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58254-102">SYNOPSIS</span></span>
<span data-ttu-id="58254-103">Információkat ad vissza az eseményindítók futásról.</span><span class="sxs-lookup"><span data-stu-id="58254-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="58254-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58254-104">SYNTAX</span></span>

### <span data-ttu-id="58254-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58254-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58254-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="58254-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58254-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58254-107">DESCRIPTION</span></span>
<span data-ttu-id="58254-108">A **Get-AzDataFactoryV2TriggerRun** parancs részletes információkat ad vissza arról, hogy az eseményindító a megadott eseményindítóhoz fut-e a megadott időkeretben.</span><span class="sxs-lookup"><span data-stu-id="58254-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="58254-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58254-109">EXAMPLES</span></span>

### <span data-ttu-id="58254-110">1. példa: Információk az eseményindító futtatásáról</span><span class="sxs-lookup"><span data-stu-id="58254-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="58254-111">Ez a parancs információkat tartalmaz a "WikiTrigger" futásról a "WikiADF" factoryban, amely a "2017-09-01" és a "2019-09-30" között kezdődött.</span><span class="sxs-lookup"><span data-stu-id="58254-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="58254-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58254-112">PARAMETERS</span></span>

### <span data-ttu-id="58254-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="58254-113">-DataFactory</span></span>
<span data-ttu-id="58254-114">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="58254-114">The data factory object.</span></span>

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

### <span data-ttu-id="58254-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58254-115">-DataFactoryName</span></span>
<span data-ttu-id="58254-116">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="58254-116">The data factory name.</span></span>

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

### <span data-ttu-id="58254-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58254-117">-DefaultProfile</span></span>
<span data-ttu-id="58254-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58254-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58254-119">-Name</span><span class="sxs-lookup"><span data-stu-id="58254-119">-Name</span></span>
<span data-ttu-id="58254-120">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="58254-120">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58254-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58254-121">-ResourceGroupName</span></span>
<span data-ttu-id="58254-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="58254-122">The resource group name.</span></span>

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

### <span data-ttu-id="58254-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="58254-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="58254-124">Az az időpont, amikor vagy azt követően a trigger elkezdődött ISO8601 formátumban.</span><span class="sxs-lookup"><span data-stu-id="58254-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="58254-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="58254-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="58254-126">Az az időpont, amikor vagy azt megelőzően elindul az eseményindító ISO8601 formátumban.</span><span class="sxs-lookup"><span data-stu-id="58254-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58254-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58254-127">CommonParameters</span></span>
<span data-ttu-id="58254-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58254-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58254-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58254-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58254-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58254-130">INPUTS</span></span>

### <span data-ttu-id="58254-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="58254-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="58254-132">System.String</span><span class="sxs-lookup"><span data-stu-id="58254-132">System.String</span></span>

## <span data-ttu-id="58254-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58254-133">OUTPUTS</span></span>

### <span data-ttu-id="58254-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="58254-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="58254-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58254-135">NOTES</span></span>

## <span data-ttu-id="58254-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58254-136">RELATED LINKS</span></span>

[<span data-ttu-id="58254-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="58254-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="58254-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="58254-138">Stop-AzDataFactoryV2Trigger</span></span>]()

