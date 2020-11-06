---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 5004b50cf5bb5b22a95ef00bf19f0e783fd04cb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503796"
---
# <span data-ttu-id="c7667-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c7667-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="c7667-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7667-102">SYNOPSIS</span></span>
<span data-ttu-id="c7667-103">Információt kap az eseményindítókkal kapcsolatban az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="c7667-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7667-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7667-104">SYNTAX</span></span>

### <span data-ttu-id="c7667-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7667-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7667-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c7667-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7667-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7667-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7667-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7667-108">DESCRIPTION</span></span>
<span data-ttu-id="c7667-109">A **Get-AzureRmDataFactoryV2Trigger** parancsmag információkat kap az adatgyárban lévő eseményindítókkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="c7667-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="c7667-110">Ha megad egy trigger nevét, a parancsmag információt kap az adott triggerről.</span><span class="sxs-lookup"><span data-stu-id="c7667-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="c7667-111">Ha nem ad meg nevet, a parancsmag információkat kap az adatfeldolgozó összes eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="c7667-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="c7667-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c7667-112">EXAMPLES</span></span>

### <span data-ttu-id="c7667-113">1. példa: információ kérése egy adott triggerről</span><span class="sxs-lookup"><span data-stu-id="c7667-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="c7667-114">A "WikiADF" Data Factory "az adatfeldolgozóban" létrehozott összes eseményindító listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7667-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="c7667-115">2. példa: információk kérése az összes eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="c7667-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="c7667-116">A "WikiADF" Data Factory "ScheduledTrigger" nevű egyetlen triggert kap.</span><span class="sxs-lookup"><span data-stu-id="c7667-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="c7667-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7667-117">PARAMETERS</span></span>

### <span data-ttu-id="c7667-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c7667-118">-DataFactory</span></span>
<span data-ttu-id="c7667-119">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="c7667-119">The data factory object.</span></span>

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

### <span data-ttu-id="c7667-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c7667-120">-DataFactoryName</span></span>
<span data-ttu-id="c7667-121">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c7667-121">The data factory name.</span></span>

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

### <span data-ttu-id="c7667-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7667-122">-DefaultProfile</span></span>
<span data-ttu-id="c7667-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7667-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7667-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7667-124">-Name</span></span>
<span data-ttu-id="c7667-125">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="c7667-125">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7667-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7667-126">-ResourceGroupName</span></span>
<span data-ttu-id="c7667-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7667-127">The resource group name.</span></span>

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

### <span data-ttu-id="c7667-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7667-128">-ResourceId</span></span>
<span data-ttu-id="c7667-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c7667-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7667-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7667-130">CommonParameters</span></span>
<span data-ttu-id="c7667-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7667-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7667-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7667-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7667-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7667-133">INPUTS</span></span>

### <span data-ttu-id="c7667-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c7667-134">System.String</span></span>
<span data-ttu-id="c7667-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c7667-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="c7667-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7667-136">OUTPUTS</span></span>

### <span data-ttu-id="c7667-137">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c7667-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c7667-138">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="c7667-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="c7667-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7667-139">NOTES</span></span>

## <span data-ttu-id="c7667-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7667-140">RELATED LINKS</span></span>

[<span data-ttu-id="c7667-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c7667-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c7667-142">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c7667-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c7667-143">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c7667-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c7667-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c7667-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()