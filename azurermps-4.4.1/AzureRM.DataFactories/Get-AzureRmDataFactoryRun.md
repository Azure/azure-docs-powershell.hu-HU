---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: db3992a8df2cbd27c560827a702f9562e64ddcb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680590"
---
# <span data-ttu-id="40879-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="40879-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="40879-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40879-102">SYNOPSIS</span></span>
<span data-ttu-id="40879-103">Az Azure Data Factory-ban az adatkészletek adatszeleteit futtatja.</span><span class="sxs-lookup"><span data-stu-id="40879-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40879-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40879-104">SYNTAX</span></span>

### <span data-ttu-id="40879-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40879-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40879-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="40879-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40879-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="40879-107">DESCRIPTION</span></span>
<span data-ttu-id="40879-108">A **Get-AzureRmDataFactoryRun** parancsmag az Azure Data Factory adatkészletben található adatkészletek adatszeletéhez tartozó futásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="40879-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="40879-109">Az adatfeldolgozó adatkészlete az időtengelyen kívüli szeletekre épül.</span><span class="sxs-lookup"><span data-stu-id="40879-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="40879-110">A szeletek szélességét az ütemterv határozza meg óránként vagy naponta.</span><span class="sxs-lookup"><span data-stu-id="40879-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="40879-111">A Run egy szelet feldolgozási egysége.</span><span class="sxs-lookup"><span data-stu-id="40879-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="40879-112">Lehet, hogy egy vagy több futás van egy slice-ra, ha újból próbálkozik, vagy ha a slice-ot a meghibásodások miatt újra futtatja.</span><span class="sxs-lookup"><span data-stu-id="40879-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="40879-113">A szeletet a kezdési időpontja azonosítja.</span><span class="sxs-lookup"><span data-stu-id="40879-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="40879-114">A szelet kezdési időpontjának beolvasásához használja az Get-AzureRmDataFactorySlice parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="40879-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>

<span data-ttu-id="40879-115">Ha például a következő slice-hoz szeretne futni, használja a 2015-04-02T20:00:00 kezdési időpontot.</span><span class="sxs-lookup"><span data-stu-id="40879-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>

<span data-ttu-id="40879-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM End: 5/3/2014 8:00:00 PM RetryCount: 0 Status: Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="40879-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="40879-117">Példák</span><span class="sxs-lookup"><span data-stu-id="40879-117">EXAMPLES</span></span>

### <span data-ttu-id="40879-118">Példa 1: adatkészlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="40879-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="40879-119">Ez a parancs minden futást a WikiADF nevű adatDAWikiAggregatedDatai adatkészletnek a 05/21/2014-as verziójában, a 4 PM GMT-től kezdődően futtatja.</span><span class="sxs-lookup"><span data-stu-id="40879-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="40879-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40879-120">PARAMETERS</span></span>

### <span data-ttu-id="40879-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="40879-121">-DataFactory</span></span>
<span data-ttu-id="40879-122">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="40879-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="40879-123">Ez a parancsmag akkor fog futni, ha az adatfeldolgozóhoz tartozó Slice-elemek szerepelnek, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="40879-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40879-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="40879-124">-DataFactoryName</span></span>
<span data-ttu-id="40879-125">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40879-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="40879-126">Ez a parancsmag akkor fog futni, ha az adatfeldolgozóhoz tartozó Slice-elemek szerepelnek, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="40879-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="40879-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="40879-127">-DatasetName</span></span>
<span data-ttu-id="40879-128">Az adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40879-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="40879-129">Ez a parancsmag a paraméter által megadott adatkészlethez tartozó szeletekhez fog futni.</span><span class="sxs-lookup"><span data-stu-id="40879-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40879-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40879-130">-ResourceGroupName</span></span>
<span data-ttu-id="40879-131">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40879-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="40879-132">Ez a parancsmag beilleszti a Factory függvényt azokhoz a szeletekhez, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="40879-132">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="40879-133">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="40879-133">-StartDateTime</span></span>
<span data-ttu-id="40879-134">Az időszak kezdését **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="40879-134">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="40879-135">Ez a parancsmag az adott időszaknak megfelelő adatszeletek esetén fut.</span><span class="sxs-lookup"><span data-stu-id="40879-135">This cmdlet gets runs for the data slices that match this time period.</span></span>

<span data-ttu-id="40879-136">A *StartDateTime* a ISO8601 formátumban kell megadni, ahogy az alábbi példákban:</span><span class="sxs-lookup"><span data-stu-id="40879-136">*StartDateTime* must be specified in the ISO8601 format, as in the following examples:</span></span> 

<span data-ttu-id="40879-137">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time)</span><span class="sxs-lookup"><span data-stu-id="40879-137">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="40879-138">Az alapértelmezett időzóna-kijelölés az UTC.</span><span class="sxs-lookup"><span data-stu-id="40879-138">The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40879-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40879-139">-DefaultProfile</span></span>
<span data-ttu-id="40879-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40879-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40879-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40879-141">CommonParameters</span></span>
<span data-ttu-id="40879-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40879-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40879-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40879-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40879-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40879-144">INPUTS</span></span>

## <span data-ttu-id="40879-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40879-145">OUTPUTS</span></span>

### <span data-ttu-id="40879-146">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft. WindowsAzure. commands. Utilities, Version = 0.8.2.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="40879-146">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="40879-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40879-147">NOTES</span></span>
* <span data-ttu-id="40879-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="40879-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="40879-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40879-149">RELATED LINKS</span></span>

[<span data-ttu-id="40879-150">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="40879-150">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


