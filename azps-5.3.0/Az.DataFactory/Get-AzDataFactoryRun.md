---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480437"
---
# <span data-ttu-id="fa995-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="fa995-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="fa995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa995-102">SYNOPSIS</span></span>
<span data-ttu-id="fa995-103">Egy adatkészlet adatszeletéhez fut az Azure Data Factoryban.</span><span class="sxs-lookup"><span data-stu-id="fa995-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="fa995-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa995-104">SYNTAX</span></span>

### <span data-ttu-id="fa995-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa995-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa995-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fa995-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa995-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa995-107">DESCRIPTION</span></span>
<span data-ttu-id="fa995-108">A **Get-AzDataFactoryRun** parancsmag az Azure Data Factoryban egy adatkészlet adatszeletéhez futtatja az adatokat.</span><span class="sxs-lookup"><span data-stu-id="fa995-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="fa995-109">Egy adatüzem adatkészlete szeletekből áll az időtengelyen.</span><span class="sxs-lookup"><span data-stu-id="fa995-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="fa995-110">A szeletek szélességét az ütemezés határozza meg óránként vagy naponta.</span><span class="sxs-lookup"><span data-stu-id="fa995-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="fa995-111">A futtatás egy szelet feldolgozásának egy mértékegysége.</span><span class="sxs-lookup"><span data-stu-id="fa995-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="fa995-112">Egy vagy több futtatás is lehet a szelethez újrajátszások esetén, illetve arra az esetre, ha hibák miatt újrafuttatja a szeletet.</span><span class="sxs-lookup"><span data-stu-id="fa995-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="fa995-113">A szeleteket a kezdési időpont azonosítja.</span><span class="sxs-lookup"><span data-stu-id="fa995-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="fa995-114">A szelet kezdési idejét a Get-AzDataFactorySlice ki.</span><span class="sxs-lookup"><span data-stu-id="fa995-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="fa995-115">A következő szelet futtatásához például használja a 2015-04-02T20:00:00 kezdési időt.</span><span class="sxs-lookup"><span data-stu-id="fa995-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="fa995-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingBlogaignEffectivenessBlobDataset Start : 2014.05.02.00:00 End : 2014.05.03 08:00:00 RetryCount: 0 Status: Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="fa995-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="fa995-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa995-117">EXAMPLES</span></span>

### <span data-ttu-id="fa995-118">1. példa: Adatkészlet lekérte</span><span class="sxs-lookup"><span data-stu-id="fa995-118">Example 1: Get a dataset</span></span>
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

<span data-ttu-id="fa995-119">Ez a parancs a DAWikiAggregatedData nevű adatkészlet szeletei számára fut a WikiADF adatüzemben, amely 2014.05.21-től (GMT) 2014.05.05-től kezdődik.</span><span class="sxs-lookup"><span data-stu-id="fa995-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="fa995-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa995-120">PARAMETERS</span></span>

### <span data-ttu-id="fa995-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fa995-121">-DataFactory</span></span>
<span data-ttu-id="fa995-122">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="fa995-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fa995-123">Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó szeletekre fut.</span><span class="sxs-lookup"><span data-stu-id="fa995-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa995-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fa995-124">-DataFactoryName</span></span>
<span data-ttu-id="fa995-125">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa995-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fa995-126">Ez a parancsmag a paraméter által megadott adat factoryhoz tartozó szeletekre fut.</span><span class="sxs-lookup"><span data-stu-id="fa995-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa995-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="fa995-127">-DatasetName</span></span>
<span data-ttu-id="fa995-128">Az adatkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa995-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="fa995-129">Ez a parancsmag a paraméter által megadott adatkészlethez tartozó szeletekre fut.</span><span class="sxs-lookup"><span data-stu-id="fa995-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa995-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa995-130">-DefaultProfile</span></span>
<span data-ttu-id="fa995-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fa995-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa995-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa995-132">-ResourceGroupName</span></span>
<span data-ttu-id="fa995-133">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa995-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fa995-134">Ez a parancsmag a paraméter által megadott csoporthoz tartozó szeletek gyári futását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa995-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa995-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="fa995-135">-StartDateTime</span></span>
<span data-ttu-id="fa995-136">Egy időtartomány kezdő időpontját adja meg **DateTime-objektumként.**</span><span class="sxs-lookup"><span data-stu-id="fa995-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="fa995-137">Ez a parancsmag az adott időszaknak megfelelő adatszeleteket futtatja.</span><span class="sxs-lookup"><span data-stu-id="fa995-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="fa995-138">A *StartDateTime* értéket ISO8601 formátumban kell megadni, ahogy az alábbi példákban is látható: 2015-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Csendes-óceáni téli idő) Az alapértelmezett időzóna-tervező az UTC.</span><span class="sxs-lookup"><span data-stu-id="fa995-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="fa995-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa995-139">CommonParameters</span></span>
<span data-ttu-id="fa995-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa995-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa995-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa995-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa995-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa995-142">INPUTS</span></span>

### <span data-ttu-id="fa995-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa995-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fa995-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fa995-144">System.String</span></span>

## <span data-ttu-id="fa995-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa995-145">OUTPUTS</span></span>

### <span data-ttu-id="fa995-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="fa995-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="fa995-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa995-147">NOTES</span></span>
* <span data-ttu-id="fa995-148">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="fa995-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fa995-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa995-149">RELATED LINKS</span></span>

[<span data-ttu-id="fa995-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="fa995-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


