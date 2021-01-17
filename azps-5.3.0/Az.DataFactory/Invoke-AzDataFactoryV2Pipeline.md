---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477138"
---
# <span data-ttu-id="2efec-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="2efec-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="2efec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2efec-102">SYNOPSIS</span></span>
  <span data-ttu-id="2efec-103">Elindít egy folyamatot, hogy elindítsa a futtatásot.</span><span class="sxs-lookup"><span data-stu-id="2efec-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="2efec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2efec-104">SYNTAX</span></span>

### <span data-ttu-id="2efec-105">ByFactoryNameByParameterFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2efec-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efec-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="2efec-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efec-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="2efec-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2efec-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="2efec-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2efec-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2efec-109">DESCRIPTION</span></span>
<span data-ttu-id="2efec-110">Az **Invoke-AzDataFactoryV2Pipeline** parancs elindít egy futtatást a megadott folyamaton, és a futtatás azonosítóját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="2efec-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="2efec-111">Ez a GUID-azonosító a **Get-AzDataFactoryV2PipelineRun** vagy **a Get-AzDataFactoryV2ActivityRun** eszköznek is átadható, hogy további részleteket szerezzen a futtatásról.</span><span class="sxs-lookup"><span data-stu-id="2efec-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="2efec-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2efec-112">EXAMPLES</span></span>

### <span data-ttu-id="2efec-113">1. példa: Folyamat meghívása a futtatás indítani</span><span class="sxs-lookup"><span data-stu-id="2efec-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="2efec-114">Ez a parancs elindítja a "DPWikisample" folyamat futtatását a "WikiADF" factoryban.</span><span class="sxs-lookup"><span data-stu-id="2efec-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="2efec-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="2efec-115">Example 2</span></span>

<span data-ttu-id="2efec-116">Elindít egy folyamatot, hogy elindítsa a futtatásot.</span><span class="sxs-lookup"><span data-stu-id="2efec-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="2efec-117">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="2efec-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="2efec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2efec-118">PARAMETERS</span></span>

### <span data-ttu-id="2efec-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2efec-119">-DataFactoryName</span></span>
<span data-ttu-id="2efec-120">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="2efec-120">The data factory name.</span></span>

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

### <span data-ttu-id="2efec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efec-121">-DefaultProfile</span></span>
<span data-ttu-id="2efec-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2efec-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2efec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2efec-123">-InputObject</span></span>
<span data-ttu-id="2efec-124">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="2efec-124">The data factory object.</span></span>

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

### <span data-ttu-id="2efec-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="2efec-125">-IsRecovery</span></span>
<span data-ttu-id="2efec-126">Helyreállítási mód jelzője.</span><span class="sxs-lookup"><span data-stu-id="2efec-126">Recovery mode flag.</span></span> <span data-ttu-id="2efec-127">Ha a helyreállítási mód igazra van állítva, a megadott hivatkozott folyamat fut, és az új futtatás ugyanazon groupId csoportban lesz csoportosítva.</span><span class="sxs-lookup"><span data-stu-id="2efec-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="2efec-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2efec-128">-Parameter</span></span>
<span data-ttu-id="2efec-129">A folyamat futtatásának paraméterei.</span><span class="sxs-lookup"><span data-stu-id="2efec-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="2efec-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="2efec-130">-ParameterFile</span></span>
<span data-ttu-id="2efec-131">A fájl neve a folyamat futtatásához szükséges paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="2efec-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="2efec-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="2efec-132">-PipelineName</span></span>
<span data-ttu-id="2efec-133">A folyamat neve.</span><span class="sxs-lookup"><span data-stu-id="2efec-133">The pipeline name.</span></span>

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

### <span data-ttu-id="2efec-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="2efec-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="2efec-135">A pipeline run ID for rerun.</span><span class="sxs-lookup"><span data-stu-id="2efec-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="2efec-136">Ha a futtatásazonosító meg van adva, a megadott futtatás paramétereit használja a rendszer új futtatás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="2efec-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="2efec-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2efec-137">-ResourceGroupName</span></span>
<span data-ttu-id="2efec-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2efec-138">The resource group name.</span></span>

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

### <span data-ttu-id="2efec-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="2efec-139">-StartActivityName</span></span>
<span data-ttu-id="2efec-140">Helyreállítási módban az újrafuttatás ebből a tevékenységből indul ki.</span><span class="sxs-lookup"><span data-stu-id="2efec-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="2efec-141">Ha nincs megadva, az összes tevékenység futni fog.</span><span class="sxs-lookup"><span data-stu-id="2efec-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="2efec-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="2efec-142">-StartFromFailure</span></span>
<span data-ttu-id="2efec-143">Indítsa el az újrafuttatás jelölőt a sikertelen tevékenységekről.</span><span class="sxs-lookup"><span data-stu-id="2efec-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="2efec-144">Ha a helyreállítási mód meg van adva, az újrafuttatás sikertelen tevékenységekből indul.</span><span class="sxs-lookup"><span data-stu-id="2efec-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="2efec-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2efec-145">-Confirm</span></span>
<span data-ttu-id="2efec-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2efec-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2efec-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2efec-147">-WhatIf</span></span>
<span data-ttu-id="2efec-148">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2efec-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2efec-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efec-149">CommonParameters</span></span>
<span data-ttu-id="2efec-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2efec-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efec-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2efec-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efec-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2efec-152">INPUTS</span></span>

### <span data-ttu-id="2efec-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="2efec-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="2efec-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2efec-154">System.String</span></span>

### <span data-ttu-id="2efec-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2efec-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2efec-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2efec-156">OUTPUTS</span></span>

### <span data-ttu-id="2efec-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="2efec-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="2efec-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2efec-158">NOTES</span></span>

## <span data-ttu-id="2efec-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2efec-159">RELATED LINKS</span></span>

[<span data-ttu-id="2efec-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2efec-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="2efec-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="2efec-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

