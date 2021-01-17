---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480374"
---
# <span data-ttu-id="d8c67-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d8c67-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="d8c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c67-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c67-103">Leállít egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="d8c67-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="d8c67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8c67-104">SYNTAX</span></span>

### <span data-ttu-id="d8c67-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8c67-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c67-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d8c67-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c67-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c67-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c67-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8c67-108">DESCRIPTION</span></span>
<span data-ttu-id="d8c67-109">A **Stop-AzDataFactoryV2Trigger** parancsmag leállít egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="d8c67-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="d8c67-110">Ha az eseményindító "Elindítva" állapotban van, a parancsmag leállítja az eseményindítót, és a továbbiakban nem indítja el a folyamatokat.</span><span class="sxs-lookup"><span data-stu-id="d8c67-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="d8c67-111">Ha az eseményindító már "Leállítva" állapotban van, ennek a parancsmagnak nincs hatása.</span><span class="sxs-lookup"><span data-stu-id="d8c67-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="d8c67-112">Ha az Kényszerítés paraméter meg van adva, a parancsmag nem kéri a parancssort az eseményindító leállítása előtt.</span><span class="sxs-lookup"><span data-stu-id="d8c67-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="d8c67-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8c67-113">EXAMPLES</span></span>

### <span data-ttu-id="d8c67-114">1. példa: Eseményindító leállítása</span><span class="sxs-lookup"><span data-stu-id="d8c67-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="d8c67-115">Leállítja az "ScheduledTrigger" eseményindítót a "WikiADF" adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="d8c67-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="d8c67-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8c67-116">PARAMETERS</span></span>

### <span data-ttu-id="d8c67-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8c67-117">-DataFactoryName</span></span>
<span data-ttu-id="d8c67-118">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="d8c67-118">The data factory name.</span></span>

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

### <span data-ttu-id="d8c67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c67-119">-DefaultProfile</span></span>
<span data-ttu-id="d8c67-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8c67-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8c67-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d8c67-121">-Force</span></span>
<span data-ttu-id="d8c67-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="d8c67-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d8c67-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8c67-123">-InputObject</span></span>
<span data-ttu-id="d8c67-124">Indítsa el az objektumot.</span><span class="sxs-lookup"><span data-stu-id="d8c67-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="d8c67-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d8c67-125">-Name</span></span>
<span data-ttu-id="d8c67-126">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="d8c67-126">The trigger name.</span></span>

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

### <span data-ttu-id="d8c67-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c67-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8c67-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8c67-128">The resource group name.</span></span>

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

### <span data-ttu-id="d8c67-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c67-129">-ResourceId</span></span>
<span data-ttu-id="d8c67-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="d8c67-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d8c67-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8c67-131">-Confirm</span></span>
<span data-ttu-id="d8c67-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8c67-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c67-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c67-133">-WhatIf</span></span>
<span data-ttu-id="d8c67-134">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d8c67-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d8c67-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c67-135">CommonParameters</span></span>
<span data-ttu-id="d8c67-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c67-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c67-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c67-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c67-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8c67-138">INPUTS</span></span>

### <span data-ttu-id="d8c67-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d8c67-139">System.String</span></span>

### <span data-ttu-id="d8c67-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d8c67-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="d8c67-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8c67-141">OUTPUTS</span></span>

### <span data-ttu-id="d8c67-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d8c67-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="d8c67-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8c67-143">NOTES</span></span>

## <span data-ttu-id="d8c67-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8c67-144">RELATED LINKS</span></span>

[<span data-ttu-id="d8c67-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d8c67-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d8c67-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d8c67-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d8c67-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d8c67-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d8c67-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d8c67-148">Remove-AzDataFactoryV2Trigger</span></span>]()
