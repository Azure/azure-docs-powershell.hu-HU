---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 82af1131e2730cf1f78c0c04ff8540e2ef371d2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492297"
---
# <span data-ttu-id="b4f58-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b4f58-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="b4f58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4f58-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f58-103">Az indítót eltávolítja az adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="b4f58-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4f58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4f58-104">SYNTAX</span></span>

### <span data-ttu-id="b4f58-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4f58-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f58-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4f58-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f58-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f58-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f58-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4f58-108">DESCRIPTION</span></span>
<span data-ttu-id="b4f58-109">A **Remove-AzureRmDataFactoryV2Trigger** parancsmag eltávolítja az indítót egy adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="b4f58-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="b4f58-110">Ha meg van adva az _erő_ paraméter, a parancsmag nem kérdez rá, mielőtt eltávolítja az indítót.</span><span class="sxs-lookup"><span data-stu-id="b4f58-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="b4f58-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b4f58-111">EXAMPLES</span></span>

### <span data-ttu-id="b4f58-112">1. példa: trigger eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b4f58-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="b4f58-113">Távolítsa el az "ScheduledTrigger" nevű triggert az "WikiADF" adatgyárból.</span><span class="sxs-lookup"><span data-stu-id="b4f58-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="b4f58-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4f58-114">PARAMETERS</span></span>

### <span data-ttu-id="b4f58-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b4f58-115">-DataFactoryName</span></span>
<span data-ttu-id="b4f58-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="b4f58-116">The data factory name.</span></span>

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

### <span data-ttu-id="b4f58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f58-117">-DefaultProfile</span></span>
<span data-ttu-id="b4f58-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4f58-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4f58-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b4f58-119">-Force</span></span>
<span data-ttu-id="b4f58-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b4f58-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b4f58-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4f58-121">-InputObject</span></span>
<span data-ttu-id="b4f58-122">Az eltávolítandó indító objektum.</span><span class="sxs-lookup"><span data-stu-id="b4f58-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="b4f58-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4f58-123">-Name</span></span>
<span data-ttu-id="b4f58-124">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="b4f58-124">The trigger name.</span></span>

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

### <span data-ttu-id="b4f58-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f58-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4f58-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b4f58-126">The resource group name.</span></span>

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

### <span data-ttu-id="b4f58-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f58-127">-ResourceId</span></span>
<span data-ttu-id="b4f58-128">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="b4f58-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b4f58-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4f58-129">-Confirm</span></span>
<span data-ttu-id="b4f58-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4f58-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f58-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f58-131">-WhatIf</span></span>
<span data-ttu-id="b4f58-132">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4f58-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b4f58-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f58-133">CommonParameters</span></span>
<span data-ttu-id="b4f58-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4f58-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f58-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f58-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f58-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f58-136">INPUTS</span></span>

### <span data-ttu-id="b4f58-137">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b4f58-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="b4f58-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b4f58-138">System.String</span></span>

## <span data-ttu-id="b4f58-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f58-139">OUTPUTS</span></span>

### <span data-ttu-id="b4f58-140">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b4f58-140">System.Object</span></span>

## <span data-ttu-id="b4f58-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4f58-141">NOTES</span></span>

## <span data-ttu-id="b4f58-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4f58-142">RELATED LINKS</span></span>

[<span data-ttu-id="b4f58-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b4f58-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b4f58-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b4f58-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b4f58-145">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b4f58-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b4f58-146">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b4f58-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

