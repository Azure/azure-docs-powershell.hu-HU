---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847309"
---
# <span data-ttu-id="74fc3-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="74fc3-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="74fc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="74fc3-103">Információt kap az adatfeldolgozó-adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="74fc3-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="74fc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74fc3-104">SYNTAX</span></span>

### <span data-ttu-id="74fc3-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74fc3-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74fc3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="74fc3-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74fc3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="74fc3-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74fc3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="74fc3-108">DESCRIPTION</span></span>
<span data-ttu-id="74fc3-109">Az Get-AzDataFactoryV2Dataset parancsmag információkat kap az Azure Data Factory adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="74fc3-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="74fc3-110">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="74fc3-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="74fc3-111">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó összes adatkészletéről.</span><span class="sxs-lookup"><span data-stu-id="74fc3-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="74fc3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="74fc3-112">EXAMPLES</span></span>

### <span data-ttu-id="74fc3-113">1. példa: információk kérése az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="74fc3-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="74fc3-114">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="74fc3-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="74fc3-115">2. példa: információk kérése egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="74fc3-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="74fc3-116">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="74fc3-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="74fc3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74fc3-117">PARAMETERS</span></span>

### <span data-ttu-id="74fc3-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="74fc3-118">-DataFactory</span></span>
<span data-ttu-id="74fc3-119">Egy PSDataFactory-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="74fc3-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="74fc3-120">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="74fc3-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74fc3-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="74fc3-121">-DataFactoryName</span></span>
<span data-ttu-id="74fc3-122">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74fc3-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="74fc3-123">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="74fc3-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="74fc3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fc3-124">-DefaultProfile</span></span>
<span data-ttu-id="74fc3-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74fc3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74fc3-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74fc3-126">-Name</span></span>
<span data-ttu-id="74fc3-127">Annak az adatkészletnek a nevét adja meg, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="74fc3-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fc3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74fc3-128">-ResourceGroupName</span></span>
<span data-ttu-id="74fc3-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74fc3-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="74fc3-130">Ez a parancsmag azokat az adatkészleteket kapja meg, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="74fc3-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="74fc3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74fc3-131">-ResourceId</span></span>
<span data-ttu-id="74fc3-132">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="74fc3-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="74fc3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fc3-133">CommonParameters</span></span>
<span data-ttu-id="74fc3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74fc3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fc3-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74fc3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fc3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74fc3-136">INPUTS</span></span>

### <span data-ttu-id="74fc3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="74fc3-137">System.String</span></span>

### <span data-ttu-id="74fc3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="74fc3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="74fc3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74fc3-139">OUTPUTS</span></span>

### <span data-ttu-id="74fc3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="74fc3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="74fc3-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74fc3-141">NOTES</span></span>
<span data-ttu-id="74fc3-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="74fc3-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="74fc3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74fc3-143">RELATED LINKS</span></span>

[<span data-ttu-id="74fc3-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="74fc3-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="74fc3-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="74fc3-145">Remove-AzDataFactoryV2Dataset</span></span>]()
