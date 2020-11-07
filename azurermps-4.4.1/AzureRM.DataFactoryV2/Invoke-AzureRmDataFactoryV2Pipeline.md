---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679784"
---
# <span data-ttu-id="8a665-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="8a665-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="8a665-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a665-102">SYNOPSIS</span></span>
  <span data-ttu-id="8a665-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="8a665-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a665-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a665-104">SYNTAX</span></span>

### <span data-ttu-id="8a665-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a665-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8a665-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="8a665-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8a665-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="8a665-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8a665-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="8a665-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8a665-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a665-109">DESCRIPTION</span></span>
<span data-ttu-id="8a665-110">Az **AzureRmDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8a665-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="8a665-111">Ezt a GUID-ot átadhatja a **Get-AzureRmDataFactoryV2PipelineRun** vagy a **Get-AzureRmDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="8a665-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="8a665-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8a665-112">EXAMPLES</span></span>

### <span data-ttu-id="8a665-113">1. példa: a futószalag indítását kezdeményezi a futtatáshoz</span><span class="sxs-lookup"><span data-stu-id="8a665-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="8a665-114">Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.</span><span class="sxs-lookup"><span data-stu-id="8a665-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="8a665-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a665-115">PARAMETERS</span></span>

### <span data-ttu-id="8a665-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a665-116">-Confirm</span></span>
<span data-ttu-id="8a665-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a665-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a665-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8a665-118">-DataFactoryName</span></span>
<span data-ttu-id="8a665-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="8a665-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="8a665-120">-ParameterFile</span></span>
<span data-ttu-id="8a665-121">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="8a665-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-122">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="8a665-122">-Parameter</span></span>
<span data-ttu-id="8a665-123">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="8a665-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a665-124">-InputObject</span></span>
<span data-ttu-id="8a665-125">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="8a665-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="8a665-126">-PipelineName</span></span>
<span data-ttu-id="8a665-127">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="8a665-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a665-128">-ResourceGroupName</span></span>
<span data-ttu-id="8a665-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8a665-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a665-130">-WhatIf</span></span>
<span data-ttu-id="8a665-131">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8a665-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="8a665-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a665-132">INPUTS</span></span>

### <span data-ttu-id="8a665-133">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8a665-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="8a665-134">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8a665-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="8a665-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a665-135">OUTPUTS</span></span>

### <span data-ttu-id="8a665-136">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="8a665-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="8a665-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a665-137">NOTES</span></span>

## <span data-ttu-id="8a665-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a665-138">RELATED LINKS</span></span>
[<span data-ttu-id="8a665-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8a665-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="8a665-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="8a665-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

