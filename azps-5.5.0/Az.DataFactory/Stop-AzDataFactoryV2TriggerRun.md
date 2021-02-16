---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162050"
---
# <span data-ttu-id="81293-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="81293-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="81293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81293-102">SYNOPSIS</span></span>
<span data-ttu-id="81293-103">Leállít egy eseményindítót egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="81293-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="81293-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81293-104">SYNTAX</span></span>

### <span data-ttu-id="81293-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81293-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81293-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81293-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81293-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81293-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81293-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81293-108">DESCRIPTION</span></span>
<span data-ttu-id="81293-109">A **Stop-AzDataFactoryV2TriggerRun** parancsmag leállít egy eseményindítót az eseményindító nevével és eseményindító-azonosítójával megadott adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="81293-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="81293-110">Jelenleg csak a WaitingOnDependency State verzióban támogatott TumblingWindowTwlers esetén.</span><span class="sxs-lookup"><span data-stu-id="81293-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="81293-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81293-111">EXAMPLES</span></span>

### <span data-ttu-id="81293-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="81293-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="81293-113">Ez a parancs leállítja a trigger futtatását a (0858600246800588497807248799CU16) azonosítóval a gyári WikiADF-ben.</span><span class="sxs-lookup"><span data-stu-id="81293-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="81293-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81293-114">PARAMETERS</span></span>

### <span data-ttu-id="81293-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="81293-115">-DataFactory</span></span>
<span data-ttu-id="81293-116">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="81293-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81293-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="81293-117">-DataFactoryName</span></span>
<span data-ttu-id="81293-118">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="81293-118">The data factory name.</span></span>

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

### <span data-ttu-id="81293-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81293-119">-DefaultProfile</span></span>
<span data-ttu-id="81293-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81293-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81293-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81293-121">-InputObject</span></span>
<span data-ttu-id="81293-122">Az eseményindítóval kapcsolatos információk lefutnak.</span><span class="sxs-lookup"><span data-stu-id="81293-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81293-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81293-123">-PassThru</span></span>
<span data-ttu-id="81293-124">Ha a parancsmag írása igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="81293-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="81293-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81293-125">-ResourceGroupName</span></span>
<span data-ttu-id="81293-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81293-126">The resource group name.</span></span>

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

### <span data-ttu-id="81293-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="81293-127">-TriggerName</span></span>
<span data-ttu-id="81293-128">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="81293-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81293-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="81293-129">-TriggerRunId</span></span>
<span data-ttu-id="81293-130">Az eseményindító futtatásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="81293-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81293-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81293-131">-Confirm</span></span>
<span data-ttu-id="81293-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="81293-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81293-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81293-133">-WhatIf</span></span>
<span data-ttu-id="81293-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="81293-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81293-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81293-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81293-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81293-136">CommonParameters</span></span>
<span data-ttu-id="81293-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81293-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81293-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81293-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81293-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81293-139">INPUTS</span></span>

### <span data-ttu-id="81293-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="81293-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="81293-141">System.String</span><span class="sxs-lookup"><span data-stu-id="81293-141">System.String</span></span>

### <span data-ttu-id="81293-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="81293-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="81293-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81293-143">OUTPUTS</span></span>

### <span data-ttu-id="81293-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="81293-144">System.Boolean</span></span>

## <span data-ttu-id="81293-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81293-145">NOTES</span></span>

## <span data-ttu-id="81293-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81293-146">RELATED LINKS</span></span>
