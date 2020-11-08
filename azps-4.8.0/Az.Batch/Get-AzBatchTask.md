---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: bf1a70dc697366099f1949878e81a25bd3adb0fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025781"
---
# <span data-ttu-id="3a9ea-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a9ea-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="3a9ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9ea-103">A kötegelt feladatokat kapja a projektben.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="3a9ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a9ea-104">SYNTAX</span></span>

### <span data-ttu-id="3a9ea-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a9ea-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a9ea-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="3a9ea-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a9ea-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="3a9ea-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a9ea-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a9ea-108">DESCRIPTION</span></span>
<span data-ttu-id="3a9ea-109">A **Get-AzBatchTask** parancsmag Azure-köteg-műveleteket kap egy kötegelt feladathoz.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="3a9ea-110">Adjon meg egy feladatot a *JobId* vagy a *Job* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="3a9ea-111">Ha egyetlen feladatot szeretne beszerezni, adja meg az *azonosító* paramétert.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="3a9ea-112">Megadhatja a *szűrő* paramétert a megnyitott Data Protocol (OData) szűrőhöz tartozó feladatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="3a9ea-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3a9ea-113">EXAMPLES</span></span>

### <span data-ttu-id="3a9ea-114">1. példa: tevékenység kérése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="3a9ea-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="3a9ea-115">Ez a parancs a feladatot az azonosító Task03 a Job Job01 csoportban kapja.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="3a9ea-116">A Get-AzBatchAccountKey parancsmaggal társítson egy környezetet a $Context változóhoz.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3a9ea-117">2. példa: az összes befejezett tevékenység lekérése egy megadott feladatból</span><span class="sxs-lookup"><span data-stu-id="3a9ea-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="3a9ea-118">Ez a parancs a befejezett feladatokat az azonosító Job02 tartalmazó feladatból kapja.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="3a9ea-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a9ea-119">PARAMETERS</span></span>

### <span data-ttu-id="3a9ea-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3a9ea-120">-BatchContext</span></span>
<span data-ttu-id="3a9ea-121">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3a9ea-122">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3a9ea-123">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3a9ea-124">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3a9ea-125">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3a9ea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ea-126">-DefaultProfile</span></span>
<span data-ttu-id="3a9ea-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a9ea-128">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="3a9ea-128">-Expand</span></span>
<span data-ttu-id="3a9ea-129">A OData kibontási záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="3a9ea-130">Adjon meg egy értéket ehhez a paraméterhez a fő entitáshoz társított entitások beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="3a9ea-131">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="3a9ea-131">-Filter</span></span>
<span data-ttu-id="3a9ea-132">A tevékenységek OData-szűrési záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="3a9ea-133">Ha nem ad meg szűrőt, ez a parancsmag a köteg vagy a feladat összes tevékenységét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="3a9ea-134">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3a9ea-134">-Id</span></span>
<span data-ttu-id="3a9ea-135">Annak a tevékenységnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="3a9ea-136">A helyettesítő karakterek nem adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="3a9ea-137">-Job</span><span class="sxs-lookup"><span data-stu-id="3a9ea-137">-Job</span></span>
<span data-ttu-id="3a9ea-138">Azt a feladatot adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="3a9ea-139">**PSCloudJob** objektum beolvasásához használja az Get-AzBatchJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="3a9ea-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="3a9ea-140">-JobId</span></span>
<span data-ttu-id="3a9ea-141">Annak a feladatnak az AZONOSÍTÓját adja meg, amely a parancsmag által kapott feladatokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3a9ea-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3a9ea-142">-MaxCount</span></span>
<span data-ttu-id="3a9ea-143">Az eredményül adott feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="3a9ea-144">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="3a9ea-145">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="3a9ea-146">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="3a9ea-146">-Select</span></span>
<span data-ttu-id="3a9ea-147">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="3a9ea-148">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="3a9ea-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9ea-149">CommonParameters</span></span>
<span data-ttu-id="3a9ea-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a9ea-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9ea-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9ea-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a9ea-152">INPUTS</span></span>

### <span data-ttu-id="3a9ea-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3a9ea-153">System.String</span></span>

### <span data-ttu-id="3a9ea-154">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="3a9ea-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="3a9ea-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3a9ea-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3a9ea-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a9ea-156">OUTPUTS</span></span>

### <span data-ttu-id="3a9ea-157">Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3a9ea-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="3a9ea-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a9ea-158">NOTES</span></span>

## <span data-ttu-id="3a9ea-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a9ea-159">RELATED LINKS</span></span>

[<span data-ttu-id="3a9ea-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3a9ea-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3a9ea-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="3a9ea-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="3a9ea-162">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a9ea-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="3a9ea-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a9ea-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="3a9ea-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a9ea-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="3a9ea-165">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3a9ea-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
