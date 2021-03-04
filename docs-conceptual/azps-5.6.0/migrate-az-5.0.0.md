---
title: Migrálási útmutató az Az 5.0.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 5.0.0-s verziójában található kompatibilitástörő változások listáját.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: edfbe14ae3a42bb0b385fe9d6b5fa681a1aa2101
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881985"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="35ecf-103">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="35ecf-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="35ecf-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 4.0.0-s és 5.0.0-s verziója között.</span><span class="sxs-lookup"><span data-stu-id="35ecf-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="35ecf-105">Migrálási útmutató az Az 5.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="35ecf-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="35ecf-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="35ecf-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="35ecf-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="35ecf-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="35ecf-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="35ecf-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="35ecf-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35ecf-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="35ecf-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35ecf-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="35ecf-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="35ecf-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="35ecf-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="35ecf-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="35ecf-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="35ecf-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="35ecf-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35ecf-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="35ecf-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="35ecf-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="35ecf-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="35ecf-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="35ecf-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35ecf-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="35ecf-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="35ecf-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="35ecf-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="35ecf-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="35ecf-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="35ecf-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="35ecf-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="35ecf-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="35ecf-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="35ecf-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="35ecf-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="35ecf-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="35ecf-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="35ecf-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="35ecf-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="35ecf-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="35ecf-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="35ecf-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="35ecf-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="35ecf-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="35ecf-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="35ecf-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="35ecf-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="35ecf-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="35ecf-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="35ecf-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="35ecf-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="35ecf-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="35ecf-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="35ecf-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="35ecf-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="35ecf-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="35ecf-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="35ecf-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="35ecf-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="35ecf-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="35ecf-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="35ecf-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="35ecf-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="35ecf-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="35ecf-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="35ecf-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="35ecf-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="35ecf-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="35ecf-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35ecf-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="35ecf-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="35ecf-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="35ecf-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="35ecf-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="35ecf-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="35ecf-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="35ecf-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="35ecf-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="35ecf-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35ecf-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="35ecf-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="35ecf-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="35ecf-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="35ecf-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="35ecf-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="35ecf-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="35ecf-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="35ecf-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="35ecf-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="35ecf-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="35ecf-169">New-AzAksCluster</span></span>

