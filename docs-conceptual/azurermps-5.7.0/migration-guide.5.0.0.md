---
title: A Microsoft Azure PowerShell 5.0.0 használhatatlanná tévő változásai
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell 5-ös verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: f8dc413a91876e53e62d25cc38ac3b3ef6afda8e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534593"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>A Microsoft Azure PowerShell 5.0.0 használhatatlanná tévő változásai

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak. Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is. A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.

## <a name="table-of-contents"></a>Tartalomjegyzék

- [Az ApiManagement-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-apimanagement-cmdlets)
- [A Batch-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-batch-cmdlets)
- [A Compute-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-compute-cmdlets)
- [Az EventHub-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-eventhub-cmdlets)
- [Az Insights-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-insights-cmdlets)
- [A Network-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-network-cmdlets)
- [A Resources-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-resources-cmdlets)
- [A ServiceBus-parancsmagok használhatatlanná tévő változásai](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Az ApiManagement-parancsmagok használhatatlanná tévő változásai

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- A „UserName” és a „Password” paraméter értéke PSCredential lett

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>A Batch-parancsmagok használhatatlanná tévő változásai

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- A `Password` paraméter értéke SecureString (biztonságos sztring) lett

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- A `Password` paraméter értéke SecureString (biztonságos sztring) lett

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- A `Password` paraméter értéke SecureString (biztonságos sztring) lett

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - A `RunElevated` kapcsoló el lett távolítva, és a `UserIdentity` lépett a helyébe.

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

Ez befolyásolja a `RunElevated` tulajdonságot a következők esetében: `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` és `PSJobReleaseTask`.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- A `PSMultiInstanceSettings` konstruktor ezentúl nem egy kötelezően megadandó `numberOfInstances`, hanem egy kötelezően megadandó `coordinationCommandLine` paramétert vesz fel.

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - A `PSCloudTask``RunElevated` tulajdonsága el lett távolítva. A `UserIdentity` tulajdonság lépett a `RunElevated` helyébe.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

Ez befolyásolja a `RunElevated` tulajdonságot a következők esetében: `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` és `PSJobReleaseTask`.

### <a name="multiple-types"></a>**Többféle típus**

- A `PSExitConditions``SchedulingError` tulajdonsága új nevet kapott: `PreProcessingError`.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**Többféle típus**

- A `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` és `PSTaskExecutionInformation``SchedulingError` tulajdonsága új nevet kapott: `FailureInformation`.
  - A rendszer a `FailureInformation` tulajdonságot adja vissza minden tevékenységhiba esetén, beleértve a korábbi ütemezési hibákat, a tevékenységek nullától eltérő kilépési kódjait, és az új kimeneti fájlok szolgáltatásának sikertelen fájlfeltöltéseit.
  - A szerkezet nem változott, tehát a típus használatakor nincs szükség a kód megváltoztatására.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

A változás a következőket is érinti: Get-AzureBatchPool, Get-AzureBatchSubtask és Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - A `TargetDedicated` el lett távolítva, és a `TargetDedicatedComputeNodes` és `TargetLowPriorityComputeNodes` léptek a helyébe.
 - A `TargetDedicatedComputeNodes` kapott egy `TargetDedicated` aliast.

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

Szintén érintettek az alábbiak: Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - A `PSCloudPool``TargetDedicated` és `CurrentDedicated` tulajdonságai új nevet kaptak: `TargetDedicatedComputeNodes` és `CurrentDedicatedComputeNodes`.

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

### <a name="type-pscloudpool"></a>**Type PSCloudPool**

- A `PSCloudPool``ResizeError` tulajdonsága új nevet kapott: `ResizeErrors`. Ez mostantól egy gyűjtemény.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- A `PSPoolSpecification``TargetDedicated` tulajdonsága új nevet kapott: `TargetDedicatedComputeNodes`.

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

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - A `Name` el lett távolítva, és a `Path` lépett a helyébe.
 - A `Path` kapott egy `Name` aliast.

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

Szintén érintettek az alábbiak: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>**PSNodeFile** típus

 - A `PSNodeFile``Name` tulajdonsága új nevet kapott: `Path`.

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- A `PSSubtaskInformation``PreviousState` és `State` tulajdonságai mostantól nem `TaskState`, hanem `SubtaskState` típusúak.
  - A `TaskState` tulajdonsággal ellentétben a `SubtaskState` tulajdonságnak nincs `Active` értéke, mivel az alfeladatok nem lehetnek `Active` állapotban.

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>A Compute-parancsmagok használhatatlanná tévő változásai

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- A „UserName” és a „Password” paraméter értéke PSCredential lett

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Az EventHub-parancsmagok használhatatlanná tévő változásai

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- A „New-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmEventHubAuthorizationRule”
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- A „Get-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmEventHubAuthorizationRule”
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- A „Set-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Set-AzureRmEventHubAuthorizationRule”
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- A „Remove-AzureRmEventHubNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Remove-AzureRmEventHubAuthorizationRule”
    
### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- A „New-AzureRmEventHubNamespaceKey” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmEventHubKey”
    
### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- A „Get-AzureRmEventHubNamespaceKey” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmEventHubKey”
    
### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva. 

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
    
### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva. 

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
    
### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- A NamespceAttributes „Status” és „Enabled” tulajdonságai el lesznek távolítva. 

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
  
### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- A ConsumerGroupAttributes „EventHubPath” tulajdonsága el lesz távolítva.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Az Insights-parancsmagok használhatatlanná tévő változásai

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- Az **Add-AzureRMLogAlertRule** parancsmag elavult.
- A parancsmag használatának október 1-jétől kezdve nem lesz hatása, mivel a funkció tevékenyégnapló-riasztásokra vált át. További információ: https://aka.ms/migratemealerts.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- A **Get-AzureRMUsage** parancsmag elavult.

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- Kimeneti változás: az EventData objektum EventChannels mezője (amelyet a fenti parancsmagok adnak vissza) elavult, mivel mostantól egy állandó értéket ad vissza (Admin,Operation).

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- Kimeneti változás: a parancsmag kimenete egybesimított lesz (a tulajdonságok mező kiiktatásával) a felhasználói élmény javítása érdekében.

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

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- Kimeneti változás: az AutoscaleSettingResourceName mező elavult, mivel mindig a Name mezővel egyenlő.

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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- Kimeneti változás: módosult a kimenet típusa, mostantól egyetlen objektumot ad vissza, amely tartalmazza a kérés azonosítóját és az állapotkódot.

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

## <a name="breaking-changes-to-network-cmdlets"></a>A Network-parancsmagok használhatatlanná tévő változásai

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>A Resources-parancsmagok használhatatlanná tévő változásai

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- A „Password” paraméter értéke SecureString (biztonságos karakterlánc) lett

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>A ServiceBus-parancsmagok használhatatlanná tévő változásai

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- A „Get-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.    

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- A „Get-AzureRmServiceBusTopicKey” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- A „New-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- A „New-AzureRmServiceBusTopicKey” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmServiceBusKey”.

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- A „Remove-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Remove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- A „Set-AzureRmServiceBusTopicAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- A „New-AzureRmServiceBusNamespaceKey” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmServiceBusKey”.

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- A „Get-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- A „Get-AzureRmServiceBusQueueKey” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- A „New-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- A „New-AzureRmServiceBusQueueKey” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmServiceBusKey”.

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- A „Remove-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „GRemove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- A „Set-AzureRmServiceBusQueueAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- A „Get-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmServiceBusAuthorizationRule”.

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- A „Get-AzureRmServiceBusNamespaceKey” parancsmag el lett távolítva. Használja a következőt: „Get-AzureRmServiceBusKey”.

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- A „New-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „New-AzureRmServiceBusAuthorizationRule”.

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- A „Remove-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Remove-AzureRmServiceBusAuthorizationRule”.

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- A „Set-AzureRmServiceBusNamespaceAuthorizationRule” parancsmag el lett távolítva. Használja a következőt: „Set-AzureRmServiceBusAuthorizationRule”.

### <a name="type-namespaceattributes"></a>**NamespaceAttributes típus**
- Az alábbi tulajdonságok lettek eltávolítva:
    - Engedélyezve
    - status
   
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

### <a name="type-queueattribute"></a>**QueueAttribute típus**
- Az alábbi tulajdonságok lettek megjelölve elavultként:
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

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
   
### <a name="type-topicattribute"></a>**TopicAttribute típus**
- Az alábbi tulajdonságok lettek megjelölve elavultként:
    - Hely
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

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
   
### <a name="type-subscriptionattribute"></a>**SubscriptionAttribute típus**
- Az alábbi tulajdonságok lettek megjelölve elavultként:
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Hely
   
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