---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847117"
---
# <span data-ttu-id="7d54b-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d54b-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="7d54b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d54b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d54b-103">Triggert hoz létre egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="7d54b-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="7d54b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d54b-104">SYNTAX</span></span>

### <span data-ttu-id="7d54b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d54b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d54b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d54b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d54b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d54b-107">DESCRIPTION</span></span>
<span data-ttu-id="7d54b-108">A **set-AzDataFactoryV2Trigger** parancsmag létrehoz egy triggert egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="7d54b-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="7d54b-109">Ha a már létező triggerhez nevet ad meg, a parancsmag megerősítést kér, mielőtt lecseréli az indítót.</span><span class="sxs-lookup"><span data-stu-id="7d54b-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="7d54b-110">Ha megadja az _erő_ paramétert, a parancsmag a meglévő triggert a megerősítés kérése nélkül váltja fel.</span><span class="sxs-lookup"><span data-stu-id="7d54b-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="7d54b-111">Az eseményindítók a "leállt" állapotban jönnek létre, ami azt jelenti, hogy nem azonnal kezdenek hivatkozni a rájuk hivatkozó csővezetékekre.</span><span class="sxs-lookup"><span data-stu-id="7d54b-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="7d54b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7d54b-112">EXAMPLES</span></span>

### <span data-ttu-id="7d54b-113">Példa 1: trigger létrehozása</span><span class="sxs-lookup"><span data-stu-id="7d54b-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="7d54b-114">Hozzon létre egy új triggert, az "WikiADF" Data Factory "ScheduledTrigger" nevűt.</span><span class="sxs-lookup"><span data-stu-id="7d54b-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="7d54b-115">Az trigger a "leállt" állapotban jön létre, ami azt jelenti, hogy az nem azonnal indul el.</span><span class="sxs-lookup"><span data-stu-id="7d54b-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="7d54b-116">Az indítót a parancsmag használatával indíthatja el `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="7d54b-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="7d54b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d54b-117">PARAMETERS</span></span>

### <span data-ttu-id="7d54b-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7d54b-118">-DataFactoryName</span></span>
<span data-ttu-id="7d54b-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="7d54b-119">The data factory name.</span></span>

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

### <span data-ttu-id="7d54b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d54b-120">-DefaultProfile</span></span>
<span data-ttu-id="7d54b-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d54b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d54b-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7d54b-122">-DefinitionFile</span></span>
<span data-ttu-id="7d54b-123">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="7d54b-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d54b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7d54b-124">-Force</span></span>
<span data-ttu-id="7d54b-125">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7d54b-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7d54b-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d54b-126">-Name</span></span>
<span data-ttu-id="7d54b-127">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="7d54b-127">The trigger name.</span></span>

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

### <span data-ttu-id="7d54b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d54b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7d54b-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7d54b-129">The resource group name.</span></span>

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

### <span data-ttu-id="7d54b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d54b-130">-ResourceId</span></span>
<span data-ttu-id="7d54b-131">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="7d54b-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7d54b-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d54b-132">-Confirm</span></span>
<span data-ttu-id="7d54b-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d54b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d54b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d54b-134">-WhatIf</span></span>
<span data-ttu-id="7d54b-135">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7d54b-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7d54b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d54b-136">CommonParameters</span></span>
<span data-ttu-id="7d54b-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d54b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d54b-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d54b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d54b-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d54b-139">INPUTS</span></span>

### <span data-ttu-id="7d54b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7d54b-140">System.String</span></span>

## <span data-ttu-id="7d54b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d54b-141">OUTPUTS</span></span>

### <span data-ttu-id="7d54b-142">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7d54b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7d54b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d54b-143">NOTES</span></span>

## <span data-ttu-id="7d54b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d54b-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d54b-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d54b-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7d54b-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d54b-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7d54b-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d54b-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7d54b-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d54b-148">Remove-AzDataFactoryV2Trigger</span></span>]()
