---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 7c14b5c53cdffa51671a64ad40fe18a400ae6803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502156"
---
# <span data-ttu-id="0b14f-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0b14f-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="0b14f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b14f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b14f-103">Információt kap az eseményindítókkal kapcsolatban az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0b14f-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b14f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b14f-104">SYNTAX</span></span>

### <span data-ttu-id="0b14f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b14f-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b14f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0b14f-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b14f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b14f-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b14f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b14f-108">DESCRIPTION</span></span>
<span data-ttu-id="0b14f-109">A **Get-AzureRmDataFactoryV2Trigger** parancsmag információkat kap az adatgyárban lévő eseményindítókkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="0b14f-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="0b14f-110">Ha megad egy trigger nevét, a parancsmag információt kap az adott triggerről.</span><span class="sxs-lookup"><span data-stu-id="0b14f-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="0b14f-111">Ha nem ad meg nevet, a parancsmag információkat kap az adatfeldolgozó összes eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="0b14f-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="0b14f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0b14f-112">EXAMPLES</span></span>

### <span data-ttu-id="0b14f-113">1. példa: információ kérése egy adott triggerről</span><span class="sxs-lookup"><span data-stu-id="0b14f-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="0b14f-114">A "WikiADF" Data Factory "az adatfeldolgozóban" létrehozott összes eseményindító listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0b14f-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="0b14f-115">2. példa: információk kérése az összes eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="0b14f-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="0b14f-116">A "WikiADF" Data Factory "ScheduledTrigger" nevű egyetlen triggert kap.</span><span class="sxs-lookup"><span data-stu-id="0b14f-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="0b14f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b14f-117">PARAMETERS</span></span>

### <span data-ttu-id="0b14f-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b14f-118">-DataFactory</span></span>
<span data-ttu-id="0b14f-119">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="0b14f-119">The data factory object.</span></span>

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

### <span data-ttu-id="0b14f-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0b14f-120">-DataFactoryName</span></span>
<span data-ttu-id="0b14f-121">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0b14f-121">The data factory name.</span></span>

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

### <span data-ttu-id="0b14f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b14f-122">-DefaultProfile</span></span>
<span data-ttu-id="0b14f-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b14f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b14f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0b14f-124">-Name</span></span>
<span data-ttu-id="0b14f-125">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="0b14f-125">The trigger name.</span></span>

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

### <span data-ttu-id="0b14f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b14f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b14f-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0b14f-127">The resource group name.</span></span>

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

### <span data-ttu-id="0b14f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b14f-128">-ResourceId</span></span>
<span data-ttu-id="0b14f-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0b14f-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0b14f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b14f-130">CommonParameters</span></span>
<span data-ttu-id="0b14f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b14f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b14f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b14f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b14f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b14f-133">INPUTS</span></span>

### <span data-ttu-id="0b14f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0b14f-134">System.String</span></span>

### <span data-ttu-id="0b14f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0b14f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="0b14f-136">Paraméterek: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b14f-136">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="0b14f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b14f-137">OUTPUTS</span></span>

### <span data-ttu-id="0b14f-138">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0b14f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0b14f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b14f-139">NOTES</span></span>

## <span data-ttu-id="0b14f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b14f-140">RELATED LINKS</span></span>

[<span data-ttu-id="0b14f-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0b14f-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0b14f-142">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0b14f-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0b14f-143">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0b14f-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0b14f-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0b14f-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
