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
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250426"
---
# <a name="release-notes"></a><span data-ttu-id="a7bb5-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="a7bb5-103">Release notes</span></span>

<span data-ttu-id="a7bb5-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="a7bb5-105">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a7bb5-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7bb5-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7bb5-106">General</span></span>
* <span data-ttu-id="a7bb5-107">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-108">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-109">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7bb5-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-110">AzureRM.Compute</span></span>
* <span data-ttu-id="a7bb5-111">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="a7bb5-112">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="a7bb5-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="a7bb5-113">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="a7bb5-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a7bb5-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a7bb5-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="a7bb5-115">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="a7bb5-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7bb5-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7bb5-116">AzureRM.Network</span></span>
* <span data-ttu-id="a7bb5-117">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="a7bb5-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a7bb5-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a7bb5-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a7bb5-119">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="a7bb5-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7bb5-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7bb5-120">AzureRM.Resources</span></span>
* <span data-ttu-id="a7bb5-121">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7bb5-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7bb5-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7bb5-123">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7bb5-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7bb5-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7bb5-125">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="a7bb5-126">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="a7bb5-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="a7bb5-127">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="a7bb5-128">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a7bb5-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="a7bb5-129">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="a7bb5-130">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="a7bb5-131">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="a7bb5-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7bb5-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7bb5-132">AzureRM.Websites</span></span>
* <span data-ttu-id="a7bb5-133">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="a7bb5-134">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="a7bb5-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-135">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-136">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7bb5-137">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="a7bb5-138">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="a7bb5-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="a7bb5-139">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="a7bb5-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7bb5-140">Azure.Storage</span></span>
* <span data-ttu-id="a7bb5-141">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="a7bb5-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="a7bb5-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a7bb5-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7bb5-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a7bb5-144">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="a7bb5-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7bb5-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="a7bb5-146">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a7bb5-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7bb5-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a7bb5-148">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="a7bb5-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a7bb5-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="a7bb5-150">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a7bb5-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a7bb5-151">AzureRM.Automation</span></span>
* <span data-ttu-id="a7bb5-152">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="a7bb5-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="a7bb5-153">AzureRM.Backup</span></span>
* <span data-ttu-id="a7bb5-154">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a7bb5-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a7bb5-155">AzureRM.Batch</span></span>
* <span data-ttu-id="a7bb5-156">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="a7bb5-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="a7bb5-157">AzureRM.Billing</span></span>
* <span data-ttu-id="a7bb5-158">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="a7bb5-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="a7bb5-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="a7bb5-160">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="a7bb5-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a7bb5-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="a7bb5-162">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7bb5-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-163">AzureRM.Compute</span></span>
* <span data-ttu-id="a7bb5-164">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7bb5-165">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="a7bb5-166">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="a7bb5-167">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a7bb5-168">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="a7bb5-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a7bb5-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a7bb5-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="a7bb5-170">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="a7bb5-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a7bb5-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="a7bb5-172">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="a7bb5-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a7bb5-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="a7bb5-174">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="a7bb5-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="a7bb5-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="a7bb5-176">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a7bb5-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7bb5-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a7bb5-178">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a7bb5-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a7bb5-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a7bb5-180">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7bb5-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7bb5-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7bb5-182">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="a7bb5-183">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a7bb5-184">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7bb5-185">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="a7bb5-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="a7bb5-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="a7bb5-187">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="a7bb5-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a7bb5-188">AzureRM.Dns</span></span>
* <span data-ttu-id="a7bb5-189">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a7bb5-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a7bb5-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a7bb5-191">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7bb5-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7bb5-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7bb5-193">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="a7bb5-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a7bb5-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="a7bb5-195">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a7bb5-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a7bb5-196">AzureRM.Insights</span></span>
* <span data-ttu-id="a7bb5-197">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="a7bb5-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="a7bb5-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="a7bb5-199">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7bb5-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7bb5-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7bb5-201">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a7bb5-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a7bb5-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a7bb5-203">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="a7bb5-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a7bb5-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="a7bb5-205">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="a7bb5-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="a7bb5-207">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="a7bb5-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a7bb5-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="a7bb5-209">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="a7bb5-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="a7bb5-210">AzureRM.Media</span></span>
* <span data-ttu-id="a7bb5-211">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7bb5-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7bb5-212">AzureRM.Network</span></span>
* <span data-ttu-id="a7bb5-213">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="a7bb5-214">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a7bb5-215">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="a7bb5-216">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a7bb5-217">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="a7bb5-218">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="a7bb5-219">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="a7bb5-220">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="a7bb5-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="a7bb5-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a7bb5-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="a7bb5-222">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="a7bb5-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a7bb5-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a7bb5-224">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a7bb5-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a7bb5-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a7bb5-226">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="a7bb5-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a7bb5-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="a7bb5-228">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="a7bb5-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7bb5-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="a7bb5-230">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a7bb5-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7bb5-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7bb5-232">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="a7bb5-233">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="a7bb5-234">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="a7bb5-235">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="a7bb5-236">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="a7bb5-237">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="a7bb5-238">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a7bb5-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a7bb5-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a7bb5-240">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="a7bb5-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bb5-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="a7bb5-242">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a7bb5-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a7bb5-243">AzureRM.Relay</span></span>
* <span data-ttu-id="a7bb5-244">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7bb5-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7bb5-245">AzureRM.Resources</span></span>
* <span data-ttu-id="a7bb5-246">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="a7bb5-247">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="a7bb5-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7bb5-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7bb5-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7bb5-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7bb5-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7bb5-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7bb5-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7bb5-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7bb5-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a7bb5-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="a7bb5-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a7bb5-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="a7bb5-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a7bb5-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="a7bb5-255">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="a7bb5-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="a7bb5-256">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="a7bb5-257">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a7bb5-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a7bb5-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a7bb5-259">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7bb5-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7bb5-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7bb5-261">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a7bb5-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7bb5-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a7bb5-263">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7bb5-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7bb5-264">AzureRM.Sql</span></span>
* <span data-ttu-id="a7bb5-265">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a7bb5-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a7bb5-266">AzureRM.Storage</span></span>
* <span data-ttu-id="a7bb5-267">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="a7bb5-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="a7bb5-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="a7bb5-269">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a7bb5-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a7bb5-270">AzureRM.Tags</span></span>
* <span data-ttu-id="a7bb5-271">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7bb5-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7bb5-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7bb5-273">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="a7bb5-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="a7bb5-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="a7bb5-275">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7bb5-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7bb5-276">AzureRM.Websites</span></span>
* <span data-ttu-id="a7bb5-277">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="a7bb5-278">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a7bb5-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7bb5-279">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7bb5-279">General</span></span>
* <span data-ttu-id="a7bb5-280">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-281">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-282">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="a7bb5-283">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="a7bb5-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a7bb5-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7bb5-284">Azure.Storage</span></span>
* <span data-ttu-id="a7bb5-285">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="a7bb5-286">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a7bb5-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7bb5-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a7bb5-288">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="a7bb5-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a7bb5-289">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="a7bb5-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a7bb5-290">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="a7bb5-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a7bb5-291">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="a7bb5-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a7bb5-292">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="a7bb5-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a7bb5-293">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="a7bb5-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7bb5-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-294">AzureRM.Compute</span></span>
* <span data-ttu-id="a7bb5-295">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a7bb5-296">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="a7bb5-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a7bb5-297">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a7bb5-298">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="a7bb5-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a7bb5-299">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a7bb5-300">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a7bb5-301">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="a7bb5-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a7bb5-302">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="a7bb5-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a7bb5-303">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a7bb5-304">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a7bb5-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7bb5-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a7bb5-306">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a7bb5-307">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a7bb5-308">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a7bb5-309">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7bb5-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7bb5-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7bb5-311">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="a7bb5-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7bb5-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7bb5-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7bb5-313">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a7bb5-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a7bb5-314">AzureRM.Insights</span></span>
* <span data-ttu-id="a7bb5-315">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a7bb5-316">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="a7bb5-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7bb5-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7bb5-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7bb5-318">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="a7bb5-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7bb5-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7bb5-319">AzureRM.Network</span></span>
* <span data-ttu-id="a7bb5-320">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7bb5-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7bb5-321">AzureRM.Resources</span></span>
* <span data-ttu-id="a7bb5-322">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a7bb5-323">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="a7bb5-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7bb5-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7bb5-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7bb5-325">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a7bb5-326">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="a7bb5-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a7bb5-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7bb5-327">AzureRM.Sql</span></span>
* <span data-ttu-id="a7bb5-328">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a7bb5-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7bb5-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a7bb5-330">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a7bb5-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="a7bb5-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a7bb5-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="a7bb5-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a7bb5-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="a7bb5-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a7bb5-334">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="a7bb5-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a7bb5-335">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="a7bb5-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a7bb5-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a7bb5-336">AzureRM.Storage</span></span>
* <span data-ttu-id="a7bb5-337">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a7bb5-338">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="a7bb5-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a7bb5-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7bb5-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a7bb5-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7bb5-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a7bb5-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7bb5-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a7bb5-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a7bb5-342">AzureRM.Tags</span></span>
* <span data-ttu-id="a7bb5-343">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="a7bb5-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a7bb5-344">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a7bb5-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-345">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-346">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a7bb5-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a7bb5-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7bb5-347">Azure.Storage</span></span>
* <span data-ttu-id="a7bb5-348">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="a7bb5-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="a7bb5-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a7bb5-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="a7bb5-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a7bb5-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a7bb5-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7bb5-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a7bb5-352">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a7bb5-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a7bb5-353">AzureRM.Automation</span></span>
* <span data-ttu-id="a7bb5-354">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7bb5-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-355">AzureRM.Compute</span></span>
* <span data-ttu-id="a7bb5-356">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a7bb5-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a7bb5-357">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a7bb5-358">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a7bb5-359">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="a7bb5-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a7bb5-360">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7bb5-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7bb5-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7bb5-362">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="a7bb5-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7bb5-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7bb5-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7bb5-364">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="a7bb5-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a7bb5-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a7bb5-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a7bb5-366">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a7bb5-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7bb5-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7bb5-367">AzureRM.Network</span></span>
* <span data-ttu-id="a7bb5-368">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a7bb5-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a7bb5-369">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a7bb5-370">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="a7bb5-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a7bb5-371">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="a7bb5-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a7bb5-372">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="a7bb5-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a7bb5-373">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a7bb5-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a7bb5-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a7bb5-374">AzureRM.Relay</span></span>
* <span data-ttu-id="a7bb5-375">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7bb5-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7bb5-376">AzureRM.Resources</span></span>
* <span data-ttu-id="a7bb5-377">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a7bb5-378">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a7bb5-379">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a7bb5-380">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a7bb5-381">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="a7bb5-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a7bb5-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7bb5-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7bb5-383">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a7bb5-384">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a7bb5-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7bb5-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7bb5-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7bb5-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7bb5-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7bb5-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7bb5-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7bb5-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a7bb5-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a7bb5-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a7bb5-390">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="a7bb5-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a7bb5-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7bb5-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a7bb5-392">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="a7bb5-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7bb5-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7bb5-393">AzureRM.Sql</span></span>
* <span data-ttu-id="a7bb5-394">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a7bb5-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a7bb5-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a7bb5-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a7bb5-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7bb5-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7bb5-397">AzureRM.Websites</span></span>
* <span data-ttu-id="a7bb5-398">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a7bb5-399">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="a7bb5-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a7bb5-400">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="a7bb5-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a7bb5-401">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="a7bb5-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7bb5-402">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="a7bb5-402">General</span></span>
* <span data-ttu-id="a7bb5-403">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-404">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-405">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7bb5-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-406">AzureRM.Compute</span></span>
* <span data-ttu-id="a7bb5-407">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="a7bb5-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a7bb5-408">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a7bb5-409">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a7bb5-410">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="a7bb5-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a7bb5-411">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a7bb5-412">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="a7bb5-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a7bb5-413">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a7bb5-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a7bb5-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a7bb5-415">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a7bb5-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a7bb5-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a7bb5-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a7bb5-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a7bb5-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a7bb5-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7bb5-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7bb5-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7bb5-420">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a7bb5-421">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a7bb5-422">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a7bb5-423">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a7bb5-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7bb5-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="a7bb5-425">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="a7bb5-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a7bb5-426">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a7bb5-427">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a7bb5-428">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7bb5-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7bb5-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7bb5-430">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="a7bb5-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a7bb5-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7bb5-431">AzureRM.Network</span></span>
* <span data-ttu-id="a7bb5-432">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a7bb5-433">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="a7bb5-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a7bb5-434">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a7bb5-435">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a7bb5-436">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a7bb5-437">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a7bb5-438">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a7bb5-439">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a7bb5-440">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a7bb5-441">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a7bb5-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7bb5-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7bb5-443">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a7bb5-444">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a7bb5-445">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7bb5-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7bb5-446">AzureRM.Resources</span></span>
* <span data-ttu-id="a7bb5-447">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a7bb5-448">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a7bb5-449">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="a7bb5-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a7bb5-450">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a7bb5-451">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a7bb5-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a7bb5-452">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7bb5-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a7bb5-453">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7bb5-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a7bb5-454">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a7bb5-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a7bb5-455">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7bb5-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a7bb5-456">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="a7bb5-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a7bb5-457">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a7bb5-458">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="a7bb5-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a7bb5-459">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a7bb5-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7bb5-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a7bb5-461">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7bb5-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7bb5-462">AzureRM.Sql</span></span>
* <span data-ttu-id="a7bb5-463">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="a7bb5-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a7bb5-464">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a7bb5-465">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a7bb5-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-466">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-467">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="a7bb5-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a7bb5-468">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="a7bb5-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a7bb5-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a7bb5-469">Azure.Storage</span></span>
* <span data-ttu-id="a7bb5-470">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7bb5-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-471">AzureRM.Compute</span></span>
* <span data-ttu-id="a7bb5-472">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="a7bb5-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a7bb5-473">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="a7bb5-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a7bb5-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a7bb5-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a7bb5-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a7bb5-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a7bb5-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a7bb5-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a7bb5-477">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a7bb5-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7bb5-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a7bb5-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7bb5-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a7bb5-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7bb5-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a7bb5-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7bb5-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a7bb5-482">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7bb5-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a7bb5-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7bb5-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a7bb5-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a7bb5-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a7bb5-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a7bb5-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a7bb5-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7bb5-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a7bb5-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7bb5-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a7bb5-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7bb5-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a7bb5-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a7bb5-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a7bb5-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a7bb5-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a7bb5-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a7bb5-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a7bb5-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a7bb5-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a7bb5-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a7bb5-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a7bb5-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a7bb5-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a7bb5-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a7bb5-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a7bb5-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a7bb5-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a7bb5-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a7bb5-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a7bb5-498">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a7bb5-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7bb5-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7bb5-500">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="a7bb5-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a7bb5-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a7bb5-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a7bb5-502">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a7bb5-503">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="a7bb5-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a7bb5-504">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a7bb5-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7bb5-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7bb5-506">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a7bb5-507">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7bb5-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7bb5-508">AzureRM.Sql</span></span>
* <span data-ttu-id="a7bb5-509">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="a7bb5-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7bb5-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7bb5-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7bb5-511">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="a7bb5-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7bb5-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7bb5-512">AzureRM.Websites</span></span>
* <span data-ttu-id="a7bb5-513">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="a7bb5-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a7bb5-514">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="a7bb5-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a7bb5-515">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a7bb5-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a7bb5-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a7bb5-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a7bb5-517">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="a7bb5-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a7bb5-518">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="a7bb5-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-519">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-520">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="a7bb5-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a7bb5-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a7bb5-521">AzureRM.Compute</span></span>
* <span data-ttu-id="a7bb5-522">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="a7bb5-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a7bb5-523">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="a7bb5-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a7bb5-524">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a7bb5-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7bb5-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a7bb5-526">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a7bb5-527">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="a7bb5-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a7bb5-528">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a7bb5-529">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="a7bb5-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a7bb5-530">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="a7bb5-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a7bb5-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7bb5-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a7bb5-532">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="a7bb5-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a7bb5-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7bb5-533">AzureRM.Network</span></span>
* <span data-ttu-id="a7bb5-534">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="a7bb5-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a7bb5-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a7bb5-535">AzureRM.Resources</span></span>
* <span data-ttu-id="a7bb5-536">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="a7bb5-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a7bb5-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a7bb5-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a7bb5-538">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="a7bb5-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a7bb5-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7bb5-539">AzureRM.Sql</span></span>
* <span data-ttu-id="a7bb5-540">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="a7bb5-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a7bb5-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7bb5-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a7bb5-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7bb5-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a7bb5-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a7bb5-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a7bb5-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a7bb5-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a7bb5-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7bb5-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a7bb5-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a7bb5-546">AzureRM.Websites</span></span>
* <span data-ttu-id="a7bb5-547">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a7bb5-548">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="a7bb5-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a7bb5-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a7bb5-549">AzureRM.Profile</span></span>
* <span data-ttu-id="a7bb5-550">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="a7bb5-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a7bb5-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7bb5-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a7bb5-552">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a7bb5-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7bb5-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a7bb5-554">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="a7bb5-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a7bb5-555">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7bb5-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a7bb5-556">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7bb5-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a7bb5-557">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a7bb5-558">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7bb5-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a7bb5-559">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="a7bb5-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a7bb5-560">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="a7bb5-560">Added support for MSI identity</span></span>
* <span data-ttu-id="a7bb5-561">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="a7bb5-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a7bb5-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a7bb5-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a7bb5-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7bb5-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a7bb5-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a7bb5-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a7bb5-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a7bb5-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a7bb5-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a7bb5-566">AzureRM.Batch</span></span>
* <span data-ttu-id="a7bb5-567">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a7bb5-568">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a7bb5-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a7bb5-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="a7bb5-570">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="a7bb5-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a7bb5-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7bb5-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a7bb5-572">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a7bb5-573">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a7bb5-574">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="a7bb5-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a7bb5-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a7bb5-575">AzureRM.Network</span></span>
* <span data-ttu-id="a7bb5-576">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="a7bb5-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a7bb5-577">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="a7bb5-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a7bb5-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7bb5-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a7bb5-579">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a7bb5-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a7bb5-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a7bb5-581">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a7bb5-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a7bb5-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a7bb5-583">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="a7bb5-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a7bb5-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a7bb5-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a7bb5-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7bb5-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a7bb5-586">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="a7bb5-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a7bb5-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a7bb5-587">AzureRM.Sql</span></span>
* <span data-ttu-id="a7bb5-588">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="a7bb5-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a7bb5-589">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a7bb5-590">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a7bb5-591">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a7bb5-592">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="a7bb5-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a7bb5-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7bb5-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a7bb5-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7bb5-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a7bb5-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a7bb5-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a7bb5-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a7bb5-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a7bb5-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a7bb5-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a7bb5-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7bb5-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a7bb5-599">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="a7bb5-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
