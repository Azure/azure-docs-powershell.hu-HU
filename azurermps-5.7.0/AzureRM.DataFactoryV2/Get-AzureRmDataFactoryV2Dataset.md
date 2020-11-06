---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 171431e317b9edbafe83f7c0c836f5543fcbd65d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496612"
---
# <span data-ttu-id="fd679-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fd679-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="fd679-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd679-102">SYNOPSIS</span></span>
<span data-ttu-id="fd679-103">Információt kap az adatfeldolgozó-adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="fd679-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd679-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd679-104">SYNTAX</span></span>

### <span data-ttu-id="fd679-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd679-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd679-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fd679-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd679-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd679-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd679-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd679-108">DESCRIPTION</span></span>
<span data-ttu-id="fd679-109">Az Get-AzureRmDataFactoryV2Dataset parancsmag információkat kap az Azure Data Factory adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="fd679-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="fd679-110">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="fd679-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="fd679-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó összes adatkészletéről.</span><span class="sxs-lookup"><span data-stu-id="fd679-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="fd679-112">Példák</span><span class="sxs-lookup"><span data-stu-id="fd679-112">EXAMPLES</span></span>

### <span data-ttu-id="fd679-113">1. példa: információk kérése az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="fd679-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="fd679-114">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="fd679-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="fd679-115">2. példa: információk kérése egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="fd679-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="fd679-116">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="fd679-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="fd679-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd679-117">PARAMETERS</span></span>

### <span data-ttu-id="fd679-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fd679-118">-DataFactory</span></span>
<span data-ttu-id="fd679-119">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fd679-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="fd679-120">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd679-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="fd679-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fd679-121">-DataFactoryName</span></span>
<span data-ttu-id="fd679-122">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd679-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fd679-123">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd679-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd679-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd679-124">-DefaultProfile</span></span>
<span data-ttu-id="fd679-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd679-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd679-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd679-126">-Name</span></span>
<span data-ttu-id="fd679-127">Annak az adatkészletnek a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="fd679-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd679-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd679-128">-ResourceGroupName</span></span>
<span data-ttu-id="fd679-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd679-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fd679-130">Ez a parancsmag azokat az adatkészleteket kapja meg, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="fd679-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd679-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd679-131">-ResourceId</span></span>
<span data-ttu-id="fd679-132">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="fd679-132">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd679-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd679-133">CommonParameters</span></span>
<span data-ttu-id="fd679-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd679-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd679-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd679-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd679-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd679-136">INPUTS</span></span>

### <span data-ttu-id="fd679-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fd679-137">System.String</span></span>
<span data-ttu-id="fd679-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fd679-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="fd679-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd679-139">OUTPUTS</span></span>

### <span data-ttu-id="fd679-140">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Command. DataFactoryV2, Version = 0.1.9.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fd679-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fd679-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="fd679-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="fd679-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd679-142">NOTES</span></span>
<span data-ttu-id="fd679-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="fd679-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fd679-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd679-144">RELATED LINKS</span></span>

[<span data-ttu-id="fd679-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fd679-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="fd679-146">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fd679-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
