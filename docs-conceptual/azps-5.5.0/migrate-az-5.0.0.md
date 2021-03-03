---
title: Migrálási útmutató az Az 5.0.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 5.0.0-s verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: edfbe14ae3a42bb0b385fe9d6b5fa681a1aa2101
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684928"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="6f718-103">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="6f718-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="6f718-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 4.0.0-s és 5.0.0-s verziója között.</span><span class="sxs-lookup"><span data-stu-id="6f718-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="6f718-105">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="6f718-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="6f718-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6f718-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="6f718-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="6f718-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="6f718-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="6f718-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="6f718-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f718-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="6f718-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f718-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="6f718-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6f718-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="6f718-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="6f718-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="6f718-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="6f718-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="6f718-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f718-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="6f718-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6f718-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="6f718-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6f718-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="6f718-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6f718-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="6f718-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6f718-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="6f718-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6f718-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="6f718-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6f718-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="6f718-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6f718-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="6f718-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6f718-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="6f718-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="6f718-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="6f718-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="6f718-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="6f718-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="6f718-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="6f718-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="6f718-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="6f718-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="6f718-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="6f718-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="6f718-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="6f718-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="6f718-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="6f718-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="6f718-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="6f718-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="6f718-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="6f718-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="6f718-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="6f718-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="6f718-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="6f718-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="6f718-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="6f718-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="6f718-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="6f718-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="6f718-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="6f718-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="6f718-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="6f718-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="6f718-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="6f718-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="6f718-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="6f718-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f718-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="6f718-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6f718-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="6f718-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="6f718-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="6f718-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6f718-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="6f718-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6f718-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="6f718-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f718-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="6f718-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="6f718-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="6f718-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="6f718-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="6f718-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="6f718-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6f718-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="6f718-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6f718-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="6f718-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="6f718-169">New-AzAksCluster</span></span>

- <span data-ttu-id="6f718-170">A `NodeOsType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez, ez mindig `Linux` lesz.</span><span class="sxs-lookup"><span data-stu-id="6f718-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="6f718-171">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="6f718-172">A `NodeVmSetType` alapértelmezett értéke `AvailabilitySet` értékről `VirtualMachineScaleSets` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="6f718-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="6f718-173">A `NetworkPlugin` alapértelmezett értéke `none` értékről `azure` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="6f718-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-174">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-175">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="6f718-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="6f718-176">Set-AzAksCluster</span></span>

<span data-ttu-id="6f718-177">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-178">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-179">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="6f718-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f718-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="6f718-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f718-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="6f718-182">A(z) `StorageAccountName` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-183">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="6f718-184">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-184">After</span></span>

<span data-ttu-id="6f718-185">A `Classic` elavult, és `StorageAccountName` el lett távolítva, mert az csak a klasszikus Container Registryvel működik.</span><span class="sxs-lookup"><span data-stu-id="6f718-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="6f718-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6f718-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="6f718-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="6f718-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="6f718-188">Az `IncludeSlot` kapcsolóparaméter egy kivételével a `Get-AzFunctionApp` készlet összes paraméteréből el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6f718-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="6f718-189">A parancsmag mostantól támogatja az üzembehelyezési pontok lekérését az eredményekben, ha az `-IncludeSlot` meg van adva.</span><span class="sxs-lookup"><span data-stu-id="6f718-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="6f718-190">Ez a funkció a parancsmag előző verziójában nem működött.</span><span class="sxs-lookup"><span data-stu-id="6f718-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="6f718-191">Ez azonban ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="6f718-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="6f718-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="6f718-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="6f718-193">A `-DisableApplicationInsights` ki lett javítva a `New-AzFunctionApp` parancsmagban, hogy a beállítás megadásakor ne jöjjön létre Application Insights-projekt.</span><span class="sxs-lookup"><span data-stu-id="6f718-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="6f718-194">A PowerShell 6.2-függvényalkalmazások létrehozása mostantól nem támogatott, mivel a PowerShell 6.2 kifutó kiadás.</span><span class="sxs-lookup"><span data-stu-id="6f718-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="6f718-195">Jelenleg azt javasoljuk az ügyfeleknek, hogy ehelyett PowerShell 7.0-függvényalkalmazásokat készítsenek.</span><span class="sxs-lookup"><span data-stu-id="6f718-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="6f718-196">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows-rendszerű PowerShell-függvényalkalmazások esetén 6.2-ről 7.0-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6f718-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="6f718-197">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows- és Linux-rendszerű Node-függvényalkalmazások esetén 10-ről 12-re változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6f718-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="6f718-198">A felhasználók azonban továbbra is létrehozhatnak a Node 10-függvényalkalmazásokat a `-Runtime Node` és a `-RuntimeVersion 10` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="6f718-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="6f718-199">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Linux-rendszerű Python-függvényalkalmazások esetén 3.7-ről 3.8-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="6f718-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="6f718-200">A felhasználók azonban továbbra is létrehozhatnak a Python 3.7-függvényalkalmazásokat a `-Runtime Python` és a `-RuntimeVersion 3.7` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="6f718-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-201">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-201">Before</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a><span data-ttu-id="6f718-202">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-202">After</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a><span data-ttu-id="6f718-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f718-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="6f718-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6f718-204">New-AzKeyVault</span></span>

<span data-ttu-id="6f718-205">A(z) `DisableSoftDelete` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-206">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="6f718-207">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-207">After</span></span>

<span data-ttu-id="6f718-208">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="6f718-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="6f718-209">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="6f718-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="6f718-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6f718-210">Update-AzKeyVault</span></span>

<span data-ttu-id="6f718-211">Az `EnableSoftDelete` és `SoftDeleteRetentionInDays` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-212">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="6f718-213">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-213">After</span></span>

<span data-ttu-id="6f718-214">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="6f718-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="6f718-215">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="6f718-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="6f718-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6f718-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="6f718-217">Az `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` típus `SecretValueText` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="6f718-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="6f718-218">Alkalmazza a `-AsPlainText` parancsot az egyszerű szöveges titok beszerzésére, vagy `$secret.SecretValue` írja be a típust a `SecureString` szkriptbe.</span><span class="sxs-lookup"><span data-stu-id="6f718-218">Either apply a `-AsPlainText` to the call to get the plain text secret, or use `$secret.SecretValue` of type `SecureString` in your script.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-219">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="6f718-220">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-220">After</span></span>

```powershell
$secretInPlainText = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret -AsPlainText
```

## <a name="azmanagedservices"></a><span data-ttu-id="6f718-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6f718-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="6f718-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6f718-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="6f718-223">A(z) `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-224">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-225">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="6f718-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6f718-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="6f718-227">Az `RegistrationDefinitionName` és `RegistrationDefinitionResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-228">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-229">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="6f718-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="6f718-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="6f718-231">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-232">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-233">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="6f718-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6f718-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="6f718-235">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-236">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-237">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="6f718-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="6f718-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="6f718-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="6f718-240">A(z) `ApiVersion` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-241">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-242">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="6f718-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="6f718-244">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="6f718-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-245">Get-AzDeployment</span></span>

