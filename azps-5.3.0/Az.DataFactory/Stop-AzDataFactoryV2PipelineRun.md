---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477053"
---
# <span data-ttu-id="03d85-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="03d85-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="03d85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03d85-102">SYNOPSIS</span></span>
<span data-ttu-id="03d85-103">Leállítja egy folyamat futtatását egy adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="03d85-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="03d85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03d85-104">SYNTAX</span></span>

### <span data-ttu-id="03d85-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03d85-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03d85-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03d85-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03d85-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="03d85-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03d85-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03d85-108">DESCRIPTION</span></span>
<span data-ttu-id="03d85-109">A **Stop-AzDataFactoryV2PipelineRun parancsmag** leállítja a folyamatot egy, a folyamatfuttassa azonosítóval megadott adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="03d85-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="03d85-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03d85-110">EXAMPLES</span></span>

### <span data-ttu-id="03d85-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="03d85-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="03d85-112">Ez a parancs leállítja a prognózis futtatását a b9730a13-aa12-4926-a8b3-8e3a974ab0bd azonosítóval a WikiADF gyári wikiadF-ben.</span><span class="sxs-lookup"><span data-stu-id="03d85-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="03d85-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03d85-113">PARAMETERS</span></span>

### <span data-ttu-id="03d85-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="03d85-114">-DataFactory</span></span>
<span data-ttu-id="03d85-115">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="03d85-115">The data factory object.</span></span>

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

### <span data-ttu-id="03d85-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="03d85-116">-DataFactoryName</span></span>
<span data-ttu-id="03d85-117">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="03d85-117">The data factory name.</span></span>

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

### <span data-ttu-id="03d85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d85-118">-DefaultProfile</span></span>
<span data-ttu-id="03d85-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03d85-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03d85-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03d85-120">-InputObject</span></span>
<span data-ttu-id="03d85-121">A folyamat futtatásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="03d85-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03d85-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03d85-122">-PassThru</span></span>
<span data-ttu-id="03d85-123">Ha a parancsmag írása igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="03d85-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="03d85-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="03d85-124">-PipelineRunId</span></span>
<span data-ttu-id="03d85-125">A folyamat futtatásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="03d85-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="03d85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03d85-126">-ResourceGroupName</span></span>
<span data-ttu-id="03d85-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03d85-127">The resource group name.</span></span>

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

### <span data-ttu-id="03d85-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03d85-128">-Confirm</span></span>
<span data-ttu-id="03d85-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03d85-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03d85-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03d85-130">-WhatIf</span></span>
<span data-ttu-id="03d85-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03d85-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03d85-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03d85-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03d85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d85-133">CommonParameters</span></span>
<span data-ttu-id="03d85-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d85-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03d85-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d85-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03d85-136">INPUTS</span></span>

### <span data-ttu-id="03d85-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="03d85-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="03d85-138">System.String</span><span class="sxs-lookup"><span data-stu-id="03d85-138">System.String</span></span>

### <span data-ttu-id="03d85-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="03d85-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="03d85-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03d85-140">OUTPUTS</span></span>

### <span data-ttu-id="03d85-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03d85-141">System.Boolean</span></span>

## <span data-ttu-id="03d85-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03d85-142">NOTES</span></span>

## <span data-ttu-id="03d85-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03d85-143">RELATED LINKS</span></span>
