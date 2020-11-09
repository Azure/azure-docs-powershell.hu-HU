---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298577"
---
# <span data-ttu-id="4fac5-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="4fac5-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="4fac5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fac5-102">SYNOPSIS</span></span>
<span data-ttu-id="4fac5-103">Az Azure Data Factory-ban az adatkészletek adatszeleteit futtatja.</span><span class="sxs-lookup"><span data-stu-id="4fac5-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="4fac5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fac5-104">SYNTAX</span></span>

### <span data-ttu-id="4fac5-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fac5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fac5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4fac5-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fac5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fac5-107">DESCRIPTION</span></span>
<span data-ttu-id="4fac5-108">A **Get-AzDataFactoryRun** parancsmag az Azure Data Factory adatkészletben található adatkészletek adatszeletéhez tartozó futásokat kapja.</span><span class="sxs-lookup"><span data-stu-id="4fac5-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="4fac5-109">Az adatfeldolgozó adatkészlete az időtengelyen kívüli szeletekre épül.</span><span class="sxs-lookup"><span data-stu-id="4fac5-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="4fac5-110">A szeletek szélességét az ütemterv határozza meg óránként vagy naponta.</span><span class="sxs-lookup"><span data-stu-id="4fac5-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="4fac5-111">A Run egy szelet feldolgozási egysége.</span><span class="sxs-lookup"><span data-stu-id="4fac5-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="4fac5-112">Lehet, hogy egy vagy több futás van egy slice-ra, ha újból próbálkozik, vagy ha a slice-ot a meghibásodások miatt újra futtatja.</span><span class="sxs-lookup"><span data-stu-id="4fac5-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="4fac5-113">A szeletet a kezdési időpontja azonosítja.</span><span class="sxs-lookup"><span data-stu-id="4fac5-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="4fac5-114">A szelet kezdési időpontjának beolvasásához használja az Get-AzDataFactorySlice parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4fac5-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="4fac5-115">Ha például a következő slice-hoz szeretne futni, használja a 2015-04-02T20:00:00 kezdési időpontot.</span><span class="sxs-lookup"><span data-stu-id="4fac5-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="4fac5-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM End: 5/3/2014 8:00:00 PM RetryCount: 0 Status: Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="4fac5-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="4fac5-117">Példák</span><span class="sxs-lookup"><span data-stu-id="4fac5-117">EXAMPLES</span></span>

### <span data-ttu-id="4fac5-118">Példa 1: adatkészlet beszerzése</span><span class="sxs-lookup"><span data-stu-id="4fac5-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

<span data-ttu-id="4fac5-119">Ez a parancs minden futást a WikiADF nevű adatDAWikiAggregatedDatai adatkészletnek a 05/21/2014-as verziójában, a 4 PM GMT-től kezdődően futtatja.</span><span class="sxs-lookup"><span data-stu-id="4fac5-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="4fac5-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fac5-120">PARAMETERS</span></span>

### <span data-ttu-id="4fac5-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fac5-121">-DataFactory</span></span>
<span data-ttu-id="4fac5-122">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4fac5-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4fac5-123">Ez a parancsmag akkor fog futni, ha az adatfeldolgozóhoz tartozó Slice-elemek szerepelnek, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4fac5-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4fac5-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4fac5-124">-DataFactoryName</span></span>
<span data-ttu-id="4fac5-125">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fac5-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4fac5-126">Ez a parancsmag akkor fog futni, ha az adatfeldolgozóhoz tartozó Slice-elemek szerepelnek, és ez a paraméter határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4fac5-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4fac5-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="4fac5-127">-DatasetName</span></span>
<span data-ttu-id="4fac5-128">Az adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fac5-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="4fac5-129">Ez a parancsmag a paraméter által megadott adatkészlethez tartozó szeletekhez fog futni.</span><span class="sxs-lookup"><span data-stu-id="4fac5-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="4fac5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fac5-130">-DefaultProfile</span></span>
<span data-ttu-id="4fac5-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4fac5-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fac5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fac5-132">-ResourceGroupName</span></span>
<span data-ttu-id="4fac5-133">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fac5-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4fac5-134">Ez a parancsmag beilleszti a Factory függvényt azokhoz a szeletekhez, amelyek a paraméter által definiált csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="4fac5-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4fac5-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="4fac5-135">-StartDateTime</span></span>
<span data-ttu-id="4fac5-136">Az időszak kezdését **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fac5-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="4fac5-137">Ez a parancsmag az adott időszaknak megfelelő adatszeletek esetén fut.</span><span class="sxs-lookup"><span data-stu-id="4fac5-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="4fac5-138">A *StartDateTime* a ISO8601-formátumban kell megadni, ahogyan az alábbi példákban: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific standard Time): az alapértelmezett időzóna-jelző az UTC.</span><span class="sxs-lookup"><span data-stu-id="4fac5-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="4fac5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fac5-139">CommonParameters</span></span>
<span data-ttu-id="4fac5-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fac5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fac5-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fac5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fac5-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fac5-142">INPUTS</span></span>

### <span data-ttu-id="4fac5-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4fac5-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4fac5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4fac5-144">System.String</span></span>

## <span data-ttu-id="4fac5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fac5-145">OUTPUTS</span></span>

### <span data-ttu-id="4fac5-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="4fac5-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="4fac5-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fac5-147">NOTES</span></span>
* <span data-ttu-id="4fac5-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="4fac5-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4fac5-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fac5-149">RELATED LINKS</span></span>

[<span data-ttu-id="4fac5-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="4fac5-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


