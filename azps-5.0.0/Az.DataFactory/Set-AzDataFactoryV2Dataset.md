---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298253"
---
# <span data-ttu-id="4b3f6-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b3f6-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="4b3f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3f6-103">Adatkészletet hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="4b3f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b3f6-104">SYNTAX</span></span>

### <span data-ttu-id="4b3f6-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b3f6-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b3f6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b3f6-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b3f6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b3f6-107">DESCRIPTION</span></span>
<span data-ttu-id="4b3f6-108">Az Set-AzDataFactoryV2Dataset parancsmag létrehoz egy adatkészletet az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="4b3f6-109">Ha olyan adatkészletet ad meg, amely már létezik, ez a parancsmag az adatkészlet visszavonása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="4b3f6-110">Ha az erő paramétert adja meg, a parancsmag a létező adatkészletet megerősítés nélkül cseréli le.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="4b3f6-111">Végezze el ezeket a műveleteket a következő sorrendben:-------hoz létre egy adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="4b3f6-112">– Kapcsolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-112">-- Create linked services.</span></span>
<span data-ttu-id="4b3f6-113">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-113">-- Create datasets.</span></span>
<span data-ttu-id="4b3f6-114">– Csővezeték létrehozása.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-114">-- Create a pipeline.</span></span>
<span data-ttu-id="4b3f6-115">Ha az adatfeldolgozóban már létezik azonos nevű adatkészlet, ez a parancsmag arra kéri, hogy erősítse meg, hogy felülírja-e a meglévő adatkészletet az új adatkészlettel.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="4b3f6-116">Ha a meglévő adatkészlet felülírásának megerősítését hagyja jóvá, az adatkészlet-definíciót is lecseréli a program.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="4b3f6-117">Példák</span><span class="sxs-lookup"><span data-stu-id="4b3f6-117">EXAMPLES</span></span>

### <span data-ttu-id="4b3f6-118">1. példa: adatkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="4b3f6-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="4b3f6-119">A parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="4b3f6-120">A parancs az adatkészletet az DAWikipediaClickEvents.jsfájlon lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="4b3f6-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b3f6-121">PARAMETERS</span></span>

### <span data-ttu-id="4b3f6-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4b3f6-122">-DataFactoryName</span></span>
<span data-ttu-id="4b3f6-123">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4b3f6-124">Ez a parancsmag létrehoz egy adatkészletet az adatgyárban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b3f6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3f6-125">-DefaultProfile</span></span>
<span data-ttu-id="4b3f6-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b3f6-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4b3f6-127">-DefinitionFile</span></span>
<span data-ttu-id="4b3f6-128">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-128">The JSON file path.</span></span>

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

### <span data-ttu-id="4b3f6-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4b3f6-129">-Force</span></span>
<span data-ttu-id="4b3f6-130">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4b3f6-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b3f6-131">-Name</span></span>
<span data-ttu-id="4b3f6-132">A létrehozandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b3f6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b3f6-133">-ResourceGroupName</span></span>
<span data-ttu-id="4b3f6-134">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4b3f6-135">Ez a parancsmag létrehoz egy adatkészletet abban a csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b3f6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b3f6-136">-ResourceId</span></span>
<span data-ttu-id="4b3f6-137">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4b3f6-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b3f6-138">-Confirm</span></span>
<span data-ttu-id="4b3f6-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b3f6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b3f6-140">-WhatIf</span></span>
<span data-ttu-id="4b3f6-141">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4b3f6-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4b3f6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3f6-142">CommonParameters</span></span>
<span data-ttu-id="4b3f6-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b3f6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b3f6-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b3f6-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3f6-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b3f6-145">INPUTS</span></span>

### <span data-ttu-id="4b3f6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4b3f6-146">System.String</span></span>

## <span data-ttu-id="4b3f6-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b3f6-147">OUTPUTS</span></span>

### <span data-ttu-id="4b3f6-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="4b3f6-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="4b3f6-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b3f6-149">NOTES</span></span>
<span data-ttu-id="4b3f6-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="4b3f6-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4b3f6-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b3f6-151">RELATED LINKS</span></span>

[<span data-ttu-id="4b3f6-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b3f6-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="4b3f6-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4b3f6-153">Remove-AzDataFactoryV2Dataset</span></span>]()
