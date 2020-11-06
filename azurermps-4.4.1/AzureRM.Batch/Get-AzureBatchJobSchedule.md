---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497135"
---
# <span data-ttu-id="cf055-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf055-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="cf055-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf055-102">SYNOPSIS</span></span>
<span data-ttu-id="cf055-103">Kötegelt munka ütemezéseit kapja.</span><span class="sxs-lookup"><span data-stu-id="cf055-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf055-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf055-104">SYNTAX</span></span>

### <span data-ttu-id="cf055-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf055-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf055-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="cf055-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf055-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf055-107">DESCRIPTION</span></span>
<span data-ttu-id="cf055-108">A **Get-AzureBatchJobSchedule** parancsmag Azure kötegelt feladatok ütemezéseit kapja meg a *BatchContext* paraméter által megadott köteg számlára.</span><span class="sxs-lookup"><span data-stu-id="cf055-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="cf055-109">Adjon meg egy azonosítót egyetlen munkaütemezés beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="cf055-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="cf055-110">Adja meg azt a *szűrési* paramétert, amely egy Open Data Protocol (OData) szűrőnek megfelelő munkabeosztásokat kap.</span><span class="sxs-lookup"><span data-stu-id="cf055-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="cf055-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cf055-111">EXAMPLES</span></span>

### <span data-ttu-id="cf055-112">Példa 1: beosztás beszerzése az azonosító megadásával</span><span class="sxs-lookup"><span data-stu-id="cf055-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="cf055-113">Ez a parancs a JobSchedule23 AZONOSÍTÓval rendelkező munkabeosztást kapja.</span><span class="sxs-lookup"><span data-stu-id="cf055-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="cf055-114">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="cf055-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cf055-115">2. példa: nyomtatási ütemtervek beszerzése szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="cf055-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 : 
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="cf055-116">Ez a parancs a *szűrési* paraméter megadásával beilleszti az összes olyan munkabeosztást, amelynek a feladattal kezdődő azonosítói vannak.</span><span class="sxs-lookup"><span data-stu-id="cf055-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="cf055-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf055-117">PARAMETERS</span></span>

### <span data-ttu-id="cf055-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cf055-118">-BatchContext</span></span>
<span data-ttu-id="cf055-119">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="cf055-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf055-120">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cf055-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf055-121">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="cf055-121">-Expand</span></span>
<span data-ttu-id="cf055-122">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf055-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="cf055-123">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="cf055-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf055-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="cf055-124">-Filter</span></span>
<span data-ttu-id="cf055-125">Egy OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cf055-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="cf055-126">Ez a parancsmag olyan munkabeosztásokat ad eredményül, amelyek megfelelnek a paraméter által megadott szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="cf055-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="cf055-127">Ha nem ad meg szűrőt, ez a parancsmag a köteg környezetéhez tartozó összes nyomtatási ütemtervet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cf055-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf055-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cf055-128">-Id</span></span>
<span data-ttu-id="cf055-129">A parancsmag által beolvasott ütemterv AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf055-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="cf055-130">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="cf055-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf055-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cf055-131">-MaxCount</span></span>
<span data-ttu-id="cf055-132">Az eredményül adott munkabeosztások maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf055-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="cf055-133">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="cf055-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="cf055-134">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="cf055-134">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf055-135">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="cf055-135">-Select</span></span>
<span data-ttu-id="cf055-136">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="cf055-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="cf055-137">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="cf055-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf055-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf055-138">-DefaultProfile</span></span>
<span data-ttu-id="cf055-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf055-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf055-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf055-140">CommonParameters</span></span>
<span data-ttu-id="cf055-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf055-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf055-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf055-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf055-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf055-143">INPUTS</span></span>

### <span data-ttu-id="cf055-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf055-144">BatchAccountContext</span></span>
<span data-ttu-id="cf055-145">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cf055-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cf055-146">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="cf055-146">String</span></span>
<span data-ttu-id="cf055-147">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="cf055-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cf055-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf055-148">OUTPUTS</span></span>

### <span data-ttu-id="cf055-149">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf055-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="cf055-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf055-150">NOTES</span></span>

## <span data-ttu-id="cf055-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf055-151">RELATED LINKS</span></span>

[<span data-ttu-id="cf055-152">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf055-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf055-153">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf055-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf055-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cf055-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cf055-155">Új – AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf055-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf055-156">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf055-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf055-157">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf055-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf055-158">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cf055-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


