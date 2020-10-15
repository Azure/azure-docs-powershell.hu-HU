---
title: Migrálási útmutató az Az 4.1.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 4.1.0-s verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c64541beb5eb0d3db38932fb3915de865919641b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001907"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="7e061-103">Migrálási útmutató az Az 4.1.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="7e061-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="7e061-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 3.0.0-s és 4.1.0-s verziója között.</span><span class="sxs-lookup"><span data-stu-id="7e061-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="7e061-105">Migrálási útmutató az Az 4.1.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="7e061-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="7e061-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e061-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="7e061-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e061-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="7e061-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="7e061-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="7e061-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="7e061-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="7e061-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="7e061-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="7e061-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e061-111">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="7e061-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e061-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="7e061-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e061-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="7e061-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e061-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="7e061-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e061-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="7e061-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e061-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="7e061-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e061-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="7e061-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="7e061-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="7e061-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="7e061-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="7e061-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="7e061-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="7e061-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="7e061-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="7e061-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="7e061-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="7e061-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e061-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="7e061-124">A `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` típus `Type` tulajdonságának típusa `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` helyett a következő lett: `System.String`.</span><span class="sxs-lookup"><span data-stu-id="7e061-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="7e061-125">A(z) `New-AzApiManagement` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-126">A(z) `New-AzApiManagement` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="7e061-127">A(z) `Set-AzApiManagement` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-128">A(z) `Set-AzApiManagement` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="7e061-129">A `Get-AzApiManagementProperty` parancsmagot a `Get-AzApiManagementNamedValue` parancsmag helyettesíti.</span><span class="sxs-lookup"><span data-stu-id="7e061-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="7e061-130">A `New-AzApiManagementProperty` parancsmagot a `New-AzApiManagementNamedValue` parancsmag helyettesíti.</span><span class="sxs-lookup"><span data-stu-id="7e061-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="7e061-131">A `Remove-AzApiManagementProperty` parancsmagot a `Remove-AzApiManagementNamedValue` parancsmag helyettesíti.</span><span class="sxs-lookup"><span data-stu-id="7e061-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="7e061-132">A `Set-AzApiManagementProperty` parancsmagot a `Set-AzApiManagementNamedValue` parancsmag helyettesíti.</span><span class="sxs-lookup"><span data-stu-id="7e061-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="7e061-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7e061-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="7e061-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="7e061-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="7e061-135">Az `Microsoft.Azure.Commands.Batch.Models.PSApplication` típus `ApplicationPackages` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="7e061-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="7e061-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="7e061-137">Az `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` típus `PublicIPs` tulajdonsága el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="7e061-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="7e061-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="7e061-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="7e061-139">A `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` típus `StorageUrlExpiry` tulajdonságának típusa `System.DateTime` helyett a következő lett: `System.DateTime?`.</span><span class="sxs-lookup"><span data-stu-id="7e061-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="7e061-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7e061-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="7e061-141">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="7e061-142">A(z) `Get-AzVMImage` parancsmag a továbbiakban nem támogatja a(z) `FilterExpression` paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-143">A(z) `Get-AzVMImage` parancsmaghoz tartozó `ListVMImage` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="7e061-144">A(z) `New-AzVMConfig` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-145">A(z) `New-AzVMConfig` parancsmaghoz tartozó `AssignIdentityParameterSet` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="7e061-146">A(z) `Update-AzVM` parancsmag a továbbiakban nem támogatja a(z) `AssignIdentity` paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-147">A(z) `Update-AzVM` parancsmaghoz tartozó `AssignIdentityParameterSet` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="7e061-148">A(z) `VirtualMachines`, `VirtualMachineScaleSets` és `AvailabilitySets` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="7e061-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="7e061-149">Az `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` típus `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` és `AvailabilitySetsColocationStatus` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-150">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-150">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="7e061-151">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-151">After</span></span>

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

- <span data-ttu-id="7e061-152">A(z) `VirtualMachines`, `VirtualMachineScaleSets` és `AvailabilitySets` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="7e061-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="7e061-153">Az `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` típus `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` és `AvailabilitySetsColocationStatus` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-154">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-154">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="7e061-155">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-155">After</span></span>

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

- <span data-ttu-id="7e061-156">A(z) `VirtualMachines`, `VirtualMachineScaleSets` és `AvailabilitySets` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="7e061-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="7e061-157">Az `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` típus `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` és `AvailabilitySetsColocationStatus` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-158">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-158">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="7e061-159">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-159">After</span></span>

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

