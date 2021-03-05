---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: b0058f21f472f14e97898ea81636fa000034bed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006933"
---
# <span data-ttu-id="912c8-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="912c8-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="912c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="912c8-102">SYNOPSIS</span></span>
<span data-ttu-id="912c8-103">Eseményindítót hoz létre egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="912c8-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="912c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="912c8-104">SYNTAX</span></span>

### <span data-ttu-id="912c8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="912c8-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="912c8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="912c8-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="912c8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="912c8-107">DESCRIPTION</span></span>
<span data-ttu-id="912c8-108">A **Set-AzDataFactoryV2Trigger** parancsmag létrehoz egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="912c8-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="912c8-109">Ha egy már létező eseményindító nevét adja meg, a parancsmag megerősítést kér az eseményindító cseréje előtt.</span><span class="sxs-lookup"><span data-stu-id="912c8-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="912c8-110">Ha a _Force_ paramétert adja meg, a parancsmag megerősítés kérése nélkül lecseréli a meglévő eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="912c8-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="912c8-111">Az eseményindítók "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem kezdődnek azonnal a hivatkozott prognózisok.</span><span class="sxs-lookup"><span data-stu-id="912c8-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="912c8-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="912c8-112">EXAMPLES</span></span>

### <span data-ttu-id="912c8-113">1. példa: Eseményindító létrehozása</span><span class="sxs-lookup"><span data-stu-id="912c8-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="912c8-114">Hozzon létre egy "ScheduledTrigger" nevű új eseményindítót a "WikiADF" adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="912c8-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="912c8-115">Az eseményindító "Leállítva" állapotban jön létre, ami azt jelenti, hogy nem indul el azonnal.</span><span class="sxs-lookup"><span data-stu-id="912c8-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="912c8-116">A parancsmag használatával elindítható egy `Start-AzDataFactoryV2Trigger` eseményindító.</span><span class="sxs-lookup"><span data-stu-id="912c8-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="912c8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="912c8-117">PARAMETERS</span></span>

### <span data-ttu-id="912c8-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="912c8-118">-DataFactoryName</span></span>
<span data-ttu-id="912c8-119">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="912c8-119">The data factory name.</span></span>

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

### <span data-ttu-id="912c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912c8-120">-DefaultProfile</span></span>
<span data-ttu-id="912c8-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="912c8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="912c8-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="912c8-122">-DefinitionFile</span></span>
<span data-ttu-id="912c8-123">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="912c8-123">The JSON file path.</span></span>

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

### <span data-ttu-id="912c8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="912c8-124">-Force</span></span>
<span data-ttu-id="912c8-125">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="912c8-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="912c8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="912c8-126">-Name</span></span>
<span data-ttu-id="912c8-127">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="912c8-127">The trigger name.</span></span>

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

### <span data-ttu-id="912c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="912c8-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="912c8-129">The resource group name.</span></span>

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

### <span data-ttu-id="912c8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="912c8-130">-ResourceId</span></span>
<span data-ttu-id="912c8-131">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="912c8-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="912c8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="912c8-132">-Confirm</span></span>
<span data-ttu-id="912c8-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="912c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="912c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="912c8-134">-WhatIf</span></span>
<span data-ttu-id="912c8-135">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="912c8-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="912c8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912c8-136">CommonParameters</span></span>
<span data-ttu-id="912c8-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912c8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912c8-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="912c8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912c8-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="912c8-139">INPUTS</span></span>

### <span data-ttu-id="912c8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="912c8-140">System.String</span></span>

## <span data-ttu-id="912c8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="912c8-141">OUTPUTS</span></span>

### <span data-ttu-id="912c8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="912c8-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="912c8-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="912c8-143">NOTES</span></span>

## <span data-ttu-id="912c8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="912c8-144">RELATED LINKS</span></span>

[<span data-ttu-id="912c8-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="912c8-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="912c8-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="912c8-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="912c8-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="912c8-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="912c8-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="912c8-148">Remove-AzDataFactoryV2Trigger</span></span>]()
