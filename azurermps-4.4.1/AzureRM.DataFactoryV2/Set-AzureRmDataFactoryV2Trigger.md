---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8bf4a713784b367363e4f1f9167cfb144d06c0d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505971"
---
# <span data-ttu-id="0f6e1-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f6e1-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="0f6e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6e1-103">Triggert hoz létre egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f6e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f6e1-104">SYNTAX</span></span>

### <span data-ttu-id="0f6e1-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f6e1-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0f6e1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f6e1-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0f6e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f6e1-107">DESCRIPTION</span></span>

<span data-ttu-id="0f6e1-108">A **set-AzureRmDataFactoryV2Trigger** parancsmag létrehoz egy triggert egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="0f6e1-109">Ha a már létező triggerhez nevet ad meg, a parancsmag megerősítést kér, mielőtt lecseréli az indítót.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="0f6e1-110">Ha megadja az _erő_ paramétert, a parancsmag a meglévő triggert a megerősítés kérése nélkül váltja fel.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="0f6e1-111">Az eseményindítók a "leállt" állapotban jönnek létre, ami azt jelenti, hogy nem azonnal kezdenek hivatkozni a rájuk hivatkozó csővezetékekre.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="0f6e1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0f6e1-112">EXAMPLES</span></span>

### <span data-ttu-id="0f6e1-113">Példa 1: trigger létrehozása</span><span class="sxs-lookup"><span data-stu-id="0f6e1-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

```

<span data-ttu-id="0f6e1-114">Hozzon létre egy új triggert, az "WikiADF" Data Factory "ScheduledTrigger" nevűt.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="0f6e1-115">Az trigger a "leállt" állapotban jön létre, ami azt jelenti, hogy az nem azonnal indul el.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="0f6e1-116">Az indítót a parancsmag használatával indíthatja el `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="0f6e1-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="0f6e1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f6e1-117">PARAMETERS</span></span>

### <span data-ttu-id="0f6e1-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f6e1-118">-Confirm</span></span>
<span data-ttu-id="0f6e1-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6e1-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f6e1-120">-DataFactoryName</span></span>
<span data-ttu-id="0f6e1-121">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-121">The data factory name.</span></span>

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

### <span data-ttu-id="0f6e1-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0f6e1-122">-DefinitionFile</span></span>
<span data-ttu-id="0f6e1-123">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-123">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6e1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0f6e1-124">-Force</span></span>
<span data-ttu-id="0f6e1-125">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0f6e1-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f6e1-126">-Name</span></span>
<span data-ttu-id="0f6e1-127">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-127">The trigger name.</span></span>

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

### <span data-ttu-id="0f6e1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6e1-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f6e1-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-129">The resource group name.</span></span>

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

### <span data-ttu-id="0f6e1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f6e1-130">-ResourceId</span></span>
<span data-ttu-id="0f6e1-131">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0f6e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6e1-132">-WhatIf</span></span>
<span data-ttu-id="0f6e1-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0f6e1-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="0f6e1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f6e1-134">INPUTS</span></span>

### <span data-ttu-id="0f6e1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0f6e1-135">System.String</span></span>


## <span data-ttu-id="0f6e1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f6e1-136">OUTPUTS</span></span>

### <span data-ttu-id="0f6e1-137">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="0f6e1-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="0f6e1-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f6e1-138">NOTES</span></span>

## <span data-ttu-id="0f6e1-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f6e1-139">RELATED LINKS</span></span>
[<span data-ttu-id="0f6e1-140">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f6e1-140">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0f6e1-141">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f6e1-141">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0f6e1-142">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f6e1-142">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0f6e1-143">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0f6e1-143">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