<span data-ttu-id="7e061-160">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="7e061-161">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="7e061-162">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="7e061-163">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="7e061-164">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="7e061-165">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="7e061-166">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="7e061-167">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="7e061-168">A(z) `AutomaticRepairMaxInstanceRepairsPercent` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-169">A(z) `AssignIdentity` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-170">A(z) `__AllParameterSets` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="7e061-171">A(z) `ExplicitIdentityParameterSet` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="7e061-172">A(z) `AssignIdentityParameterSet` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="7e061-173">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="7e061-174">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="7e061-175">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="7e061-176">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="7e061-177">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="7e061-178">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="7e061-179">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="7e061-180">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="7e061-181">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="7e061-182">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="7e061-183">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="7e061-184">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="7e061-185">A(z) `AutomaticRepairMaxInstanceRepairsPercent` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-186">A(z) `__AllParameterSets` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="7e061-187">A(z) `ExplicitIdentityParameterSet` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="7e061-188">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="7e061-189">A `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` típus `AutomaticRepairsPolicy` tulajdonságának típusa `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` helyett a következő lett: `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="7e061-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e061-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="7e061-191">A(z) `New-AzKeyVaultCertificateOrganizationDetails` alias el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="7e061-192">Használja a következőt: `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="7e061-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-193">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="7e061-194">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="7e061-195">A(z) `New-AzKeyVaultCertificateAdministratorDetails` alias el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="7e061-196">Használja a következőt: `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="7e061-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-197">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="7e061-198">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="7e061-199">A(z) `-EnableSoftDelete` el lett távolítva, mert a helyreállítható törlés alapértelmezés szerint engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="7e061-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="7e061-200">Ha nem szeretné alkalmazni ezt a viselkedést, használja a következőt: `-DisableSoftDelete`.</span><span class="sxs-lookup"><span data-stu-id="7e061-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-201">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="7e061-202">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="7e061-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7e061-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="7e061-204">A `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` típus `RetentionPolicy` tulajdonságának típusa `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` helyett a következő lett: `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="7e061-205">A `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` típus `RetentionPolicy` tulajdonságának típusa `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` helyett a következő lett: `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="7e061-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="7e061-206">A(z) `New-AzMetricAlertRuleV2Criteria` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="7e061-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7e061-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="7e061-208">A(z) `RoundTripTimeMs` tulajdonság általános típusa `System.Nullable1[System.Int32]` helyett a következő lett: `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="7e061-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="7e061-209">A(z) `SuccessThresholdRoundTripTimeMs` paraméter általános típusa `System.Nullable1[System.Int32]` helyett a következő lett: `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="7e061-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="7e061-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e061-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="7e061-211">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="7e061-212">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="7e061-213">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="7e061-214">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="7e061-215">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="7e061-216">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="7e061-217">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="7e061-218">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="7e061-219">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="7e061-220">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="7e061-221">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="7e061-222">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="7e061-223">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="7e061-224">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="7e061-225">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="7e061-226">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="7e061-227">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="7e061-228">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` típus `Metadata` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="7e061-229">Az SDK már nem támogatta a `Get-AzOperationalInsightsSavedSearchResult` parancsmagot, ezért el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="7e061-230">Az SDK már nem támogatta a `Get-AzOperationalInsightsSearchResult` parancsmagot, ezért el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="7e061-231">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="7e061-232">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="7e061-233">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="7e061-234">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="7e061-235">Az SDK már nem támogatta a `Get-AzOperationalInsightsLinkTarget` parancsmagot, ezért el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="7e061-236">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="7e061-237">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="7e061-238">A(z) `New-AzOperationalInsightsWorkspace` parancsmag a továbbiakban nem támogatja a(z) `CustomerId` paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="7e061-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="7e061-239">A(z) `New-AzOperationalInsightsWorkspace` parancsmaghoz tartozó `__AllParameterSets` paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="7e061-240">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="7e061-241">Az `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` típus `PortalUrl` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="7e061-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7e061-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="7e061-243">A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="7e061-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="7e061-244">A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="7e061-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="7e061-245">A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="7e061-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="7e061-246">A(z) `TenantLevel` paraméter el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="7e061-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="7e061-247">A(z) `Aliases` tulajdonság általános típusa `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` helyett a következő lett: `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span><span class="sxs-lookup"><span data-stu-id="7e061-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="7e061-248">A(z) `New-AzPolicyAssignment` parancsmag a továbbiakban nem támogatja a(z) `System.Management.Automation.PSObject` típust a(z) `PolicyDefinition` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="7e061-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="7e061-249">A(z) `New-AzPolicyAssignment` parancsmag a továbbiakban nem támogatja a(z) `System.Management.Automation.PSObject` típust a(z) `PolicySetDefinition` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="7e061-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="7e061-250">A `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` típus `Status` tulajdonságának típusa `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` helyett a következő lett: `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="7e061-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="7e061-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7e061-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="7e061-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="7e061-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="7e061-253">A NetWorkRule DefaultAction értéke megváltozott erről: Engedélyezés = 1, Letiltás = 0, erre: Engedélyezés = 0, Letiltás = 1.</span><span class="sxs-lookup"><span data-stu-id="7e061-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="7e061-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="7e061-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="7e061-255">A következő 2 tulajdonság el lett távolítva az AzureStorageTable.CloudTable.ServiceClient kimeneti objektumból: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="7e061-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="7e061-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="7e061-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="7e061-257">A kimenet típusa CloudFile helyett mostantól AzureStorageFile, az eredeti kimenet az új kimenet CloudFile gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="7e061-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-258">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="7e061-259">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="7e061-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="7e061-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="7e061-261">A kimenet típusa CloudFileDirectory helyett mostantól AzureStorageFileDirectory, az eredeti kimenet az új kimenet CloudFileDirectory gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="7e061-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-262">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="7e061-263">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="7e061-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="7e061-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="7e061-265">A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet CloudFileShare gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="7e061-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-266">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="7e061-267">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="7e061-268">A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet CloudFileShare.Properties gyermek-altulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="7e061-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-269">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="7e061-270">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-270">After</span></span>

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

<span data-ttu-id="7e061-271">Az alfájlkönyvtárak szülő-címtárobjektum és a -Path használatával történő eltávolításakor a -Path tulajdonság már nem adható meg egy megegyező típussal (sztringgel) rendelkező folyamatból.</span><span class="sxs-lookup"><span data-stu-id="7e061-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="7e061-272">Előtte</span><span class="sxs-lookup"><span data-stu-id="7e061-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="7e061-273">Utána</span><span class="sxs-lookup"><span data-stu-id="7e061-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
