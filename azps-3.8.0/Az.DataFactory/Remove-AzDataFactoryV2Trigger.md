---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847162"
---
# <span data-ttu-id="7e695-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7e695-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="7e695-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e695-102">SYNOPSIS</span></span>
<span data-ttu-id="7e695-103">Az indítót eltávolítja az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="7e695-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="7e695-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e695-104">SYNTAX</span></span>

### <span data-ttu-id="7e695-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e695-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e695-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7e695-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e695-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e695-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e695-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e695-108">DESCRIPTION</span></span>
<span data-ttu-id="7e695-109">A **Remove-AzDataFactoryV2Trigger** parancsmag eltávolítja az indítót egy adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="7e695-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="7e695-110">Ha meg van adva az _erő_ paraméter, a parancsmag nem kérdez rá, mielőtt eltávolítja az indítót.</span><span class="sxs-lookup"><span data-stu-id="7e695-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="7e695-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7e695-111">EXAMPLES</span></span>

### <span data-ttu-id="7e695-112">1. példa: trigger eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7e695-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="7e695-113">Távolítsa el az "ScheduledTrigger" nevű triggert az "WikiADF" adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="7e695-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="7e695-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e695-114">PARAMETERS</span></span>

### <span data-ttu-id="7e695-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7e695-115">-DataFactoryName</span></span>
<span data-ttu-id="7e695-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="7e695-116">The data factory name.</span></span>

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

### <span data-ttu-id="7e695-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e695-117">-DefaultProfile</span></span>
<span data-ttu-id="7e695-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e695-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e695-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7e695-119">-Force</span></span>
<span data-ttu-id="7e695-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7e695-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7e695-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e695-121">-InputObject</span></span>
<span data-ttu-id="7e695-122">Az eltávolítandó indító objektum.</span><span class="sxs-lookup"><span data-stu-id="7e695-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="7e695-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e695-123">-Name</span></span>
<span data-ttu-id="7e695-124">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="7e695-124">The trigger name.</span></span>

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

### <span data-ttu-id="7e695-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e695-125">-ResourceGroupName</span></span>
<span data-ttu-id="7e695-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7e695-126">The resource group name.</span></span>

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

### <span data-ttu-id="7e695-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e695-127">-ResourceId</span></span>
<span data-ttu-id="7e695-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="7e695-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7e695-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e695-129">-Confirm</span></span>
<span data-ttu-id="7e695-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e695-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e695-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e695-131">-WhatIf</span></span>
<span data-ttu-id="7e695-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e695-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7e695-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e695-133">CommonParameters</span></span>
<span data-ttu-id="7e695-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e695-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e695-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e695-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e695-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e695-136">INPUTS</span></span>

### <span data-ttu-id="7e695-137">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7e695-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="7e695-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7e695-138">System.String</span></span>

## <span data-ttu-id="7e695-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e695-139">OUTPUTS</span></span>

### <span data-ttu-id="7e695-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e695-140">System.Boolean</span></span>

## <span data-ttu-id="7e695-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e695-141">NOTES</span></span>

## <span data-ttu-id="7e695-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e695-142">RELATED LINKS</span></span>

[<span data-ttu-id="7e695-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7e695-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7e695-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7e695-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7e695-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7e695-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7e695-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7e695-146">Stop-AzDataFactoryV2Trigger</span></span>]()

