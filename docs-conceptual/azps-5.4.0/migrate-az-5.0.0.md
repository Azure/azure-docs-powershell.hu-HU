---
title: Migrálási útmutató az Az 5.0.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 5.0.0-s verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573666"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="191d1-103">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="191d1-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="191d1-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 4.0.0-s és 5.0.0-s verziója között.</span><span class="sxs-lookup"><span data-stu-id="191d1-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="191d1-105">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="191d1-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="191d1-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="191d1-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="191d1-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="191d1-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="191d1-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="191d1-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="191d1-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="191d1-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="191d1-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="191d1-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="191d1-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="191d1-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="191d1-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="191d1-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="191d1-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="191d1-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="191d1-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="191d1-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="191d1-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="191d1-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="191d1-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="191d1-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="191d1-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="191d1-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="191d1-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="191d1-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="191d1-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="191d1-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="191d1-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="191d1-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="191d1-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="191d1-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="191d1-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="191d1-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="191d1-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="191d1-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="191d1-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="191d1-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="191d1-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="191d1-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="191d1-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="191d1-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="191d1-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="191d1-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="191d1-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="191d1-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="191d1-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="191d1-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="191d1-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="191d1-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="191d1-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="191d1-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="191d1-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="191d1-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="191d1-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="191d1-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="191d1-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="191d1-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="191d1-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="191d1-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="191d1-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="191d1-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="191d1-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="191d1-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="191d1-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="191d1-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="191d1-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="191d1-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="191d1-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="191d1-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="191d1-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="191d1-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="191d1-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="191d1-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="191d1-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="191d1-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="191d1-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="191d1-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="191d1-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="191d1-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="191d1-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="191d1-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="191d1-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="191d1-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="191d1-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="191d1-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="191d1-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="191d1-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="191d1-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="191d1-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="191d1-169">New-AzAksCluster</span></span>

