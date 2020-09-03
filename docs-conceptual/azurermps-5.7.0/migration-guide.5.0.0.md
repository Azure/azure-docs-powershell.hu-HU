---
title: A Microsoft Azure PowerShell 5.0.0 használhatatlanná tévő változásai
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell 5-ös verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 81f52ee8b84f60d59a7f2d53b6675129ac054fd6
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243735"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="8c150-103">A Microsoft Azure PowerShell 5.0.0 használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="8c150-104">Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak.</span><span class="sxs-lookup"><span data-stu-id="8c150-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="8c150-105">Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is.</span><span class="sxs-lookup"><span data-stu-id="8c150-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="8c150-106">A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="8c150-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="8c150-107">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="8c150-107">Table of Contents</span></span>

- [<span data-ttu-id="8c150-108">Az ApiManagement-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="8c150-109">A Batch-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="8c150-110">A Compute-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="8c150-111">Az EventHub-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="8c150-112">Az Insights-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="8c150-113">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="8c150-114">A Resources-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="8c150-115">A ServiceBus-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="8c150-116">Az ApiManagement-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="8c150-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="8c150-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="8c150-118">A „UserName” és a „Password” paraméter értéke PSCredential lett</span><span class="sxs-lookup"><span data-stu-id="8c150-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="8c150-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="8c150-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="8c150-120">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="8c150-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="8c150-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="8c150-122">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="8c150-123">A Batch-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="8c150-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="8c150-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="8c150-125">A `Password` paraméter értéke SecureString (biztonságos sztring) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="8c150-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="8c150-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="8c150-127">A `Password` paraméter értéke SecureString (biztonságos sztring) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="8c150-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="8c150-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="8c150-129">A `Password` paraméter értéke SecureString (biztonságos sztring) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="8c150-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="8c150-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="8c150-131">A `RunElevated` kapcsoló el lett távolítva, és a `UserIdentity` lépett a helyébe.</span><span class="sxs-lookup"><span data-stu-id="8c150-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="8c150-132">Ez befolyásolja a `RunElevated` tulajdonságot a következők esetében: `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` és `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="8c150-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="8c150-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="8c150-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="8c150-134">A `PSMultiInstanceSettings` konstruktor ezentúl nem egy kötelezően megadandó `numberOfInstances`, hanem egy kötelezően megadandó `coordinationCommandLine` paramétert vesz fel.</span><span class="sxs-lookup"><span data-stu-id="8c150-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="8c150-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="8c150-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="8c150-136">A `PSCloudTask``RunElevated` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="8c150-137">A `UserIdentity` tulajdonság lépett a `RunElevated` helyébe.</span><span class="sxs-lookup"><span data-stu-id="8c150-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="8c150-138">Ez befolyásolja a `RunElevated` tulajdonságot a következők esetében: `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` és `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="8c150-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="8c150-139">**Többféle típus**</span><span class="sxs-lookup"><span data-stu-id="8c150-139">**Multiple types**</span></span>

- <span data-ttu-id="8c150-140">A `PSExitConditions``SchedulingError` tulajdonsága új nevet kapott: `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="8c150-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="8c150-141">**Többféle típus**</span><span class="sxs-lookup"><span data-stu-id="8c150-141">**Multiple types**</span></span>

- <span data-ttu-id="8c150-142">A `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` és `PSTaskExecutionInformation``SchedulingError` tulajdonsága új nevet kapott: `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="8c150-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="8c150-143">A rendszer a `FailureInformation` tulajdonságot adja vissza minden tevékenységhiba esetén,</span><span class="sxs-lookup"><span data-stu-id="8c150-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="8c150-144">beleértve a korábbi ütemezési hibákat, a tevékenységek nullától eltérő kilépési kódjait, és az új kimeneti fájlok szolgáltatásának sikertelen fájlfeltöltéseit.</span><span class="sxs-lookup"><span data-stu-id="8c150-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="8c150-145">A szerkezet nem változott, tehát a típus használatakor nincs szükség a kód megváltoztatására.</span><span class="sxs-lookup"><span data-stu-id="8c150-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="8c150-146">A változás a következőket is érinti: Get-AzureBatchPool, Get-AzureBatchSubtask és Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="8c150-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="8c150-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="8c150-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="8c150-148">A `TargetDedicated` el lett távolítva, és a `TargetDedicatedComputeNodes` és `TargetLowPriorityComputeNodes` léptek a helyébe.</span><span class="sxs-lookup"><span data-stu-id="8c150-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="8c150-149">A `TargetDedicatedComputeNodes` kapott egy `TargetDedicated` aliast.</span><span class="sxs-lookup"><span data-stu-id="8c150-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="8c150-150">Szintén érintettek az alábbiak: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="8c150-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="8c150-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="8c150-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="8c150-152">A `PSCloudPool``TargetDedicated` és `CurrentDedicated` tulajdonságai új nevet kaptak: `TargetDedicatedComputeNodes` és `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="8c150-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="8c150-153">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="8c150-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="8c150-154">A `PSCloudPool``ResizeError` tulajdonsága új nevet kapott: `ResizeErrors`. Ez mostantól egy gyűjtemény.</span><span class="sxs-lookup"><span data-stu-id="8c150-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="8c150-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="8c150-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="8c150-156">A `PSPoolSpecification``TargetDedicated` tulajdonsága új nevet kapott: `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="8c150-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
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

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="8c150-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="8c150-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="8c150-158">A `Name` el lett távolítva, és a `Path` lépett a helyébe.</span><span class="sxs-lookup"><span data-stu-id="8c150-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="8c150-159">A `Path` kapott egy `Name` aliast.</span><span class="sxs-lookup"><span data-stu-id="8c150-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="8c150-160">Szintén érintettek az alábbiak: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="8c150-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="8c150-161">**PSNodeFile** típus</span><span class="sxs-lookup"><span data-stu-id="8c150-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="8c150-162">A `PSNodeFile``Name` tulajdonsága új nevet kapott: `Path`.</span><span class="sxs-lookup"><span data-stu-id="8c150-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="8c150-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="8c150-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="8c150-164">A `PSSubtaskInformation``PreviousState` és `State` tulajdonságai mostantól nem `TaskState`, hanem `SubtaskState` típusúak.</span><span class="sxs-lookup"><span data-stu-id="8c150-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="8c150-165">A `TaskState` tulajdonsággal ellentétben a `SubtaskState` tulajdonságnak nincs `Active` értéke, mivel az alfeladatok nem lehetnek `Active` állapotban.</span><span class="sxs-lookup"><span data-stu-id="8c150-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="8c150-166">A Compute-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="8c150-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="8c150-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="8c150-168">A „UserName” és a „Password” paraméter értéke PSCredential lett</span><span class="sxs-lookup"><span data-stu-id="8c150-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="8c150-169">Az EventHub-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8c150-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-171">A „New-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-172">Használja a következőt: „New-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="8c150-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8c150-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-174">A „Get-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-175">Használja a következőt: „Get-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="8c150-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8c150-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-177">A „Set-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-178">Használja a következőt: „Set-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="8c150-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8c150-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-180">A „Remove-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-181">Használja a következőt: „Remove-AzureRmEventHubAuthorizationRule”</span><span class="sxs-lookup"><span data-stu-id="8c150-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>

### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="8c150-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="8c150-183">A „New-AzureRmEventHubNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-184">Használja a következőt: „New-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="8c150-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>

### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="8c150-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="8c150-186">A „Get-AzureRmEventHubNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-187">Használja a következőt: „Get-AzureRmEventHubKey”</span><span class="sxs-lookup"><span data-stu-id="8c150-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="8c150-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="8c150-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="8c150-189">A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="8c150-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="8c150-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="8c150-191">A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="8c150-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="8c150-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="8c150-193">A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
```

### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="8c150-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="8c150-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="8c150-195">A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="8c150-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="8c150-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="8c150-197">A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="8c150-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="8c150-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="8c150-199">A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="8c150-200">Az Insights-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="8c150-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="8c150-202">Az **Add-AzureRMLogAlertRule** parancsmag elavult.</span><span class="sxs-lookup"><span data-stu-id="8c150-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="8c150-203">A parancsmag használatának október 1-jétől kezdve nem lesz hatása, mivel a funkció tevékenyégnapló-riasztásokra vált át.</span><span class="sxs-lookup"><span data-stu-id="8c150-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="8c150-204">További információ: https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="8c150-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="8c150-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="8c150-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="8c150-206">A **Get-AzureRMUsage** parancsmag elavult.</span><span class="sxs-lookup"><span data-stu-id="8c150-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="8c150-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="8c150-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="8c150-208">Kimeneti változás: az EventData objektum EventChannels mezője (amelyet a fenti parancsmagok adnak vissza) elavult, mivel mostantól egy állandó értéket ad vissza (Admin,Operation).</span><span class="sxs-lookup"><span data-stu-id="8c150-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="8c150-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="8c150-210">Kimeneti változás: a parancsmag kimenete egybesimított lesz (a tulajdonságok mező kiiktatásával) a felhasználói élmény javítása érdekében.</span><span class="sxs-lookup"><span data-stu-id="8c150-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
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

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="8c150-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="8c150-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="8c150-212">Kimeneti változás: az AutoscaleSettingResourceName mező elavult, mivel mindig a Name mezővel egyenlő.</span><span class="sxs-lookup"><span data-stu-id="8c150-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="8c150-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="8c150-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="8c150-214">Kimeneti változás: módosult a kimenet típusa, mostantól egyetlen objektumot ad vissza, amely tartalmazza a kérés azonosítóját és az állapotkódot.</span><span class="sxs-lookup"><span data-stu-id="8c150-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
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

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="8c150-215">A Network-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="8c150-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="8c150-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="8c150-217">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="8c150-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="8c150-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="8c150-219">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="8c150-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="8c150-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="8c150-221">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="8c150-222">A Resources-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="8c150-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="8c150-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="8c150-224">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="8c150-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="8c150-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="8c150-226">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="8c150-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="8c150-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="8c150-228">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="8c150-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="8c150-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="8c150-230">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="8c150-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="8c150-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="8c150-232">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="8c150-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="8c150-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="8c150-234">A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett</span><span class="sxs-lookup"><span data-stu-id="8c150-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="8c150-235">A ServiceBus-parancsmagok használhatatlanná tévő változásai</span><span class="sxs-lookup"><span data-stu-id="8c150-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8c150-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-237">A „Get-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-238">Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="8c150-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="8c150-240">A „Get-AzureRmServiceBusTopicKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-241">Használja a következőt: „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="8c150-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8c150-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-243">A „New-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-244">Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="8c150-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="8c150-246">A „New-AzureRmServiceBusTopicKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-247">Használja a következőt: „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="8c150-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8c150-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-249">A „Remove-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-250">Használja a következőt: „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8c150-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-252">A „Set-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-253">Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="8c150-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="8c150-255">A „New-AzureRmServiceBusNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-256">Használja a következőt: „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="8c150-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8c150-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-258">A „Get-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-259">Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="8c150-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="8c150-261">A „Get-AzureRmServiceBusQueueKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-262">Használja a következőt: „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="8c150-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8c150-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-264">A „New-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-265">Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="8c150-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="8c150-267">A „New-AzureRmServiceBusQueueKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-268">Használja a következőt: „New-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="8c150-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8c150-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-270">A „Remove-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-271">Használja a következőt: „GRemove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8c150-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-273">A „Set-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-274">Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8c150-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-276">A „Get-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-277">Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="8c150-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8c150-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="8c150-279">A „Get-AzureRmServiceBusNamespaceKey” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-280">Használja a következőt: „Get-AzureRmServiceBusKey”.</span><span class="sxs-lookup"><span data-stu-id="8c150-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8c150-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-282">A „New-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-283">Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8c150-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-285">A „Remove-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-286">Használja a következőt: „Remove-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8c150-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8c150-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8c150-288">A „Set-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8c150-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8c150-289">Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.</span><span class="sxs-lookup"><span data-stu-id="8c150-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="8c150-290">**NamespaceAttributes típus**</span><span class="sxs-lookup"><span data-stu-id="8c150-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="8c150-291">Az alábbi tulajdonságok lettek eltávolítva:</span><span class="sxs-lookup"><span data-stu-id="8c150-291">The following properties have been removed</span></span>
    - <span data-ttu-id="8c150-292">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8c150-292">Enabled</span></span>
    - <span data-ttu-id="8c150-293">status</span><span class="sxs-lookup"><span data-stu-id="8c150-293">Status</span></span>

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="8c150-294">**QueueAttribute típus**</span><span class="sxs-lookup"><span data-stu-id="8c150-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="8c150-295">Az alábbi tulajdonságok lettek megjelölve elavultként:</span><span class="sxs-lookup"><span data-stu-id="8c150-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="8c150-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="8c150-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="8c150-297">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8c150-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="8c150-298">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="8c150-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="8c150-299">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="8c150-299">SupportOrdering</span></span>

```powershell-interactive
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

### <a name="type-topicattribute"></a><span data-ttu-id="8c150-300">**TopicAttribute típus**</span><span class="sxs-lookup"><span data-stu-id="8c150-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="8c150-301">Az alábbi tulajdonságok lettek megjelölve elavultként:</span><span class="sxs-lookup"><span data-stu-id="8c150-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="8c150-302">Hely</span><span class="sxs-lookup"><span data-stu-id="8c150-302">Location</span></span>
    - <span data-ttu-id="8c150-303">IsExpress</span><span class="sxs-lookup"><span data-stu-id="8c150-303">IsExpress</span></span>
    - <span data-ttu-id="8c150-304">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="8c150-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="8c150-305">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="8c150-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="8c150-306">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="8c150-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="8c150-307">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8c150-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
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

### <a name="type-subscriptionattribute"></a><span data-ttu-id="8c150-308">**SubscriptionAttribute típus**</span><span class="sxs-lookup"><span data-stu-id="8c150-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="8c150-309">Az alábbi tulajdonságok lettek megjelölve elavultként:</span><span class="sxs-lookup"><span data-stu-id="8c150-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="8c150-310">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="8c150-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="8c150-311">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8c150-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="8c150-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="8c150-312">IsReadOnly</span></span>
    - <span data-ttu-id="8c150-313">Hely</span><span class="sxs-lookup"><span data-stu-id="8c150-313">Location</span></span>

```powershell-interactive
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
