---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153459"
---
# <span data-ttu-id="95239-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95239-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="95239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95239-102">SYNOPSIS</span></span>
<span data-ttu-id="95239-103">Elindít egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="95239-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="95239-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95239-104">SYNTAX</span></span>

### <span data-ttu-id="95239-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95239-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95239-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="95239-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95239-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="95239-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95239-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95239-108">DESCRIPTION</span></span>
<span data-ttu-id="95239-109">A **Start-AzDataFactoryV2Trigger** parancsmag elindít egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="95239-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="95239-110">Ha az eseményindító "Leállítva" állapotban van, a parancsmag elindítja az eseményindítót, és végül a definíciója alapján meghívja a prognózisokat.</span><span class="sxs-lookup"><span data-stu-id="95239-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="95239-111">Ha az eseményindító már "Elindítva" állapotban van, ennek a parancsmagnak nincs hatása.</span><span class="sxs-lookup"><span data-stu-id="95239-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="95239-112">Ha az Kényszerítés paraméter meg van adva, a parancsmag nem kéri a parancsmagot az eseményindító indítása előtt.</span><span class="sxs-lookup"><span data-stu-id="95239-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="95239-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95239-113">EXAMPLES</span></span>

### <span data-ttu-id="95239-114">1. példa: Eseményindító kezdése</span><span class="sxs-lookup"><span data-stu-id="95239-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="95239-115">Elindít egy "ScheduledTrigger" eseményindítót a "WikiADF" adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="95239-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="95239-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95239-116">PARAMETERS</span></span>

### <span data-ttu-id="95239-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="95239-117">-DataFactoryName</span></span>
<span data-ttu-id="95239-118">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="95239-118">The data factory name.</span></span>

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

### <span data-ttu-id="95239-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95239-119">-DefaultProfile</span></span>
<span data-ttu-id="95239-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95239-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95239-121">-Force</span><span class="sxs-lookup"><span data-stu-id="95239-121">-Force</span></span>
<span data-ttu-id="95239-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="95239-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="95239-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95239-123">-InputObject</span></span>
<span data-ttu-id="95239-124">Indítsa el az objektumot.</span><span class="sxs-lookup"><span data-stu-id="95239-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="95239-125">-Name</span><span class="sxs-lookup"><span data-stu-id="95239-125">-Name</span></span>
<span data-ttu-id="95239-126">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="95239-126">The trigger name.</span></span>

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

### <span data-ttu-id="95239-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95239-127">-ResourceGroupName</span></span>
<span data-ttu-id="95239-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="95239-128">The resource group name.</span></span>

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

### <span data-ttu-id="95239-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95239-129">-ResourceId</span></span>
<span data-ttu-id="95239-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="95239-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="95239-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95239-131">-Confirm</span></span>
<span data-ttu-id="95239-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="95239-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95239-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95239-133">-WhatIf</span></span>
<span data-ttu-id="95239-134">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="95239-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="95239-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95239-135">CommonParameters</span></span>
<span data-ttu-id="95239-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95239-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95239-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95239-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95239-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95239-138">INPUTS</span></span>

### <span data-ttu-id="95239-139">System.String</span><span class="sxs-lookup"><span data-stu-id="95239-139">System.String</span></span>

### <span data-ttu-id="95239-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="95239-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="95239-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95239-141">OUTPUTS</span></span>

### <span data-ttu-id="95239-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="95239-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="95239-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95239-143">NOTES</span></span>

## <span data-ttu-id="95239-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95239-144">RELATED LINKS</span></span>

[<span data-ttu-id="95239-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95239-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="95239-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95239-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="95239-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95239-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="95239-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95239-148">Remove-AzDataFactoryV2Trigger</span></span>]()
