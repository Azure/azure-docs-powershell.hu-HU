---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: d93cd05122d0a2c321ef4ab6d858f975e84bc9a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496244"
---
# <span data-ttu-id="67dc9-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="67dc9-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="67dc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="67dc9-103">Leállít egy pieline a Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="67dc9-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67dc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67dc9-104">SYNTAX</span></span>

### <span data-ttu-id="67dc9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67dc9-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67dc9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67dc9-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67dc9-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="67dc9-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67dc9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="67dc9-108">DESCRIPTION</span></span>
<span data-ttu-id="67dc9-109">A **stop-AzureRmDataFactoryV2PipelineRun** parancsmag leállítja a pieline futtatási azonosítójával megadott adatgyárban lévő csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="67dc9-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="67dc9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="67dc9-110">EXAMPLES</span></span>

### <span data-ttu-id="67dc9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="67dc9-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="67dc9-112">Ez a parancs a gyári WikiADF az azonosító b9730a13-AA12-4926-a8b3-8e3a974ab0bd leállítja a csővezeték futtatását.</span><span class="sxs-lookup"><span data-stu-id="67dc9-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="67dc9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67dc9-113">PARAMETERS</span></span>

### <span data-ttu-id="67dc9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc9-114">-DataFactory</span></span>
<span data-ttu-id="67dc9-115">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="67dc9-115">The data factory object.</span></span>

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

### <span data-ttu-id="67dc9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="67dc9-116">-DataFactoryName</span></span>
<span data-ttu-id="67dc9-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="67dc9-117">The data factory name.</span></span>

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

### <span data-ttu-id="67dc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67dc9-118">-DefaultProfile</span></span>
<span data-ttu-id="67dc9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67dc9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67dc9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67dc9-120">-InputObject</span></span>
<span data-ttu-id="67dc9-121">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="67dc9-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="67dc9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67dc9-122">-PassThru</span></span>
<span data-ttu-id="67dc9-123">Ha meg van adva, akkor a parancsmag az igaz értéket adja meg, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="67dc9-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="67dc9-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="67dc9-124">-PipelineRunId</span></span>
<span data-ttu-id="67dc9-125">A csővezeték Run azonosítója.</span><span class="sxs-lookup"><span data-stu-id="67dc9-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="67dc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67dc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="67dc9-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="67dc9-127">The resource group name.</span></span>

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

### <span data-ttu-id="67dc9-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67dc9-128">-Confirm</span></span>
<span data-ttu-id="67dc9-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67dc9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67dc9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67dc9-130">-WhatIf</span></span>
<span data-ttu-id="67dc9-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67dc9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67dc9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67dc9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67dc9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67dc9-133">CommonParameters</span></span>
<span data-ttu-id="67dc9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67dc9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67dc9-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67dc9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67dc9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67dc9-136">INPUTS</span></span>

### <span data-ttu-id="67dc9-137">Microsoft. Azure. Command. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="67dc9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="67dc9-138">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="67dc9-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="67dc9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="67dc9-139">System.String</span></span>

### <span data-ttu-id="67dc9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="67dc9-141">Paraméterek: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="67dc9-141">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="67dc9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67dc9-142">OUTPUTS</span></span>

### <span data-ttu-id="67dc9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67dc9-143">System.Boolean</span></span>

## <span data-ttu-id="67dc9-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67dc9-144">NOTES</span></span>

## <span data-ttu-id="67dc9-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67dc9-145">RELATED LINKS</span></span>
