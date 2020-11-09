---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298604"
---
# <span data-ttu-id="19536-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="19536-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="19536-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19536-102">SYNOPSIS</span></span>
<span data-ttu-id="19536-103">Információt kap az adatkészletekről az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="19536-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="19536-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19536-104">SYNTAX</span></span>

### <span data-ttu-id="19536-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19536-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19536-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="19536-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19536-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19536-107">DESCRIPTION</span></span>
<span data-ttu-id="19536-108">A **Get-AzDataFactoryDataset** parancsmag információkat kaphat az Azure Data Factory adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="19536-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="19536-109">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="19536-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="19536-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó összes adatkészletéről.</span><span class="sxs-lookup"><span data-stu-id="19536-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="19536-111">Példák</span><span class="sxs-lookup"><span data-stu-id="19536-111">EXAMPLES</span></span>

### <span data-ttu-id="19536-112">1. példa: információk kérése az összes adatkészletről</span><span class="sxs-lookup"><span data-stu-id="19536-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
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

<span data-ttu-id="19536-113">Ez a parancs információkat kap az WikiADF nevű adatfeldolgozóban található összes adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="19536-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="19536-114">2. példa: információk kérése egy adott adatkészletről</span><span class="sxs-lookup"><span data-stu-id="19536-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="19536-115">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletben.</span><span class="sxs-lookup"><span data-stu-id="19536-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="19536-116">3. példa: adott adatkészlet helyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="19536-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="19536-117">Ez a parancs információt kap a DAWikipediaClickEvents nevű adatkészletről az WikiADF nevű Data Factory nevű adatkészletről, majd normál pont jelöléssel jeleníti meg az adatkészlethez társított **helyet** .</span><span class="sxs-lookup"><span data-stu-id="19536-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="19536-118">Azt is megteheti, hogy hozzárendeli a **Get-AzDataFactoryDataset** parancsmag kimenetét egy változóhoz, majd az adott változóban tárolt adatkészlet-objektumhoz társított hely tulajdonságot a pont jelöléssel jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="19536-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="19536-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19536-119">PARAMETERS</span></span>

### <span data-ttu-id="19536-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="19536-120">-DataFactory</span></span>
<span data-ttu-id="19536-121">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="19536-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="19536-122">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="19536-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="19536-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="19536-123">-DataFactoryName</span></span>
<span data-ttu-id="19536-124">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19536-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="19536-125">Ez a parancsmag olyan adatkészleteket kap, amelyek az adatfeldolgozóhoz tartoznak, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="19536-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="19536-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19536-126">-DefaultProfile</span></span>
<span data-ttu-id="19536-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="19536-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19536-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19536-128">-Name</span></span>
<span data-ttu-id="19536-129">Annak az adatkészletnek a nevét adja meg, amelyre a parancsmag információt kap.</span><span class="sxs-lookup"><span data-stu-id="19536-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="19536-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19536-130">-ResourceGroupName</span></span>
<span data-ttu-id="19536-131">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="19536-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="19536-132">Ez a parancsmag azokat az adatkészleteket kapja meg, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="19536-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="19536-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19536-133">CommonParameters</span></span>
<span data-ttu-id="19536-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19536-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19536-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19536-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19536-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19536-136">INPUTS</span></span>

### <span data-ttu-id="19536-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="19536-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="19536-138">System. String</span><span class="sxs-lookup"><span data-stu-id="19536-138">System.String</span></span>

## <span data-ttu-id="19536-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19536-139">OUTPUTS</span></span>

### <span data-ttu-id="19536-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="19536-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="19536-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19536-141">NOTES</span></span>
* <span data-ttu-id="19536-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="19536-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="19536-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19536-143">RELATED LINKS</span></span>

[<span data-ttu-id="19536-144">Új – AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="19536-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="19536-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="19536-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


