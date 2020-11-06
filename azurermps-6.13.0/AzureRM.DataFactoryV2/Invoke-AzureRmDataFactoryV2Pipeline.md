---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e7bfd0b72f5dffe4e5ff4d7e52394846d5f17afa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494086"
---
# <span data-ttu-id="20082-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="20082-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="20082-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20082-102">SYNOPSIS</span></span>
  <span data-ttu-id="20082-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="20082-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20082-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20082-104">SYNTAX</span></span>

### <span data-ttu-id="20082-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20082-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20082-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="20082-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20082-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="20082-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20082-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="20082-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20082-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="20082-109">DESCRIPTION</span></span>
<span data-ttu-id="20082-110">Az **AzureRmDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="20082-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="20082-111">Ezt a GUID-ot átadhatja a **Get-AzureRmDataFactoryV2PipelineRun** vagy a **Get-AzureRmDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="20082-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="20082-112">Példák</span><span class="sxs-lookup"><span data-stu-id="20082-112">EXAMPLES</span></span>

### <span data-ttu-id="20082-113">1. példa: a futószalag indítását kezdeményezi a futtatáshoz</span><span class="sxs-lookup"><span data-stu-id="20082-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="20082-114">Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.</span><span class="sxs-lookup"><span data-stu-id="20082-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="20082-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20082-115">PARAMETERS</span></span>

### <span data-ttu-id="20082-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="20082-116">-DataFactoryName</span></span>
<span data-ttu-id="20082-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="20082-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20082-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20082-118">-DefaultProfile</span></span>
<span data-ttu-id="20082-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20082-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20082-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20082-120">-InputObject</span></span>
<span data-ttu-id="20082-121">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="20082-121">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20082-122">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="20082-122">-Parameter</span></span>
<span data-ttu-id="20082-123">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="20082-123">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20082-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="20082-124">-ParameterFile</span></span>
<span data-ttu-id="20082-125">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="20082-125">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20082-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="20082-126">-PipelineName</span></span>
<span data-ttu-id="20082-127">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="20082-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20082-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20082-128">-ResourceGroupName</span></span>
<span data-ttu-id="20082-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="20082-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20082-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20082-130">-Confirm</span></span>
<span data-ttu-id="20082-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20082-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20082-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20082-132">-WhatIf</span></span>
<span data-ttu-id="20082-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="20082-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="20082-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20082-134">CommonParameters</span></span>
<span data-ttu-id="20082-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20082-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20082-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20082-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20082-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20082-137">INPUTS</span></span>

### <span data-ttu-id="20082-138">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="20082-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="20082-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="20082-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="20082-140">System. String</span><span class="sxs-lookup"><span data-stu-id="20082-140">System.String</span></span>

### <span data-ttu-id="20082-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="20082-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="20082-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20082-142">OUTPUTS</span></span>

### <span data-ttu-id="20082-143">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="20082-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="20082-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20082-144">NOTES</span></span>

## <span data-ttu-id="20082-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20082-145">RELATED LINKS</span></span>

[<span data-ttu-id="20082-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="20082-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="20082-147">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="20082-147">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

