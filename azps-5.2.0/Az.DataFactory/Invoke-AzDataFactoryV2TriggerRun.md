---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370759"
---
# <span data-ttu-id="9064b-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="9064b-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="9064b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9064b-102">SYNOPSIS</span></span>
 <span data-ttu-id="9064b-103">Egy eseményindító futtatásának egy másik példányát hívja meg.</span><span class="sxs-lookup"><span data-stu-id="9064b-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="9064b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9064b-104">SYNTAX</span></span>

### <span data-ttu-id="9064b-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9064b-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9064b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9064b-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9064b-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="9064b-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9064b-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9064b-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9064b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9064b-109">DESCRIPTION</span></span>
<span data-ttu-id="9064b-110">Az **Invoke-AzDataFactoryV2TriggerRun parancs** egy újabb eseményindító-futtatáspéldányt indít új eseményindító-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="9064b-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="9064b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9064b-111">EXAMPLES</span></span>

### <span data-ttu-id="9064b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9064b-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="9064b-113">Egy eseményindító másik példányát indítja el egy új eseményindító futtatásának azonosítójával, és megtartja az eredeti eseményindító futtatásával egy időben aStartTime és a windowEndTime ablakot.</span><span class="sxs-lookup"><span data-stu-id="9064b-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="9064b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9064b-114">PARAMETERS</span></span>

### <span data-ttu-id="9064b-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9064b-115">-DataFactory</span></span>
<span data-ttu-id="9064b-116">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="9064b-116">The data factory object.</span></span>

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

### <span data-ttu-id="9064b-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9064b-117">-DataFactoryName</span></span>
<span data-ttu-id="9064b-118">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="9064b-118">The data factory name.</span></span>

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

### <span data-ttu-id="9064b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9064b-119">-DefaultProfile</span></span>
<span data-ttu-id="9064b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9064b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9064b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9064b-121">-InputObject</span></span>
<span data-ttu-id="9064b-122">Az eseményindítóval kapcsolatos információk lefutnak.</span><span class="sxs-lookup"><span data-stu-id="9064b-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="9064b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9064b-123">-PassThru</span></span>
<span data-ttu-id="9064b-124">Ha a parancsmag írása igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="9064b-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="9064b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9064b-125">-ResourceGroupName</span></span>
<span data-ttu-id="9064b-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9064b-126">The resource group name.</span></span>

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

### <span data-ttu-id="9064b-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="9064b-127">-TriggerName</span></span>
<span data-ttu-id="9064b-128">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="9064b-128">The trigger name.</span></span>

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

### <span data-ttu-id="9064b-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="9064b-129">-TriggerRunId</span></span>
<span data-ttu-id="9064b-130">Az eseményindító futtatásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="9064b-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="9064b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9064b-131">-Confirm</span></span>
<span data-ttu-id="9064b-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9064b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9064b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9064b-133">-WhatIf</span></span>
<span data-ttu-id="9064b-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9064b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9064b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9064b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9064b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9064b-136">CommonParameters</span></span>
<span data-ttu-id="9064b-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9064b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9064b-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9064b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9064b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9064b-139">INPUTS</span></span>

### <span data-ttu-id="9064b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="9064b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="9064b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9064b-141">System.String</span></span>

### <span data-ttu-id="9064b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9064b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="9064b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9064b-143">OUTPUTS</span></span>

### <span data-ttu-id="9064b-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="9064b-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="9064b-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9064b-145">NOTES</span></span>

## <span data-ttu-id="9064b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9064b-146">RELATED LINKS</span></span>
