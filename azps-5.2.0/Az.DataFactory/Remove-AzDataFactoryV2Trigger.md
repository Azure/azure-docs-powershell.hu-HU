---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365733"
---
# <span data-ttu-id="24221-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24221-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="24221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24221-102">SYNOPSIS</span></span>
<span data-ttu-id="24221-103">Eltávolít egy eseményindítót egy adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="24221-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="24221-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="24221-104">SYNTAX</span></span>

### <span data-ttu-id="24221-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24221-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24221-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24221-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24221-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24221-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24221-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="24221-108">DESCRIPTION</span></span>
<span data-ttu-id="24221-109">A **Remove-AzDataFactoryV2Trigger** parancsmag eltávolít egy eseményindítót egy adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="24221-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="24221-110">Ha az _Kényszerítés_ paraméter meg van adva, a parancsmag nem kéri a parancsmagot az eseményindító eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="24221-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="24221-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="24221-111">EXAMPLES</span></span>

### <span data-ttu-id="24221-112">1. példa: Eseményindító eltávolítása</span><span class="sxs-lookup"><span data-stu-id="24221-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="24221-113">Távolítsa el az "ScheduledTrigger" eseményindítót a "WikiADF" adat factoryból.</span><span class="sxs-lookup"><span data-stu-id="24221-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="24221-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24221-114">PARAMETERS</span></span>

### <span data-ttu-id="24221-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24221-115">-DataFactoryName</span></span>
<span data-ttu-id="24221-116">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="24221-116">The data factory name.</span></span>

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

### <span data-ttu-id="24221-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24221-117">-DefaultProfile</span></span>
<span data-ttu-id="24221-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24221-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24221-119">-Force</span><span class="sxs-lookup"><span data-stu-id="24221-119">-Force</span></span>
<span data-ttu-id="24221-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="24221-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="24221-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24221-121">-InputObject</span></span>
<span data-ttu-id="24221-122">Az eltávolítható Eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="24221-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="24221-123">-Name</span><span class="sxs-lookup"><span data-stu-id="24221-123">-Name</span></span>
<span data-ttu-id="24221-124">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="24221-124">The trigger name.</span></span>

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

### <span data-ttu-id="24221-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24221-125">-ResourceGroupName</span></span>
<span data-ttu-id="24221-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24221-126">The resource group name.</span></span>

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

### <span data-ttu-id="24221-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24221-127">-ResourceId</span></span>
<span data-ttu-id="24221-128">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="24221-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24221-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24221-129">-Confirm</span></span>
<span data-ttu-id="24221-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="24221-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24221-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24221-131">-WhatIf</span></span>
<span data-ttu-id="24221-132">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="24221-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="24221-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24221-133">CommonParameters</span></span>
<span data-ttu-id="24221-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24221-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24221-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24221-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24221-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24221-136">INPUTS</span></span>

### <span data-ttu-id="24221-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="24221-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="24221-138">System.String</span><span class="sxs-lookup"><span data-stu-id="24221-138">System.String</span></span>

## <span data-ttu-id="24221-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24221-139">OUTPUTS</span></span>

### <span data-ttu-id="24221-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24221-140">System.Boolean</span></span>

## <span data-ttu-id="24221-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="24221-141">NOTES</span></span>

## <span data-ttu-id="24221-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24221-142">RELATED LINKS</span></span>

[<span data-ttu-id="24221-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24221-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24221-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24221-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24221-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24221-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24221-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24221-146">Stop-AzDataFactoryV2Trigger</span></span>]()

