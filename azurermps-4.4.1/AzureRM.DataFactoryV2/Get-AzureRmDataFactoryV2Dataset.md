---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505107"
---
# <span data-ttu-id="e8d93-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e8d93-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="e8d93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8d93-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d93-103">Információt kap az adatfeldolgozó-adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="e8d93-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8d93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8d93-104">SYNTAX</span></span>

### <span data-ttu-id="e8d93-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8d93-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="e8d93-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e8d93-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="e8d93-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8d93-107">DESCRIPTION</span></span>
<span data-ttu-id="e8d93-108">Az Get-AzureRmDataFactoryV2Dataset parancsmag információkat kap az Azure Data Factory adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="e8d93-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="e8d93-109">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="e8d93-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="e8d93-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó összes adatkészletéről.</span><span class="sxs-lookup"><span data-stu-id="e8d93-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="e8d93-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e8d93-111">EXAMPLES</span></span>

### <span data-ttu-id="e8d93-112">1. példa: információk kérése az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="e8d93-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="e8d93-113">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="e8d93-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e8d93-114">2. példa: információk kérése egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="e8d93-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="e8d93-115">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="e8d93-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="e8d93-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8d93-116">PARAMETERS</span></span>

### <span data-ttu-id="e8d93-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e8d93-117">-DataFactory</span></span>
<span data-ttu-id="e8d93-118">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e8d93-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="e8d93-119">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8d93-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d93-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8d93-120">-DataFactoryName</span></span>
<span data-ttu-id="e8d93-121">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8d93-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e8d93-122">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8d93-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d93-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8d93-123">-Name</span></span>
<span data-ttu-id="e8d93-124">Annak az adatkészletnek a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="e8d93-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d93-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8d93-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8d93-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e8d93-127">Ez a parancsmag azokat az adatkészleteket kapja meg, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="e8d93-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e8d93-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8d93-128">INPUTS</span></span>

### <span data-ttu-id="e8d93-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e8d93-129">System.String</span></span>
<span data-ttu-id="e8d93-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8d93-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="e8d93-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8d93-131">OUTPUTS</span></span>

### <span data-ttu-id="e8d93-132">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Command. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e8d93-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e8d93-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e8d93-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="e8d93-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8d93-134">NOTES</span></span>
<span data-ttu-id="e8d93-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="e8d93-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e8d93-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8d93-136">RELATED LINKS</span></span>
[<span data-ttu-id="e8d93-137">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e8d93-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="e8d93-138">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e8d93-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
