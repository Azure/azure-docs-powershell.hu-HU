---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 5b3052682785a694b3fb0999bb5df761eb3b96be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836466"
---
# <span data-ttu-id="5b362-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b362-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5b362-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b362-102">SYNOPSIS</span></span>
<span data-ttu-id="5b362-103">Az indítót eltávolítja az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="5b362-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="5b362-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b362-104">SYNTAX</span></span>

### <span data-ttu-id="5b362-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b362-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b362-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b362-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b362-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b362-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b362-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b362-108">DESCRIPTION</span></span>
<span data-ttu-id="5b362-109">A **Remove-AzDataFactoryV2Trigger** parancsmag eltávolítja az indítót egy adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="5b362-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="5b362-110">Ha meg van adva az _erő_ paraméter, a parancsmag nem kérdez rá, mielőtt eltávolítja az indítót.</span><span class="sxs-lookup"><span data-stu-id="5b362-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="5b362-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5b362-111">EXAMPLES</span></span>

### <span data-ttu-id="5b362-112">1. példa: trigger eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5b362-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5b362-113">Távolítsa el az "ScheduledTrigger" nevű triggert az "WikiADF" adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="5b362-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="5b362-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b362-114">PARAMETERS</span></span>

### <span data-ttu-id="5b362-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5b362-115">-DataFactoryName</span></span>
<span data-ttu-id="5b362-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="5b362-116">The data factory name.</span></span>

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

### <span data-ttu-id="5b362-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b362-117">-DefaultProfile</span></span>
<span data-ttu-id="5b362-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b362-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b362-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b362-119">-Force</span></span>
<span data-ttu-id="5b362-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5b362-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5b362-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b362-121">-InputObject</span></span>
<span data-ttu-id="5b362-122">Az eltávolítandó indító objektum.</span><span class="sxs-lookup"><span data-stu-id="5b362-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="5b362-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b362-123">-Name</span></span>
<span data-ttu-id="5b362-124">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="5b362-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b362-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b362-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b362-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5b362-126">The resource group name.</span></span>

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

### <span data-ttu-id="5b362-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b362-127">-ResourceId</span></span>
<span data-ttu-id="5b362-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5b362-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5b362-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b362-129">-Confirm</span></span>
<span data-ttu-id="5b362-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b362-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b362-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b362-131">-WhatIf</span></span>
<span data-ttu-id="5b362-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b362-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5b362-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b362-133">CommonParameters</span></span>
<span data-ttu-id="5b362-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b362-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b362-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b362-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b362-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b362-136">INPUTS</span></span>

### <span data-ttu-id="5b362-137">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5b362-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="5b362-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5b362-138">System.String</span></span>

## <span data-ttu-id="5b362-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b362-139">OUTPUTS</span></span>

### <span data-ttu-id="5b362-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b362-140">System.Boolean</span></span>

## <span data-ttu-id="5b362-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b362-141">NOTES</span></span>

## <span data-ttu-id="5b362-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b362-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b362-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b362-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b362-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b362-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b362-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b362-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b362-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b362-146">Stop-AzDataFactoryV2Trigger</span></span>]()

