---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497140"
---
# <span data-ttu-id="aad74-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="aad74-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="aad74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aad74-102">SYNOPSIS</span></span>
<span data-ttu-id="aad74-103">Kötegelt feladatokat kap egy köteg-vagy projekt-ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="aad74-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aad74-104">SYNTAX</span></span>

### <span data-ttu-id="aad74-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aad74-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aad74-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="aad74-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aad74-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="aad74-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aad74-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aad74-108">DESCRIPTION</span></span>
<span data-ttu-id="aad74-109">A **Get-AzureBatchJob** parancsmag az Azure kötegelt feldolgozásokat kapja a *BatchAccountContext* paraméterrel megadott köteg számlára.</span><span class="sxs-lookup"><span data-stu-id="aad74-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="aad74-110">Az *ID* paramétert használva egyetlen feladatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="aad74-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="aad74-111">A *szűrő* paraméterrel az Open Data Protocol (OData) szűrőhöz tartozó feladatok is elérhetők.</span><span class="sxs-lookup"><span data-stu-id="aad74-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="aad74-112">Ha projekt-ütemezési azonosítót vagy **PSCloudJobSchedule** -példányt ad meg, ez a parancsmag csak az adott projekthez tartozó feladatokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="aad74-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="aad74-113">Példák</span><span class="sxs-lookup"><span data-stu-id="aad74-113">EXAMPLES</span></span>

### <span data-ttu-id="aad74-114">Példa 1: kötegelt feladat beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="aad74-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="aad74-115">Ez a parancs a Job01 AZONOSÍTÓval rendelkező feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="aad74-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="aad74-116">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="aad74-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="aad74-117">2. példa: az aktív munkafolyamatok beszerzése ütemtervhez</span><span class="sxs-lookup"><span data-stu-id="aad74-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="aad74-118">Ez a parancs beilleszti az aktív munkafolyamatokat a JobSchedule27 azonosító munkabeosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="aad74-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="aad74-119">3. példa: a munkabeosztásban minden feladat beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="aad74-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="aad74-120">Ez a parancs azt a munkabeosztást kapja, amely az azonosító JobSchedule27 az Get-AzureBatchJobSchedule parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="aad74-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="aad74-121">A parancs a munkabeosztást átadja az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="aad74-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aad74-122">A parancs a projekt minden feladatát megkapja.</span><span class="sxs-lookup"><span data-stu-id="aad74-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="aad74-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aad74-123">PARAMETERS</span></span>

### <span data-ttu-id="aad74-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aad74-124">-BatchContext</span></span>
<span data-ttu-id="aad74-125">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="aad74-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aad74-126">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aad74-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="aad74-127">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="aad74-127">-Expand</span></span>
<span data-ttu-id="aad74-128">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aad74-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="aad74-129">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="aad74-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="aad74-130">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="aad74-130">-Filter</span></span>
<span data-ttu-id="aad74-131">A OData-szűrési záradékot adja meg a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="aad74-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="aad74-132">Ha nem ad meg szűrőt, ez a parancsmag a köteg-vagy a projekt-ütemterv minden feladatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="aad74-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad74-133">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="aad74-133">-Id</span></span>
<span data-ttu-id="aad74-134">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="aad74-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="aad74-135">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="aad74-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad74-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="aad74-136">-JobSchedule</span></span>
<span data-ttu-id="aad74-137">Itt adhatja meg azt a **PSCloudJobSchedule** -objektumot, amely a munkafolyamatokat tartalmazó projekt ütemtervét képviseli.</span><span class="sxs-lookup"><span data-stu-id="aad74-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="aad74-138">**PSCloudJobSchedule** objektum beolvasásához használja az Get-AzureBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aad74-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad74-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="aad74-139">-JobScheduleId</span></span>
<span data-ttu-id="aad74-140">A munkabeosztást tartalmazó projekt AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aad74-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad74-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="aad74-141">-MaxCount</span></span>
<span data-ttu-id="aad74-142">A visszaadni kívánt feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aad74-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="aad74-143">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="aad74-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="aad74-144">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="aad74-144">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad74-145">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="aad74-145">-Select</span></span>
<span data-ttu-id="aad74-146">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="aad74-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="aad74-147">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="aad74-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="aad74-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad74-148">-DefaultProfile</span></span>
<span data-ttu-id="aad74-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aad74-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad74-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad74-150">CommonParameters</span></span>
<span data-ttu-id="aad74-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aad74-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad74-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad74-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad74-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aad74-153">INPUTS</span></span>

### <span data-ttu-id="aad74-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aad74-154">BatchAccountContext</span></span>
<span data-ttu-id="aad74-155">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="aad74-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="aad74-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aad74-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="aad74-157">A ' JobSchedule ' paraméter az "PSCloudJobSchedule" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="aad74-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="aad74-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aad74-158">OUTPUTS</span></span>

### <span data-ttu-id="aad74-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="aad74-159">PSCloudJob</span></span>

## <span data-ttu-id="aad74-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aad74-160">NOTES</span></span>

## <span data-ttu-id="aad74-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aad74-161">RELATED LINKS</span></span>

[<span data-ttu-id="aad74-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="aad74-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="aad74-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="aad74-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="aad74-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aad74-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="aad74-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="aad74-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="aad74-166">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="aad74-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="aad74-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="aad74-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="aad74-168">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="aad74-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="aad74-169">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aad74-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


