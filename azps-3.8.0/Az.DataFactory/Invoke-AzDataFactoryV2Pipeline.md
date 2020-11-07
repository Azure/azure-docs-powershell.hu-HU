---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 87d4cfadd183a6aa2652b86336b4dc8d089936fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847241"
---
# <span data-ttu-id="f7b38-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f7b38-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f7b38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7b38-102">SYNOPSIS</span></span>
  <span data-ttu-id="f7b38-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="f7b38-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="f7b38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7b38-104">SYNTAX</span></span>

### <span data-ttu-id="f7b38-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7b38-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b38-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="f7b38-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b38-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="f7b38-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b38-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="f7b38-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b38-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7b38-109">DESCRIPTION</span></span>
<span data-ttu-id="f7b38-110">Az **AzDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f7b38-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="f7b38-111">Ezt a GUID-ot átadhatja a **Get-AzDataFactoryV2PipelineRun** vagy a **Get-AzDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="f7b38-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="f7b38-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f7b38-112">EXAMPLES</span></span>

### <span data-ttu-id="f7b38-113">1. példa: a futószalag indítását kezdeményezi a futtatáshoz</span><span class="sxs-lookup"><span data-stu-id="f7b38-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="f7b38-114">Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.</span><span class="sxs-lookup"><span data-stu-id="f7b38-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="f7b38-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7b38-115">PARAMETERS</span></span>

### <span data-ttu-id="f7b38-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f7b38-116">-DataFactoryName</span></span>
<span data-ttu-id="f7b38-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="f7b38-117">The data factory name.</span></span>

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

### <span data-ttu-id="f7b38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b38-118">-DefaultProfile</span></span>
<span data-ttu-id="f7b38-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7b38-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7b38-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7b38-120">-InputObject</span></span>
<span data-ttu-id="f7b38-121">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="f7b38-121">The data factory object.</span></span>

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

### <span data-ttu-id="f7b38-122">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="f7b38-122">-Parameter</span></span>
<span data-ttu-id="f7b38-123">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="f7b38-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="f7b38-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="f7b38-124">-ParameterFile</span></span>
<span data-ttu-id="f7b38-125">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="f7b38-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="f7b38-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f7b38-126">-PipelineName</span></span>
<span data-ttu-id="f7b38-127">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="f7b38-127">The pipeline name.</span></span>

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

### <span data-ttu-id="f7b38-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b38-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7b38-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7b38-129">The resource group name.</span></span>

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

### <span data-ttu-id="f7b38-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7b38-130">-Confirm</span></span>
<span data-ttu-id="f7b38-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7b38-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b38-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b38-132">-WhatIf</span></span>
<span data-ttu-id="f7b38-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f7b38-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f7b38-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b38-134">CommonParameters</span></span>
<span data-ttu-id="f7b38-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7b38-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b38-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b38-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b38-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b38-137">INPUTS</span></span>

### <span data-ttu-id="f7b38-138">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f7b38-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="f7b38-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f7b38-139">System.String</span></span>

### <span data-ttu-id="f7b38-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7b38-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f7b38-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7b38-141">OUTPUTS</span></span>

### <span data-ttu-id="f7b38-142">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f7b38-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="f7b38-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7b38-143">NOTES</span></span>

## <span data-ttu-id="f7b38-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7b38-144">RELATED LINKS</span></span>

[<span data-ttu-id="f7b38-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f7b38-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="f7b38-146">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="f7b38-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

