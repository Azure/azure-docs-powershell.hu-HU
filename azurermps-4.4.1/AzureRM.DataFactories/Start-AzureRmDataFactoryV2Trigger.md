---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: d49e04f4a791f6cbf5d609d6553fddcc26dc34e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679098"
---
# <span data-ttu-id="5d57b-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5d57b-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5d57b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d57b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d57b-103">Indítót indít az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="5d57b-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d57b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d57b-104">SYNTAX</span></span>

### <span data-ttu-id="5d57b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d57b-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d57b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d57b-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d57b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d57b-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d57b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d57b-108">DESCRIPTION</span></span>
<span data-ttu-id="5d57b-109">A **Start-AzureRmDataFactoryV2Trigger** parancsmag elindítja az indítót az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="5d57b-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="5d57b-110">Ha az indító a "leállt" állapotban van, a parancsmag elindítja az indítót, és az előbbi a futószalagokat a definíciója alapján hívja fel.</span><span class="sxs-lookup"><span data-stu-id="5d57b-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="5d57b-111">Ha az indító már a "Started" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="5d57b-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="5d57b-112">Ha meg van adva az erő paraméter, a parancsmag nem jelenik meg az indítás megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="5d57b-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="5d57b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5d57b-113">EXAMPLES</span></span>

### <span data-ttu-id="5d57b-114">1. példa: trigger indítása</span><span class="sxs-lookup"><span data-stu-id="5d57b-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5d57b-115">Elindítja az "WikiADF" Data Factory "ScheduledTrigger" nevű triggert.</span><span class="sxs-lookup"><span data-stu-id="5d57b-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="5d57b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d57b-116">PARAMETERS</span></span>

### <span data-ttu-id="5d57b-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5d57b-117">-Confirm</span></span>
<span data-ttu-id="5d57b-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5d57b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d57b-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5d57b-119">-DataFactoryName</span></span>
<span data-ttu-id="5d57b-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="5d57b-120">The data factory name.</span></span>

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

### <span data-ttu-id="5d57b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5d57b-121">-Force</span></span>
<span data-ttu-id="5d57b-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5d57b-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5d57b-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d57b-123">-Name</span></span>
<span data-ttu-id="5d57b-124">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="5d57b-124">The trigger name.</span></span>

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

### <span data-ttu-id="5d57b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d57b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d57b-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d57b-126">The resource group name.</span></span>

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

### <span data-ttu-id="5d57b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d57b-127">-ResourceId</span></span>
<span data-ttu-id="5d57b-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5d57b-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5d57b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d57b-129">-InputObject</span></span>
<span data-ttu-id="5d57b-130">Objektum elindítása az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="5d57b-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="5d57b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d57b-131">-WhatIf</span></span>
<span data-ttu-id="5d57b-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5d57b-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5d57b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d57b-133">-DefaultProfile</span></span>
<span data-ttu-id="5d57b-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d57b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d57b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d57b-135">CommonParameters</span></span>
<span data-ttu-id="5d57b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d57b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d57b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d57b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d57b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d57b-138">INPUTS</span></span>

### <span data-ttu-id="5d57b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5d57b-139">System.String</span></span>
<span data-ttu-id="5d57b-140">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5d57b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5d57b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d57b-141">OUTPUTS</span></span>

### <span data-ttu-id="5d57b-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5d57b-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5d57b-143">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5d57b-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5d57b-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d57b-144">NOTES</span></span>

## <span data-ttu-id="5d57b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d57b-145">RELATED LINKS</span></span>

[<span data-ttu-id="5d57b-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5d57b-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5d57b-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5d57b-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5d57b-148">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5d57b-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5d57b-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5d57b-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
