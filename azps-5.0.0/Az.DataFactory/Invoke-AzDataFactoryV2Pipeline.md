---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298466"
---
# <span data-ttu-id="4f748-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4f748-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="4f748-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f748-102">SYNOPSIS</span></span>
  <span data-ttu-id="4f748-103">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="4f748-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="4f748-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f748-104">SYNTAX</span></span>

### <span data-ttu-id="4f748-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f748-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f748-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="4f748-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f748-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="4f748-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f748-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="4f748-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f748-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f748-109">DESCRIPTION</span></span>
<span data-ttu-id="4f748-110">Az **AzDataFactoryV2Pipeline** parancs a megadott csővezetéken futtatja a futást, és a futtatott érték azonosítóját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4f748-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="4f748-111">Ezt a GUID-ot átadhatja a **Get-AzDataFactoryV2PipelineRun** vagy a **Get-AzDataFactoryV2ActivityRun** , ha további részleteket szeretne kapni erről a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="4f748-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="4f748-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4f748-112">EXAMPLES</span></span>

### <span data-ttu-id="4f748-113">1. példa: a futószalag indítását kezdeményezi a futtatáshoz</span><span class="sxs-lookup"><span data-stu-id="4f748-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="4f748-114">Ez a parancs elindítja a Run for "DPWikisample" ("WikiADF") csővezetéket az "" gyárban.</span><span class="sxs-lookup"><span data-stu-id="4f748-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="4f748-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="4f748-115">Example 2</span></span>

<span data-ttu-id="4f748-116">Arra hívja fel a futószalagot, hogy indítsa el a futtatását.</span><span class="sxs-lookup"><span data-stu-id="4f748-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="4f748-117">autogenerated</span><span class="sxs-lookup"><span data-stu-id="4f748-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="4f748-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f748-118">PARAMETERS</span></span>

### <span data-ttu-id="4f748-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4f748-119">-DataFactoryName</span></span>
<span data-ttu-id="4f748-120">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="4f748-120">The data factory name.</span></span>

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

### <span data-ttu-id="4f748-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f748-121">-DefaultProfile</span></span>
<span data-ttu-id="4f748-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f748-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f748-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f748-123">-InputObject</span></span>
<span data-ttu-id="4f748-124">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="4f748-124">The data factory object.</span></span>

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

### <span data-ttu-id="4f748-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="4f748-125">-IsRecovery</span></span>
<span data-ttu-id="4f748-126">Helyreállítási mód jelölője</span><span class="sxs-lookup"><span data-stu-id="4f748-126">Recovery mode flag.</span></span> <span data-ttu-id="4f748-127">Ha a helyreállítási mód True értékre van állítva, akkor a megadott hivatkozott csővezeték fut, és az új Futtatás ugyanabba a groupId lesz csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="4f748-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f748-128">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="4f748-128">-Parameter</span></span>
<span data-ttu-id="4f748-129">A csővezeték-Futtatás paraméterei.</span><span class="sxs-lookup"><span data-stu-id="4f748-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="4f748-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="4f748-130">-ParameterFile</span></span>
<span data-ttu-id="4f748-131">Annak a fájlnak a neve, amelyen a csővezeték-Futtatás paraméterei láthatók.</span><span class="sxs-lookup"><span data-stu-id="4f748-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="4f748-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4f748-132">-PipelineName</span></span>
<span data-ttu-id="4f748-133">A csővezeték neve.</span><span class="sxs-lookup"><span data-stu-id="4f748-133">The pipeline name.</span></span>

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

### <span data-ttu-id="4f748-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4f748-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="4f748-135">Az újraindításhoz használt pipeline-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4f748-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="4f748-136">Ha meg van adva a futtatási azonosító, a program a megadott Futtatás paramétereit fogja használni az új Futtatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="4f748-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f748-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f748-137">-ResourceGroupName</span></span>
<span data-ttu-id="4f748-138">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f748-138">The resource group name.</span></span>

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

### <span data-ttu-id="4f748-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="4f748-139">-StartActivityName</span></span>
<span data-ttu-id="4f748-140">Helyreállítási módban a program az ismétlést ebből a tevékenységből kezdi.</span><span class="sxs-lookup"><span data-stu-id="4f748-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="4f748-141">Ha nincs megadva, a program minden tevékenységet futtat.</span><span class="sxs-lookup"><span data-stu-id="4f748-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f748-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="4f748-142">-StartFromFailure</span></span>
<span data-ttu-id="4f748-143">Indítsa újra a sikertelen tevékenységek jelölőt.</span><span class="sxs-lookup"><span data-stu-id="4f748-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="4f748-144">Ha meg van adva a helyreállítási mód, az újrakezdés sikertelen tevékenységekről fog kezdődni.</span><span class="sxs-lookup"><span data-stu-id="4f748-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f748-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f748-145">-Confirm</span></span>
<span data-ttu-id="4f748-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f748-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f748-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f748-147">-WhatIf</span></span>
<span data-ttu-id="4f748-148">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4f748-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4f748-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f748-149">CommonParameters</span></span>
<span data-ttu-id="4f748-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f748-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f748-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4f748-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f748-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f748-152">INPUTS</span></span>

### <span data-ttu-id="4f748-153">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="4f748-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="4f748-154">System. String</span><span class="sxs-lookup"><span data-stu-id="4f748-154">System.String</span></span>

### <span data-ttu-id="4f748-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f748-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f748-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f748-156">OUTPUTS</span></span>

### <span data-ttu-id="4f748-157">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="4f748-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="4f748-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f748-158">NOTES</span></span>

## <span data-ttu-id="4f748-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f748-159">RELATED LINKS</span></span>

[<span data-ttu-id="4f748-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4f748-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="4f748-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="4f748-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

