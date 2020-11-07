---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: e5afbdd389d1ee9e1b74895743ed47ceed0b4ae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667046"
---
# <span data-ttu-id="71fd3-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="71fd3-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="71fd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="71fd3-103">Információt kap az eseményindítókkal kapcsolatban az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="71fd3-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="71fd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71fd3-104">SYNTAX</span></span>

### <span data-ttu-id="71fd3-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71fd3-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71fd3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="71fd3-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71fd3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="71fd3-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71fd3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="71fd3-108">DESCRIPTION</span></span>
<span data-ttu-id="71fd3-109">A **Get-AzDataFactoryV2Trigger** parancsmag információkat kap az adatgyárban lévő eseményindítókkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="71fd3-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="71fd3-110">Ha megad egy trigger nevét, a parancsmag információt kap az adott triggerről.</span><span class="sxs-lookup"><span data-stu-id="71fd3-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="71fd3-111">Ha nem ad meg nevet, a parancsmag információkat kap az adatfeldolgozó összes eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="71fd3-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="71fd3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="71fd3-112">EXAMPLES</span></span>

### <span data-ttu-id="71fd3-113">1. példa: információ kérése egy adott triggerről</span><span class="sxs-lookup"><span data-stu-id="71fd3-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="71fd3-114">A "WikiADF" Data Factory "az adatfeldolgozóban" létrehozott összes eseményindító listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="71fd3-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="71fd3-115">2. példa: információk kérése az összes eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="71fd3-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="71fd3-116">A "WikiADF" Data Factory "ScheduledTrigger" nevű egyetlen triggert kap.</span><span class="sxs-lookup"><span data-stu-id="71fd3-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="71fd3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71fd3-117">PARAMETERS</span></span>

### <span data-ttu-id="71fd3-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="71fd3-118">-DataFactory</span></span>
<span data-ttu-id="71fd3-119">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="71fd3-119">The data factory object.</span></span>

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

### <span data-ttu-id="71fd3-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="71fd3-120">-DataFactoryName</span></span>
<span data-ttu-id="71fd3-121">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="71fd3-121">The data factory name.</span></span>

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

### <span data-ttu-id="71fd3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fd3-122">-DefaultProfile</span></span>
<span data-ttu-id="71fd3-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71fd3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71fd3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71fd3-124">-Name</span></span>
<span data-ttu-id="71fd3-125">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="71fd3-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fd3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71fd3-126">-ResourceGroupName</span></span>
<span data-ttu-id="71fd3-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="71fd3-127">The resource group name.</span></span>

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

### <span data-ttu-id="71fd3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71fd3-128">-ResourceId</span></span>
<span data-ttu-id="71fd3-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="71fd3-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fd3-130">CommonParameters</span></span>
<span data-ttu-id="71fd3-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71fd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fd3-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71fd3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fd3-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71fd3-133">INPUTS</span></span>

### <span data-ttu-id="71fd3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="71fd3-134">System.String</span></span>

### <span data-ttu-id="71fd3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="71fd3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="71fd3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71fd3-136">OUTPUTS</span></span>

### <span data-ttu-id="71fd3-137">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="71fd3-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="71fd3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71fd3-138">NOTES</span></span>

## <span data-ttu-id="71fd3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71fd3-139">RELATED LINKS</span></span>

[<span data-ttu-id="71fd3-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="71fd3-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="71fd3-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="71fd3-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="71fd3-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="71fd3-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="71fd3-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="71fd3-143">Remove-AzDataFactoryV2Trigger</span></span>]()
