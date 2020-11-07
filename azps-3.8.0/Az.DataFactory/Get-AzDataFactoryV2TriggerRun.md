---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847266"
---
# <span data-ttu-id="e3ad8-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="e3ad8-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="e3ad8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ad8-103">Információt ad az indításról.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="e3ad8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3ad8-104">SYNTAX</span></span>

### <span data-ttu-id="e3ad8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3ad8-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3ad8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e3ad8-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3ad8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3ad8-107">DESCRIPTION</span></span>
<span data-ttu-id="e3ad8-108">A **Get-AzDataFactoryV2TriggerRun** parancs részletes információt ad az adott időkeretben megadott triggerről.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="e3ad8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e3ad8-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ad8-110">1. példa: a trigger Run-ról szóló információk beszerzése</span><span class="sxs-lookup"><span data-stu-id="e3ad8-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="e3ad8-111">Ez a parancs a "2017-09-01" és a "2019-09-30" között megjelenő "WikiADF" gyári "WikiTrigger"-ra vonatkozó információkat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="e3ad8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3ad8-112">PARAMETERS</span></span>

### <span data-ttu-id="e3ad8-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3ad8-113">-DataFactory</span></span>
<span data-ttu-id="e3ad8-114">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-114">The data factory object.</span></span>

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

### <span data-ttu-id="e3ad8-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e3ad8-115">-DataFactoryName</span></span>
<span data-ttu-id="e3ad8-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-116">The data factory name.</span></span>

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

### <span data-ttu-id="e3ad8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ad8-117">-DefaultProfile</span></span>
<span data-ttu-id="e3ad8-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3ad8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3ad8-119">-Name</span></span>
<span data-ttu-id="e3ad8-120">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-120">The trigger name.</span></span>

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

### <span data-ttu-id="e3ad8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ad8-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3ad8-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-122">The resource group name.</span></span>

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

### <span data-ttu-id="e3ad8-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="e3ad8-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="e3ad8-124">Az az időpont, amikor az indító futtatása ISO8601 formátumban kezdődik.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="e3ad8-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="e3ad8-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="e3ad8-126">Az a dátum, amelyen vagy amely előtt a trigger futása ISO8601 formátumban lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="e3ad8-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="e3ad8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ad8-127">CommonParameters</span></span>
<span data-ttu-id="e3ad8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3ad8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ad8-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ad8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ad8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ad8-130">INPUTS</span></span>

### <span data-ttu-id="e3ad8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3ad8-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="e3ad8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e3ad8-132">System.String</span></span>

## <span data-ttu-id="e3ad8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ad8-133">OUTPUTS</span></span>

### <span data-ttu-id="e3ad8-134">Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="e3ad8-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="e3ad8-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3ad8-135">NOTES</span></span>

## <span data-ttu-id="e3ad8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3ad8-136">RELATED LINKS</span></span>

[<span data-ttu-id="e3ad8-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e3ad8-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e3ad8-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e3ad8-138">Stop-AzDataFactoryV2Trigger</span></span>]()
