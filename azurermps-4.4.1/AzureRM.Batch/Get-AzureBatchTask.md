---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: fb01af87d28323e3e25c46868f94e892b835afc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502779"
---
# <span data-ttu-id="a4f83-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4f83-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="a4f83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4f83-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f83-103">A kötegelt feladatokat kapja a projektben.</span><span class="sxs-lookup"><span data-stu-id="a4f83-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4f83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4f83-104">SYNTAX</span></span>

### <span data-ttu-id="a4f83-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4f83-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4f83-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="a4f83-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4f83-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="a4f83-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4f83-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4f83-108">DESCRIPTION</span></span>
<span data-ttu-id="a4f83-109">A **Get-AzureBatchTask** parancsmag Azure-köteg-műveleteket kap egy kötegelt feladathoz.</span><span class="sxs-lookup"><span data-stu-id="a4f83-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="a4f83-110">Adjon meg egy feladatot a *JobId* vagy a *Job* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="a4f83-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="a4f83-111">Ha egyetlen feladatot szeretne beszerezni, adja meg az *azonosító* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a4f83-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="a4f83-112">Megadhatja a *szűrő* paramétert a megnyitott Data Protocol (OData) szűrőhöz tartozó feladatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="a4f83-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="a4f83-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a4f83-113">EXAMPLES</span></span>

### <span data-ttu-id="a4f83-114">1. példa: tevékenység kérése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="a4f83-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="a4f83-115">Ez a parancs a feladatot az azonosító Task03 a Job Job01 csoportban kapja.</span><span class="sxs-lookup"><span data-stu-id="a4f83-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="a4f83-116">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="a4f83-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a4f83-117">2. példa: az összes befejezett tevékenység lekérése egy megadott feladatból</span><span class="sxs-lookup"><span data-stu-id="a4f83-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="a4f83-118">Ez a parancs a befejezett feladatokat az azonosító Job02 tartalmazó feladatból kapja.</span><span class="sxs-lookup"><span data-stu-id="a4f83-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="a4f83-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4f83-119">PARAMETERS</span></span>

### <span data-ttu-id="a4f83-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a4f83-120">-BatchContext</span></span>
<span data-ttu-id="a4f83-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="a4f83-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a4f83-122">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4f83-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a4f83-123">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="a4f83-123">-Expand</span></span>
<span data-ttu-id="a4f83-124">A OData kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4f83-124">Specifies an OData expand clause.</span></span>
<span data-ttu-id="a4f83-125">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="a4f83-125">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="a4f83-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="a4f83-126">-Filter</span></span>
<span data-ttu-id="a4f83-127">A tevékenységek OData-szűrési záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4f83-127">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="a4f83-128">Ha nem ad meg szűrőt, ez a parancsmag a köteg vagy a feladat összes tevékenységét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a4f83-128">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="a4f83-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a4f83-129">-Id</span></span>
<span data-ttu-id="a4f83-130">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a4f83-130">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="a4f83-131">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="a4f83-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f83-132">-Job</span><span class="sxs-lookup"><span data-stu-id="a4f83-132">-Job</span></span>
<span data-ttu-id="a4f83-133">Azt a feladatot adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a4f83-133">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="a4f83-134">**PSCloudJob** objektum beolvasásához használja az Get-AzureBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4f83-134">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f83-135">-JobId</span><span class="sxs-lookup"><span data-stu-id="a4f83-135">-JobId</span></span>
<span data-ttu-id="a4f83-136">Annak a feladatnak az AZONOSÍTÓját adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a4f83-136">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f83-137">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a4f83-137">-MaxCount</span></span>
<span data-ttu-id="a4f83-138">Az eredményül adott feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4f83-138">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="a4f83-139">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="a4f83-139">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="a4f83-140">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="a4f83-140">The default value is 1000.</span></span>

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

### <span data-ttu-id="a4f83-141">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="a4f83-141">-Select</span></span>
<span data-ttu-id="a4f83-142">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a4f83-142">Specifies an OData select clause.</span></span>
<span data-ttu-id="a4f83-143">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="a4f83-143">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="a4f83-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f83-144">-DefaultProfile</span></span>
<span data-ttu-id="a4f83-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4f83-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4f83-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f83-146">CommonParameters</span></span>
<span data-ttu-id="a4f83-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4f83-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f83-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f83-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f83-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4f83-149">INPUTS</span></span>

### <span data-ttu-id="a4f83-150">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a4f83-150">BatchAccountContext</span></span>
<span data-ttu-id="a4f83-151">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a4f83-151">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a4f83-152">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a4f83-152">PSCloudJob</span></span>
<span data-ttu-id="a4f83-153">A ' Job ' paraméter elfogadja a "PSCloudJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a4f83-153">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="a4f83-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4f83-154">OUTPUTS</span></span>

### <span data-ttu-id="a4f83-155">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a4f83-155">PSCloudTask</span></span>

## <span data-ttu-id="a4f83-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4f83-156">NOTES</span></span>

## <span data-ttu-id="a4f83-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4f83-157">RELATED LINKS</span></span>

[<span data-ttu-id="a4f83-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a4f83-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a4f83-159">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4f83-159">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a4f83-160">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4f83-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="a4f83-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4f83-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="a4f83-162">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a4f83-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="a4f83-163">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a4f83-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