<span data-ttu-id="6f718-246">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="6f718-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="6f718-248">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="6f718-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="6f718-250">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="6f718-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="6f718-252">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="6f718-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="6f718-254">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="6f718-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="6f718-256">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="6f718-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-257">New-AzDeployment</span></span>

<span data-ttu-id="6f718-258">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="6f718-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="6f718-260">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="6f718-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="6f718-262">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="6f718-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-263">Remove-AzDeployment</span></span>

<span data-ttu-id="6f718-264">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="6f718-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="6f718-266">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="6f718-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="6f718-268">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="6f718-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="6f718-270">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="6f718-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="6f718-272">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="6f718-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="6f718-274">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="6f718-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-275">Stop-AzDeployment</span></span>

<span data-ttu-id="6f718-276">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="6f718-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="6f718-278">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="6f718-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="6f718-280">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="6f718-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-281">Test-AzDeployment</span></span>

<span data-ttu-id="6f718-282">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="6f718-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="6f718-284">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="6f718-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="6f718-286">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="6f718-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6f718-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="6f718-288">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="6f718-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="6f718-290">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="6f718-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="6f718-292">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="6f718-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="6f718-294">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="6f718-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6f718-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="6f718-296">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="6f718-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="6f718-298">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="6f718-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f718-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="6f718-300">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="6f718-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="6f718-302">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="6f718-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="6f718-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="6f718-304">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="6f718-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f718-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="6f718-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6f718-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="6f718-307">A(z) `IsAzureADOnlyAuthentication` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-308">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="6f718-309">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="6f718-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="6f718-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="6f718-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6f718-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="6f718-312">A `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` paraméterek a továbbiakban nem támogatottak, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-313">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="6f718-314">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="6f718-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6f718-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="6f718-316">Az `Suspend` és `Resume` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="6f718-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f718-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="6f718-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="6f718-319">A(z) `PrivateLinkResourceType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-320">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="6f718-321">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="6f718-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="6f718-323">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="6f718-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="6f718-325">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="6f718-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="6f718-327">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="6f718-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f718-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="6f718-329">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="6f718-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="6f718-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6f718-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="6f718-331">Az `FilterType` és `FilterItem` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="6f718-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="6f718-332">Előtte</span><span class="sxs-lookup"><span data-stu-id="6f718-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="6f718-333">Utána</span><span class="sxs-lookup"><span data-stu-id="6f718-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
