---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847114"
---
# <span data-ttu-id="a9d5b-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9d5b-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="a9d5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d5b-103">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="a9d5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9d5b-104">SYNTAX</span></span>

### <span data-ttu-id="a9d5b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9d5b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d5b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9d5b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d5b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9d5b-107">DESCRIPTION</span></span>
<span data-ttu-id="a9d5b-108">Az Set-AzDataFactoryV2Pipeline parancsmag létrehoz egy csővezetéket az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="a9d5b-109">Ha már létezik egy olyan csővezeték neve, amely már létezik, a parancsmag kéri a megerősítést, mielőtt felülírja a futószalagot.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="a9d5b-110">Ha az erő paramétert adja meg, a parancsmag megerősítés nélkül lecseréli a meglévő csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="a9d5b-111">Végezze el ezeket a műveleteket a következő sorrendben:-------hoz létre egy adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="a9d5b-112">– Kapcsolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-112">-- Create linked services.</span></span>
<span data-ttu-id="a9d5b-113">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-113">-- Create datasets.</span></span>
<span data-ttu-id="a9d5b-114">– Csővezeték létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-114">-- Create a pipeline.</span></span>
<span data-ttu-id="a9d5b-115">Ha az adatfeldolgozóban már létezik egy azonos nevű csővezeték, ez a parancsmag arra kéri, hogy erősítse meg, hogy felülírja-e a meglévő csővezetéket az új adatkapcsolattal.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="a9d5b-116">Ha a meglévő csővezeték felülírását erősítse meg, a program a csővezeték-definíciót is lecseréli.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="a9d5b-117">Példák</span><span class="sxs-lookup"><span data-stu-id="a9d5b-117">EXAMPLES</span></span>

### <span data-ttu-id="a9d5b-118">Példa 1: csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="a9d5b-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="a9d5b-119">Ez a parancs létrehoz egy DPWikisample nevű csővezetéket az ADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="a9d5b-120">A parancs a munkafolyamatot a fájl DPWikisample.jsban lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="a9d5b-121">Ez a fájl olyan tevékenységekre vonatkozó információkat tartalmaz, mint például a folyamat másolása és a HDInsight tevékenység a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="a9d5b-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9d5b-122">PARAMETERS</span></span>

### <span data-ttu-id="a9d5b-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a9d5b-123">-DataFactoryName</span></span>
<span data-ttu-id="a9d5b-124">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a9d5b-125">Ez a parancsmag létrehoz egy csővezetéket az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9d5b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d5b-126">-DefaultProfile</span></span>
<span data-ttu-id="a9d5b-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d5b-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a9d5b-128">-DefinitionFile</span></span>
<span data-ttu-id="a9d5b-129">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-129">The JSON file path.</span></span>

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

### <span data-ttu-id="a9d5b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a9d5b-130">-Force</span></span>
<span data-ttu-id="a9d5b-131">Azt jelzi, hogy ez a parancsmag egy meglévő csővezetéket cserél le, nem kell megerősítést kérnie.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a9d5b-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9d5b-132">-Name</span></span>
<span data-ttu-id="a9d5b-133">A létrehozandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="a9d5b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d5b-134">-ResourceGroupName</span></span>
<span data-ttu-id="a9d5b-135">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a9d5b-136">Ez a parancsmag létrehoz egy futószalagot annak a csoportnak, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9d5b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9d5b-137">-ResourceId</span></span>
<span data-ttu-id="a9d5b-138">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a9d5b-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9d5b-139">-Confirm</span></span>
<span data-ttu-id="a9d5b-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d5b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d5b-141">-WhatIf</span></span>
<span data-ttu-id="a9d5b-142">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a9d5b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d5b-143">CommonParameters</span></span>
<span data-ttu-id="a9d5b-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9d5b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d5b-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d5b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d5b-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9d5b-146">INPUTS</span></span>

### <span data-ttu-id="a9d5b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d5b-147">System.String</span></span>

## <span data-ttu-id="a9d5b-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9d5b-148">OUTPUTS</span></span>

### <span data-ttu-id="a9d5b-149">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a9d5b-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="a9d5b-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9d5b-150">NOTES</span></span>
<span data-ttu-id="a9d5b-151">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="a9d5b-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a9d5b-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9d5b-152">RELATED LINKS</span></span>

[<span data-ttu-id="a9d5b-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9d5b-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a9d5b-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9d5b-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a9d5b-155">Meghívó-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9d5b-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
