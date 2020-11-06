---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505087"
---
# <span data-ttu-id="24273-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24273-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="24273-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24273-102">SYNOPSIS</span></span>
<span data-ttu-id="24273-103">Információt kap az eseményindítókkal kapcsolatban az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="24273-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24273-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24273-104">SYNTAX</span></span>

### <span data-ttu-id="24273-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24273-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="24273-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="24273-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="24273-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24273-107">DESCRIPTION</span></span>
<span data-ttu-id="24273-108">A **Get-AzureRmDataFactoryV2Trigger** parancsmag információkat kap az adatgyárban lévő eseményindítókkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="24273-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="24273-109">Ha megad egy trigger nevét, a parancsmag információt kap az adott triggerről.</span><span class="sxs-lookup"><span data-stu-id="24273-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="24273-110">Ha nem ad meg nevet, a parancsmag információkat kap az adatfeldolgozó összes eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="24273-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="24273-111">Példák</span><span class="sxs-lookup"><span data-stu-id="24273-111">EXAMPLES</span></span>

### <span data-ttu-id="24273-112">1. példa: információ kérése egy adott triggerről</span><span class="sxs-lookup"><span data-stu-id="24273-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="24273-113">A "WikiADF" Data Factory "az adatfeldolgozóban" létrehozott összes eseményindító listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24273-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="24273-114">2. példa: információk kérése az összes eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="24273-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="24273-115">A "WikiADF" Data Factory "ScheduledTrigger" nevű egyetlen triggert kap.</span><span class="sxs-lookup"><span data-stu-id="24273-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="24273-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24273-116">PARAMETERS</span></span>

### <span data-ttu-id="24273-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="24273-117">-DataFactory</span></span>
<span data-ttu-id="24273-118">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="24273-118">The data factory object.</span></span>

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

### <span data-ttu-id="24273-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24273-119">-DataFactoryName</span></span>
<span data-ttu-id="24273-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="24273-120">The data factory name.</span></span>

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

### <span data-ttu-id="24273-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24273-121">-Name</span></span>
<span data-ttu-id="24273-122">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="24273-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24273-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24273-123">-ResourceGroupName</span></span>
<span data-ttu-id="24273-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="24273-124">The resource group name.</span></span>

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

## <span data-ttu-id="24273-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24273-125">INPUTS</span></span>

### <span data-ttu-id="24273-126">System. String</span><span class="sxs-lookup"><span data-stu-id="24273-126">System.String</span></span>
<span data-ttu-id="24273-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="24273-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="24273-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24273-128">OUTPUTS</span></span>

### <span data-ttu-id="24273-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="24273-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="24273-130">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="24273-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="24273-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24273-131">NOTES</span></span>

## <span data-ttu-id="24273-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24273-132">RELATED LINKS</span></span>
[<span data-ttu-id="24273-133">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24273-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24273-134">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24273-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24273-135">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24273-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24273-136">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24273-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
