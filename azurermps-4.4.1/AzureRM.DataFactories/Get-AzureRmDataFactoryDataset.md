---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 0898b65c0a124b278d0878ac1749e955011e1dab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492488"
---
# <span data-ttu-id="a7801-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a7801-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="a7801-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7801-102">SYNOPSIS</span></span>
<span data-ttu-id="a7801-103">Információt kap az adatkészletekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="a7801-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7801-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7801-104">SYNTAX</span></span>

### <span data-ttu-id="a7801-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7801-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7801-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a7801-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7801-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7801-107">DESCRIPTION</span></span>
<span data-ttu-id="a7801-108">A **Get-AzureRmDataFactoryDataset** parancsmag információkat kaphat az Azure Data Factory adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="a7801-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="a7801-109">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="a7801-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="a7801-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó összes adatkészletéről.</span><span class="sxs-lookup"><span data-stu-id="a7801-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="a7801-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a7801-111">EXAMPLES</span></span>

### <span data-ttu-id="a7801-112">1. példa: információk kérése az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="a7801-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="a7801-113">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="a7801-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="a7801-114">2. példa: információk kérése egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="a7801-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="a7801-115">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="a7801-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="a7801-116">3. példa: adott adatkészlet helyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a7801-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="a7801-117">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletről, majd normál pont jelöléssel jeleníti meg az adatkészlethez társított **helyet** .</span><span class="sxs-lookup"><span data-stu-id="a7801-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="a7801-118">Azt is megteheti, hogy hozzárendeli a **Get-AzureRmDataFactoryDataset** parancsmag kimenetét egy változóhoz, majd az adott változóban tárolt adatkészlet-objektumhoz társított hely tulajdonságot a pont jelöléssel jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="a7801-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="a7801-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7801-119">PARAMETERS</span></span>

### <span data-ttu-id="a7801-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a7801-120">-DataFactory</span></span>
<span data-ttu-id="a7801-121">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a7801-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a7801-122">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7801-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7801-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a7801-123">-DataFactoryName</span></span>
<span data-ttu-id="a7801-124">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7801-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a7801-125">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7801-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7801-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a7801-126">-Name</span></span>
<span data-ttu-id="a7801-127">Annak az adatkészletnek a nevét adja meg, amelyre a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="a7801-127">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="a7801-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7801-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7801-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7801-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a7801-130">Ez a parancsmag azokat az adatkészleteket kapja meg, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="a7801-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7801-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7801-131">-DefaultProfile</span></span>
<span data-ttu-id="a7801-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7801-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7801-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7801-133">CommonParameters</span></span>
<span data-ttu-id="a7801-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7801-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7801-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7801-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7801-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7801-136">INPUTS</span></span>

## <span data-ttu-id="a7801-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7801-137">OUTPUTS</span></span>

### <span data-ttu-id="a7801-138">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="a7801-138">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="a7801-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7801-139">NOTES</span></span>
* <span data-ttu-id="a7801-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="a7801-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a7801-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7801-141">RELATED LINKS</span></span>

[<span data-ttu-id="a7801-142">Új – AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a7801-142">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="a7801-143">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a7801-143">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


