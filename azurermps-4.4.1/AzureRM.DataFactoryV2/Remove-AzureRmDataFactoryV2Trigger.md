---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505984"
---
# <span data-ttu-id="b7630-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b7630-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="b7630-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7630-102">SYNOPSIS</span></span>
<span data-ttu-id="b7630-103">Az indítót eltávolítja az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="b7630-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7630-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7630-104">SYNTAX</span></span>

### <span data-ttu-id="b7630-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7630-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b7630-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7630-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b7630-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7630-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b7630-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7630-108">DESCRIPTION</span></span>
<span data-ttu-id="b7630-109">A **Remove-AzureRmDataFactoryV2Trigger** parancsmag eltávolítja az indítót egy adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="b7630-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="b7630-110">Ha meg van adva az _erő_ paraméter, a parancsmag nem kérdez rá, mielőtt eltávolítja az indítót.</span><span class="sxs-lookup"><span data-stu-id="b7630-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="b7630-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b7630-111">EXAMPLES</span></span>

### <span data-ttu-id="b7630-112">1. példa: trigger eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b7630-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="b7630-113">Távolítsa el az "ScheduledTrigger" nevű triggert az "WikiADF" adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="b7630-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="b7630-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7630-114">PARAMETERS</span></span>

### <span data-ttu-id="b7630-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7630-115">-Confirm</span></span>
<span data-ttu-id="b7630-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7630-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7630-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b7630-117">-DataFactoryName</span></span>
<span data-ttu-id="b7630-118">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="b7630-118">The data factory name.</span></span>

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

### <span data-ttu-id="b7630-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b7630-119">-Force</span></span>
<span data-ttu-id="b7630-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b7630-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b7630-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7630-121">-Name</span></span>
<span data-ttu-id="b7630-122">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="b7630-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7630-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7630-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7630-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7630-124">The resource group name.</span></span>

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

### <span data-ttu-id="b7630-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7630-125">-ResourceId</span></span>
<span data-ttu-id="b7630-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="b7630-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b7630-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7630-127">-InputObject</span></span>
<span data-ttu-id="b7630-128">Az eltávolítandó indító objektum.</span><span class="sxs-lookup"><span data-stu-id="b7630-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="b7630-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7630-129">-WhatIf</span></span>
<span data-ttu-id="b7630-130">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b7630-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="b7630-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7630-131">INPUTS</span></span>

### <span data-ttu-id="b7630-132">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b7630-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="b7630-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b7630-133">System.String</span></span>


## <span data-ttu-id="b7630-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7630-134">OUTPUTS</span></span>

### <span data-ttu-id="b7630-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b7630-135">System.Object</span></span>

## <span data-ttu-id="b7630-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7630-136">NOTES</span></span>

## <span data-ttu-id="b7630-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7630-137">RELATED LINKS</span></span>
[<span data-ttu-id="b7630-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b7630-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b7630-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b7630-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b7630-140">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b7630-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b7630-141">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b7630-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

