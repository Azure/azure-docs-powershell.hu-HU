---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298190"
---
# <span data-ttu-id="08c2e-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="08c2e-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="08c2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="08c2e-103">Az adatgyárban futó csővezeték leállítása</span><span class="sxs-lookup"><span data-stu-id="08c2e-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="08c2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08c2e-104">SYNTAX</span></span>

### <span data-ttu-id="08c2e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08c2e-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08c2e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="08c2e-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08c2e-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="08c2e-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c2e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="08c2e-108">DESCRIPTION</span></span>
<span data-ttu-id="08c2e-109">A **stop-AzDataFactoryV2PipelineRun** parancsmag a PIPELINE Run azonosítóval megadott adatgyárban leállítja a csővezeték futását.</span><span class="sxs-lookup"><span data-stu-id="08c2e-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="08c2e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="08c2e-110">EXAMPLES</span></span>

### <span data-ttu-id="08c2e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08c2e-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="08c2e-112">Ez a parancs a gyári WikiADF az azonosító b9730a13-AA12-4926-a8b3-8e3a974ab0bd leállítja a csővezeték futtatását.</span><span class="sxs-lookup"><span data-stu-id="08c2e-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="08c2e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08c2e-113">PARAMETERS</span></span>

### <span data-ttu-id="08c2e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="08c2e-114">-DataFactory</span></span>
<span data-ttu-id="08c2e-115">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="08c2e-115">The data factory object.</span></span>

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

### <span data-ttu-id="08c2e-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="08c2e-116">-DataFactoryName</span></span>
<span data-ttu-id="08c2e-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="08c2e-117">The data factory name.</span></span>

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

### <span data-ttu-id="08c2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c2e-118">-DefaultProfile</span></span>
<span data-ttu-id="08c2e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08c2e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08c2e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08c2e-120">-InputObject</span></span>
<span data-ttu-id="08c2e-121">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="08c2e-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="08c2e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08c2e-122">-PassThru</span></span>
<span data-ttu-id="08c2e-123">Ha meg van adva, akkor a parancsmag az igaz értéket adja meg, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="08c2e-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="08c2e-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="08c2e-124">-PipelineRunId</span></span>
<span data-ttu-id="08c2e-125">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="08c2e-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="08c2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="08c2e-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="08c2e-127">The resource group name.</span></span>

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

### <span data-ttu-id="08c2e-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08c2e-128">-Confirm</span></span>
<span data-ttu-id="08c2e-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08c2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c2e-130">-WhatIf</span></span>
<span data-ttu-id="08c2e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08c2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08c2e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08c2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c2e-133">CommonParameters</span></span>
<span data-ttu-id="08c2e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08c2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c2e-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c2e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c2e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08c2e-136">INPUTS</span></span>

### <span data-ttu-id="08c2e-137">Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="08c2e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="08c2e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="08c2e-138">System.String</span></span>

### <span data-ttu-id="08c2e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="08c2e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="08c2e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08c2e-140">OUTPUTS</span></span>

### <span data-ttu-id="08c2e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08c2e-141">System.Boolean</span></span>

## <span data-ttu-id="08c2e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08c2e-142">NOTES</span></span>

## <span data-ttu-id="08c2e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08c2e-143">RELATED LINKS</span></span>
