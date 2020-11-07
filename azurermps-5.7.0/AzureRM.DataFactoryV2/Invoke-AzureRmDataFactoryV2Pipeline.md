---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 1503d7307c38c72eece2eb7cb3d6e9f1543be8bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680173"
---
# <span data-ttu-id="1e6c2-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1e6c2-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="1e6c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e6c2-102">SYNOPSIS</span></span>
  <span data-ttu-id="1e6c2-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e6c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e6c2-104">SYNTAX</span></span>

### <span data-ttu-id="1e6c2-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e6c2-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e6c2-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e6c2-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e6c2-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e6c2-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e6c2-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="1e6c2-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e6c2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e6c2-109">DESCRIPTION</span></span>
<span data-ttu-id="1e6c2-110">Az **AzureRmDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="1e6c2-111">Ezt a GUID-ot átadhatja a **Get-AzureRmDataFactoryV2PipelineRun** vagy a **Get-AzureRmDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="1e6c2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1e6c2-112">EXAMPLES</span></span>

### <span data-ttu-id="1e6c2-113">1. példa: a futószalag indítását kezdeményezi a futtatáshoz</span><span class="sxs-lookup"><span data-stu-id="1e6c2-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="1e6c2-114">Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="1e6c2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e6c2-115">PARAMETERS</span></span>

### <span data-ttu-id="1e6c2-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1e6c2-116">-DataFactoryName</span></span>
<span data-ttu-id="1e6c2-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-117">The data factory name.</span></span>

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

### <span data-ttu-id="1e6c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c2-118">-DefaultProfile</span></span>
<span data-ttu-id="1e6c2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e6c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e6c2-120">-InputObject</span></span>
<span data-ttu-id="1e6c2-121">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-121">The data factory object.</span></span>

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

### <span data-ttu-id="1e6c2-122">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="1e6c2-122">-Parameter</span></span>
<span data-ttu-id="1e6c2-123">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1e6c2-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="1e6c2-124">-ParameterFile</span></span>
<span data-ttu-id="1e6c2-125">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="1e6c2-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="1e6c2-126">-PipelineName</span></span>
<span data-ttu-id="1e6c2-127">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-127">The pipeline name.</span></span>

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

### <span data-ttu-id="1e6c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="1e6c2-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-129">The resource group name.</span></span>

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

### <span data-ttu-id="1e6c2-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e6c2-130">-Confirm</span></span>
<span data-ttu-id="1e6c2-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6c2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6c2-132">-WhatIf</span></span>
<span data-ttu-id="1e6c2-133">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1e6c2-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1e6c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6c2-134">CommonParameters</span></span>
<span data-ttu-id="1e6c2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e6c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6c2-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6c2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e6c2-137">INPUTS</span></span>

### <span data-ttu-id="1e6c2-138">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1e6c2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="1e6c2-139">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e6c2-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e6c2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e6c2-140">OUTPUTS</span></span>

### <span data-ttu-id="1e6c2-141">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1e6c2-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="1e6c2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e6c2-142">NOTES</span></span>

## <span data-ttu-id="1e6c2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e6c2-143">RELATED LINKS</span></span>

[<span data-ttu-id="1e6c2-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="1e6c2-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="1e6c2-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="1e6c2-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

