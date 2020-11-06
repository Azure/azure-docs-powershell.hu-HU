---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: 2b9b9fbeb4c1e29ef4a56b1dd00e09579fbbe7b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502620"
---
# <span data-ttu-id="b4da6-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4da6-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="b4da6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4da6-102">SYNOPSIS</span></span>
<span data-ttu-id="b4da6-103">Kötegelt feladatokat kap egy köteg-vagy projekt-ütemtervhez.</span><span class="sxs-lookup"><span data-stu-id="b4da6-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4da6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4da6-104">SYNTAX</span></span>

### <span data-ttu-id="b4da6-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4da6-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4da6-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="b4da6-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4da6-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4da6-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4da6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4da6-108">DESCRIPTION</span></span>
<span data-ttu-id="b4da6-109">A **Get-AzureBatchJob** parancsmag az Azure kötegelt feldolgozásokat kapja a *BatchAccountContext* paraméterrel megadott köteg számlára.</span><span class="sxs-lookup"><span data-stu-id="b4da6-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="b4da6-110">Az *ID* paramétert használva egyetlen feladatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="b4da6-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="b4da6-111">A *szűrő* paraméterrel az Open Data Protocol (OData) szűrőhöz tartozó feladatok is elérhetők.</span><span class="sxs-lookup"><span data-stu-id="b4da6-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="b4da6-112">Ha projekt-ütemezési azonosítót vagy **PSCloudJobSchedule** -példányt ad meg, ez a parancsmag csak az adott projekthez tartozó feladatokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b4da6-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="b4da6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b4da6-113">EXAMPLES</span></span>

### <span data-ttu-id="b4da6-114">Példa 1: kötegelt feladat beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="b4da6-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="b4da6-115">Ez a parancs a Job01 AZONOSÍTÓval rendelkező feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="b4da6-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="b4da6-116">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="b4da6-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b4da6-117">2. példa: az aktív munkafolyamatok beszerzése ütemtervhez</span><span class="sxs-lookup"><span data-stu-id="b4da6-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="b4da6-118">Ez a parancs beilleszti az aktív munkafolyamatokat a JobSchedule27 azonosító munkabeosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="b4da6-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="b4da6-119">3. példa: a munkabeosztásban minden feladat beolvasása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="b4da6-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="b4da6-120">Ez a parancs azt a munkabeosztást kapja, amely az azonosító JobSchedule27 az Get-AzureBatchJobSchedule parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b4da6-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="b4da6-121">A parancs a munkabeosztást átadja az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="b4da6-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4da6-122">A parancs a projekt minden feladatát megkapja.</span><span class="sxs-lookup"><span data-stu-id="b4da6-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="b4da6-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4da6-123">PARAMETERS</span></span>

### <span data-ttu-id="b4da6-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4da6-124">-BatchContext</span></span>
<span data-ttu-id="b4da6-125">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b4da6-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4da6-126">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b4da6-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4da6-127">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="b4da6-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4da6-128">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="b4da6-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4da6-129">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="b4da6-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4da6-130">-DefaultProfile</span></span>
<span data-ttu-id="b4da6-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4da6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4da6-132">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="b4da6-132">-Expand</span></span>
<span data-ttu-id="b4da6-133">Az Open Data Protocol (OData) kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4da6-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b4da6-134">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz tartozó társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="b4da6-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-135">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b4da6-135">-Filter</span></span>
<span data-ttu-id="b4da6-136">A OData-szűrési záradékot adja meg a feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="b4da6-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="b4da6-137">Ha nem ad meg szűrőt, ez a parancsmag a köteg-vagy a projekt-ütemterv minden feladatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b4da6-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-138">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b4da6-138">-Id</span></span>
<span data-ttu-id="b4da6-139">Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b4da6-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="b4da6-140">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="b4da6-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4da6-141">-JobSchedule</span></span>
<span data-ttu-id="b4da6-142">Itt adhatja meg azt a **PSCloudJobSchedule** -objektumot, amely a munkafolyamatokat tartalmazó projekt ütemtervét képviseli.</span><span class="sxs-lookup"><span data-stu-id="b4da6-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="b4da6-143">**PSCloudJobSchedule** objektum beolvasásához használja az Get-AzureBatchJobSchedule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4da6-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="b4da6-144">-JobScheduleId</span></span>
<span data-ttu-id="b4da6-145">A munkabeosztást tartalmazó projekt AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4da6-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b4da6-146">-MaxCount</span></span>
<span data-ttu-id="b4da6-147">A visszaadni kívánt feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4da6-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="b4da6-148">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="b4da6-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b4da6-149">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="b4da6-149">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-150">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="b4da6-150">-Select</span></span>
<span data-ttu-id="b4da6-151">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b4da6-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="b4da6-152">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="b4da6-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4da6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4da6-153">CommonParameters</span></span>
<span data-ttu-id="b4da6-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4da6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4da6-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4da6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4da6-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4da6-156">INPUTS</span></span>

### <span data-ttu-id="b4da6-157">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4da6-157">BatchAccountContext</span></span>
<span data-ttu-id="b4da6-158">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b4da6-158">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b4da6-159">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4da6-159">PSCloudJobSchedule</span></span>
<span data-ttu-id="b4da6-160">A ' JobSchedule ' paraméter az "PSCloudJobSchedule" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b4da6-160">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="b4da6-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4da6-161">OUTPUTS</span></span>

### <span data-ttu-id="b4da6-162">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b4da6-162">PSCloudJob</span></span>

## <span data-ttu-id="b4da6-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4da6-163">NOTES</span></span>

## <span data-ttu-id="b4da6-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4da6-164">RELATED LINKS</span></span>

[<span data-ttu-id="b4da6-165">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4da6-165">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="b4da6-166">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4da6-166">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="b4da6-167">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b4da6-167">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b4da6-168">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b4da6-168">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="b4da6-169">Új – AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4da6-169">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="b4da6-170">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4da6-170">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="b4da6-171">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4da6-171">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="b4da6-172">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b4da6-172">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


