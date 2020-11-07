---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3054824876ccaff24f319ae14c704cd975e79434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679484"
---
# <span data-ttu-id="e13c6-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e13c6-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="e13c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e13c6-102">SYNOPSIS</span></span>

<span data-ttu-id="e13c6-103">Az adatgyárban lévő trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="e13c6-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e13c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e13c6-104">SYNTAX</span></span>

### <span data-ttu-id="e13c6-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e13c6-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e13c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e13c6-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e13c6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e13c6-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e13c6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e13c6-108">DESCRIPTION</span></span>

<span data-ttu-id="e13c6-109">A **stop-AzureRmDataFactoryV2Trigger** parancsmag leállítja az adatgyárban lévő triggert.</span><span class="sxs-lookup"><span data-stu-id="e13c6-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="e13c6-110">Ha az indító az "Elindítva" állapotban van, a parancsmag leállítja az indítási fázist, és már nem indítja el a csővezetékeket.</span><span class="sxs-lookup"><span data-stu-id="e13c6-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="e13c6-111">Ha az indító már a "leállt" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="e13c6-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="e13c6-112">Ha meg van adva az erő paraméter, a parancsmag nem kérdez rá, mielőtt leállítja az aktiválást.</span><span class="sxs-lookup"><span data-stu-id="e13c6-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>


## <span data-ttu-id="e13c6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e13c6-113">EXAMPLES</span></span>

### <span data-ttu-id="e13c6-114">Példa 1: trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="e13c6-114">Example 1: Stop a trigger</span></span>

```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="e13c6-115">Az "WikiADF" Data Factory "ScheduledTrigger" nevű triggerének leállítása.</span><span class="sxs-lookup"><span data-stu-id="e13c6-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="e13c6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e13c6-116">PARAMETERS</span></span>

### <span data-ttu-id="e13c6-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e13c6-117">-Confirm</span></span>
<span data-ttu-id="e13c6-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e13c6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e13c6-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e13c6-119">-DataFactoryName</span></span>
<span data-ttu-id="e13c6-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="e13c6-120">The data factory name.</span></span>

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

### <span data-ttu-id="e13c6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e13c6-121">-Force</span></span>
<span data-ttu-id="e13c6-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e13c6-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e13c6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e13c6-123">-Name</span></span>
<span data-ttu-id="e13c6-124">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="e13c6-124">The trigger name.</span></span>

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

### <span data-ttu-id="e13c6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e13c6-125">-ResourceGroupName</span></span>
<span data-ttu-id="e13c6-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e13c6-126">The resource group name.</span></span>

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

### <span data-ttu-id="e13c6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e13c6-127">-ResourceId</span></span>
<span data-ttu-id="e13c6-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="e13c6-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e13c6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e13c6-129">-InputObject</span></span>
<span data-ttu-id="e13c6-130">Objektum elindítása az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="e13c6-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="e13c6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e13c6-131">-WhatIf</span></span>
<span data-ttu-id="e13c6-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e13c6-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="e13c6-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e13c6-133">INPUTS</span></span>

### <span data-ttu-id="e13c6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e13c6-134">System.String</span></span>
<span data-ttu-id="e13c6-135">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e13c6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="e13c6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e13c6-136">OUTPUTS</span></span>

### <span data-ttu-id="e13c6-137">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e13c6-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e13c6-138">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e13c6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="e13c6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e13c6-139">NOTES</span></span>

## <span data-ttu-id="e13c6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e13c6-140">RELATED LINKS</span></span>
[<span data-ttu-id="e13c6-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e13c6-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e13c6-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e13c6-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e13c6-143">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e13c6-143">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e13c6-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e13c6-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
