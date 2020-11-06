---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: dc4630359070e627a3c65c63f21c23f987cb9a31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496255"
---
# <span data-ttu-id="81cf2-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81cf2-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="81cf2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="81cf2-103">Triggert hoz létre egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="81cf2-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81cf2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81cf2-104">SYNTAX</span></span>

### <span data-ttu-id="81cf2-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81cf2-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81cf2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81cf2-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81cf2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81cf2-107">DESCRIPTION</span></span>
<span data-ttu-id="81cf2-108">A **set-AzureRmDataFactoryV2Trigger** parancsmag létrehoz egy triggert egy adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="81cf2-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="81cf2-109">Ha a már létező triggerhez nevet ad meg, a parancsmag megerősítést kér, mielőtt lecseréli az indítót.</span><span class="sxs-lookup"><span data-stu-id="81cf2-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="81cf2-110">Ha megadja az _erő_ paramétert, a parancsmag a meglévő triggert a megerősítés kérése nélkül váltja fel.</span><span class="sxs-lookup"><span data-stu-id="81cf2-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="81cf2-111">Az eseményindítók a "leállt" állapotban jönnek létre, ami azt jelenti, hogy nem azonnal kezdenek hivatkozni a rájuk hivatkozó csővezetékekre.</span><span class="sxs-lookup"><span data-stu-id="81cf2-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="81cf2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="81cf2-112">EXAMPLES</span></span>

### <span data-ttu-id="81cf2-113">Példa 1: trigger létrehozása</span><span class="sxs-lookup"><span data-stu-id="81cf2-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="81cf2-114">Hozzon létre egy új triggert, az "WikiADF" Data Factory "ScheduledTrigger" nevűt.</span><span class="sxs-lookup"><span data-stu-id="81cf2-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="81cf2-115">Az trigger a "leállt" állapotban jön létre, ami azt jelenti, hogy az nem azonnal indul el.</span><span class="sxs-lookup"><span data-stu-id="81cf2-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="81cf2-116">Az indítót a parancsmag használatával indíthatja el `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="81cf2-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="81cf2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81cf2-117">PARAMETERS</span></span>

### <span data-ttu-id="81cf2-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="81cf2-118">-DataFactoryName</span></span>
<span data-ttu-id="81cf2-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="81cf2-119">The data factory name.</span></span>

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

### <span data-ttu-id="81cf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cf2-120">-DefaultProfile</span></span>
<span data-ttu-id="81cf2-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81cf2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81cf2-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="81cf2-122">-DefinitionFile</span></span>
<span data-ttu-id="81cf2-123">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="81cf2-123">The JSON file path.</span></span>

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

### <span data-ttu-id="81cf2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="81cf2-124">-Force</span></span>
<span data-ttu-id="81cf2-125">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="81cf2-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="81cf2-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81cf2-126">-Name</span></span>
<span data-ttu-id="81cf2-127">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="81cf2-127">The trigger name.</span></span>

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

### <span data-ttu-id="81cf2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cf2-128">-ResourceGroupName</span></span>
<span data-ttu-id="81cf2-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="81cf2-129">The resource group name.</span></span>

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

### <span data-ttu-id="81cf2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81cf2-130">-ResourceId</span></span>
<span data-ttu-id="81cf2-131">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="81cf2-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="81cf2-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81cf2-132">-Confirm</span></span>
<span data-ttu-id="81cf2-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81cf2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81cf2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cf2-134">-WhatIf</span></span>
<span data-ttu-id="81cf2-135">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="81cf2-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="81cf2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cf2-136">CommonParameters</span></span>
<span data-ttu-id="81cf2-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81cf2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cf2-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81cf2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cf2-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81cf2-139">INPUTS</span></span>

### <span data-ttu-id="81cf2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="81cf2-140">System.String</span></span>

## <span data-ttu-id="81cf2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81cf2-141">OUTPUTS</span></span>

### <span data-ttu-id="81cf2-142">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="81cf2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="81cf2-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81cf2-143">NOTES</span></span>

## <span data-ttu-id="81cf2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81cf2-144">RELATED LINKS</span></span>

[<span data-ttu-id="81cf2-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81cf2-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="81cf2-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81cf2-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="81cf2-147">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81cf2-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="81cf2-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81cf2-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
