---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: 1a177f0987f27f81f0ab27d5e35db11df17ae005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493266"
---
# <span data-ttu-id="bdd40-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdd40-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="bdd40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdd40-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd40-103">A kötegelt feladatokat kapja a projektben.</span><span class="sxs-lookup"><span data-stu-id="bdd40-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdd40-104">SYNTAX</span></span>

### <span data-ttu-id="bdd40-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdd40-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd40-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="bdd40-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdd40-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bdd40-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdd40-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdd40-108">DESCRIPTION</span></span>
<span data-ttu-id="bdd40-109">A **Get-AzureBatchTask** parancsmag Azure-köteg-műveleteket kap egy kötegelt feladathoz.</span><span class="sxs-lookup"><span data-stu-id="bdd40-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="bdd40-110">Adjon meg egy feladatot a *JobId* vagy a *Job* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="bdd40-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="bdd40-111">Ha egyetlen feladatot szeretne beszerezni, adja meg az *azonosító* paramétert.</span><span class="sxs-lookup"><span data-stu-id="bdd40-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="bdd40-112">Megadhatja a *szűrő* paramétert a megnyitott Data Protocol (OData) szűrőhöz tartozó feladatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="bdd40-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="bdd40-113">Példák</span><span class="sxs-lookup"><span data-stu-id="bdd40-113">EXAMPLES</span></span>

### <span data-ttu-id="bdd40-114">1. példa: tevékenység kérése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="bdd40-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="bdd40-115">Ez a parancs a feladatot az azonosító Task03 a Job Job01 csoportban kapja.</span><span class="sxs-lookup"><span data-stu-id="bdd40-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="bdd40-116">A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="bdd40-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bdd40-117">2. példa: az összes befejezett tevékenység lekérése egy megadott feladatból</span><span class="sxs-lookup"><span data-stu-id="bdd40-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="bdd40-118">Ez a parancs a befejezett feladatokat az azonosító Job02 tartalmazó feladatból kapja.</span><span class="sxs-lookup"><span data-stu-id="bdd40-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="bdd40-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdd40-119">PARAMETERS</span></span>

### <span data-ttu-id="bdd40-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bdd40-120">-BatchContext</span></span>
<span data-ttu-id="bdd40-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="bdd40-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bdd40-122">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="bdd40-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bdd40-123">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="bdd40-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bdd40-124">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="bdd40-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bdd40-125">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="bdd40-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bdd40-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd40-126">-DefaultProfile</span></span>
<span data-ttu-id="bdd40-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdd40-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd40-128">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="bdd40-128">-Expand</span></span>
<span data-ttu-id="bdd40-129">A OData kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdd40-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="bdd40-130">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="bdd40-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="bdd40-131">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="bdd40-131">-Filter</span></span>
<span data-ttu-id="bdd40-132">A tevékenységek OData-szűrési záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdd40-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="bdd40-133">Ha nem ad meg szűrőt, ez a parancsmag a köteg vagy a feladat összes tevékenységét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bdd40-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="bdd40-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bdd40-134">-Id</span></span>
<span data-ttu-id="bdd40-135">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="bdd40-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="bdd40-136">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="bdd40-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd40-137">-Job</span><span class="sxs-lookup"><span data-stu-id="bdd40-137">-Job</span></span>
<span data-ttu-id="bdd40-138">Azt a feladatot adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bdd40-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="bdd40-139">**PSCloudJob** objektum beolvasásához használja az Get-AzureBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bdd40-139">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd40-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="bdd40-140">-JobId</span></span>
<span data-ttu-id="bdd40-141">Annak a feladatnak az AZONOSÍTÓját adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bdd40-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd40-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bdd40-142">-MaxCount</span></span>
<span data-ttu-id="bdd40-143">Az eredményül adott feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdd40-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="bdd40-144">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="bdd40-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="bdd40-145">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="bdd40-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="bdd40-146">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="bdd40-146">-Select</span></span>
<span data-ttu-id="bdd40-147">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bdd40-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="bdd40-148">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="bdd40-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="bdd40-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd40-149">CommonParameters</span></span>
<span data-ttu-id="bdd40-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdd40-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd40-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd40-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd40-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd40-152">INPUTS</span></span>

### <span data-ttu-id="bdd40-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bdd40-153">BatchAccountContext</span></span>
<span data-ttu-id="bdd40-154">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bdd40-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bdd40-155">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="bdd40-155">PSCloudJob</span></span>
<span data-ttu-id="bdd40-156">A ' Job ' paraméter elfogadja a "PSCloudJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bdd40-156">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="bdd40-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd40-157">OUTPUTS</span></span>

### <span data-ttu-id="bdd40-158">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bdd40-158">PSCloudTask</span></span>

## <span data-ttu-id="bdd40-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdd40-159">NOTES</span></span>

## <span data-ttu-id="bdd40-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdd40-160">RELATED LINKS</span></span>

[<span data-ttu-id="bdd40-161">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bdd40-161">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bdd40-162">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="bdd40-162">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="bdd40-163">Új – AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdd40-163">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="bdd40-164">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdd40-164">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="bdd40-165">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="bdd40-165">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="bdd40-166">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bdd40-166">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


