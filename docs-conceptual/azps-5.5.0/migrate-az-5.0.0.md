---
title: Migrálási útmutató az Az 5.0.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 5.0.0-s verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012699"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="f0724-103">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="f0724-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="f0724-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 4.0.0-s és 5.0.0-s verziója között.</span><span class="sxs-lookup"><span data-stu-id="f0724-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="f0724-105">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="f0724-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="f0724-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f0724-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="f0724-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="f0724-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="f0724-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="f0724-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="f0724-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0724-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="f0724-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0724-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="f0724-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f0724-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="f0724-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="f0724-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="f0724-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="f0724-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="f0724-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f0724-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="f0724-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0724-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="f0724-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0724-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="f0724-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f0724-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="f0724-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f0724-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="f0724-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f0724-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="f0724-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f0724-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="f0724-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f0724-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="f0724-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f0724-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="f0724-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="f0724-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="f0724-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="f0724-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="f0724-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="f0724-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="f0724-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="f0724-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="f0724-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="f0724-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="f0724-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="f0724-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="f0724-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="f0724-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="f0724-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="f0724-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="f0724-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="f0724-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="f0724-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="f0724-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="f0724-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="f0724-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="f0724-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="f0724-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="f0724-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="f0724-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="f0724-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="f0724-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="f0724-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="f0724-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="f0724-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="f0724-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="f0724-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="f0724-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="f0724-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f0724-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="f0724-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f0724-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="f0724-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="f0724-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="f0724-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f0724-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="f0724-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f0724-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="f0724-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f0724-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="f0724-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="f0724-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="f0724-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="f0724-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="f0724-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="f0724-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f0724-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="f0724-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f0724-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="f0724-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="f0724-169">New-AzAksCluster</span></span>

- <span data-ttu-id="f0724-170">A `NodeOsType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez, ez mindig `Linux` lesz.</span><span class="sxs-lookup"><span data-stu-id="f0724-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="f0724-171">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="f0724-172">A `NodeVmSetType` alapértelmezett értéke `AvailabilitySet` értékről `VirtualMachineScaleSets` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f0724-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="f0724-173">A `NetworkPlugin` alapértelmezett értéke `none` értékről `azure` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f0724-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-174">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-175">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="f0724-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="f0724-176">Set-AzAksCluster</span></span>

<span data-ttu-id="f0724-177">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-178">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-179">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="f0724-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0724-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="f0724-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f0724-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="f0724-182">A(z) `StorageAccountName` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-183">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="f0724-184">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-184">After</span></span>

<span data-ttu-id="f0724-185">A `Classic` elavult, és `StorageAccountName` el lett távolítva, mert az csak a klasszikus Container Registryvel működik.</span><span class="sxs-lookup"><span data-stu-id="f0724-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="f0724-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f0724-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="f0724-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="f0724-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="f0724-188">Az `IncludeSlot` kapcsolóparaméter egy kivételével a `Get-AzFunctionApp` készlet összes paraméteréből el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f0724-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="f0724-189">A parancsmag mostantól támogatja az üzembehelyezési pontok lekérését az eredményekben, ha az `-IncludeSlot` meg van adva.</span><span class="sxs-lookup"><span data-stu-id="f0724-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="f0724-190">Ez a funkció a parancsmag előző verziójában nem működött.</span><span class="sxs-lookup"><span data-stu-id="f0724-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="f0724-191">Ez azonban ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="f0724-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="f0724-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="f0724-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="f0724-193">A `-DisableApplicationInsights` ki lett javítva a `New-AzFunctionApp` parancsmagban, hogy a beállítás megadásakor ne jöjjön létre Application Insights-projekt.</span><span class="sxs-lookup"><span data-stu-id="f0724-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="f0724-194">A PowerShell 6.2-függvényalkalmazások létrehozása mostantól nem támogatott, mivel a PowerShell 6.2 kifutó kiadás.</span><span class="sxs-lookup"><span data-stu-id="f0724-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="f0724-195">Jelenleg azt javasoljuk az ügyfeleknek, hogy ehelyett PowerShell 7.0-függvényalkalmazásokat készítsenek.</span><span class="sxs-lookup"><span data-stu-id="f0724-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="f0724-196">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows-rendszerű PowerShell-függvényalkalmazások esetén 6.2-ről 7.0-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f0724-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="f0724-197">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows- és Linux-rendszerű Node-függvényalkalmazások esetén 10-ről 12-re változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f0724-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="f0724-198">A felhasználók azonban továbbra is létrehozhatnak a Node 10-függvényalkalmazásokat a `-Runtime Node` és a `-RuntimeVersion 10` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="f0724-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="f0724-199">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Linux-rendszerű Python-függvényalkalmazások esetén 3.7-ről 3.8-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f0724-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="f0724-200">A felhasználók azonban továbbra is létrehozhatnak a Python 3.7-függvényalkalmazásokat a `-Runtime Python` és a `-RuntimeVersion 3.7` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="f0724-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-201">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="f0724-202">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="f0724-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f0724-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="f0724-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0724-204">New-AzKeyVault</span></span>

<span data-ttu-id="f0724-205">A(z) `DisableSoftDelete` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-206">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="f0724-207">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-207">After</span></span>

<span data-ttu-id="f0724-208">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="f0724-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="f0724-209">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="f0724-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="f0724-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0724-210">Update-AzKeyVault</span></span>

<span data-ttu-id="f0724-211">Az `EnableSoftDelete` és `SoftDeleteRetentionInDays` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-212">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="f0724-213">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-213">After</span></span>

<span data-ttu-id="f0724-214">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="f0724-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="f0724-215">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="f0724-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="f0724-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f0724-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="f0724-217">Az `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` típus `SecretValueText` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f0724-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="f0724-218">A `SecretValueText` tulajdonság lecserélve a `SecretValue` tulajdonságra.</span><span class="sxs-lookup"><span data-stu-id="f0724-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-219">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="f0724-220">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="f0724-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f0724-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="f0724-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f0724-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="f0724-223">A(z) `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-224">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-225">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="f0724-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f0724-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="f0724-227">Az `RegistrationDefinitionName` és `RegistrationDefinitionResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-228">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-229">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="f0724-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f0724-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="f0724-231">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-232">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-233">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="f0724-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f0724-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="f0724-235">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-236">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-237">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="f0724-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="f0724-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="f0724-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="f0724-240">A(z) `ApiVersion` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-241">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-242">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="f0724-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="f0724-244">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="f0724-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-245">Get-AzDeployment</span></span>

