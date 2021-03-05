---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: df23225193b0b7fe057b13b5114bb3ce227d584e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009638"
---
# <span data-ttu-id="85efc-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="85efc-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="85efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85efc-102">SYNOPSIS</span></span>
<span data-ttu-id="85efc-103">Eltávolít egy eseményindítót egy adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="85efc-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="85efc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85efc-104">SYNTAX</span></span>

### <span data-ttu-id="85efc-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85efc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85efc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="85efc-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85efc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="85efc-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85efc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85efc-108">DESCRIPTION</span></span>
<span data-ttu-id="85efc-109">A **Remove-AzDataFactoryV2Trigger** parancsmag eltávolít egy eseményindítót egy adatüzemből.</span><span class="sxs-lookup"><span data-stu-id="85efc-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="85efc-110">Ha az _Kényszerítés_ paraméter meg van adva, a parancsmag nem kéri a parancsmagot az eseményindító eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="85efc-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="85efc-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85efc-111">EXAMPLES</span></span>

### <span data-ttu-id="85efc-112">1. példa: Eseményindító eltávolítása</span><span class="sxs-lookup"><span data-stu-id="85efc-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="85efc-113">Távolítsa el az "ScheduledTrigger" eseményindítót a "WikiADF" adat factoryból.</span><span class="sxs-lookup"><span data-stu-id="85efc-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="85efc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85efc-114">PARAMETERS</span></span>

### <span data-ttu-id="85efc-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="85efc-115">-DataFactoryName</span></span>
<span data-ttu-id="85efc-116">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="85efc-116">The data factory name.</span></span>

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

### <span data-ttu-id="85efc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85efc-117">-DefaultProfile</span></span>
<span data-ttu-id="85efc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85efc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85efc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="85efc-119">-Force</span></span>
<span data-ttu-id="85efc-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="85efc-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="85efc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85efc-121">-InputObject</span></span>
<span data-ttu-id="85efc-122">Az eltávolítható Eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="85efc-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="85efc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="85efc-123">-Name</span></span>
<span data-ttu-id="85efc-124">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="85efc-124">The trigger name.</span></span>

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

### <span data-ttu-id="85efc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85efc-125">-ResourceGroupName</span></span>
<span data-ttu-id="85efc-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="85efc-126">The resource group name.</span></span>

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

### <span data-ttu-id="85efc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85efc-127">-ResourceId</span></span>
<span data-ttu-id="85efc-128">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="85efc-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="85efc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85efc-129">-Confirm</span></span>
<span data-ttu-id="85efc-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="85efc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85efc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85efc-131">-WhatIf</span></span>
<span data-ttu-id="85efc-132">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="85efc-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="85efc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85efc-133">CommonParameters</span></span>
<span data-ttu-id="85efc-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85efc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85efc-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85efc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85efc-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85efc-136">INPUTS</span></span>

### <span data-ttu-id="85efc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="85efc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="85efc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="85efc-138">System.String</span></span>

## <span data-ttu-id="85efc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85efc-139">OUTPUTS</span></span>

### <span data-ttu-id="85efc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85efc-140">System.Boolean</span></span>

## <span data-ttu-id="85efc-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85efc-141">NOTES</span></span>

## <span data-ttu-id="85efc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85efc-142">RELATED LINKS</span></span>

[<span data-ttu-id="85efc-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="85efc-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="85efc-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="85efc-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="85efc-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="85efc-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="85efc-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="85efc-146">Stop-AzDataFactoryV2Trigger</span></span>]()

