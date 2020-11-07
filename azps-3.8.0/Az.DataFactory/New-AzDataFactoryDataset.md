---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847237"
---
# <span data-ttu-id="aeacd-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="aeacd-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="aeacd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aeacd-102">SYNOPSIS</span></span>
<span data-ttu-id="aeacd-103">Adatkészletet hoz létre az adatfeldolgozóban.</span><span class="sxs-lookup"><span data-stu-id="aeacd-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="aeacd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aeacd-104">SYNTAX</span></span>

### <span data-ttu-id="aeacd-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aeacd-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aeacd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="aeacd-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeacd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aeacd-107">DESCRIPTION</span></span>
<span data-ttu-id="aeacd-108">A **New-AzDataFactoryDataset** parancsmag létrehoz egy adatkészletet az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="aeacd-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="aeacd-109">Ha olyan adatkészletet ad meg, amely már létezik, ez a parancsmag az adatkészlet visszavonása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aeacd-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="aeacd-110">Ha az *erő* paramétert adja meg, a parancsmag a létező adatkészletet megerősítés nélkül cseréli le.</span><span class="sxs-lookup"><span data-stu-id="aeacd-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="aeacd-111">Végezze el ezeket a műveleteket az alábbi sorrendben:</span><span class="sxs-lookup"><span data-stu-id="aeacd-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="aeacd-112">Adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="aeacd-112">Create a data factory.</span></span> 
- <span data-ttu-id="aeacd-113">Kapcsolt szolgáltatások létrehozása</span><span class="sxs-lookup"><span data-stu-id="aeacd-113">Create linked services.</span></span> 
- <span data-ttu-id="aeacd-114">Adatkészletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="aeacd-114">Create datasets.</span></span> 
- <span data-ttu-id="aeacd-115">Csővezeték létrehozása</span><span class="sxs-lookup"><span data-stu-id="aeacd-115">Create a pipeline.</span></span>
<span data-ttu-id="aeacd-116">Ha az adatfeldolgozóban már létezik azonos nevű adatkészlet, ez a parancsmag arra kéri, hogy erősítse meg, hogy felülírja-e a meglévő adatkészletet az új adatkészlettel.</span><span class="sxs-lookup"><span data-stu-id="aeacd-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="aeacd-117">Ha a meglévő adatkészlet felülírásának megerősítését hagyja jóvá, az adatkészlet-definíciót is lecseréli a program.</span><span class="sxs-lookup"><span data-stu-id="aeacd-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="aeacd-118">Példák</span><span class="sxs-lookup"><span data-stu-id="aeacd-118">EXAMPLES</span></span>

### <span data-ttu-id="aeacd-119">1. példa: adatkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="aeacd-119">Example 1: Create a dataset</span></span>
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

<span data-ttu-id="aeacd-120">A parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet a WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="aeacd-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="aeacd-121">A parancs az adatkészletet az DAWikipediaClickEvents.jsfájlon lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="aeacd-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="aeacd-122">2. példa: új adatkészlet elérhetőségének megtekintése</span><span class="sxs-lookup"><span data-stu-id="aeacd-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="aeacd-123">Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, az előző példában szereplő módon, majd hozzárendeli az adatkészletet a $Dataset változóhoz.</span><span class="sxs-lookup"><span data-stu-id="aeacd-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="aeacd-124">A második parancs normál képpont jelöléssel jeleníti meg az adatkészlet elérhetőségi tulajdonságának részleteit.</span><span class="sxs-lookup"><span data-stu-id="aeacd-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="aeacd-125">3. példa: új adatkészlet helyének megtekintése</span><span class="sxs-lookup"><span data-stu-id="aeacd-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="aeacd-126">Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, az előző példában szereplő módon, majd hozzárendeli az adatkészletet a $Dataset változóhoz.</span><span class="sxs-lookup"><span data-stu-id="aeacd-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="aeacd-127">A második parancs az adatkészlet tartózkodási hely tulajdonságával kapcsolatos részleteket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="aeacd-128">Példa 4: új adatkészlet érvényességi szabályainak megtekintése</span><span class="sxs-lookup"><span data-stu-id="aeacd-128">Example 4: View validation rules for a new dataset</span></span>
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

<span data-ttu-id="aeacd-129">Az első parancs létrehoz egy DA_WikipediaClickEvents nevű adatkészletet, az előző példában szereplő módon, majd hozzárendeli az adatkészletet a $Dataset változóhoz.</span><span class="sxs-lookup"><span data-stu-id="aeacd-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="aeacd-130">A második parancs részletesen részletezi az adatkészlet érvényességi szabályait, majd a pipeline operátor segítségével átadja őket a Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="aeacd-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aeacd-131">A Windows PowerShell-parancsmag formázza a találatokat.</span><span class="sxs-lookup"><span data-stu-id="aeacd-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="aeacd-132">További információért írja be a következőt: `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="aeacd-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="aeacd-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aeacd-133">PARAMETERS</span></span>

### <span data-ttu-id="aeacd-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="aeacd-134">-DataFactory</span></span>
<span data-ttu-id="aeacd-135">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="aeacd-136">Ez a parancsmag létrehoz egy adatkészletet az adatgyárban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aeacd-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aeacd-137">-DataFactoryName</span></span>
<span data-ttu-id="aeacd-138">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="aeacd-139">Ez a parancsmag létrehoz egy adatkészletet az adatgyárban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aeacd-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeacd-140">-DefaultProfile</span></span>
<span data-ttu-id="aeacd-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aeacd-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeacd-142">-Fájl</span><span class="sxs-lookup"><span data-stu-id="aeacd-142">-File</span></span>
<span data-ttu-id="aeacd-143">Itt adhatja meg az adatkészlet leírását tartalmazó JavaScript-objektum (JSON) fájl teljes elérési útját.</span><span class="sxs-lookup"><span data-stu-id="aeacd-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="aeacd-144">-Force</span><span class="sxs-lookup"><span data-stu-id="aeacd-144">-Force</span></span>
<span data-ttu-id="aeacd-145">Azt jelzi, hogy ez a parancsmag egy meglévő adatkészletet cserél le anélkül, hogy megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aeacd-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="aeacd-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aeacd-146">-Name</span></span>
<span data-ttu-id="aeacd-147">A létrehozandó adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="aeacd-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeacd-148">-ResourceGroupName</span></span>
<span data-ttu-id="aeacd-149">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="aeacd-150">Ez a parancsmag létrehoz egy adatkészletet abban a csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aeacd-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aeacd-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aeacd-151">-Confirm</span></span>
<span data-ttu-id="aeacd-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aeacd-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeacd-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeacd-153">-WhatIf</span></span>
<span data-ttu-id="aeacd-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aeacd-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeacd-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aeacd-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeacd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeacd-156">CommonParameters</span></span>
<span data-ttu-id="aeacd-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aeacd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeacd-158">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeacd-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeacd-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aeacd-159">INPUTS</span></span>

### <span data-ttu-id="aeacd-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="aeacd-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="aeacd-161">System. String</span><span class="sxs-lookup"><span data-stu-id="aeacd-161">System.String</span></span>

## <span data-ttu-id="aeacd-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aeacd-162">OUTPUTS</span></span>

### <span data-ttu-id="aeacd-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="aeacd-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="aeacd-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aeacd-164">NOTES</span></span>
* <span data-ttu-id="aeacd-165">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="aeacd-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aeacd-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aeacd-166">RELATED LINKS</span></span>

[<span data-ttu-id="aeacd-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="aeacd-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="aeacd-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="aeacd-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)

