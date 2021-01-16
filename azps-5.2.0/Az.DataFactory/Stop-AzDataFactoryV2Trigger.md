---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358327"
---
# <span data-ttu-id="31285-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31285-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="31285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31285-102">SYNOPSIS</span></span>
<span data-ttu-id="31285-103">Leállít egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="31285-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="31285-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="31285-104">SYNTAX</span></span>

### <span data-ttu-id="31285-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31285-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31285-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31285-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31285-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="31285-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31285-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="31285-108">DESCRIPTION</span></span>
<span data-ttu-id="31285-109">A **Stop-AzDataFactoryV2Trigger** parancsmag leállít egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="31285-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="31285-110">Ha az eseményindító "Elindítva" állapotban van, a parancsmag leállítja az eseményindítót, és a továbbiakban nem indítja el a folyamatokat.</span><span class="sxs-lookup"><span data-stu-id="31285-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="31285-111">Ha az eseményindító már "Leállítva" állapotban van, ennek a parancsmagnak nincs hatása.</span><span class="sxs-lookup"><span data-stu-id="31285-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="31285-112">Ha az Kényszerítés paraméter meg van adva, a parancsmag nem kéri a parancssort az eseményindító leállítása előtt.</span><span class="sxs-lookup"><span data-stu-id="31285-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="31285-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="31285-113">EXAMPLES</span></span>

### <span data-ttu-id="31285-114">1. példa: Eseményindító leállítása</span><span class="sxs-lookup"><span data-stu-id="31285-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="31285-115">Leállítja az "ScheduledTrigger" eseményindítót a "WikiADF" adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="31285-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="31285-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31285-116">PARAMETERS</span></span>

### <span data-ttu-id="31285-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="31285-117">-DataFactoryName</span></span>
<span data-ttu-id="31285-118">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="31285-118">The data factory name.</span></span>

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

### <span data-ttu-id="31285-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31285-119">-DefaultProfile</span></span>
<span data-ttu-id="31285-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31285-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31285-121">-Force</span><span class="sxs-lookup"><span data-stu-id="31285-121">-Force</span></span>
<span data-ttu-id="31285-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="31285-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="31285-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31285-123">-InputObject</span></span>
<span data-ttu-id="31285-124">Indítsa el az objektumot.</span><span class="sxs-lookup"><span data-stu-id="31285-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="31285-125">-Name</span><span class="sxs-lookup"><span data-stu-id="31285-125">-Name</span></span>
<span data-ttu-id="31285-126">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="31285-126">The trigger name.</span></span>

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

### <span data-ttu-id="31285-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31285-127">-ResourceGroupName</span></span>
<span data-ttu-id="31285-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="31285-128">The resource group name.</span></span>

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

### <span data-ttu-id="31285-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31285-129">-ResourceId</span></span>
<span data-ttu-id="31285-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="31285-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="31285-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31285-131">-Confirm</span></span>
<span data-ttu-id="31285-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="31285-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31285-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31285-133">-WhatIf</span></span>
<span data-ttu-id="31285-134">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="31285-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="31285-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31285-135">CommonParameters</span></span>
<span data-ttu-id="31285-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31285-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31285-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31285-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31285-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31285-138">INPUTS</span></span>

### <span data-ttu-id="31285-139">System.String</span><span class="sxs-lookup"><span data-stu-id="31285-139">System.String</span></span>

### <span data-ttu-id="31285-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="31285-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="31285-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31285-141">OUTPUTS</span></span>

### <span data-ttu-id="31285-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="31285-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="31285-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="31285-143">NOTES</span></span>

## <span data-ttu-id="31285-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31285-144">RELATED LINKS</span></span>

[<span data-ttu-id="31285-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31285-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="31285-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31285-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="31285-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31285-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="31285-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31285-148">Remove-AzDataFactoryV2Trigger</span></span>]()
