---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 5af781170418ea2ab9e0dda9dcd06107e9e784bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667038"
---
# <span data-ttu-id="ccca9-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ccca9-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="ccca9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccca9-102">SYNOPSIS</span></span>
  <span data-ttu-id="ccca9-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="ccca9-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="ccca9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccca9-104">SYNTAX</span></span>

### <span data-ttu-id="ccca9-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccca9-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccca9-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="ccca9-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccca9-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="ccca9-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccca9-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="ccca9-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccca9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccca9-109">DESCRIPTION</span></span>
<span data-ttu-id="ccca9-110">Az **AzDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ccca9-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="ccca9-111">Ezt a GUID-ot átadhatja a **Get-AzDataFactoryV2PipelineRun** vagy a **Get-AzDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="ccca9-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="ccca9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ccca9-112">EXAMPLES</span></span>

### <span data-ttu-id="ccca9-113">1. példa: a futószalag indítását kezdeményezi a futtatáshoz</span><span class="sxs-lookup"><span data-stu-id="ccca9-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="ccca9-114">Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.</span><span class="sxs-lookup"><span data-stu-id="ccca9-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="ccca9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccca9-115">PARAMETERS</span></span>

### <span data-ttu-id="ccca9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ccca9-116">-DataFactoryName</span></span>
<span data-ttu-id="ccca9-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ccca9-117">The data factory name.</span></span>

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

### <span data-ttu-id="ccca9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccca9-118">-DefaultProfile</span></span>
<span data-ttu-id="ccca9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccca9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccca9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccca9-120">-InputObject</span></span>
<span data-ttu-id="ccca9-121">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="ccca9-121">The data factory object.</span></span>

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

### <span data-ttu-id="ccca9-122">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="ccca9-122">-Parameter</span></span>
<span data-ttu-id="ccca9-123">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="ccca9-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="ccca9-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="ccca9-124">-ParameterFile</span></span>
<span data-ttu-id="ccca9-125">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="ccca9-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="ccca9-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="ccca9-126">-PipelineName</span></span>
<span data-ttu-id="ccca9-127">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="ccca9-127">The pipeline name.</span></span>

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

### <span data-ttu-id="ccca9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccca9-128">-ResourceGroupName</span></span>
<span data-ttu-id="ccca9-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ccca9-129">The resource group name.</span></span>

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

### <span data-ttu-id="ccca9-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccca9-130">-Confirm</span></span>
<span data-ttu-id="ccca9-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccca9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccca9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccca9-132">-WhatIf</span></span>
<span data-ttu-id="ccca9-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ccca9-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ccca9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccca9-134">CommonParameters</span></span>
<span data-ttu-id="ccca9-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccca9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccca9-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccca9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccca9-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccca9-137">INPUTS</span></span>

### <span data-ttu-id="ccca9-138">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ccca9-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="ccca9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ccca9-139">System.String</span></span>

### <span data-ttu-id="ccca9-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ccca9-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ccca9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccca9-141">OUTPUTS</span></span>

### <span data-ttu-id="ccca9-142">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ccca9-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="ccca9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccca9-143">NOTES</span></span>

## <span data-ttu-id="ccca9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccca9-144">RELATED LINKS</span></span>

[<span data-ttu-id="ccca9-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ccca9-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="ccca9-146">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="ccca9-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

