---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: e359a99d1d420d9494b16719e61bec4d7ed670a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495411"
---
# <span data-ttu-id="0c88e-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0c88e-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="0c88e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c88e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c88e-103">Az adatgyárban lévő trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="0c88e-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c88e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c88e-104">SYNTAX</span></span>

### <span data-ttu-id="0c88e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c88e-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c88e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c88e-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c88e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c88e-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c88e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c88e-108">DESCRIPTION</span></span>
<span data-ttu-id="0c88e-109">A **stop-AzureRmDataFactoryV2Trigger** parancsmag leállítja az adatgyárban lévő triggert.</span><span class="sxs-lookup"><span data-stu-id="0c88e-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="0c88e-110">Ha az indító az "Elindítva" állapotban van, a parancsmag leállítja az indítási fázist, és már nem indítja el a csővezetékeket.</span><span class="sxs-lookup"><span data-stu-id="0c88e-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="0c88e-111">Ha az indító már a "leállt" állapotban van, ez a parancsmag nincs befolyással.</span><span class="sxs-lookup"><span data-stu-id="0c88e-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="0c88e-112">Ha meg van adva az erő paraméter, a parancsmag nem kérdez rá, mielőtt leállítja az aktiválást.</span><span class="sxs-lookup"><span data-stu-id="0c88e-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="0c88e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0c88e-113">EXAMPLES</span></span>

### <span data-ttu-id="0c88e-114">Példa 1: trigger leállítása</span><span class="sxs-lookup"><span data-stu-id="0c88e-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="0c88e-115">Az "WikiADF" Data Factory "ScheduledTrigger" nevű triggerének leállítása.</span><span class="sxs-lookup"><span data-stu-id="0c88e-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="0c88e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c88e-116">PARAMETERS</span></span>

### <span data-ttu-id="0c88e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0c88e-117">-DataFactoryName</span></span>
<span data-ttu-id="0c88e-118">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0c88e-118">The data factory name.</span></span>

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

### <span data-ttu-id="0c88e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c88e-119">-DefaultProfile</span></span>
<span data-ttu-id="0c88e-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c88e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c88e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0c88e-121">-Force</span></span>
<span data-ttu-id="0c88e-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0c88e-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0c88e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c88e-123">-InputObject</span></span>
<span data-ttu-id="0c88e-124">Objektum elindítása az indításhoz.</span><span class="sxs-lookup"><span data-stu-id="0c88e-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="0c88e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c88e-125">-Name</span></span>
<span data-ttu-id="0c88e-126">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="0c88e-126">The trigger name.</span></span>

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

### <span data-ttu-id="0c88e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c88e-127">-ResourceGroupName</span></span>
<span data-ttu-id="0c88e-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0c88e-128">The resource group name.</span></span>

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

### <span data-ttu-id="0c88e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c88e-129">-ResourceId</span></span>
<span data-ttu-id="0c88e-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0c88e-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0c88e-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c88e-131">-Confirm</span></span>
<span data-ttu-id="0c88e-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c88e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c88e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c88e-133">-WhatIf</span></span>
<span data-ttu-id="0c88e-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0c88e-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0c88e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c88e-135">CommonParameters</span></span>
<span data-ttu-id="0c88e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c88e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c88e-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c88e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c88e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c88e-138">INPUTS</span></span>

### <span data-ttu-id="0c88e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0c88e-139">System.String</span></span>
<span data-ttu-id="0c88e-140">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0c88e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0c88e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c88e-141">OUTPUTS</span></span>

### <span data-ttu-id="0c88e-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0c88e-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0c88e-143">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0c88e-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="0c88e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c88e-144">NOTES</span></span>

## <span data-ttu-id="0c88e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c88e-145">RELATED LINKS</span></span>

[<span data-ttu-id="0c88e-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0c88e-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0c88e-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0c88e-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0c88e-148">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0c88e-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0c88e-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0c88e-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
