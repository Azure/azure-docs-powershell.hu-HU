---
title: Migrálási útmutató az Az 4.1.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 4.1.0-s verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5f42bbb65313d1caa839443d463b61cc743ca0a5
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242664"
---
# <a name="migration-guide-for-az-410"></a>Migrálási útmutató az Az 4.1.0-s verziójához

Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 3.0.0-s és 4.1.0-s verziója között.

- [Migrálási útmutató az Az 4.1.0-s verziójához](#migration-guide-for-az-410)
  - [Az.ApiManagement](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [Az.Batch](#azbatch)
    - [`Get-AzBatchApplication`, `New-AzBatchApplication`](#get-azbatchapplication-new-azbatchapplication)
    - [`Get-AzBatchComputeNode`, `New-AzBatchPool`](#get-azbatchcomputenode-new-azbatchpool)
    - [`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [Az.Compute](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [Az.KeyVault](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [Az.Monitor](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [Az.Network](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [Az.OperationalInsights](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [Az.Resources](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [Az.Storage](#azstorage)
    - [`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [`New-AzStorageTable`, `Get-AzStorageTable`](#new-azstoragetable-get-azstoragetable)
    - [`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a>Az.ApiManagement

### `Add-AzApiManagementRegion`

A `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` típus `Type` tulajdonságának típusa `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` helyett a következő lett: `System.String`.

### `New-AzApiManagement`

- A(z) `New-AzApiManagement` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.
- A(z) `New-AzApiManagement` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.

### `Set-AzApiManagement`

- A(z) `Set-AzApiManagement` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.
- A(z) `Set-AzApiManagement` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.

### `Get-AzApiManagementProperty`

A `Get-AzApiManagementProperty` parancsmagot a `Get-AzureApiManagementNamedValue` parancsmag helyettesíti.

### `New-AzApiManagementProperty`

A `New-AzApiManagementProperty` parancsmagot a `New-AzureApiManagementNamedValue` parancsmag helyettesíti.

### `Remove-AzApiManagementProperty`

A `Remove-AzApiManagementProperty` parancsmagot a `Remove-AzureApiManagementNamedValue` parancsmag helyettesíti.

### `Set-AzApiManagementProperty`

A `Set-AzApiManagementProperty` parancsmagot a `Set-AzureApiManagementNamedValue` parancsmag helyettesíti.

## <a name="azbatch"></a>Az.Batch

### <a name="get-azbatchapplication-new-azbatchapplication"></a>`Get-AzBatchApplication`, `New-AzBatchApplication`

Az `Microsoft.Azure.Commands.Batch.Models.PSApplication` típus `ApplicationPackages` tulajdonsága el lett távolítva.

### <a name="get-azbatchcomputenode-new-azbatchpool"></a>`Get-AzBatchComputeNode`, `New-AzBatchPool`

Az `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` típus `PublicIPs` tulajdonsága el lett távolítva

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a>`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`

A `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` típus `StorageUrlExpiry` tulajdonságának típusa `System.DateTime` helyett a következő lett: `System.DateTime?`.

## <a name="azcompute"></a>Az.Compute

### `Remove-AzVmssDiagnosticsExtension`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVMImage`

- A(z) `Get-AzVMImage` parancsmag a továbbiakban nem támogatja a(z) `FilterExpression` paramétert, és nem található alias az eredeti paraméternévhez.
- A(z) `Get-AzVMImage` parancsmaghoz tartozó `ListVMImage` paraméterkészlet el lett távolítva.

### `New-AzVMConfig`

- A(z) `New-AzVMConfig` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.
- A(z) `New-AzVMConfig` parancsmaghoz tartozó `AssignIdentityParameterSet` paraméterkészlet el lett távolítva.

### `Update-AzVM`

- A(z) `Update-AzVM` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.
- A(z) `Update-AzVM` parancsmaghoz tartozó `AssignIdentityParameterSet` paraméterkészlet el lett távolítva.

### `New-AzProximityPlacementGroup`

- A(z) `VirtualMachines`, `VirtualMachineScaleSets` és `AvailabilitySets` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- Az `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` típus `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` és `AvailabilitySetsColocationStatus` tulajdonsága el lett távolítva.

#### <a name="before"></a>Előtte

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>Utána

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- A(z) `VirtualMachines`, `VirtualMachineScaleSets` és `AvailabilitySets` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- Az `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` típus `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` és `AvailabilitySetsColocationStatus` tulajdonsága el lett távolítva.

#### <a name="before"></a>Előtte

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>Utána

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- A(z) `VirtualMachines`, `VirtualMachineScaleSets` és `AvailabilitySets` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- Az `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` típus `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` és `AvailabilitySetsColocationStatus` tulajdonsága el lett távolítva.

#### <a name="before"></a>Előtte

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>Utána

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssDataDisk`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssExtension`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssNetworkInterfaceConfiguration`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSecret`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSshPublicKey`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssWinRMListener`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmssConfig`

- A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- A(z) `AutomaticRepairMaxInstanceRepairsPercent` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.
- A(z) `AssignIdentity` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.
- A(z) `__AllParameterSets` paraméterkészlet el lett távolítva.
- A(z) `ExplicitIdentityParameterSet` paraméterkészlet el lett távolítva.
- A(z) `AssignIdentityParameterSet` paraméterkészlet el lett távolítva.

### `Remove-AzVmssDataDisk`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssExtension`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssNetworkInterfaceConfiguration`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssBootDiagnostic`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOsProfile`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssRollingUpgradePolicy`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssStorageProfile`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmss`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Repair-AzVmssServiceFabricUpdateDomain`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVmss`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOrchestrationServiceState`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Update-AzVmss`

- A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- A(z) `AutomaticRepairMaxInstanceRepairsPercent` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.
- A(z) `__AllParameterSets` paraméterkészlet el lett távolítva.
- A(z) `ExplicitIdentityParameterSet` paraméterkészlet el lett távolítva.

### `Add-AzVmssDiagnosticsExtension`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Disable-AzVmssDiskEncryption`

A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

## <a name="azkeyvault"></a>Az.KeyVault

### `New-AzKeyVaultCertificateOrganizationDetail`

A(z) `New-AzKeyVaultCertificateOrganizationDetails` alias el lett távolítva. Használja a következőt: `New-AzKeyVaultCertificateOrganizationDetail`.

#### <a name="before"></a>Előtte

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a>Utána

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

A(z) `New-AzKeyVaultCertificateAdministratorDetails` alias el lett távolítva. Használja a következőt: `New-AzKeyVaultCertificateAdministratorDetail`.

#### <a name="before"></a>Előtte

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a>Utána

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

A(z) `-EnableSoftDelete` el lett távolítva, mert a helyreállítható törlés alapértelmezés szerint engedélyezve van. Ha nem szeretné alkalmazni ezt a viselkedést, használja a következőt: `-DisableSoftDelete`.

#### <a name="before"></a>Előtte

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a>Utána

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a>Az.Monitor

### `Add-AzLogProfile`

A `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` típus `RetentionPolicy` tulajdonságának típusa `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` helyett a következő lett: `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `Get-AzLogProfile`

A `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` típus `RetentionPolicy` tulajdonságának típusa `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` helyett a következő lett: `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `New-AzMetricAlertRuleV2Criteria`

A(z) `New-AzMetricAlertRuleV2Criteria` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.

## <a name="aznetwork"></a>Az.Network

### `Get-AzNetworkWatcherConnectionMonitor`

A(z) `RoundTripTimeMs` tulajdonság általános típusa `System.Nullable1[System.Int32]` helyett a következő lett: `System.Nullable1[System.Double]`.

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

A(z) `SuccessThresholdRoundTripTimeMs` paraméter általános típusa `System.Nullable1[System.Int32]` helyett a következő lett: `System.Nullable1[System.Double]`.

## <a name="azoperationalinsights"></a>Az.OperationalInsights

### `Get-AzOperationalInsightsDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsApplicationInsightsDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsAzureActivityLogDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsCustomLogDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsLinuxSyslogDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsWindowsEventDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Remove-AzOperationalInsightsDataSource`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Disable-AzOperationalInsightsIISLogCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Enable-AzOperationalInsightsIISLogCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Get-AzOperationalInsightsSavedSearch`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` típus `Metadata` tulajdonsága el lett távolítva.

### `Get-AzOperationalInsightsSavedSearchResult`

Az SDK már nem támogatta a `Get-AzOperationalInsightsSavedSearchResult` parancsmagot, ezért el lett távolítva.

### `Get-AzOperationalInsightsSearchResult`

Az SDK már nem támogatta a `Get-AzOperationalInsightsSearchResult` parancsmagot, ezért el lett távolítva.

### `Get-AzOperationalInsightsStorageInsight`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsStorageInsight`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Remove-AzOperationalInsightsStorageInsight`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Set-AzOperationalInsightsStorageInsight`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Get-AzOperationalInsightsLinkTarget`

Az SDK már nem támogatta a `Get-AzOperationalInsightsLinkTarget` parancsmagot, ezért el lett távolítva.

### `Get-AzOperationalInsightsWorkspace`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `New-AzOperationalInsightsWorkspace`

- Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.
- A(z) `New-AzOperationalInsightsWorkspace` parancsmag a továbbiakban nem támogatja a(z) `CustomerId` paramétert, és nem található alias az eredeti paraméternévhez.
- A(z) `New-AzOperationalInsightsWorkspace` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.

### `Set-AzOperationalInsightsWorkspace`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

### `Invoke-AzOperationalInsightsQuery`

Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.

## <a name="azresources"></a>Az.Resources

### `Get-AzDeploymentScript`

A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzDeploymentScriptLog`

A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Save-AzDeploymentScriptLog`

A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

A(z) `TenantLevel` paraméter el lett távolítva.

### `Get-AzPolicyAlias`

A(z) `Aliases` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.

### `New-AzPolicyAssignment`

- A(z) `New-AzPolicyAssignment` parancsmag a továbbiakban nem támogatja a(z) `System.Management.Automation.PSObject` típust a(z) `PolicyDefinition` paraméter esetében.
- A(z) `New-AzPolicyAssignment` parancsmag a továbbiakban nem támogatja a(z) `System.Management.Automation.PSObject` típust a(z) `PolicySetDefinition` paraméter esetében.

### `Remove-AzDeploymentScript`

A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

## <a name="azstorage"></a>Az.Storage

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a>`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`

A NetWorkRule DefaultAction értéke megváltozott erről: Engedélyezés = 1, Letiltás = 0, erre: Engedélyezés = 0, Letiltás = 1.

### <a name="new-azstoragetable-get-azstoragetable"></a>`New-AzStorageTable`, `Get-AzStorageTable`

A következő 2 tulajdonság el lett távolítva az AzureStorageTable.CloudTable.ServiceClient kimeneti objektumból: ConnectionPolicy, ConsistencyLevel.

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a>`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`

A kimenet típusa CloudFile helyett mostantól AzureStorageFile, az eredeti kimenet az új kimenet CloudFile gyermektulajdonsága lesz

#### <a name="before"></a>Előtte

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a>Utána

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a>`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`

A kimenet típusa CloudFileDirectory helyett mostantól AzureStorageFileDirectory, az eredeti kimenet az új kimenet CloudFileDirectory gyermektulajdonsága lesz

#### <a name="before"></a>Előtte

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Utána

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a>`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`

A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet CloudFileShare gyermektulajdonsága lesz

#### <a name="before"></a>Előtte

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a>Utána

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet CloudFileShare.Properties gyermek-altulajdonsága lesz

#### <a name="before"></a>Előtte

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a>Utána

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

Az alfájlkönyvtárak szülő-címtárobjektum és a -Path használatával történő eltávolításakor a -Path tulajdonság már nem adható meg egy megegyező típussal (sztringgel) rendelkező folyamatból.

#### <a name="before"></a>Előtte

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>Utána

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
