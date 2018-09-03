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
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117699"
---
# <a name="release-notes"></a><span data-ttu-id="ba860-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="ba860-103">Release notes</span></span>

<span data-ttu-id="ba860-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="ba860-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="ba860-105">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="ba860-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ba860-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="ba860-106">General</span></span>
* <span data-ttu-id="ba860-107">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="ba860-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ba860-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-108">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-109">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="ba860-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ba860-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ba860-110">AzureRM.Compute</span></span>
* <span data-ttu-id="ba860-111">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="ba860-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ba860-112">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="ba860-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ba860-113">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="ba860-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ba860-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba860-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="ba860-115">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="ba860-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ba860-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ba860-116">AzureRM.Network</span></span>
* <span data-ttu-id="ba860-117">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="ba860-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ba860-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ba860-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ba860-119">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="ba860-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ba860-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ba860-120">AzureRM.Resources</span></span>
* <span data-ttu-id="ba860-121">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="ba860-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ba860-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba860-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ba860-123">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="ba860-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ba860-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ba860-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ba860-125">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="ba860-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ba860-126">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="ba860-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ba860-127">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="ba860-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ba860-128">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="ba860-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ba860-129">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="ba860-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ba860-130">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="ba860-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ba860-131">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="ba860-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ba860-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ba860-132">AzureRM.Websites</span></span>
* <span data-ttu-id="ba860-133">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="ba860-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ba860-134">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="ba860-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ba860-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-135">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-136">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ba860-137">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="ba860-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ba860-138">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="ba860-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ba860-139">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ba860-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ba860-140">Azure.Storage</span></span>
* <span data-ttu-id="ba860-141">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ba860-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ba860-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ba860-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba860-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ba860-144">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ba860-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba860-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ba860-146">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ba860-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba860-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ba860-148">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ba860-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ba860-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ba860-150">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ba860-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ba860-151">AzureRM.Automation</span></span>
* <span data-ttu-id="ba860-152">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ba860-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ba860-153">AzureRM.Backup</span></span>
* <span data-ttu-id="ba860-154">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ba860-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ba860-155">AzureRM.Batch</span></span>
* <span data-ttu-id="ba860-156">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ba860-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ba860-157">AzureRM.Billing</span></span>
* <span data-ttu-id="ba860-158">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ba860-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ba860-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="ba860-160">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ba860-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ba860-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ba860-162">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ba860-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ba860-163">AzureRM.Compute</span></span>
* <span data-ttu-id="ba860-164">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ba860-165">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="ba860-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ba860-166">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="ba860-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ba860-167">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ba860-168">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="ba860-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ba860-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ba860-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="ba860-170">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ba860-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ba860-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ba860-172">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ba860-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ba860-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ba860-174">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ba860-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ba860-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ba860-176">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ba860-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ba860-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ba860-178">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ba860-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ba860-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ba860-180">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ba860-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba860-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ba860-182">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="ba860-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ba860-183">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ba860-184">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ba860-185">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ba860-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ba860-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ba860-187">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ba860-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ba860-188">AzureRM.Dns</span></span>
* <span data-ttu-id="ba860-189">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ba860-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ba860-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ba860-191">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ba860-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba860-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="ba860-193">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ba860-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ba860-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ba860-195">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ba860-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ba860-196">AzureRM.Insights</span></span>
* <span data-ttu-id="ba860-197">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ba860-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ba860-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="ba860-199">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ba860-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba860-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ba860-201">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ba860-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ba860-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ba860-203">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ba860-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ba860-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ba860-205">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ba860-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ba860-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ba860-207">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ba860-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ba860-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ba860-209">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ba860-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ba860-210">AzureRM.Media</span></span>
* <span data-ttu-id="ba860-211">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ba860-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ba860-212">AzureRM.Network</span></span>
* <span data-ttu-id="ba860-213">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ba860-214">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ba860-215">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ba860-216">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ba860-217">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ba860-218">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ba860-219">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ba860-220">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="ba860-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ba860-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ba860-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ba860-222">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ba860-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba860-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ba860-224">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ba860-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ba860-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ba860-226">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ba860-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ba860-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ba860-228">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ba860-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ba860-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ba860-230">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ba860-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ba860-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ba860-232">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ba860-233">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="ba860-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ba860-234">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="ba860-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ba860-235">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ba860-236">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ba860-237">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="ba860-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ba860-238">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="ba860-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ba860-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ba860-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ba860-240">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ba860-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ba860-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ba860-242">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ba860-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ba860-243">AzureRM.Relay</span></span>
* <span data-ttu-id="ba860-244">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ba860-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ba860-245">AzureRM.Resources</span></span>
* <span data-ttu-id="ba860-246">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="ba860-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ba860-247">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="ba860-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ba860-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ba860-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ba860-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ba860-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ba860-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ba860-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ba860-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ba860-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ba860-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ba860-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ba860-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ba860-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ba860-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ba860-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ba860-255">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="ba860-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ba860-256">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="ba860-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ba860-257">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ba860-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ba860-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ba860-259">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ba860-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba860-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ba860-261">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ba860-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba860-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ba860-263">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ba860-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ba860-264">AzureRM.Sql</span></span>
* <span data-ttu-id="ba860-265">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ba860-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ba860-266">AzureRM.Storage</span></span>
* <span data-ttu-id="ba860-267">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ba860-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ba860-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ba860-269">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ba860-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ba860-270">AzureRM.Tags</span></span>
* <span data-ttu-id="ba860-271">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ba860-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ba860-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ba860-273">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ba860-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ba860-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ba860-275">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ba860-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ba860-276">AzureRM.Websites</span></span>
* <span data-ttu-id="ba860-277">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="ba860-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ba860-278">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="ba860-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ba860-279">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="ba860-279">General</span></span>
* <span data-ttu-id="ba860-280">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="ba860-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ba860-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-281">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-282">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="ba860-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ba860-283">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="ba860-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ba860-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ba860-284">Azure.Storage</span></span>
* <span data-ttu-id="ba860-285">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="ba860-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ba860-286">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ba860-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba860-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ba860-288">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="ba860-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ba860-289">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="ba860-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ba860-290">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="ba860-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ba860-291">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="ba860-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ba860-292">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="ba860-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ba860-293">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="ba860-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ba860-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ba860-294">AzureRM.Compute</span></span>
* <span data-ttu-id="ba860-295">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="ba860-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ba860-296">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="ba860-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ba860-297">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="ba860-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ba860-298">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="ba860-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ba860-299">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="ba860-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ba860-300">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="ba860-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ba860-301">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="ba860-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ba860-302">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="ba860-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ba860-303">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="ba860-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ba860-304">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="ba860-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ba860-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ba860-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ba860-306">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="ba860-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ba860-307">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="ba860-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ba860-308">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ba860-309">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ba860-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba860-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ba860-311">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="ba860-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ba860-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba860-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="ba860-313">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="ba860-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ba860-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ba860-314">AzureRM.Insights</span></span>
* <span data-ttu-id="ba860-315">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="ba860-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ba860-316">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="ba860-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ba860-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba860-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ba860-318">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="ba860-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ba860-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ba860-319">AzureRM.Network</span></span>
* <span data-ttu-id="ba860-320">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ba860-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ba860-321">AzureRM.Resources</span></span>
* <span data-ttu-id="ba860-322">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="ba860-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ba860-323">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="ba860-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ba860-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba860-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ba860-325">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="ba860-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ba860-326">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="ba860-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ba860-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ba860-327">AzureRM.Sql</span></span>
* <span data-ttu-id="ba860-328">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="ba860-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ba860-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba860-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ba860-330">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="ba860-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ba860-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="ba860-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ba860-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="ba860-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ba860-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="ba860-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ba860-334">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="ba860-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ba860-335">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="ba860-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ba860-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ba860-336">AzureRM.Storage</span></span>
* <span data-ttu-id="ba860-337">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="ba860-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ba860-338">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="ba860-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ba860-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba860-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ba860-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba860-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ba860-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba860-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ba860-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ba860-342">AzureRM.Tags</span></span>
* <span data-ttu-id="ba860-343">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="ba860-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ba860-344">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="ba860-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ba860-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-345">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-346">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="ba860-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ba860-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ba860-347">Azure.Storage</span></span>
* <span data-ttu-id="ba860-348">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="ba860-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ba860-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ba860-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ba860-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ba860-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ba860-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba860-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ba860-352">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="ba860-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ba860-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ba860-353">AzureRM.Automation</span></span>
* <span data-ttu-id="ba860-354">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="ba860-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ba860-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ba860-355">AzureRM.Compute</span></span>
* <span data-ttu-id="ba860-356">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ba860-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ba860-357">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="ba860-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ba860-358">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="ba860-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ba860-359">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="ba860-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ba860-360">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="ba860-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ba860-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba860-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="ba860-362">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="ba860-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ba860-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba860-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ba860-364">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="ba860-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ba860-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ba860-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ba860-366">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba860-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ba860-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ba860-367">AzureRM.Network</span></span>
* <span data-ttu-id="ba860-368">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ba860-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ba860-369">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="ba860-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ba860-370">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="ba860-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ba860-371">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="ba860-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ba860-372">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="ba860-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ba860-373">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ba860-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ba860-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ba860-374">AzureRM.Relay</span></span>
* <span data-ttu-id="ba860-375">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="ba860-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ba860-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ba860-376">AzureRM.Resources</span></span>
* <span data-ttu-id="ba860-377">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="ba860-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ba860-378">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="ba860-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ba860-379">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="ba860-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ba860-380">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="ba860-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ba860-381">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="ba860-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ba860-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba860-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ba860-383">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="ba860-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ba860-384">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="ba860-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ba860-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ba860-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ba860-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ba860-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ba860-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ba860-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ba860-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ba860-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ba860-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ba860-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ba860-390">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="ba860-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ba860-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba860-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ba860-392">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="ba860-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ba860-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ba860-393">AzureRM.Sql</span></span>
* <span data-ttu-id="ba860-394">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="ba860-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ba860-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ba860-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ba860-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ba860-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ba860-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ba860-397">AzureRM.Websites</span></span>
* <span data-ttu-id="ba860-398">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="ba860-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ba860-399">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="ba860-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ba860-400">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="ba860-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ba860-401">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="ba860-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ba860-402">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="ba860-402">General</span></span>
* <span data-ttu-id="ba860-403">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="ba860-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ba860-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-404">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-405">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="ba860-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ba860-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ba860-406">AzureRM.Compute</span></span>
* <span data-ttu-id="ba860-407">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="ba860-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ba860-408">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ba860-409">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="ba860-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ba860-410">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="ba860-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ba860-411">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="ba860-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ba860-412">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="ba860-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ba860-413">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="ba860-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ba860-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ba860-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ba860-415">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="ba860-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ba860-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ba860-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ba860-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ba860-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ba860-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ba860-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ba860-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba860-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ba860-420">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="ba860-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ba860-421">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="ba860-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ba860-422">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="ba860-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ba860-423">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="ba860-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ba860-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ba860-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="ba860-425">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="ba860-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ba860-426">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="ba860-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ba860-427">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="ba860-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ba860-428">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="ba860-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ba860-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba860-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ba860-430">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="ba860-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ba860-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ba860-431">AzureRM.Network</span></span>
* <span data-ttu-id="ba860-432">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="ba860-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ba860-433">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="ba860-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ba860-434">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ba860-435">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ba860-436">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ba860-437">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ba860-438">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ba860-439">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ba860-440">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ba860-441">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="ba860-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ba860-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ba860-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ba860-443">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="ba860-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ba860-444">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ba860-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ba860-445">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="ba860-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ba860-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ba860-446">AzureRM.Resources</span></span>
* <span data-ttu-id="ba860-447">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="ba860-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ba860-448">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="ba860-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ba860-449">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="ba860-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ba860-450">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="ba860-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ba860-451">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ba860-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ba860-452">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="ba860-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ba860-453">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="ba860-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ba860-454">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ba860-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ba860-455">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="ba860-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ba860-456">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="ba860-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ba860-457">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="ba860-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ba860-458">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="ba860-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ba860-459">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="ba860-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ba860-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ba860-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ba860-461">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="ba860-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ba860-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ba860-462">AzureRM.Sql</span></span>
* <span data-ttu-id="ba860-463">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="ba860-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ba860-464">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="ba860-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ba860-465">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="ba860-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ba860-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-466">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-467">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="ba860-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ba860-468">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="ba860-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ba860-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ba860-469">Azure.Storage</span></span>
* <span data-ttu-id="ba860-470">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="ba860-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ba860-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ba860-471">AzureRM.Compute</span></span>
* <span data-ttu-id="ba860-472">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="ba860-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ba860-473">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="ba860-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ba860-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ba860-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ba860-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ba860-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ba860-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ba860-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ba860-477">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="ba860-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ba860-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba860-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ba860-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba860-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ba860-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba860-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ba860-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba860-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ba860-482">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba860-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ba860-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ba860-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ba860-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ba860-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ba860-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ba860-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ba860-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ba860-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ba860-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ba860-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ba860-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ba860-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ba860-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ba860-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ba860-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ba860-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ba860-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ba860-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ba860-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ba860-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ba860-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ba860-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ba860-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ba860-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ba860-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ba860-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ba860-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ba860-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ba860-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ba860-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ba860-498">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="ba860-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ba860-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba860-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ba860-500">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="ba860-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ba860-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ba860-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ba860-502">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="ba860-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ba860-503">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="ba860-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ba860-504">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="ba860-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ba860-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ba860-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ba860-506">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ba860-507">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ba860-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ba860-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ba860-508">AzureRM.Sql</span></span>
* <span data-ttu-id="ba860-509">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="ba860-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ba860-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ba860-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ba860-511">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="ba860-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ba860-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ba860-512">AzureRM.Websites</span></span>
* <span data-ttu-id="ba860-513">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="ba860-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ba860-514">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="ba860-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ba860-515">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="ba860-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ba860-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ba860-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ba860-517">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="ba860-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ba860-518">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="ba860-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ba860-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-519">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-520">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="ba860-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ba860-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ba860-521">AzureRM.Compute</span></span>
* <span data-ttu-id="ba860-522">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="ba860-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ba860-523">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="ba860-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ba860-524">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="ba860-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ba860-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ba860-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ba860-526">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="ba860-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ba860-527">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="ba860-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ba860-528">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="ba860-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ba860-529">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="ba860-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ba860-530">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="ba860-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ba860-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ba860-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ba860-532">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="ba860-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ba860-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ba860-533">AzureRM.Network</span></span>
* <span data-ttu-id="ba860-534">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="ba860-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ba860-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ba860-535">AzureRM.Resources</span></span>
* <span data-ttu-id="ba860-536">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="ba860-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ba860-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ba860-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ba860-538">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="ba860-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ba860-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ba860-539">AzureRM.Sql</span></span>
* <span data-ttu-id="ba860-540">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="ba860-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ba860-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba860-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ba860-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ba860-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ba860-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ba860-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ba860-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ba860-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ba860-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba860-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ba860-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ba860-546">AzureRM.Websites</span></span>
* <span data-ttu-id="ba860-547">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="ba860-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ba860-548">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="ba860-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ba860-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ba860-549">AzureRM.Profile</span></span>
* <span data-ttu-id="ba860-550">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="ba860-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ba860-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ba860-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ba860-552">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="ba860-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ba860-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba860-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ba860-554">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="ba860-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ba860-555">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="ba860-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ba860-556">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="ba860-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ba860-557">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="ba860-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ba860-558">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="ba860-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ba860-559">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="ba860-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ba860-560">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="ba860-560">Added support for MSI identity</span></span>
* <span data-ttu-id="ba860-561">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="ba860-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ba860-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ba860-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ba860-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba860-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ba860-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ba860-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ba860-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ba860-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ba860-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ba860-566">AzureRM.Batch</span></span>
* <span data-ttu-id="ba860-567">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="ba860-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ba860-568">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="ba860-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ba860-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ba860-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="ba860-570">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="ba860-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ba860-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba860-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ba860-572">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="ba860-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ba860-573">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="ba860-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ba860-574">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="ba860-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ba860-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ba860-575">AzureRM.Network</span></span>
* <span data-ttu-id="ba860-576">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="ba860-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ba860-577">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="ba860-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ba860-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba860-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ba860-579">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="ba860-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ba860-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba860-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ba860-581">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="ba860-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ba860-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba860-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ba860-583">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="ba860-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ba860-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba860-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ba860-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ba860-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ba860-586">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="ba860-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ba860-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ba860-587">AzureRM.Sql</span></span>
* <span data-ttu-id="ba860-588">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="ba860-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ba860-589">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="ba860-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ba860-590">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="ba860-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ba860-591">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="ba860-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ba860-592">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="ba860-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ba860-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba860-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ba860-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ba860-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ba860-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ba860-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ba860-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ba860-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ba860-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba860-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ba860-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ba860-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ba860-599">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="ba860-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