<span data-ttu-id="f0724-246">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="f0724-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="f0724-248">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="f0724-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="f0724-250">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="f0724-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="f0724-252">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="f0724-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="f0724-254">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="f0724-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="f0724-256">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="f0724-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-257">New-AzDeployment</span></span>

<span data-ttu-id="f0724-258">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="f0724-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="f0724-260">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="f0724-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="f0724-262">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="f0724-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-263">Remove-AzDeployment</span></span>

<span data-ttu-id="f0724-264">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="f0724-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="f0724-266">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="f0724-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="f0724-268">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="f0724-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="f0724-270">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="f0724-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="f0724-272">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="f0724-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="f0724-274">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="f0724-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-275">Stop-AzDeployment</span></span>

<span data-ttu-id="f0724-276">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="f0724-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="f0724-278">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="f0724-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="f0724-280">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="f0724-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-281">Test-AzDeployment</span></span>

<span data-ttu-id="f0724-282">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="f0724-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="f0724-284">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="f0724-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="f0724-286">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="f0724-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f0724-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="f0724-288">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="f0724-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="f0724-290">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="f0724-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="f0724-292">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="f0724-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="f0724-294">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="f0724-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f0724-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="f0724-296">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="f0724-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="f0724-298">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="f0724-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0724-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="f0724-300">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="f0724-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="f0724-302">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="f0724-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f0724-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="f0724-304">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="f0724-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f0724-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="f0724-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f0724-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="f0724-307">A(z) `IsAzureADOnlyAuthentication` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-308">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="f0724-309">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="f0724-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="f0724-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="f0724-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f0724-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="f0724-312">A `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` paraméterek a továbbiakban nem támogatottak, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-313">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="f0724-314">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="f0724-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f0724-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="f0724-316">Az `Suspend` és `Resume` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="f0724-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f0724-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="f0724-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="f0724-319">A(z) `PrivateLinkResourceType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-320">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="f0724-321">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="f0724-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="f0724-323">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="f0724-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="f0724-325">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="f0724-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="f0724-327">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="f0724-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f0724-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="f0724-329">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="f0724-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="f0724-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f0724-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="f0724-331">Az `FilterType` és `FilterItem` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f0724-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="f0724-332">Előtte</span><span class="sxs-lookup"><span data-stu-id="f0724-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="f0724-333">Utána</span><span class="sxs-lookup"><span data-stu-id="f0724-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
