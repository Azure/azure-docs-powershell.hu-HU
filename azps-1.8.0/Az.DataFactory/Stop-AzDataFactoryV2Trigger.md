---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 9ef250a396e728da6625966eaba91d7c12f1c10c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836434"
---
# <span data-ttu-id="d5a5f-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d5a5f-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="d5a5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a5f-103">Az adatgyárban lévő trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="d5a5f-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="d5a5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5a5f-104">SYNTAX</span></span>

### <span data-ttu-id="d5a5f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5a5f-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a5f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5a5f-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a5f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a5f-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a5f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5a5f-108">DESCRIPTION</span></span>
<span data-ttu-id="d5a5f-109">A **stop-AzDataFactoryV2Trigger** parancsmag leállítja az adatgyárban lévő triggert.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="d5a5f-110">Ha az indító az "Elindítva" állapotban van, a parancsmag leállítja az indítási fázist, és már nem indítja el a csővezetékeket.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="d5a5f-111">Ha az indító már a "leállt" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="d5a5f-112">Ha meg van adva az erő paraméter, a parancsmag nem kérdez rá, mielőtt leállítja az aktiválást.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="d5a5f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d5a5f-113">EXAMPLES</span></span>

### <span data-ttu-id="d5a5f-114">Példa 1: trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="d5a5f-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="d5a5f-115">Az "WikiADF" Data Factory "ScheduledTrigger" nevű triggerének leállítása.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="d5a5f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5a5f-116">PARAMETERS</span></span>

### <span data-ttu-id="d5a5f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d5a5f-117">-DataFactoryName</span></span>
<span data-ttu-id="d5a5f-118">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-118">The data factory name.</span></span>

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

### <span data-ttu-id="d5a5f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a5f-119">-DefaultProfile</span></span>
<span data-ttu-id="d5a5f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a5f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d5a5f-121">-Force</span></span>
<span data-ttu-id="d5a5f-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d5a5f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5a5f-123">-InputObject</span></span>
<span data-ttu-id="d5a5f-124">Objektum elindítása az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="d5a5f-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5a5f-125">-Name</span></span>
<span data-ttu-id="d5a5f-126">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-126">The trigger name.</span></span>

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

### <span data-ttu-id="d5a5f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a5f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5a5f-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-128">The resource group name.</span></span>

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

### <span data-ttu-id="d5a5f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a5f-129">-ResourceId</span></span>
<span data-ttu-id="d5a5f-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d5a5f-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5a5f-131">-Confirm</span></span>
<span data-ttu-id="d5a5f-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a5f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a5f-133">-WhatIf</span></span>
<span data-ttu-id="d5a5f-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d5a5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a5f-135">CommonParameters</span></span>
<span data-ttu-id="d5a5f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5a5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a5f-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a5f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a5f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a5f-138">INPUTS</span></span>

### <span data-ttu-id="d5a5f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a5f-139">System.String</span></span>

### <span data-ttu-id="d5a5f-140">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d5a5f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="d5a5f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5a5f-141">OUTPUTS</span></span>

### <span data-ttu-id="d5a5f-142">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d5a5f-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="d5a5f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5a5f-143">NOTES</span></span>

## <span data-ttu-id="d5a5f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5a5f-144">RELATED LINKS</span></span>

[<span data-ttu-id="d5a5f-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d5a5f-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d5a5f-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d5a5f-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d5a5f-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d5a5f-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d5a5f-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d5a5f-148">Remove-AzDataFactoryV2Trigger</span></span>]()
