---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 6f6421659f47d2a6d119d5acd8e614765f356298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679858"
---
# <span data-ttu-id="8e25b-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8e25b-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="8e25b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e25b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e25b-103">Információt kap az adatkészletekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="8e25b-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e25b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e25b-104">SYNTAX</span></span>

### <span data-ttu-id="8e25b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e25b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e25b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8e25b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e25b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e25b-107">DESCRIPTION</span></span>
<span data-ttu-id="8e25b-108">A **Get-AzureRmDataFactoryDataset** parancsmag információkat kaphat az Azure Data Factory adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="8e25b-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="8e25b-109">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="8e25b-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="8e25b-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó összes adatkészletéről.</span><span class="sxs-lookup"><span data-stu-id="8e25b-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="8e25b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8e25b-111">EXAMPLES</span></span>

### <span data-ttu-id="8e25b-112">1. példa: információk kérése az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="8e25b-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="8e25b-113">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="8e25b-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8e25b-114">2. példa: információk kérése egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="8e25b-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="8e25b-115">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="8e25b-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8e25b-116">3. példa: adott adatkészlet helyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="8e25b-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="8e25b-117">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletről, majd normál pont jelöléssel jeleníti meg az adatkészlethez társított **helyet** .</span><span class="sxs-lookup"><span data-stu-id="8e25b-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="8e25b-118">Azt is megteheti, hogy hozzárendeli a **Get-AzureRmDataFactoryDataset** parancsmag kimenetét egy változóhoz, majd az adott változóban tárolt adatkészlet-objektumhoz társított hely tulajdonságot a pont jelöléssel jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="8e25b-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="8e25b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e25b-119">PARAMETERS</span></span>

### <span data-ttu-id="8e25b-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e25b-120">-DataFactory</span></span>
<span data-ttu-id="8e25b-121">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8e25b-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8e25b-122">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e25b-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e25b-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8e25b-123">-DataFactoryName</span></span>
<span data-ttu-id="8e25b-124">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e25b-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8e25b-125">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e25b-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e25b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e25b-126">-DefaultProfile</span></span>
<span data-ttu-id="8e25b-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e25b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e25b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e25b-128">-Name</span></span>
<span data-ttu-id="8e25b-129">Annak az adatkészletnek a nevét adja meg, amelyre a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="8e25b-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="8e25b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e25b-130">-ResourceGroupName</span></span>
<span data-ttu-id="8e25b-131">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e25b-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8e25b-132">Ez a parancsmag azokat az adatkészleteket kapja meg, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="8e25b-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e25b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e25b-133">CommonParameters</span></span>
<span data-ttu-id="8e25b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e25b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e25b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e25b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e25b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e25b-136">INPUTS</span></span>

### <span data-ttu-id="8e25b-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8e25b-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8e25b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e25b-138">System.String</span></span>

## <span data-ttu-id="8e25b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e25b-139">OUTPUTS</span></span>

### <span data-ttu-id="8e25b-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="8e25b-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="8e25b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e25b-141">NOTES</span></span>
* <span data-ttu-id="8e25b-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="8e25b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8e25b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e25b-143">RELATED LINKS</span></span>

[<span data-ttu-id="8e25b-144">Új – AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8e25b-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="8e25b-145">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8e25b-145">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


