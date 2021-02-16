---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208735"
---
# <span data-ttu-id="43f52-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="43f52-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="43f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43f52-102">SYNOPSIS</span></span>
<span data-ttu-id="43f52-103">Létrehoz egy prognózist a Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="43f52-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="43f52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43f52-104">SYNTAX</span></span>

### <span data-ttu-id="43f52-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43f52-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43f52-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="43f52-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f52-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43f52-107">DESCRIPTION</span></span>
<span data-ttu-id="43f52-108">A **New-AzDataFactoryPipeline** parancsmag létrehoz egy folyamatot az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="43f52-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="43f52-109">Ha egy már létező folyamat nevét adja meg, a parancsmag megerősítést kér, mielőtt lecseréli a folyamatot.</span><span class="sxs-lookup"><span data-stu-id="43f52-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="43f52-110">Ha a *Force* paramétert adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő folyamatot.</span><span class="sxs-lookup"><span data-stu-id="43f52-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="43f52-111">Ezeket a műveleteket a következő sorrendben végezze el:</span><span class="sxs-lookup"><span data-stu-id="43f52-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="43f52-112">Adatüzem létrehozása</span><span class="sxs-lookup"><span data-stu-id="43f52-112">Create a data factory.</span></span> 
- <span data-ttu-id="43f52-113">Csatolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="43f52-113">Create linked services.</span></span> 
- <span data-ttu-id="43f52-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="43f52-114">Create datasets.</span></span> 
- <span data-ttu-id="43f52-115">Folyamat létrehozása</span><span class="sxs-lookup"><span data-stu-id="43f52-115">Create a pipeline.</span></span>
<span data-ttu-id="43f52-116">Ha egy azonos nevű folyamat már létezik az adatüzemben, ez a parancsmag megkérdezi, hogy felül kell-e írnia a meglévő prognózist az új folyamattal.</span><span class="sxs-lookup"><span data-stu-id="43f52-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="43f52-117">Ha megerősíti, hogy felülírja a meglévő folyamatot, a program a folyamatdefiníciót is lecseréli.</span><span class="sxs-lookup"><span data-stu-id="43f52-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="43f52-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43f52-118">EXAMPLES</span></span>

### <span data-ttu-id="43f52-119">1. példa: Folyamat létrehozása</span><span class="sxs-lookup"><span data-stu-id="43f52-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="43f52-120">Ez a parancs létrehoz egy DPWikisample nevű prognózist az ADF nevű adatüzemben.</span><span class="sxs-lookup"><span data-stu-id="43f52-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="43f52-121">A parancs a folyamat alapja a fájlon DPWikisample.jsadatok.</span><span class="sxs-lookup"><span data-stu-id="43f52-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="43f52-122">Ez a fájl információkat tartalmaz a folyamat tevékenységeiről, például a Másolási tevékenység és a HDInsight-tevékenységről.</span><span class="sxs-lookup"><span data-stu-id="43f52-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="43f52-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43f52-123">PARAMETERS</span></span>

### <span data-ttu-id="43f52-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="43f52-124">-DataFactory</span></span>
<span data-ttu-id="43f52-125">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="43f52-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="43f52-126">Ez a parancsmag létrehoz egy folyamatot a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="43f52-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f52-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="43f52-127">-DataFactoryName</span></span>
<span data-ttu-id="43f52-128">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43f52-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="43f52-129">Ez a parancsmag létrehoz egy folyamatot a paraméter által megadott adat factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="43f52-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="43f52-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f52-130">-DefaultProfile</span></span>
<span data-ttu-id="43f52-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43f52-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43f52-132">-File</span><span class="sxs-lookup"><span data-stu-id="43f52-132">-File</span></span>
<span data-ttu-id="43f52-133">A folyamat leírását tartalmazó JavaScript objektum-notation (JSON) fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43f52-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f52-134">-Force</span><span class="sxs-lookup"><span data-stu-id="43f52-134">-Force</span></span>
<span data-ttu-id="43f52-135">Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül lecserél egy meglévő folyamatot.</span><span class="sxs-lookup"><span data-stu-id="43f52-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="43f52-136">-Name</span><span class="sxs-lookup"><span data-stu-id="43f52-136">-Name</span></span>
<span data-ttu-id="43f52-137">A létrehozni szükséges folyamat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43f52-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f52-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f52-138">-ResourceGroupName</span></span>
<span data-ttu-id="43f52-139">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43f52-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="43f52-140">Ez a parancsmag létrehoz egy prognózist a paraméter által megadott csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="43f52-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="43f52-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43f52-141">-Confirm</span></span>
<span data-ttu-id="43f52-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="43f52-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f52-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f52-143">-WhatIf</span></span>
<span data-ttu-id="43f52-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="43f52-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f52-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43f52-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f52-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f52-146">CommonParameters</span></span>
<span data-ttu-id="43f52-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f52-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f52-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f52-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f52-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43f52-149">INPUTS</span></span>

### <span data-ttu-id="43f52-150">System.String</span><span class="sxs-lookup"><span data-stu-id="43f52-150">System.String</span></span>

### <span data-ttu-id="43f52-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="43f52-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="43f52-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43f52-152">OUTPUTS</span></span>

### <span data-ttu-id="43f52-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="43f52-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="43f52-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43f52-154">NOTES</span></span>
* <span data-ttu-id="43f52-155">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="43f52-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="43f52-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43f52-156">RELATED LINKS</span></span>

[<span data-ttu-id="43f52-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="43f52-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="43f52-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="43f52-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="43f52-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="43f52-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="43f52-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="43f52-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="43f52-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="43f52-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


