---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106751"
---
# <a name="release-notes"></a><span data-ttu-id="efeb7-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="efeb7-103">Release notes</span></span>

<span data-ttu-id="efeb7-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="efeb7-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="efeb7-105">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="efeb7-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="efeb7-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="efeb7-106">AzureRM.Profile</span></span>
* <span data-ttu-id="efeb7-107">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="efeb7-108">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="efeb7-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="efeb7-109">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="efeb7-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="efeb7-110">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="efeb7-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="efeb7-111">Azure.Storage</span></span>
* <span data-ttu-id="efeb7-112">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="efeb7-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="efeb7-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="efeb7-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="efeb7-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="efeb7-115">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="efeb7-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="efeb7-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="efeb7-117">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="efeb7-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="efeb7-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="efeb7-119">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="efeb7-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="efeb7-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="efeb7-121">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="efeb7-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="efeb7-122">AzureRM.Automation</span></span>
* <span data-ttu-id="efeb7-123">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="efeb7-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="efeb7-124">AzureRM.Backup</span></span>
* <span data-ttu-id="efeb7-125">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="efeb7-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="efeb7-126">AzureRM.Batch</span></span>
* <span data-ttu-id="efeb7-127">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="efeb7-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="efeb7-128">AzureRM.Billing</span></span>
* <span data-ttu-id="efeb7-129">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="efeb7-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="efeb7-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="efeb7-131">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="efeb7-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="efeb7-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="efeb7-133">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="efeb7-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="efeb7-134">AzureRM.Compute</span></span>
* <span data-ttu-id="efeb7-135">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="efeb7-136">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="efeb7-137">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="efeb7-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="efeb7-138">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="efeb7-139">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="efeb7-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="efeb7-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="efeb7-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="efeb7-141">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="efeb7-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="efeb7-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="efeb7-143">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="efeb7-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="efeb7-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="efeb7-145">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="efeb7-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="efeb7-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="efeb7-147">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="efeb7-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="efeb7-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="efeb7-149">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="efeb7-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="efeb7-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="efeb7-151">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="efeb7-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="efeb7-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="efeb7-153">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="efeb7-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="efeb7-154">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="efeb7-155">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="efeb7-156">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="efeb7-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="efeb7-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="efeb7-158">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="efeb7-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="efeb7-159">AzureRM.Dns</span></span>
* <span data-ttu-id="efeb7-160">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="efeb7-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="efeb7-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="efeb7-162">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="efeb7-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="efeb7-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="efeb7-164">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="efeb7-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="efeb7-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="efeb7-166">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="efeb7-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="efeb7-167">AzureRM.Insights</span></span>
* <span data-ttu-id="efeb7-168">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="efeb7-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="efeb7-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="efeb7-170">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="efeb7-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="efeb7-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="efeb7-172">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="efeb7-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="efeb7-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="efeb7-174">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="efeb7-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="efeb7-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="efeb7-176">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="efeb7-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="efeb7-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="efeb7-178">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="efeb7-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="efeb7-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="efeb7-180">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="efeb7-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="efeb7-181">AzureRM.Media</span></span>
* <span data-ttu-id="efeb7-182">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="efeb7-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="efeb7-183">AzureRM.Network</span></span>
* <span data-ttu-id="efeb7-184">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="efeb7-185">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="efeb7-186">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="efeb7-187">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="efeb7-188">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="efeb7-189">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="efeb7-190">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="efeb7-191">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="efeb7-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="efeb7-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="efeb7-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="efeb7-193">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="efeb7-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="efeb7-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="efeb7-195">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="efeb7-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="efeb7-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="efeb7-197">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="efeb7-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="efeb7-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="efeb7-199">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="efeb7-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="efeb7-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="efeb7-201">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="efeb7-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="efeb7-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="efeb7-203">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="efeb7-204">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="efeb7-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="efeb7-205">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="efeb7-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="efeb7-206">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="efeb7-207">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="efeb7-208">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="efeb7-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="efeb7-209">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="efeb7-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="efeb7-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="efeb7-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="efeb7-211">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="efeb7-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="efeb7-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="efeb7-213">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="efeb7-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="efeb7-214">AzureRM.Relay</span></span>
* <span data-ttu-id="efeb7-215">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="efeb7-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="efeb7-216">AzureRM.Resources</span></span>
* <span data-ttu-id="efeb7-217">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="efeb7-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="efeb7-218">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="efeb7-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="efeb7-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="efeb7-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="efeb7-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="efeb7-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="efeb7-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="efeb7-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="efeb7-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="efeb7-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="efeb7-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="efeb7-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="efeb7-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="efeb7-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="efeb7-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="efeb7-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="efeb7-226">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="efeb7-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="efeb7-227">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="efeb7-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="efeb7-228">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="efeb7-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="efeb7-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="efeb7-230">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="efeb7-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="efeb7-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="efeb7-232">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="efeb7-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="efeb7-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="efeb7-234">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="efeb7-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="efeb7-235">AzureRM.Sql</span></span>
* <span data-ttu-id="efeb7-236">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="efeb7-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="efeb7-237">AzureRM.Storage</span></span>
* <span data-ttu-id="efeb7-238">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="efeb7-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="efeb7-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="efeb7-240">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="efeb7-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="efeb7-241">AzureRM.Tags</span></span>
* <span data-ttu-id="efeb7-242">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="efeb7-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="efeb7-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="efeb7-244">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="efeb7-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="efeb7-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="efeb7-246">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="efeb7-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="efeb7-247">AzureRM.Websites</span></span>
* <span data-ttu-id="efeb7-248">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="efeb7-249">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="efeb7-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="efeb7-250">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="efeb7-250">General</span></span>
* <span data-ttu-id="efeb7-251">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="efeb7-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="efeb7-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="efeb7-252">AzureRM.Profile</span></span>
* <span data-ttu-id="efeb7-253">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="efeb7-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="efeb7-254">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="efeb7-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="efeb7-255">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="efeb7-255">Azure.Storage</span></span>
* <span data-ttu-id="efeb7-256">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="efeb7-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="efeb7-257">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="efeb7-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="efeb7-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="efeb7-259">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="efeb7-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="efeb7-260">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="efeb7-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="efeb7-261">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="efeb7-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="efeb7-262">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="efeb7-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="efeb7-263">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="efeb7-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="efeb7-264">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="efeb7-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="efeb7-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="efeb7-265">AzureRM.Compute</span></span>
* <span data-ttu-id="efeb7-266">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="efeb7-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="efeb7-267">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="efeb7-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="efeb7-268">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="efeb7-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="efeb7-269">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="efeb7-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="efeb7-270">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="efeb7-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="efeb7-271">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="efeb7-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="efeb7-272">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="efeb7-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="efeb7-273">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="efeb7-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="efeb7-274">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="efeb7-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="efeb7-275">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="efeb7-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="efeb7-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="efeb7-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="efeb7-277">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="efeb7-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="efeb7-278">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="efeb7-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="efeb7-279">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="efeb7-280">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="efeb7-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="efeb7-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="efeb7-282">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="efeb7-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="efeb7-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="efeb7-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="efeb7-284">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="efeb7-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="efeb7-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="efeb7-285">AzureRM.Insights</span></span>
* <span data-ttu-id="efeb7-286">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="efeb7-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="efeb7-287">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="efeb7-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="efeb7-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="efeb7-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="efeb7-289">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="efeb7-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="efeb7-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="efeb7-290">AzureRM.Network</span></span>
* <span data-ttu-id="efeb7-291">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="efeb7-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="efeb7-292">AzureRM.Resources</span></span>
* <span data-ttu-id="efeb7-293">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="efeb7-294">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="efeb7-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="efeb7-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="efeb7-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="efeb7-296">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="efeb7-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="efeb7-297">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="efeb7-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="efeb7-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="efeb7-298">AzureRM.Sql</span></span>
* <span data-ttu-id="efeb7-299">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="efeb7-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="efeb7-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="efeb7-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="efeb7-301">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="efeb7-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="efeb7-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="efeb7-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="efeb7-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="efeb7-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="efeb7-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="efeb7-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="efeb7-305">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="efeb7-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="efeb7-306">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="efeb7-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="efeb7-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="efeb7-307">AzureRM.Storage</span></span>
* <span data-ttu-id="efeb7-308">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="efeb7-309">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="efeb7-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="efeb7-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="efeb7-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="efeb7-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="efeb7-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="efeb7-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="efeb7-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="efeb7-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="efeb7-313">AzureRM.Tags</span></span>
* <span data-ttu-id="efeb7-314">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="efeb7-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="efeb7-315">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="efeb7-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="efeb7-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="efeb7-316">AzureRM.Profile</span></span>
* <span data-ttu-id="efeb7-317">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="efeb7-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="efeb7-318">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="efeb7-318">Azure.Storage</span></span>
* <span data-ttu-id="efeb7-319">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="efeb7-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="efeb7-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="efeb7-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="efeb7-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="efeb7-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="efeb7-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="efeb7-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="efeb7-323">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="efeb7-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="efeb7-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="efeb7-324">AzureRM.Automation</span></span>
* <span data-ttu-id="efeb7-325">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="efeb7-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="efeb7-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="efeb7-326">AzureRM.Compute</span></span>
* <span data-ttu-id="efeb7-327">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="efeb7-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="efeb7-328">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="efeb7-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="efeb7-329">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="efeb7-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="efeb7-330">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="efeb7-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="efeb7-331">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="efeb7-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="efeb7-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="efeb7-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="efeb7-333">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="efeb7-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="efeb7-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="efeb7-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="efeb7-335">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="efeb7-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="efeb7-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="efeb7-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="efeb7-337">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="efeb7-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="efeb7-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="efeb7-338">AzureRM.Network</span></span>
* <span data-ttu-id="efeb7-339">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="efeb7-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="efeb7-340">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="efeb7-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="efeb7-341">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="efeb7-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="efeb7-342">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="efeb7-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="efeb7-343">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="efeb7-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="efeb7-344">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="efeb7-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="efeb7-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="efeb7-345">AzureRM.Relay</span></span>
* <span data-ttu-id="efeb7-346">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="efeb7-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="efeb7-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="efeb7-347">AzureRM.Resources</span></span>
* <span data-ttu-id="efeb7-348">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="efeb7-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="efeb7-349">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="efeb7-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="efeb7-350">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="efeb7-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="efeb7-351">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="efeb7-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="efeb7-352">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="efeb7-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="efeb7-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="efeb7-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="efeb7-354">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="efeb7-355">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="efeb7-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="efeb7-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="efeb7-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="efeb7-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="efeb7-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="efeb7-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="efeb7-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="efeb7-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="efeb7-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="efeb7-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="efeb7-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="efeb7-361">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="efeb7-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="efeb7-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="efeb7-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="efeb7-363">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="efeb7-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="efeb7-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="efeb7-364">AzureRM.Sql</span></span>
* <span data-ttu-id="efeb7-365">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="efeb7-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="efeb7-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="efeb7-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="efeb7-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="efeb7-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="efeb7-368">AzureRM.Websites</span></span>
* <span data-ttu-id="efeb7-369">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="efeb7-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="efeb7-370">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="efeb7-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="efeb7-371">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="efeb7-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="efeb7-372">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="efeb7-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="efeb7-373">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="efeb7-373">General</span></span>
* <span data-ttu-id="efeb7-374">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="efeb7-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="efeb7-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="efeb7-375">AzureRM.Profile</span></span>
* <span data-ttu-id="efeb7-376">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="efeb7-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="efeb7-377">AzureRM.Compute</span></span>
* <span data-ttu-id="efeb7-378">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="efeb7-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="efeb7-379">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="efeb7-380">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="efeb7-381">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="efeb7-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="efeb7-382">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="efeb7-383">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="efeb7-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="efeb7-384">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="efeb7-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="efeb7-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="efeb7-386">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="efeb7-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="efeb7-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="efeb7-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="efeb7-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="efeb7-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="efeb7-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="efeb7-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="efeb7-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="efeb7-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="efeb7-391">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="efeb7-392">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="efeb7-393">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="efeb7-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="efeb7-394">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="efeb7-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="efeb7-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="efeb7-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="efeb7-396">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="efeb7-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="efeb7-397">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="efeb7-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="efeb7-398">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="efeb7-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="efeb7-399">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="efeb7-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="efeb7-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="efeb7-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="efeb7-401">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="efeb7-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="efeb7-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="efeb7-402">AzureRM.Network</span></span>
* <span data-ttu-id="efeb7-403">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="efeb7-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="efeb7-404">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="efeb7-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="efeb7-405">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="efeb7-406">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="efeb7-407">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="efeb7-408">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="efeb7-409">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="efeb7-410">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="efeb7-411">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="efeb7-412">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="efeb7-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="efeb7-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="efeb7-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="efeb7-414">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="efeb7-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="efeb7-415">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="efeb7-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="efeb7-416">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="efeb7-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="efeb7-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="efeb7-417">AzureRM.Resources</span></span>
* <span data-ttu-id="efeb7-418">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="efeb7-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="efeb7-419">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="efeb7-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="efeb7-420">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="efeb7-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="efeb7-421">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="efeb7-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="efeb7-422">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="efeb7-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="efeb7-423">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="efeb7-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="efeb7-424">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="efeb7-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="efeb7-425">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="efeb7-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="efeb7-426">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="efeb7-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="efeb7-427">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="efeb7-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="efeb7-428">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="efeb7-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="efeb7-429">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="efeb7-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="efeb7-430">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="efeb7-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="efeb7-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="efeb7-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="efeb7-432">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="efeb7-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="efeb7-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="efeb7-433">AzureRM.Sql</span></span>
* <span data-ttu-id="efeb7-434">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="efeb7-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="efeb7-435">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="efeb7-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="efeb7-436">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="efeb7-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="efeb7-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="efeb7-437">AzureRM.Profile</span></span>
* <span data-ttu-id="efeb7-438">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="efeb7-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="efeb7-439">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="efeb7-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="efeb7-440">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="efeb7-440">Azure.Storage</span></span>
* <span data-ttu-id="efeb7-441">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="efeb7-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="efeb7-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="efeb7-442">AzureRM.Compute</span></span>
* <span data-ttu-id="efeb7-443">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="efeb7-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="efeb7-444">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="efeb7-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="efeb7-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="efeb7-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="efeb7-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="efeb7-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="efeb7-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="efeb7-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="efeb7-448">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="efeb7-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="efeb7-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efeb7-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="efeb7-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efeb7-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="efeb7-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efeb7-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="efeb7-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efeb7-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="efeb7-453">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="efeb7-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="efeb7-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="efeb7-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="efeb7-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="efeb7-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="efeb7-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="efeb7-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="efeb7-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="efeb7-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="efeb7-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="efeb7-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="efeb7-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="efeb7-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="efeb7-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="efeb7-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="efeb7-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="efeb7-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="efeb7-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="efeb7-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="efeb7-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="efeb7-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="efeb7-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="efeb7-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="efeb7-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="efeb7-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="efeb7-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="efeb7-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="efeb7-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="efeb7-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="efeb7-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="efeb7-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="efeb7-469">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="efeb7-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="efeb7-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="efeb7-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="efeb7-471">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="efeb7-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="efeb7-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="efeb7-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="efeb7-473">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="efeb7-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="efeb7-474">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="efeb7-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="efeb7-475">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="efeb7-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="efeb7-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="efeb7-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="efeb7-477">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="efeb7-478">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="efeb7-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="efeb7-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="efeb7-479">AzureRM.Sql</span></span>
* <span data-ttu-id="efeb7-480">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="efeb7-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="efeb7-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="efeb7-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="efeb7-482">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="efeb7-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="efeb7-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="efeb7-483">AzureRM.Websites</span></span>
* <span data-ttu-id="efeb7-484">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="efeb7-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="efeb7-485">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="efeb7-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="efeb7-486">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="efeb7-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="efeb7-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="efeb7-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="efeb7-488">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="efeb7-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="efeb7-489">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="efeb7-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="efeb7-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="efeb7-490">AzureRM.Profile</span></span>
* <span data-ttu-id="efeb7-491">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="efeb7-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="efeb7-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="efeb7-492">AzureRM.Compute</span></span>
* <span data-ttu-id="efeb7-493">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="efeb7-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="efeb7-494">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="efeb7-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="efeb7-495">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="efeb7-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="efeb7-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="efeb7-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="efeb7-497">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="efeb7-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="efeb7-498">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="efeb7-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="efeb7-499">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="efeb7-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="efeb7-500">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="efeb7-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="efeb7-501">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="efeb7-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="efeb7-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="efeb7-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="efeb7-503">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="efeb7-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="efeb7-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="efeb7-504">AzureRM.Network</span></span>
* <span data-ttu-id="efeb7-505">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="efeb7-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="efeb7-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="efeb7-506">AzureRM.Resources</span></span>
* <span data-ttu-id="efeb7-507">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="efeb7-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="efeb7-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="efeb7-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="efeb7-509">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="efeb7-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="efeb7-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="efeb7-510">AzureRM.Sql</span></span>
* <span data-ttu-id="efeb7-511">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="efeb7-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="efeb7-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="efeb7-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="efeb7-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="efeb7-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="efeb7-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="efeb7-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="efeb7-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="efeb7-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="efeb7-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="efeb7-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="efeb7-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="efeb7-517">AzureRM.Websites</span></span>
* <span data-ttu-id="efeb7-518">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="efeb7-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="efeb7-519">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="efeb7-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="efeb7-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="efeb7-520">AzureRM.Profile</span></span>
* <span data-ttu-id="efeb7-521">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="efeb7-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="efeb7-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="efeb7-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="efeb7-523">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="efeb7-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="efeb7-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="efeb7-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="efeb7-525">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="efeb7-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="efeb7-526">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="efeb7-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="efeb7-527">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="efeb7-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="efeb7-528">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="efeb7-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="efeb7-529">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="efeb7-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="efeb7-530">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="efeb7-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="efeb7-531">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="efeb7-531">Added support for MSI identity</span></span>
* <span data-ttu-id="efeb7-532">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="efeb7-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="efeb7-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="efeb7-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="efeb7-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="efeb7-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="efeb7-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="efeb7-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="efeb7-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="efeb7-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="efeb7-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="efeb7-537">AzureRM.Batch</span></span>
* <span data-ttu-id="efeb7-538">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="efeb7-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="efeb7-539">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="efeb7-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="efeb7-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="efeb7-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="efeb7-541">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="efeb7-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="efeb7-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="efeb7-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="efeb7-543">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="efeb7-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="efeb7-544">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="efeb7-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="efeb7-545">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="efeb7-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="efeb7-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="efeb7-546">AzureRM.Network</span></span>
* <span data-ttu-id="efeb7-547">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="efeb7-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="efeb7-548">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="efeb7-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="efeb7-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="efeb7-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="efeb7-550">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="efeb7-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="efeb7-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="efeb7-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="efeb7-552">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="efeb7-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="efeb7-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="efeb7-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="efeb7-554">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="efeb7-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="efeb7-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="efeb7-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="efeb7-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="efeb7-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="efeb7-557">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="efeb7-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="efeb7-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="efeb7-558">AzureRM.Sql</span></span>
* <span data-ttu-id="efeb7-559">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="efeb7-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="efeb7-560">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="efeb7-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="efeb7-561">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="efeb7-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="efeb7-562">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="efeb7-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="efeb7-563">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="efeb7-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="efeb7-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="efeb7-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="efeb7-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="efeb7-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="efeb7-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="efeb7-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="efeb7-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="efeb7-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="efeb7-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="efeb7-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="efeb7-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="efeb7-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="efeb7-570">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="efeb7-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
