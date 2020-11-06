---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 510f0f5b943a1a0abab1bc97ac5e70fa6f450898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493821"
---
# <span data-ttu-id="ef5c7-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ef5c7-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="ef5c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5c7-103">Futószalagot hoz létre az adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef5c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef5c7-104">SYNTAX</span></span>

### <span data-ttu-id="ef5c7-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef5c7-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef5c7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef5c7-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef5c7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef5c7-107">DESCRIPTION</span></span>
<span data-ttu-id="ef5c7-108">Az Set-AzureRmDataFactoryV2Pipeline parancsmag létrehoz egy csővezetéket az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="ef5c7-109">Ha már létezik egy olyan csővezeték neve, amely már létezik, a parancsmag kéri a megerősítést, mielőtt felülírja a futószalagot.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="ef5c7-110">Ha az erő paramétert adja meg, a parancsmag megerősítés nélkül lecseréli a meglévő csővezetéket.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="ef5c7-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="ef5c7-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="ef5c7-112">Ha az adatfeldolgozóban már létezik egy azonos nevű csővezeték, ez a parancsmag arra kéri, hogy erősítse meg, hogy felülírja-e a meglévő csővezetéket az új adatkapcsolattal.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="ef5c7-113">Ha a meglévő csővezeték felülírását erősítse meg, a program a csővezeték-definíciót is lecseréli.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="ef5c7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="ef5c7-114">EXAMPLES</span></span>

### <span data-ttu-id="ef5c7-115">Példa 1: csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="ef5c7-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="ef5c7-116">Ez a parancs létrehoz egy DPWikisample nevű csővezetéket az ADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="ef5c7-117">A parancs a munkafolyamatot a fájl DPWikisample.jsban lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="ef5c7-118">Ez a fájl olyan tevékenységekre vonatkozó információkat tartalmaz, mint például a folyamat másolása és a HDInsight tevékenység a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="ef5c7-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef5c7-119">PARAMETERS</span></span>

### <span data-ttu-id="ef5c7-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef5c7-120">-Confirm</span></span>
<span data-ttu-id="ef5c7-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef5c7-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ef5c7-122">-DataFactoryName</span></span>
<span data-ttu-id="ef5c7-123">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ef5c7-124">Ez a parancsmag létrehoz egy csővezetéket az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef5c7-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ef5c7-125">-DefinitionFile</span></span>
<span data-ttu-id="ef5c7-126">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-126">The JSON file path.</span></span>

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

### <span data-ttu-id="ef5c7-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ef5c7-127">-Force</span></span>
<span data-ttu-id="ef5c7-128">Azt jelzi, hogy ez a parancsmag egy meglévő csővezetéket cserél le, nem kell megerősítést kérnie.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ef5c7-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef5c7-129">-Name</span></span>
<span data-ttu-id="ef5c7-130">A létrehozandó csővezeték nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-130">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="ef5c7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5c7-131">-ResourceGroupName</span></span>
<span data-ttu-id="ef5c7-132">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ef5c7-133">Ez a parancsmag létrehoz egy futószalagot annak a csoportnak, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef5c7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef5c7-134">-ResourceId</span></span>
<span data-ttu-id="ef5c7-135">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ef5c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef5c7-136">-WhatIf</span></span>
<span data-ttu-id="ef5c7-137">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ef5c7-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5c7-138">-DefaultProfile</span></span>
<span data-ttu-id="ef5c7-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef5c7-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef5c7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5c7-140">CommonParameters</span></span>
<span data-ttu-id="ef5c7-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef5c7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5c7-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5c7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5c7-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef5c7-143">INPUTS</span></span>

### <span data-ttu-id="ef5c7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ef5c7-144">System.String</span></span>

## <span data-ttu-id="ef5c7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef5c7-145">OUTPUTS</span></span>

### <span data-ttu-id="ef5c7-146">Microsoft. Azure. Command. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ef5c7-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="ef5c7-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef5c7-147">NOTES</span></span>
<span data-ttu-id="ef5c7-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="ef5c7-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ef5c7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef5c7-149">RELATED LINKS</span></span>

[<span data-ttu-id="ef5c7-150">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ef5c7-150">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ef5c7-151">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ef5c7-151">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ef5c7-152">Meghívó-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ef5c7-152">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
