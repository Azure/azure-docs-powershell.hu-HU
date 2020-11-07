---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679785"
---
# <span data-ttu-id="8047f-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="8047f-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="8047f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8047f-102">SYNOPSIS</span></span>
<span data-ttu-id="8047f-103">Információt ad az indításról.</span><span class="sxs-lookup"><span data-stu-id="8047f-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8047f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8047f-104">SYNTAX</span></span>

### <span data-ttu-id="8047f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8047f-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="8047f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8047f-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="8047f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8047f-107">DESCRIPTION</span></span>
<span data-ttu-id="8047f-108">A **Get-AzureRmDataFactoryV2TriggerRun** parancs részletes információt ad az adott időkeretben megadott triggerről.</span><span class="sxs-lookup"><span data-stu-id="8047f-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="8047f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8047f-109">EXAMPLES</span></span>

### <span data-ttu-id="8047f-110">1. példa: a trigger Run-ról szóló információk beszerzése</span><span class="sxs-lookup"><span data-stu-id="8047f-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="8047f-111">Ez a parancs a "2017-09-01" és a "2019-09-30" között megjelenő "WikiADF" gyári "WikiTrigger"-ra vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="8047f-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="8047f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8047f-112">PARAMETERS</span></span>

### <span data-ttu-id="8047f-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8047f-113">-DataFactory</span></span>
<span data-ttu-id="8047f-114">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="8047f-114">The data factory object.</span></span>

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

### <span data-ttu-id="8047f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8047f-115">-DataFactoryName</span></span>
<span data-ttu-id="8047f-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="8047f-116">The data factory name.</span></span>

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

### <span data-ttu-id="8047f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8047f-117">-Name</span></span>
<span data-ttu-id="8047f-118">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="8047f-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8047f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8047f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8047f-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8047f-120">The resource group name.</span></span>

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

### <span data-ttu-id="8047f-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="8047f-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="8047f-122">Az az időpont, amikor az indító futtatása ISO8601 formátumban kezdődik.</span><span class="sxs-lookup"><span data-stu-id="8047f-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="8047f-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="8047f-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="8047f-124">Az a dátum, amelyen vagy amely előtt a trigger futása ISO8601 formátumban lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="8047f-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8047f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8047f-125">INPUTS</span></span>

### <span data-ttu-id="8047f-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8047f-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="8047f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8047f-127">System.String</span></span>


## <span data-ttu-id="8047f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8047f-128">OUTPUTS</span></span>

### <span data-ttu-id="8047f-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerRun, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8047f-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8047f-130">Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="8047f-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="8047f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8047f-131">NOTES</span></span>

## <span data-ttu-id="8047f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8047f-132">RELATED LINKS</span></span>
[<span data-ttu-id="8047f-133">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8047f-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8047f-134">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8047f-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

