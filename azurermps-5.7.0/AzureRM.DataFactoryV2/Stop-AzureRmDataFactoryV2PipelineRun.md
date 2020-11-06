---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 7ddbc2809c58172eea2cd98ce048e0e49fbb14f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495417"
---
# <span data-ttu-id="ccf67-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ccf67-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="ccf67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccf67-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf67-103">Leállít egy pieline a Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="ccf67-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccf67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccf67-104">SYNTAX</span></span>

### <span data-ttu-id="ccf67-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccf67-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccf67-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ccf67-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf67-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ccf67-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf67-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccf67-108">DESCRIPTION</span></span>
<span data-ttu-id="ccf67-109">A **stop-AzureRmDataFactoryV2PipelineRun** parancsmag leállítja a pieline futtatási azonosítójával megadott adatgyárban lévő csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="ccf67-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="ccf67-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ccf67-110">EXAMPLES</span></span>

### <span data-ttu-id="ccf67-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccf67-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="ccf67-112">Ez a parancs a gyári WikiADF az azonosító b9730a13-AA12-4926-a8b3-8e3a974ab0bd leállítja a csővezeték futtatását.</span><span class="sxs-lookup"><span data-stu-id="ccf67-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="ccf67-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccf67-113">PARAMETERS</span></span>

### <span data-ttu-id="ccf67-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ccf67-114">-DataFactory</span></span>
<span data-ttu-id="ccf67-115">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="ccf67-115">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ccf67-116">-DataFactoryName</span></span>
<span data-ttu-id="ccf67-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ccf67-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf67-118">-DefaultProfile</span></span>
<span data-ttu-id="ccf67-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccf67-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccf67-120">-InputObject</span></span>
<span data-ttu-id="ccf67-121">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ccf67-121">The Run ID of the pipeline.</span></span>

```yaml
Type: PSPipelineRun
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccf67-122">-PassThru</span></span>
<span data-ttu-id="ccf67-123">Ha meg van adva, akkor a parancsmag az igaz értéket adja meg, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="ccf67-123">If specified the cmdlet write true in case operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="ccf67-124">-PipelineRunId</span></span>
<span data-ttu-id="ccf67-125">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ccf67-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf67-126">-ResourceGroupName</span></span>
<span data-ttu-id="ccf67-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ccf67-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccf67-128">-Confirm</span></span>
<span data-ttu-id="ccf67-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccf67-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf67-130">-WhatIf</span></span>
<span data-ttu-id="ccf67-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccf67-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf67-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccf67-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf67-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf67-133">CommonParameters</span></span>
<span data-ttu-id="ccf67-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccf67-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf67-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf67-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf67-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccf67-136">INPUTS</span></span>

### <span data-ttu-id="ccf67-137">Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="ccf67-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="ccf67-138">System. String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ccf67-138">System.String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ccf67-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccf67-139">OUTPUTS</span></span>

### <span data-ttu-id="ccf67-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccf67-140">System.Boolean</span></span>

## <span data-ttu-id="ccf67-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccf67-141">NOTES</span></span>

## <span data-ttu-id="ccf67-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccf67-142">RELATED LINKS</span></span>

