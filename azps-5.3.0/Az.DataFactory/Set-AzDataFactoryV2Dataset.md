---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480389"
---
# <span data-ttu-id="e4927-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e4927-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="e4927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4927-102">SYNOPSIS</span></span>
<span data-ttu-id="e4927-103">Adatkészletet hoz létre a Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="e4927-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="e4927-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4927-104">SYNTAX</span></span>

### <span data-ttu-id="e4927-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4927-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4927-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4927-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4927-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4927-107">DESCRIPTION</span></span>
<span data-ttu-id="e4927-108">A Set-AzDataFactoryV2Dataset parancsmag létrehoz egy adatkészletet az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="e4927-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="e4927-109">Ha egy már létező adatkészlet nevét adja meg, ez a parancsmag megerősítést kér, mielőtt lecseréli az adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="e4927-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="e4927-110">Ha a Force paramétert adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="e4927-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="e4927-111">Végezze el ezeket a műveleteket a következő sorrendben: - Adatüzem létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e4927-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e4927-112">– Csatolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e4927-112">-- Create linked services.</span></span>
<span data-ttu-id="e4927-113">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e4927-113">-- Create datasets.</span></span>
<span data-ttu-id="e4927-114">– Folyamat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e4927-114">-- Create a pipeline.</span></span>
<span data-ttu-id="e4927-115">Ha egy azonos nevű adatkészlet már létezik az adatüzemben, ez a parancsmag megkérdezi, hogy felül kell-e írnia a meglévő adatkészletet az új adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="e4927-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="e4927-116">Ha megerősíti, hogy felülírja a meglévő adatkészletet, az adatkészlet-definíciót is lecseréli a program.</span><span class="sxs-lookup"><span data-stu-id="e4927-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="e4927-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4927-117">EXAMPLES</span></span>

### <span data-ttu-id="e4927-118">1. példa: Adatkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="e4927-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="e4927-119">Ezzel a paranccsal a WikiADF nevű DA_WikipediaClickEvents nevű adatkészletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4927-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="e4927-120">A parancs az adatkészletet a fájlon DAWikipediaClickEvents.jsalapján.</span><span class="sxs-lookup"><span data-stu-id="e4927-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="e4927-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4927-121">PARAMETERS</span></span>

### <span data-ttu-id="e4927-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e4927-122">-DataFactoryName</span></span>
<span data-ttu-id="e4927-123">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4927-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e4927-124">Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott adatüzemmódban.</span><span class="sxs-lookup"><span data-stu-id="e4927-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4927-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4927-125">-DefaultProfile</span></span>
<span data-ttu-id="e4927-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4927-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4927-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e4927-127">-DefinitionFile</span></span>
<span data-ttu-id="e4927-128">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e4927-128">The JSON file path.</span></span>

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

### <span data-ttu-id="e4927-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e4927-129">-Force</span></span>
<span data-ttu-id="e4927-130">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e4927-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e4927-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e4927-131">-Name</span></span>
<span data-ttu-id="e4927-132">A létrehozni szükséges adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4927-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="e4927-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4927-133">-ResourceGroupName</span></span>
<span data-ttu-id="e4927-134">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4927-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e4927-135">Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="e4927-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4927-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4927-136">-ResourceId</span></span>
<span data-ttu-id="e4927-137">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="e4927-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e4927-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4927-138">-Confirm</span></span>
<span data-ttu-id="e4927-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4927-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4927-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4927-140">-WhatIf</span></span>
<span data-ttu-id="e4927-141">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e4927-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e4927-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4927-142">CommonParameters</span></span>
<span data-ttu-id="e4927-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4927-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4927-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4927-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4927-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4927-145">INPUTS</span></span>

### <span data-ttu-id="e4927-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e4927-146">System.String</span></span>

## <span data-ttu-id="e4927-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4927-147">OUTPUTS</span></span>

### <span data-ttu-id="e4927-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e4927-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="e4927-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4927-149">NOTES</span></span>
<span data-ttu-id="e4927-150">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="e4927-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e4927-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4927-151">RELATED LINKS</span></span>

[<span data-ttu-id="e4927-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e4927-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="e4927-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e4927-153">Remove-AzDataFactoryV2Dataset</span></span>]()
