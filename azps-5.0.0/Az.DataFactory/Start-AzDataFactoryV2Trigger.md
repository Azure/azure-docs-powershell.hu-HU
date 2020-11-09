---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298214"
---
# <span data-ttu-id="33f2d-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="33f2d-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="33f2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="33f2d-103">Indítót indít az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="33f2d-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="33f2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33f2d-104">SYNTAX</span></span>

### <span data-ttu-id="33f2d-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33f2d-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33f2d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33f2d-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33f2d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33f2d-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33f2d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="33f2d-108">DESCRIPTION</span></span>
<span data-ttu-id="33f2d-109">A **Start-AzDataFactoryV2Trigger** parancsmag elindítja az indítót az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="33f2d-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="33f2d-110">Ha az indító a "leállt" állapotban van, a parancsmag elindítja az indítót, és az előbbi a futószalagokat a definíciója alapján hívja fel.</span><span class="sxs-lookup"><span data-stu-id="33f2d-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="33f2d-111">Ha az indító már a "Started" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="33f2d-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="33f2d-112">Ha meg van adva az erő paraméter, a parancsmag nem jelenik meg az indítás megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="33f2d-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="33f2d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="33f2d-113">EXAMPLES</span></span>

### <span data-ttu-id="33f2d-114">1. példa: trigger indítása</span><span class="sxs-lookup"><span data-stu-id="33f2d-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="33f2d-115">Elindítja az "WikiADF" Data Factory "ScheduledTrigger" nevű triggert.</span><span class="sxs-lookup"><span data-stu-id="33f2d-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="33f2d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33f2d-116">PARAMETERS</span></span>

### <span data-ttu-id="33f2d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="33f2d-117">-DataFactoryName</span></span>
<span data-ttu-id="33f2d-118">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="33f2d-118">The data factory name.</span></span>

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

### <span data-ttu-id="33f2d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f2d-119">-DefaultProfile</span></span>
<span data-ttu-id="33f2d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33f2d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33f2d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="33f2d-121">-Force</span></span>
<span data-ttu-id="33f2d-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="33f2d-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f2d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33f2d-123">-InputObject</span></span>
<span data-ttu-id="33f2d-124">Objektum elindítása az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="33f2d-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33f2d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="33f2d-125">-Name</span></span>
<span data-ttu-id="33f2d-126">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="33f2d-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33f2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33f2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="33f2d-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="33f2d-128">The resource group name.</span></span>

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

### <span data-ttu-id="33f2d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33f2d-129">-ResourceId</span></span>
<span data-ttu-id="33f2d-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="33f2d-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="33f2d-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="33f2d-131">-Confirm</span></span>
<span data-ttu-id="33f2d-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="33f2d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f2d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f2d-133">-WhatIf</span></span>
<span data-ttu-id="33f2d-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="33f2d-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f2d-135">CommonParameters</span></span>
<span data-ttu-id="33f2d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33f2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f2d-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f2d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f2d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33f2d-138">INPUTS</span></span>

### <span data-ttu-id="33f2d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="33f2d-139">System.String</span></span>

### <span data-ttu-id="33f2d-140">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="33f2d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="33f2d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33f2d-141">OUTPUTS</span></span>

### <span data-ttu-id="33f2d-142">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="33f2d-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="33f2d-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33f2d-143">NOTES</span></span>

## <span data-ttu-id="33f2d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33f2d-144">RELATED LINKS</span></span>

[<span data-ttu-id="33f2d-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="33f2d-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="33f2d-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="33f2d-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="33f2d-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="33f2d-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="33f2d-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="33f2d-148">Remove-AzDataFactoryV2Trigger</span></span>]()
