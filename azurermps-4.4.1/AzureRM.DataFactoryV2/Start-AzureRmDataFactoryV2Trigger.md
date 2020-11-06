---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 610aabd21fa1a3e7ae19430c4ce5d79d89f7ab3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505967"
---
# <span data-ttu-id="c0112-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c0112-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="c0112-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0112-102">SYNOPSIS</span></span>

<span data-ttu-id="c0112-103">Indítót indít az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="c0112-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0112-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0112-104">SYNTAX</span></span>

### <span data-ttu-id="c0112-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0112-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c0112-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0112-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c0112-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0112-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c0112-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0112-108">DESCRIPTION</span></span>

<span data-ttu-id="c0112-109">A **Start-AzureRmDataFactoryV2Trigger** parancsmag elindítja az indítót az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="c0112-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="c0112-110">Ha az indító a "leállt" állapotban van, a parancsmag elindítja az indítót, és az előbbi a futószalagokat a definíciója alapján hívja fel.</span><span class="sxs-lookup"><span data-stu-id="c0112-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="c0112-111">Ha az indító már a "Started" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="c0112-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="c0112-112">Ha meg van adva az erő paraméter, a parancsmag nem jelenik meg az indítás megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="c0112-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>


## <span data-ttu-id="c0112-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c0112-113">EXAMPLES</span></span>

### <span data-ttu-id="c0112-114">1. példa: trigger indítása</span><span class="sxs-lookup"><span data-stu-id="c0112-114">Example 1: Start a trigger</span></span>

```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="c0112-115">Elindítja az "WikiADF" Data Factory "ScheduledTrigger" nevű triggert.</span><span class="sxs-lookup"><span data-stu-id="c0112-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="c0112-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0112-116">PARAMETERS</span></span>

### <span data-ttu-id="c0112-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0112-117">-Confirm</span></span>
<span data-ttu-id="c0112-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0112-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0112-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c0112-119">-DataFactoryName</span></span>
<span data-ttu-id="c0112-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c0112-120">The data factory name.</span></span>

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

### <span data-ttu-id="c0112-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c0112-121">-Force</span></span>
<span data-ttu-id="c0112-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c0112-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0112-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0112-123">-Name</span></span>
<span data-ttu-id="c0112-124">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="c0112-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0112-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0112-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0112-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0112-126">The resource group name.</span></span>

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

### <span data-ttu-id="c0112-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0112-127">-ResourceId</span></span>
<span data-ttu-id="c0112-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c0112-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0112-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0112-129">-InputObject</span></span>
<span data-ttu-id="c0112-130">Objektum elindítása az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="c0112-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0112-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0112-131">-WhatIf</span></span>
<span data-ttu-id="c0112-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c0112-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c0112-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0112-133">INPUTS</span></span>

### <span data-ttu-id="c0112-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0112-134">System.String</span></span>
<span data-ttu-id="c0112-135">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="c0112-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="c0112-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0112-136">OUTPUTS</span></span>

### <span data-ttu-id="c0112-137">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c0112-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c0112-138">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="c0112-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="c0112-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0112-139">NOTES</span></span>

## <span data-ttu-id="c0112-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0112-140">RELATED LINKS</span></span>
[<span data-ttu-id="c0112-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c0112-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c0112-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c0112-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c0112-143">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c0112-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c0112-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c0112-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