- <span data-ttu-id="191d1-170">A `NodeOsType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez, ez mindig `Linux` lesz.</span><span class="sxs-lookup"><span data-stu-id="191d1-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="191d1-171">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="191d1-172">A `NodeVmSetType` alapértelmezett értéke `AvailabilitySet` értékről `VirtualMachineScaleSets` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="191d1-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="191d1-173">A `NetworkPlugin` alapértelmezett értéke `none` értékről `azure` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="191d1-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-174">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-175">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="191d1-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="191d1-176">Set-AzAksCluster</span></span>

<span data-ttu-id="191d1-177">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-178">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-179">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="191d1-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="191d1-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="191d1-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="191d1-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="191d1-182">A(z) `StorageAccountName` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-183">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="191d1-184">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-184">After</span></span>

<span data-ttu-id="191d1-185">A `Classic` elavult, és `StorageAccountName` el lett távolítva, mert az csak a klasszikus Container Registryvel működik.</span><span class="sxs-lookup"><span data-stu-id="191d1-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="191d1-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="191d1-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="191d1-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="191d1-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="191d1-188">Az `IncludeSlot` kapcsolóparaméter egy kivételével a `Get-AzFunctionApp` készlet összes paraméteréből el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="191d1-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="191d1-189">A parancsmag mostantól támogatja az üzembehelyezési pontok lekérését az eredményekben, ha az `-IncludeSlot` meg van adva.</span><span class="sxs-lookup"><span data-stu-id="191d1-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="191d1-190">Ez a funkció a parancsmag előző verziójában nem működött.</span><span class="sxs-lookup"><span data-stu-id="191d1-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="191d1-191">Ez azonban ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="191d1-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="191d1-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="191d1-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="191d1-193">A `-DisableApplicationInsights` ki lett javítva a `New-AzFunctionApp` parancsmagban, hogy a beállítás megadásakor ne jöjjön létre Application Insights-projekt.</span><span class="sxs-lookup"><span data-stu-id="191d1-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="191d1-194">A PowerShell 6.2-függvényalkalmazások létrehozása mostantól nem támogatott, mivel a PowerShell 6.2 kifutó kiadás.</span><span class="sxs-lookup"><span data-stu-id="191d1-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="191d1-195">Jelenleg azt javasoljuk az ügyfeleknek, hogy ehelyett PowerShell 7.0-függvényalkalmazásokat készítsenek.</span><span class="sxs-lookup"><span data-stu-id="191d1-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="191d1-196">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows-rendszerű PowerShell-függvényalkalmazások esetén 6.2-ről 7.0-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="191d1-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="191d1-197">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows- és Linux-rendszerű Node-függvényalkalmazások esetén 10-ről 12-re változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="191d1-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="191d1-198">A felhasználók azonban továbbra is létrehozhatnak a Node 10-függvényalkalmazásokat a `-Runtime Node` és a `-RuntimeVersion 10` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="191d1-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="191d1-199">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Linux-rendszerű Python-függvényalkalmazások esetén 3.7-ről 3.8-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="191d1-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="191d1-200">A felhasználók azonban továbbra is létrehozhatnak a Python 3.7-függvényalkalmazásokat a `-Runtime Python` és a `-RuntimeVersion 3.7` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="191d1-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-201">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="191d1-202">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="191d1-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="191d1-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="191d1-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="191d1-204">New-AzKeyVault</span></span>

<span data-ttu-id="191d1-205">A(z) `DisableSoftDelete` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-206">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="191d1-207">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-207">After</span></span>

<span data-ttu-id="191d1-208">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="191d1-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="191d1-209">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="191d1-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="191d1-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="191d1-210">Update-AzKeyVault</span></span>

<span data-ttu-id="191d1-211">Az `EnableSoftDelete` és `SoftDeleteRetentionInDays` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-212">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="191d1-213">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-213">After</span></span>

<span data-ttu-id="191d1-214">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="191d1-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="191d1-215">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="191d1-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="191d1-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="191d1-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="191d1-217">Az `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` típus `SecretValueText` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="191d1-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="191d1-218">A `SecretValueText` tulajdonság lecserélve a `SecretValue` tulajdonságra.</span><span class="sxs-lookup"><span data-stu-id="191d1-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-219">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="191d1-220">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="191d1-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="191d1-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="191d1-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="191d1-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="191d1-223">A(z) `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-224">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-225">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="191d1-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="191d1-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="191d1-227">Az `RegistrationDefinitionName` és `RegistrationDefinitionResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-228">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-229">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="191d1-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="191d1-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="191d1-231">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-232">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-233">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="191d1-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="191d1-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="191d1-235">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-236">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-237">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="191d1-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="191d1-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="191d1-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="191d1-240">A(z) `ApiVersion` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-241">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-242">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="191d1-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="191d1-244">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="191d1-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-245">Get-AzDeployment</span></span>

<span data-ttu-id="191d1-246">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="191d1-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="191d1-248">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="191d1-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="191d1-250">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="191d1-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="191d1-252">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="191d1-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="191d1-254">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="191d1-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="191d1-256">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="191d1-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-257">New-AzDeployment</span></span>

<span data-ttu-id="191d1-258">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="191d1-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="191d1-260">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="191d1-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="191d1-262">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="191d1-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-263">Remove-AzDeployment</span></span>

<span data-ttu-id="191d1-264">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="191d1-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="191d1-266">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="191d1-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="191d1-268">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="191d1-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="191d1-270">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="191d1-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="191d1-272">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="191d1-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="191d1-274">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="191d1-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-275">Stop-AzDeployment</span></span>

<span data-ttu-id="191d1-276">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="191d1-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="191d1-278">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="191d1-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="191d1-280">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="191d1-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-281">Test-AzDeployment</span></span>

<span data-ttu-id="191d1-282">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="191d1-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="191d1-284">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="191d1-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="191d1-286">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="191d1-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="191d1-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="191d1-288">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="191d1-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="191d1-290">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="191d1-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="191d1-292">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="191d1-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="191d1-294">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="191d1-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="191d1-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="191d1-296">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="191d1-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="191d1-298">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="191d1-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="191d1-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="191d1-300">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="191d1-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="191d1-302">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="191d1-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="191d1-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="191d1-304">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="191d1-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="191d1-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="191d1-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="191d1-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="191d1-307">A(z) `IsAzureADOnlyAuthentication` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-308">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="191d1-309">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="191d1-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="191d1-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="191d1-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="191d1-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="191d1-312">A `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` paraméterek a továbbiakban nem támogatottak, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-313">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="191d1-314">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="191d1-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="191d1-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="191d1-316">Az `Suspend` és `Resume` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="191d1-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="191d1-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="191d1-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="191d1-319">A(z) `PrivateLinkResourceType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-320">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="191d1-321">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="191d1-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="191d1-323">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="191d1-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="191d1-325">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="191d1-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="191d1-327">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="191d1-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="191d1-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="191d1-329">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="191d1-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="191d1-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="191d1-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="191d1-331">Az `FilterType` és `FilterItem` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="191d1-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="191d1-332">Előtte</span><span class="sxs-lookup"><span data-stu-id="191d1-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="191d1-333">Utána</span><span class="sxs-lookup"><span data-stu-id="191d1-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
