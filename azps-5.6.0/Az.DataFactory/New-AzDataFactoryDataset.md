---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: b78d1ef78d7da1f8ad035951174578766de6a4a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930114"
---
# <span data-ttu-id="c61f1-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c61f1-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="c61f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c61f1-103">Adatkészletet hoz létre a Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="c61f1-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="c61f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c61f1-104">SYNTAX</span></span>

### <span data-ttu-id="c61f1-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c61f1-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c61f1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c61f1-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c61f1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c61f1-107">DESCRIPTION</span></span>
<span data-ttu-id="c61f1-108">A **New-AzDataFactoryDataset** parancsmag létrehoz egy adatkészletet az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="c61f1-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="c61f1-109">Ha egy már létező adatkészlet nevét adja meg, ez a parancsmag megerősítést kér, mielőtt lecseréli az adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="c61f1-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="c61f1-110">Ha a Force *paramétert* adja meg, a parancsmag jóváhagyás nélkül lecseréli a meglévő adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="c61f1-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="c61f1-111">Ezeket a műveleteket a következő sorrendben végezze el:</span><span class="sxs-lookup"><span data-stu-id="c61f1-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="c61f1-112">Adatüzem létrehozása</span><span class="sxs-lookup"><span data-stu-id="c61f1-112">Create a data factory.</span></span> 
- <span data-ttu-id="c61f1-113">Csatolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="c61f1-113">Create linked services.</span></span> 
- <span data-ttu-id="c61f1-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="c61f1-114">Create datasets.</span></span> 
- <span data-ttu-id="c61f1-115">Folyamat létrehozása</span><span class="sxs-lookup"><span data-stu-id="c61f1-115">Create a pipeline.</span></span>
<span data-ttu-id="c61f1-116">Ha egy azonos nevű adatkészlet már létezik az adatüzemben, ez a parancsmag megkérdezi, hogy felül kell-e írnia a meglévő adatkészletet az új adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="c61f1-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="c61f1-117">Ha megerősíti, hogy felülírja a meglévő adatkészletet, az adatkészlet-definíciót is lecseréli a program.</span><span class="sxs-lookup"><span data-stu-id="c61f1-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="c61f1-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c61f1-118">EXAMPLES</span></span>

### <span data-ttu-id="c61f1-119">1. példa: Adatkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="c61f1-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="c61f1-120">Ezzel a paranccsal a WikiADF nevű DA_WikipediaClickEvents nevű adatkészletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c61f1-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="c61f1-121">A parancs az adatkészletet a fájlon DAWikipediaClickEvents.jsalapján.</span><span class="sxs-lookup"><span data-stu-id="c61f1-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="c61f1-122">2. példa: Új adatkészlet elérhetőségének megtekintése</span><span class="sxs-lookup"><span data-stu-id="c61f1-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="c61f1-123">Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, ahogy az előző példában is volt, majd hozzárendeli az adatkészletet a $Dataset változóhoz.</span><span class="sxs-lookup"><span data-stu-id="c61f1-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="c61f1-124">A második parancs szabványos pontjelekkel jeleníti meg az adatkészlet Elérhetőség tulajdonságának részleteit.</span><span class="sxs-lookup"><span data-stu-id="c61f1-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="c61f1-125">3. példa: Új adatkészlet helyének megtekintése</span><span class="sxs-lookup"><span data-stu-id="c61f1-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="c61f1-126">Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, ahogy az előző példában is volt, majd hozzárendeli az adatkészletet a $Dataset változóhoz.</span><span class="sxs-lookup"><span data-stu-id="c61f1-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="c61f1-127">A második parancs megjeleníti az adatkészlet Hely tulajdonságának részleteit.</span><span class="sxs-lookup"><span data-stu-id="c61f1-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="c61f1-128">4. példa: Új adatkészlet érvényességi szabályainak megtekintése</span><span class="sxs-lookup"><span data-stu-id="c61f1-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="c61f1-129">Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, ahogy az előző példában is volt, majd hozzárendeli az adatkészletet a $Dataset változóhoz.</span><span class="sxs-lookup"><span data-stu-id="c61f1-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="c61f1-130">A második parancs részletes információkat kap az adatkészlet érvényességi szabályairól, majd a folyamat műveleti Format-List átadja őket a Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c61f1-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c61f1-131">Ez a Windows PowerShell-parancsmag formázta az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="c61f1-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="c61f1-132">További információért írja be a `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="c61f1-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="c61f1-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c61f1-133">PARAMETERS</span></span>

### <span data-ttu-id="c61f1-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c61f1-134">-DataFactory</span></span>
<span data-ttu-id="c61f1-135">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="c61f1-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c61f1-136">Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott adatüzemmódban.</span><span class="sxs-lookup"><span data-stu-id="c61f1-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c61f1-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c61f1-137">-DataFactoryName</span></span>
<span data-ttu-id="c61f1-138">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c61f1-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c61f1-139">Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott adatüzemmódban.</span><span class="sxs-lookup"><span data-stu-id="c61f1-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c61f1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61f1-140">-DefaultProfile</span></span>
<span data-ttu-id="c61f1-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c61f1-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c61f1-142">-File</span><span class="sxs-lookup"><span data-stu-id="c61f1-142">-File</span></span>
<span data-ttu-id="c61f1-143">Az adatkészlet leírását tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c61f1-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="c61f1-144">-Force</span><span class="sxs-lookup"><span data-stu-id="c61f1-144">-Force</span></span>
<span data-ttu-id="c61f1-145">Azt jelzi, hogy ez a parancsmag a megerősítés kérése nélkül lecserél egy meglévő adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="c61f1-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c61f1-146">-Name</span><span class="sxs-lookup"><span data-stu-id="c61f1-146">-Name</span></span>
<span data-ttu-id="c61f1-147">A létrehozni szükséges adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c61f1-147">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61f1-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c61f1-148">-ResourceGroupName</span></span>
<span data-ttu-id="c61f1-149">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c61f1-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c61f1-150">Ez a parancsmag egy adatkészletet hoz létre a paraméter által megadott csoportban.</span><span class="sxs-lookup"><span data-stu-id="c61f1-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c61f1-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c61f1-151">-Confirm</span></span>
<span data-ttu-id="c61f1-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c61f1-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c61f1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c61f1-153">-WhatIf</span></span>
<span data-ttu-id="c61f1-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c61f1-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c61f1-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c61f1-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c61f1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61f1-156">CommonParameters</span></span>
<span data-ttu-id="c61f1-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c61f1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61f1-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c61f1-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61f1-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c61f1-159">INPUTS</span></span>

### <span data-ttu-id="c61f1-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c61f1-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c61f1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c61f1-161">System.String</span></span>

## <span data-ttu-id="c61f1-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c61f1-162">OUTPUTS</span></span>

### <span data-ttu-id="c61f1-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c61f1-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="c61f1-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c61f1-164">NOTES</span></span>
* <span data-ttu-id="c61f1-165">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="c61f1-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c61f1-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c61f1-166">RELATED LINKS</span></span>

[<span data-ttu-id="c61f1-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c61f1-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="c61f1-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c61f1-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