- <span data-ttu-id="35ecf-170">A `NodeOsType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez, ez mindig `Linux` lesz.</span><span class="sxs-lookup"><span data-stu-id="35ecf-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="35ecf-171">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="35ecf-172">A `NodeVmSetType` alapértelmezett értéke `AvailabilitySet` értékről `VirtualMachineScaleSets` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="35ecf-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="35ecf-173">A `NetworkPlugin` alapértelmezett értéke `none` értékről `azure` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="35ecf-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-174">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-175">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="35ecf-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="35ecf-176">Set-AzAksCluster</span></span>

<span data-ttu-id="35ecf-177">A `ClientIdAndSecret` alias a továbbiakban nem támogatott a `ServicePrincipalIdAndSecret` paraméter esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-178">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-179">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="35ecf-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35ecf-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="35ecf-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35ecf-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="35ecf-182">A(z) `StorageAccountName` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-183">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="35ecf-184">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-184">After</span></span>

<span data-ttu-id="35ecf-185">A `Classic` elavult, és `StorageAccountName` el lett távolítva, mert az csak a klasszikus Container Registryvel működik.</span><span class="sxs-lookup"><span data-stu-id="35ecf-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="35ecf-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="35ecf-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="35ecf-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="35ecf-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="35ecf-188">Az `IncludeSlot` kapcsolóparaméter egy kivételével a `Get-AzFunctionApp` készlet összes paraméteréből el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="35ecf-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="35ecf-189">A parancsmag mostantól támogatja az üzembehelyezési pontok lekérését az eredményekben, ha az `-IncludeSlot` meg van adva.</span><span class="sxs-lookup"><span data-stu-id="35ecf-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="35ecf-190">Ez a funkció a parancsmag előző verziójában nem működött.</span><span class="sxs-lookup"><span data-stu-id="35ecf-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="35ecf-191">Ez azonban ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="35ecf-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="35ecf-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="35ecf-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="35ecf-193">A `-DisableApplicationInsights` ki lett javítva a `New-AzFunctionApp` parancsmagban, hogy a beállítás megadásakor ne jöjjön létre Application Insights-projekt.</span><span class="sxs-lookup"><span data-stu-id="35ecf-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="35ecf-194">A PowerShell 6.2-függvényalkalmazások létrehozása mostantól nem támogatott, mivel a PowerShell 6.2 kifutó kiadás.</span><span class="sxs-lookup"><span data-stu-id="35ecf-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="35ecf-195">Jelenleg azt javasoljuk az ügyfeleknek, hogy ehelyett PowerShell 7.0-függvényalkalmazásokat készítsenek.</span><span class="sxs-lookup"><span data-stu-id="35ecf-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="35ecf-196">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows-rendszerű PowerShell-függvényalkalmazások esetén 6.2-ről 7.0-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="35ecf-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="35ecf-197">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows- és Linux-rendszerű Node-függvényalkalmazások esetén 10-ről 12-re változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="35ecf-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="35ecf-198">A felhasználók azonban továbbra is létrehozhatnak a Node 10-függvényalkalmazásokat a `-Runtime Node` és a `-RuntimeVersion 10` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="35ecf-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="35ecf-199">A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Linux-rendszerű Python-függvényalkalmazások esetén 3.7-ről 3.8-ra változott azokban az esetekben, amikor a `RuntimeVersion` paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="35ecf-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="35ecf-200">A felhasználók azonban továbbra is létrehozhatnak a Python 3.7-függvényalkalmazásokat a `-Runtime Python` és a `-RuntimeVersion 3.7` paraméter megadásával.</span><span class="sxs-lookup"><span data-stu-id="35ecf-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-201">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="35ecf-202">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="35ecf-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35ecf-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="35ecf-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="35ecf-204">New-AzKeyVault</span></span>

<span data-ttu-id="35ecf-205">A(z) `DisableSoftDelete` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-206">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="35ecf-207">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-207">After</span></span>

<span data-ttu-id="35ecf-208">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="35ecf-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="35ecf-209">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="35ecf-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="35ecf-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="35ecf-210">Update-AzKeyVault</span></span>

<span data-ttu-id="35ecf-211">Az `EnableSoftDelete` és `SoftDeleteRetentionInDays` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-212">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="35ecf-213">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-213">After</span></span>

<span data-ttu-id="35ecf-214">A helyreállítható törlési beállítás frissítésének lehetősége az Az.KeyVault 3.0.0-ban elavult.</span><span class="sxs-lookup"><span data-stu-id="35ecf-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="35ecf-215">További információk: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="35ecf-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="35ecf-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35ecf-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="35ecf-217">Az `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` típus `SecretValueText` tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="35ecf-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="35ecf-218">Alkalmazza a `-AsPlainText` parancsot az egyszerű szöveges titok beszerzésére, vagy `$secret.SecretValue` írja be a típust a `SecureString` szkriptbe.</span><span class="sxs-lookup"><span data-stu-id="35ecf-218">Either apply a `-AsPlainText` to the call to get the plain text secret, or use `$secret.SecretValue` of type `SecureString` in your script.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-219">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="35ecf-220">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-220">After</span></span>

```powershell
$secretInPlainText = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret -AsPlainText
```

## <a name="azmanagedservices"></a><span data-ttu-id="35ecf-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="35ecf-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="35ecf-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="35ecf-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="35ecf-223">A(z) `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-224">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-225">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="35ecf-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="35ecf-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="35ecf-227">Az `RegistrationDefinitionName` és `RegistrationDefinitionResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-228">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-229">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="35ecf-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="35ecf-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="35ecf-231">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-232">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-233">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="35ecf-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="35ecf-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="35ecf-235">Az `Id` és `ResourceId` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-236">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-237">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="35ecf-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="35ecf-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="35ecf-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="35ecf-240">A(z) `ApiVersion` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-241">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-242">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="35ecf-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="35ecf-244">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="35ecf-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-245">Get-AzDeployment</span></span>

<span data-ttu-id="35ecf-246">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="35ecf-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="35ecf-248">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="35ecf-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="35ecf-250">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="35ecf-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="35ecf-252">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="35ecf-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="35ecf-254">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="35ecf-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="35ecf-256">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="35ecf-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-257">New-AzDeployment</span></span>

<span data-ttu-id="35ecf-258">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="35ecf-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="35ecf-260">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="35ecf-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="35ecf-262">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="35ecf-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-263">Remove-AzDeployment</span></span>

<span data-ttu-id="35ecf-264">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="35ecf-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="35ecf-266">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="35ecf-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="35ecf-268">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="35ecf-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="35ecf-270">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="35ecf-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="35ecf-272">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="35ecf-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="35ecf-274">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="35ecf-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-275">Stop-AzDeployment</span></span>

<span data-ttu-id="35ecf-276">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="35ecf-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="35ecf-278">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="35ecf-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="35ecf-280">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="35ecf-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-281">Test-AzDeployment</span></span>

<span data-ttu-id="35ecf-282">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="35ecf-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="35ecf-284">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="35ecf-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="35ecf-286">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="35ecf-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="35ecf-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="35ecf-288">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="35ecf-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="35ecf-290">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="35ecf-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="35ecf-292">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="35ecf-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="35ecf-294">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="35ecf-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="35ecf-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="35ecf-296">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="35ecf-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="35ecf-298">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="35ecf-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="35ecf-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="35ecf-300">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="35ecf-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="35ecf-302">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="35ecf-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="35ecf-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="35ecf-304">Ugyanaz, mint a `Get-AzManagementGroupDeployment` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="35ecf-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35ecf-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="35ecf-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="35ecf-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="35ecf-307">A(z) `IsAzureADOnlyAuthentication` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-308">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="35ecf-309">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="35ecf-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="35ecf-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="35ecf-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="35ecf-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="35ecf-312">A `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` paraméterek a továbbiakban nem támogatottak, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-313">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="35ecf-314">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="35ecf-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="35ecf-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="35ecf-316">Az `Suspend` és `Resume` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="35ecf-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35ecf-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="35ecf-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="35ecf-319">A(z) `PrivateLinkResourceType` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-320">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="35ecf-321">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="35ecf-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="35ecf-323">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="35ecf-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="35ecf-325">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="35ecf-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="35ecf-327">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="35ecf-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35ecf-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="35ecf-329">Ugyanaz, mint a `Approve-AzPrivateEndpointConnection` esetében.</span><span class="sxs-lookup"><span data-stu-id="35ecf-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="35ecf-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="35ecf-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="35ecf-331">Az `FilterType` és `FilterItem` paraméter a továbbiakban nem támogatott, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="35ecf-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="35ecf-332">Előtte</span><span class="sxs-lookup"><span data-stu-id="35ecf-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="35ecf-333">Utána</span><span class="sxs-lookup"><span data-stu-id="35ecf-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
