---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477061"
---
# <span data-ttu-id="c2501-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c2501-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="c2501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2501-102">SYNOPSIS</span></span>
<span data-ttu-id="c2501-103">Létrehoz egy prognózist a Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="c2501-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="c2501-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2501-104">SYNTAX</span></span>

### <span data-ttu-id="c2501-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2501-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2501-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2501-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2501-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2501-107">DESCRIPTION</span></span>
<span data-ttu-id="c2501-108">A Set-AzDataFactoryV2Pipeline parancsmag létrehoz egy folyamatot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="c2501-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="c2501-109">Ha egy már létező folyamat nevét adja meg, a parancsmag megerősítést kér, mielőtt lecseréli a folyamatot.</span><span class="sxs-lookup"><span data-stu-id="c2501-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="c2501-110">Ha a Force paramétert adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő folyamatot.</span><span class="sxs-lookup"><span data-stu-id="c2501-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="c2501-111">Végezze el ezeket a műveleteket a következő sorrendben: - Adatüzem létrehozása.</span><span class="sxs-lookup"><span data-stu-id="c2501-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="c2501-112">– Csatolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="c2501-112">-- Create linked services.</span></span>
<span data-ttu-id="c2501-113">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="c2501-113">-- Create datasets.</span></span>
<span data-ttu-id="c2501-114">– Folyamat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="c2501-114">-- Create a pipeline.</span></span>
<span data-ttu-id="c2501-115">Ha egy azonos nevű folyamat már létezik az adatüzemben, ez a parancsmag megkérdezi, hogy felül kell-e írnia a meglévő prognózist az új folyamattal.</span><span class="sxs-lookup"><span data-stu-id="c2501-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="c2501-116">Ha megerősíti, hogy felülírja a meglévő folyamatot, a program a folyamatdefiníciót is lecseréli.</span><span class="sxs-lookup"><span data-stu-id="c2501-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="c2501-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2501-117">EXAMPLES</span></span>

### <span data-ttu-id="c2501-118">1. példa: Folyamat létrehozása</span><span class="sxs-lookup"><span data-stu-id="c2501-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="c2501-119">Ez a parancs létrehoz egy DPWikisample nevű prognózist az ADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="c2501-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="c2501-120">A parancs a folyamat alapja a fájlon DPWikisample.jsadatok.</span><span class="sxs-lookup"><span data-stu-id="c2501-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="c2501-121">Ez a fájl információkat tartalmaz a folyamat tevékenységeiről, például a Másolási tevékenység és a HDInsight-tevékenységről.</span><span class="sxs-lookup"><span data-stu-id="c2501-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="c2501-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2501-122">PARAMETERS</span></span>

### <span data-ttu-id="c2501-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c2501-123">-DataFactoryName</span></span>
<span data-ttu-id="c2501-124">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2501-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c2501-125">Ez a parancsmag létrehoz egy folyamatot a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="c2501-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c2501-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2501-126">-DefaultProfile</span></span>
<span data-ttu-id="c2501-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2501-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2501-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c2501-128">-DefinitionFile</span></span>
<span data-ttu-id="c2501-129">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c2501-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2501-130">-Force</span><span class="sxs-lookup"><span data-stu-id="c2501-130">-Force</span></span>
<span data-ttu-id="c2501-131">Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül lecserél egy meglévő folyamatot.</span><span class="sxs-lookup"><span data-stu-id="c2501-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c2501-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c2501-132">-Name</span></span>
<span data-ttu-id="c2501-133">A létrehozni szükséges folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2501-133">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2501-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2501-134">-ResourceGroupName</span></span>
<span data-ttu-id="c2501-135">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2501-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c2501-136">Ez a parancsmag létrehoz egy prognózist a paraméter által megadott csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c2501-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c2501-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2501-137">-ResourceId</span></span>
<span data-ttu-id="c2501-138">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="c2501-138">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2501-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2501-139">-Confirm</span></span>
<span data-ttu-id="c2501-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c2501-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2501-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2501-141">-WhatIf</span></span>
<span data-ttu-id="c2501-142">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c2501-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c2501-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2501-143">CommonParameters</span></span>
<span data-ttu-id="c2501-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2501-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2501-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2501-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2501-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2501-146">INPUTS</span></span>

### <span data-ttu-id="c2501-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c2501-147">System.String</span></span>

## <span data-ttu-id="c2501-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2501-148">OUTPUTS</span></span>

### <span data-ttu-id="c2501-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c2501-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="c2501-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2501-150">NOTES</span></span>
<span data-ttu-id="c2501-151">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="c2501-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c2501-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2501-152">RELATED LINKS</span></span>

[<span data-ttu-id="c2501-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c2501-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c2501-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c2501-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c2501-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c2501-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
