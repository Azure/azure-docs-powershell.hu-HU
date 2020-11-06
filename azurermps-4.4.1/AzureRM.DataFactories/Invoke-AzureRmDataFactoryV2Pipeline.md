---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: a7486c3fc50e5c6517022190e05d099329fc6001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497108"
---
# <span data-ttu-id="60eb7-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="60eb7-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="60eb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60eb7-102">SYNOPSIS</span></span>
  <span data-ttu-id="60eb7-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="60eb7-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60eb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60eb7-104">SYNTAX</span></span>

### <span data-ttu-id="60eb7-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60eb7-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60eb7-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="60eb7-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60eb7-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="60eb7-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60eb7-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="60eb7-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60eb7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="60eb7-109">DESCRIPTION</span></span>
<span data-ttu-id="60eb7-110">Az **AzureRmDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="60eb7-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="60eb7-111">Ezt a GUID-ot átadhatja a **Get-AzureRmDataFactoryV2PipelineRun** vagy a **Get-AzureRmDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="60eb7-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="60eb7-112">Példák</span><span class="sxs-lookup"><span data-stu-id="60eb7-112">EXAMPLES</span></span>

### <span data-ttu-id="60eb7-113">1. példa: a futószalag indítását kezdeményezi a futtatáshoz</span><span class="sxs-lookup"><span data-stu-id="60eb7-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="60eb7-114">Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.</span><span class="sxs-lookup"><span data-stu-id="60eb7-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="60eb7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60eb7-115">PARAMETERS</span></span>

### <span data-ttu-id="60eb7-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60eb7-116">-Confirm</span></span>
<span data-ttu-id="60eb7-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60eb7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60eb7-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="60eb7-118">-DataFactoryName</span></span>
<span data-ttu-id="60eb7-119">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="60eb7-119">The data factory name.</span></span>

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

### <span data-ttu-id="60eb7-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="60eb7-120">-ParameterFile</span></span>
<span data-ttu-id="60eb7-121">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="60eb7-121">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="60eb7-122">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="60eb7-122">-Parameter</span></span>
<span data-ttu-id="60eb7-123">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="60eb7-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="60eb7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60eb7-124">-InputObject</span></span>
<span data-ttu-id="60eb7-125">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="60eb7-125">The data factory object.</span></span>

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

### <span data-ttu-id="60eb7-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="60eb7-126">-PipelineName</span></span>
<span data-ttu-id="60eb7-127">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="60eb7-127">The pipeline name.</span></span>

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

### <span data-ttu-id="60eb7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60eb7-128">-ResourceGroupName</span></span>
<span data-ttu-id="60eb7-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="60eb7-129">The resource group name.</span></span>

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

### <span data-ttu-id="60eb7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60eb7-130">-WhatIf</span></span>
<span data-ttu-id="60eb7-131">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="60eb7-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="60eb7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60eb7-132">-DefaultProfile</span></span>
<span data-ttu-id="60eb7-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60eb7-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60eb7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60eb7-134">CommonParameters</span></span>
<span data-ttu-id="60eb7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60eb7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60eb7-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60eb7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60eb7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60eb7-137">INPUTS</span></span>

### <span data-ttu-id="60eb7-138">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="60eb7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="60eb7-139">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="60eb7-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="60eb7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60eb7-140">OUTPUTS</span></span>

### <span data-ttu-id="60eb7-141">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="60eb7-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="60eb7-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60eb7-142">NOTES</span></span>

## <span data-ttu-id="60eb7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60eb7-143">RELATED LINKS</span></span>

[<span data-ttu-id="60eb7-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="60eb7-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="60eb7-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="60eb7-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

