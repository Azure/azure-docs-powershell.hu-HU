---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 91eb23f3af613cf349219f82d133d08dd6e65b5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930122"
---
# <span data-ttu-id="2d366-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="2d366-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="2d366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d366-102">SYNOPSIS</span></span>
 <span data-ttu-id="2d366-103">Egy eseményindító futtatásának egy másik példányát hívja meg.</span><span class="sxs-lookup"><span data-stu-id="2d366-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="2d366-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d366-104">SYNTAX</span></span>

### <span data-ttu-id="2d366-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d366-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d366-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2d366-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d366-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="2d366-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d366-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2d366-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d366-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d366-109">DESCRIPTION</span></span>
<span data-ttu-id="2d366-110">Az **Invoke-AzDataFactoryV2TriggerRun parancs** egy újabb eseményindító-futtatáspéldányt indít új eseményindító-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="2d366-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="2d366-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d366-111">EXAMPLES</span></span>

### <span data-ttu-id="2d366-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2d366-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="2d366-113">Egy eseményindító másik példányát indítja el egy új eseményindító futtatásának azonosítójával, az eredeti eseményindítóval azonos windowStartTime és windowEndTime megtartásával.</span><span class="sxs-lookup"><span data-stu-id="2d366-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="2d366-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d366-114">PARAMETERS</span></span>

### <span data-ttu-id="2d366-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d366-115">-DataFactory</span></span>
<span data-ttu-id="2d366-116">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="2d366-116">The data factory object.</span></span>

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

### <span data-ttu-id="2d366-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2d366-117">-DataFactoryName</span></span>
<span data-ttu-id="2d366-118">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="2d366-118">The data factory name.</span></span>

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

### <span data-ttu-id="2d366-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d366-119">-DefaultProfile</span></span>
<span data-ttu-id="2d366-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d366-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d366-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d366-121">-InputObject</span></span>
<span data-ttu-id="2d366-122">Az eseményindítóval kapcsolatos információk lefutnak.</span><span class="sxs-lookup"><span data-stu-id="2d366-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="2d366-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d366-123">-PassThru</span></span>
<span data-ttu-id="2d366-124">Ha a parancsmag írása igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="2d366-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="2d366-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d366-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d366-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2d366-126">The resource group name.</span></span>

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

### <span data-ttu-id="2d366-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="2d366-127">-TriggerName</span></span>
<span data-ttu-id="2d366-128">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="2d366-128">The trigger name.</span></span>

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

### <span data-ttu-id="2d366-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="2d366-129">-TriggerRunId</span></span>
<span data-ttu-id="2d366-130">Az eseményindító futtatásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="2d366-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="2d366-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d366-131">-Confirm</span></span>
<span data-ttu-id="2d366-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2d366-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d366-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d366-133">-WhatIf</span></span>
<span data-ttu-id="2d366-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2d366-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d366-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d366-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d366-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d366-136">CommonParameters</span></span>
<span data-ttu-id="2d366-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d366-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d366-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d366-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d366-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d366-139">INPUTS</span></span>

### <span data-ttu-id="2d366-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="2d366-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="2d366-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2d366-141">System.String</span></span>

### <span data-ttu-id="2d366-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2d366-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2d366-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d366-143">OUTPUTS</span></span>

### <span data-ttu-id="2d366-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="2d366-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="2d366-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d366-145">NOTES</span></span>

## <span data-ttu-id="2d366-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d366-146">RELATED LINKS</span></span>
