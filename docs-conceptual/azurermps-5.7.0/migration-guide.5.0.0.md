# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="48f08-101">A Microsoft Azure PowerShell 5.0.0 használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="48f08-102">Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak.</span><span class="sxs-lookup"><span data-stu-id="48f08-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="48f08-103">Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is.</span><span class="sxs-lookup"><span data-stu-id="48f08-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="48f08-104">A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="48f08-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="48f08-105">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="48f08-105">Table of Contents</span></span>

- [<span data-ttu-id="48f08-106">Az ApiManagement-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="48f08-107">A Batch-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="48f08-108">A Compute-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="48f08-109">Az EventHub-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="48f08-110">Az Insights-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="48f08-111">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="48f08-112">A Resources-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="48f08-113">A ServiceBus-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="48f08-114">Az ApiManagement-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="48f08-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="48f08-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="48f08-116">A „UserName” és a „Password” paraméter értéke PSCredential lett</span><span class="sxs-lookup"><span data-stu-id="48f08-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="48f08-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="48f08-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="48f08-118">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="48f08-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="48f08-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="48f08-120">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="48f08-121">A Batch-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="48f08-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="48f08-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="48f08-123">A `Password` paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="48f08-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="48f08-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="48f08-125">A `Password` paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="48f08-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="48f08-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="48f08-127">A `Password` paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="48f08-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="48f08-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="48f08-129">A `RunElevated` kapcsoló el lett távolítva, és a `UserIdentity` lépett a helyébe.</span><span class="sxs-lookup"><span data-stu-id="48f08-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="48f08-130">Ez befolyásolja a `RunElevated` tulajdonságot a következők esetében: `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` és `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="48f08-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="48f08-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="48f08-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="48f08-132">A `PSMultiInstanceSettings` konstruktor ezentúl nem egy kötelezően megadandó `numberOfInstances`, hanem egy kötelezően megadandó `coordinationCommandLine` paramétert vesz fel.</span><span class="sxs-lookup"><span data-stu-id="48f08-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="48f08-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="48f08-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="48f08-134">A `PSCloudTask` `RunElevated` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="48f08-135">A `UserIdentity` tulajdonság lépett a `RunElevated` helyébe.</span><span class="sxs-lookup"><span data-stu-id="48f08-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="48f08-136">Ez befolyásolja a `RunElevated` tulajdonságot a következők esetében: `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` és `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="48f08-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="48f08-137">**Többféle típus**</span><span class="sxs-lookup"><span data-stu-id="48f08-137">**Multiple types**</span></span>

- <span data-ttu-id="48f08-138">A `PSExitConditions` `SchedulingError` tulajdonsága új nevet kapott: `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="48f08-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="48f08-139">**Többféle típus**</span><span class="sxs-lookup"><span data-stu-id="48f08-139">**Multiple types**</span></span>

- <span data-ttu-id="48f08-140">A `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` és `PSTaskExecutionInformation` `SchedulingError` tulajdonsága új nevet kapott: `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="48f08-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="48f08-141">A rendszer a `FailureInformation` tulajdonságot adja vissza minden tevékenységhiba esetén,</span><span class="sxs-lookup"><span data-stu-id="48f08-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="48f08-142">beleértve a korábbi ütemezési hibákat, a tevékenységek nullától eltérő kilépési kódjait, és az új kimeneti fájlok szolgáltatásának sikertelen fájlfeltöltéseit.</span><span class="sxs-lookup"><span data-stu-id="48f08-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="48f08-143">A szerkezet nem változott, tehát a típus használatakor nincs szükség a kód megváltoztatására.</span><span class="sxs-lookup"><span data-stu-id="48f08-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="48f08-144">A változás a következőket is érinti: Get-AzureBatchPool, Get-AzureBatchSubtask és Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="48f08-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="48f08-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="48f08-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="48f08-146">A `TargetDedicated` el lett távolítva, és a `TargetDedicatedComputeNodes` és `TargetLowPriorityComputeNodes` léptek a helyébe.</span><span class="sxs-lookup"><span data-stu-id="48f08-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="48f08-147">A `TargetDedicatedComputeNodes` kapott egy `TargetDedicated` aliast.</span><span class="sxs-lookup"><span data-stu-id="48f08-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="48f08-148">Szintén érintett: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="48f08-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="48f08-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="48f08-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="48f08-150">A `PSCloudPool` `TargetDedicated` és `CurrentDedicated` tulajdonságai új nevet kaptak: `TargetDedicatedComputeNodes` és `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="48f08-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="48f08-151">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="48f08-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="48f08-152">A `PSCloudPool` `ResizeError` tulajdonsága új nevet kapott: `ResizeErrors`. Ez mostantól egy gyűjtemény.</span><span class="sxs-lookup"><span data-stu-id="48f08-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="48f08-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="48f08-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="48f08-154">A `PSPoolSpecification` `TargetDedicated` tulajdonsága új nevet kapott: `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="48f08-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="48f08-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="48f08-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="48f08-156">A `Name` el lett távolítva, és a `Path` lépett a helyébe.</span><span class="sxs-lookup"><span data-stu-id="48f08-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="48f08-157">A `Path` kapott egy `Name` aliast.</span><span class="sxs-lookup"><span data-stu-id="48f08-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="48f08-158">Szintén érintett: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="48f08-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="48f08-159">**PSNodeFile** típus</span><span class="sxs-lookup"><span data-stu-id="48f08-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="48f08-160">A `PSNodeFile` `Name` tulajdonsága új nevet kapott: `Path`.</span><span class="sxs-lookup"><span data-stu-id="48f08-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="48f08-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="48f08-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="48f08-162">A `PSSubtaskInformation` `PreviousState` és `State` tulajdonságai mostantól nem `TaskState`, hanem `SubtaskState` típusúak.</span><span class="sxs-lookup"><span data-stu-id="48f08-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="48f08-163">A `TaskState` tulajdonsággal ellentétben a `SubtaskState` tulajdonságnak nincs `Active` értéke, mivel az alfeladatok nem lehetnek `Active` állapotban.</span><span class="sxs-lookup"><span data-stu-id="48f08-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="48f08-164">A Compute-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="48f08-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="48f08-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="48f08-166">A „UserName” és a „Password” paraméter értéke PSCredential lett</span><span class="sxs-lookup"><span data-stu-id="48f08-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="48f08-167">Az EventHub-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="48f08-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-169">A „New-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-170">Használja a következőt: „New-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="48f08-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="48f08-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-172">A „Get-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-173">Használja a következőt: „Get-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="48f08-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="48f08-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-175">A „Set-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-176">Használja a következőt: „Set-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="48f08-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="48f08-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-178">A „Remove-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-179">Használja a következőt: „Remove-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="48f08-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="48f08-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="48f08-181">A „New-AzureRmEventHubNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-182">Használja a következőt: „New-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="48f08-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="48f08-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="48f08-184">A „Get-AzureRmEventHubNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-185">Használja a következőt: „Get-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="48f08-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="48f08-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="48f08-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="48f08-187">A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="48f08-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="48f08-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="48f08-189">A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="48f08-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="48f08-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="48f08-191">A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="48f08-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="48f08-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="48f08-193">A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="48f08-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="48f08-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="48f08-195">A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="48f08-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="48f08-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="48f08-197">A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="48f08-198">Az Insights-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="48f08-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="48f08-200">Az **Add-AzureRMLogAlertRule** parancsmag elavult.</span><span class="sxs-lookup"><span data-stu-id="48f08-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="48f08-201">A parancsmag használatának október 1-jétől kezdve nem lesz hatása, mivel a funkció tevékenyégnapló-riasztásokra vált át.</span><span class="sxs-lookup"><span data-stu-id="48f08-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="48f08-202">További információ: https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="48f08-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="48f08-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="48f08-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="48f08-204">A **Get-AzureRMUsage** parancsmag elavult.</span><span class="sxs-lookup"><span data-stu-id="48f08-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="48f08-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="48f08-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="48f08-206">Kimeneti változás: az EventData objektum EventChannels mezője (amelyet a fenti parancsmagok adnak vissza) elavult, mivel mostantól egy állandó értéket ad vissza (Admin,Operation).</span><span class="sxs-lookup"><span data-stu-id="48f08-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="48f08-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="48f08-208">Kimeneti változás: a parancsmag kimenete egybesimított lesz (a tulajdonságok mező kiiktatásával) a felhasználói élmény javítása érdekében.</span><span class="sxs-lookup"><span data-stu-id="48f08-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="48f08-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="48f08-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="48f08-210">Kimeneti változás: az AutoscaleSettingResourceName mező elavult, mivel mindig a Name mezővel egyenlő.</span><span class="sxs-lookup"><span data-stu-id="48f08-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="48f08-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="48f08-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="48f08-212">Kimeneti változás: módosult a kimenet típusa, mostantól egyetlen objektumot ad vissza, amely tartalmazza a kérés azonosítóját és az állapotkódot.</span><span class="sxs-lookup"><span data-stu-id="48f08-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="48f08-213">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="48f08-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="48f08-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="48f08-215">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="48f08-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="48f08-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="48f08-217">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="48f08-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="48f08-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="48f08-219">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="48f08-220">A Resources-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="48f08-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="48f08-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="48f08-222">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="48f08-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="48f08-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="48f08-224">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="48f08-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="48f08-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="48f08-226">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="48f08-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="48f08-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="48f08-228">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="48f08-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="48f08-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="48f08-230">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="48f08-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="48f08-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="48f08-232">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="48f08-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="48f08-233">A ServiceBus-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="48f08-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="48f08-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-235">A „Get-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-236">Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="48f08-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="48f08-238">A „Get-AzureRmServiceBusTopicKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-239">Használja a következőt: „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="48f08-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="48f08-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-241">A „New-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-242">Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="48f08-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="48f08-244">A „New-AzureRmServiceBusTopicKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-245">Használja a következőt: „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="48f08-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="48f08-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-247">A „Remove-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-248">Használja a következőt: „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="48f08-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-250">A „Set-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-251">Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="48f08-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="48f08-253">A „New-AzureRmServiceBusNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-254">Használja a következőt: „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="48f08-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="48f08-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-256">A „Get-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-257">Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="48f08-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="48f08-259">A „Get-AzureRmServiceBusQueueKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-260">Használja a következőt: „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="48f08-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="48f08-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-262">A „New-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-263">Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="48f08-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="48f08-265">A „New-AzureRmServiceBusQueueKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-266">Használja a következőt: „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="48f08-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="48f08-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-268">A „Remove-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-269">Használja a következőt: „GRemove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="48f08-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-271">A „Set-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-272">Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="48f08-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-274">A „Get-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-275">Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="48f08-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="48f08-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="48f08-277">A „Get-AzureRmServiceBusNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-278">Használja a következőt: „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="48f08-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="48f08-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-280">A „New-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-281">Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="48f08-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-283">A „Remove-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-284">Használja a következőt: „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="48f08-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="48f08-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="48f08-286">A „Set-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="48f08-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="48f08-287">Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="48f08-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="48f08-288">**NamespaceAttributes típus**</span><span class="sxs-lookup"><span data-stu-id="48f08-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="48f08-289">Az alábbi tulajdonságok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="48f08-289">The following properties have been removed</span></span>
    - <span data-ttu-id="48f08-290">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="48f08-290">Enabled</span></span>
    - <span data-ttu-id="48f08-291">status</span><span class="sxs-lookup"><span data-stu-id="48f08-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="48f08-292">**QueueAttribute típus**</span><span class="sxs-lookup"><span data-stu-id="48f08-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="48f08-293">Az alábbi tulajdonságok lettek megjelölve elavultként:</span><span class="sxs-lookup"><span data-stu-id="48f08-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="48f08-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="48f08-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="48f08-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="48f08-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="48f08-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="48f08-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="48f08-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="48f08-297">SupportOrdering</span></span>

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="48f08-298">**TopicAttribute típus**</span><span class="sxs-lookup"><span data-stu-id="48f08-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="48f08-299">Az alábbi tulajdonságok lettek megjelölve elavultként:</span><span class="sxs-lookup"><span data-stu-id="48f08-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="48f08-300">Hely</span><span class="sxs-lookup"><span data-stu-id="48f08-300">Location</span></span>
    - <span data-ttu-id="48f08-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="48f08-301">IsExpress</span></span>
    - <span data-ttu-id="48f08-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="48f08-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="48f08-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="48f08-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="48f08-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="48f08-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="48f08-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="48f08-305">EntityAvailabilityStatus</span></span>

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="48f08-306">**SubscriptionAttribute típus**</span><span class="sxs-lookup"><span data-stu-id="48f08-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="48f08-307">Az alábbi tulajdonságok lettek megjelölve elavultként:</span><span class="sxs-lookup"><span data-stu-id="48f08-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="48f08-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="48f08-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="48f08-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="48f08-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="48f08-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="48f08-310">IsReadOnly</span></span>
    - <span data-ttu-id="48f08-311">Hely</span><span class="sxs-lookup"><span data-stu-id="48f08-311">Location</span></span>
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```