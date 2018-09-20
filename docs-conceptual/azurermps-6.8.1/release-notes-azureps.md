---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300833"
---
# <a name="release-notes"></a><span data-ttu-id="6c4f1-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="6c4f1-103">Release notes</span></span>

<span data-ttu-id="6c4f1-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="6c4f1-105">6.8.1 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c4f1-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="6c4f1-106">General</span></span>
* <span data-ttu-id="6c4f1-107">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6c4f1-108">Frissített közös futtatókörnyezeti szerelvények</span><span class="sxs-lookup"><span data-stu-id="6c4f1-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c4f1-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c4f1-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c4f1-110">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6c4f1-111">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="6c4f1-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="6c4f1-112">Az Import-AzureRmApiManagementApi és az \*-AzureRmApiManagementCertificate parancsmagok már tudják kezelni a relatív elérési utakat</span><span class="sxs-lookup"><span data-stu-id="6c4f1-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="6c4f1-113">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="6c4f1-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="6c4f1-114">A CertificateInformation egy beállítható tulajdonság, amely a Set-AzureRmApiManagement parancsmag megfelelő működését biztosítja.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="6c4f1-115">Javítva a nuget 4.0.4-es előzetes verziójára való frissítéssel</span><span class="sxs-lookup"><span data-stu-id="6c4f1-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="6c4f1-116">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="6c4f1-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="6c4f1-117">A termékben való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="6c4f1-118">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="6c4f1-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="6c4f1-119">Az API-ban való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="6c4f1-120">Az AzureMonitor támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-121">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-122">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6c4f1-123">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="6c4f1-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6c4f1-124">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6c4f1-125">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="6c4f1-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-126">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-127">A parancsmagkimenetek alapértelmezett ábrázolása táblanézetre módosítva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6c4f1-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6c4f1-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6c4f1-129">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="6c4f1-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="6c4f1-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c4f1-130">AzureRM.Resources</span></span>
* <span data-ttu-id="6c4f1-131">Ki lett javítva a felügyelt alkalmazások Marketplace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c4f1-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c4f1-133">Hibák kijavítva:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c4f1-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c4f1-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c4f1-135">A MultiValue útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6c4f1-136">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="6c4f1-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6c4f1-137">Az alhálózati útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6c4f1-138">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="6c4f1-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6c4f1-139">Egyéni fejlécek profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6c4f1-140">Várt állapotkód-tartományok profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6c4f1-141">Egyéni fejlécek végpontokon való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="6c4f1-142">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c4f1-143">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="6c4f1-143">General</span></span>
* <span data-ttu-id="6c4f1-144">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-145">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-146">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-147">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-148">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6c4f1-149">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="6c4f1-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6c4f1-150">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="6c4f1-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6c4f1-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c4f1-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="6c4f1-152">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="6c4f1-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-153">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-154">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="6c4f1-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6c4f1-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6c4f1-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6c4f1-156">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="6c4f1-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c4f1-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c4f1-157">AzureRM.Resources</span></span>
* <span data-ttu-id="6c4f1-158">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c4f1-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c4f1-160">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c4f1-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c4f1-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c4f1-162">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6c4f1-163">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="6c4f1-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6c4f1-164">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6c4f1-165">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="6c4f1-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6c4f1-166">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6c4f1-167">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6c4f1-168">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="6c4f1-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c4f1-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c4f1-169">AzureRM.Websites</span></span>
* <span data-ttu-id="6c4f1-170">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="6c4f1-171">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-172">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-173">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c4f1-174">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="6c4f1-175">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="6c4f1-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="6c4f1-176">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="6c4f1-177">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c4f1-177">Azure.Storage</span></span>
* <span data-ttu-id="6c4f1-178">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="6c4f1-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6c4f1-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6c4f1-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c4f1-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6c4f1-181">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="6c4f1-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c4f1-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="6c4f1-183">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c4f1-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c4f1-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c4f1-185">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="6c4f1-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6c4f1-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="6c4f1-187">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6c4f1-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6c4f1-188">AzureRM.Automation</span></span>
* <span data-ttu-id="6c4f1-189">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="6c4f1-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="6c4f1-190">AzureRM.Backup</span></span>
* <span data-ttu-id="6c4f1-191">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6c4f1-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6c4f1-192">AzureRM.Batch</span></span>
* <span data-ttu-id="6c4f1-193">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="6c4f1-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="6c4f1-194">AzureRM.Billing</span></span>
* <span data-ttu-id="6c4f1-195">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="6c4f1-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c4f1-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="6c4f1-197">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="6c4f1-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c4f1-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="6c4f1-199">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-200">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-201">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c4f1-202">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="6c4f1-203">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="6c4f1-204">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6c4f1-205">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="6c4f1-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6c4f1-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6c4f1-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="6c4f1-207">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="6c4f1-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6c4f1-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="6c4f1-209">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="6c4f1-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6c4f1-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="6c4f1-211">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="6c4f1-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="6c4f1-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="6c4f1-213">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6c4f1-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6c4f1-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6c4f1-215">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6c4f1-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6c4f1-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6c4f1-217">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c4f1-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c4f1-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c4f1-219">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="6c4f1-220">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6c4f1-221">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c4f1-222">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="6c4f1-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6c4f1-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="6c4f1-224">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="6c4f1-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="6c4f1-225">AzureRM.Dns</span></span>
* <span data-ttu-id="6c4f1-226">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6c4f1-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c4f1-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6c4f1-228">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c4f1-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c4f1-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c4f1-230">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="6c4f1-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c4f1-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="6c4f1-232">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6c4f1-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6c4f1-233">AzureRM.Insights</span></span>
* <span data-ttu-id="6c4f1-234">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6c4f1-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c4f1-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="6c4f1-236">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c4f1-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c4f1-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c4f1-238">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6c4f1-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c4f1-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6c4f1-240">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="6c4f1-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6c4f1-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="6c4f1-242">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="6c4f1-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="6c4f1-244">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="6c4f1-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6c4f1-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="6c4f1-246">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="6c4f1-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="6c4f1-247">AzureRM.Media</span></span>
* <span data-ttu-id="6c4f1-248">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-249">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-250">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="6c4f1-251">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6c4f1-252">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="6c4f1-253">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6c4f1-254">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6c4f1-255">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6c4f1-256">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="6c4f1-257">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="6c4f1-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="6c4f1-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6c4f1-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="6c4f1-259">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="6c4f1-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c4f1-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6c4f1-261">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6c4f1-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c4f1-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6c4f1-263">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6c4f1-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6c4f1-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6c4f1-265">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="6c4f1-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c4f1-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="6c4f1-267">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6c4f1-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6c4f1-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6c4f1-269">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="6c4f1-270">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="6c4f1-271">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="6c4f1-272">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c4f1-273">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="6c4f1-274">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="6c4f1-275">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6c4f1-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6c4f1-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6c4f1-277">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="6c4f1-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6c4f1-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="6c4f1-279">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6c4f1-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6c4f1-280">AzureRM.Relay</span></span>
* <span data-ttu-id="6c4f1-281">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c4f1-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c4f1-282">AzureRM.Resources</span></span>
* <span data-ttu-id="6c4f1-283">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="6c4f1-284">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="6c4f1-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c4f1-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c4f1-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c4f1-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c4f1-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c4f1-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c4f1-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c4f1-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c4f1-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c4f1-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c4f1-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6c4f1-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="6c4f1-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6c4f1-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="6c4f1-292">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="6c4f1-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="6c4f1-293">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="6c4f1-294">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6c4f1-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6c4f1-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6c4f1-296">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c4f1-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c4f1-298">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6c4f1-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c4f1-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6c4f1-300">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c4f1-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c4f1-301">AzureRM.Sql</span></span>
* <span data-ttu-id="6c4f1-302">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6c4f1-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6c4f1-303">AzureRM.Storage</span></span>
* <span data-ttu-id="6c4f1-304">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="6c4f1-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="6c4f1-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="6c4f1-306">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6c4f1-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6c4f1-307">AzureRM.Tags</span></span>
* <span data-ttu-id="6c4f1-308">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c4f1-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c4f1-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c4f1-310">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="6c4f1-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="6c4f1-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="6c4f1-312">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c4f1-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c4f1-313">AzureRM.Websites</span></span>
* <span data-ttu-id="6c4f1-314">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="6c4f1-315">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="6c4f1-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c4f1-316">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="6c4f1-316">General</span></span>
* <span data-ttu-id="6c4f1-317">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-318">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-319">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="6c4f1-320">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="6c4f1-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6c4f1-321">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c4f1-321">Azure.Storage</span></span>
* <span data-ttu-id="6c4f1-322">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="6c4f1-323">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c4f1-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c4f1-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c4f1-325">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="6c4f1-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="6c4f1-326">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="6c4f1-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="6c4f1-327">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="6c4f1-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="6c4f1-328">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="6c4f1-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="6c4f1-329">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="6c4f1-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="6c4f1-330">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="6c4f1-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-331">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-332">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="6c4f1-333">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="6c4f1-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="6c4f1-334">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="6c4f1-335">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="6c4f1-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="6c4f1-336">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="6c4f1-337">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="6c4f1-338">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="6c4f1-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="6c4f1-339">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="6c4f1-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="6c4f1-340">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="6c4f1-341">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6c4f1-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6c4f1-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6c4f1-343">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="6c4f1-344">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="6c4f1-345">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="6c4f1-346">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c4f1-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c4f1-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c4f1-348">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="6c4f1-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c4f1-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c4f1-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c4f1-350">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6c4f1-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6c4f1-351">AzureRM.Insights</span></span>
* <span data-ttu-id="6c4f1-352">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="6c4f1-353">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="6c4f1-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c4f1-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c4f1-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c4f1-355">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="6c4f1-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-356">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-357">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c4f1-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c4f1-358">AzureRM.Resources</span></span>
* <span data-ttu-id="6c4f1-359">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="6c4f1-360">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="6c4f1-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c4f1-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c4f1-362">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="6c4f1-363">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="6c4f1-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="6c4f1-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c4f1-364">AzureRM.Sql</span></span>
* <span data-ttu-id="6c4f1-365">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="6c4f1-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c4f1-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6c4f1-367">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="6c4f1-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="6c4f1-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="6c4f1-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="6c4f1-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="6c4f1-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="6c4f1-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="6c4f1-371">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="6c4f1-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="6c4f1-372">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="6c4f1-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6c4f1-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6c4f1-373">AzureRM.Storage</span></span>
* <span data-ttu-id="6c4f1-374">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="6c4f1-375">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="6c4f1-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="6c4f1-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c4f1-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6c4f1-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c4f1-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6c4f1-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c4f1-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6c4f1-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6c4f1-379">AzureRM.Tags</span></span>
* <span data-ttu-id="6c4f1-380">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="6c4f1-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="6c4f1-381">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="6c4f1-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-382">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-383">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="6c4f1-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6c4f1-384">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c4f1-384">Azure.Storage</span></span>
* <span data-ttu-id="6c4f1-385">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="6c4f1-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6c4f1-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6c4f1-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6c4f1-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c4f1-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6c4f1-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c4f1-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6c4f1-389">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6c4f1-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6c4f1-390">AzureRM.Automation</span></span>
* <span data-ttu-id="6c4f1-391">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-392">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-393">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c4f1-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6c4f1-394">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6c4f1-395">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6c4f1-396">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="6c4f1-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6c4f1-397">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c4f1-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c4f1-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c4f1-399">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="6c4f1-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c4f1-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c4f1-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c4f1-401">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="6c4f1-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6c4f1-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c4f1-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6c4f1-403">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6c4f1-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-404">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-405">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6c4f1-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6c4f1-406">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6c4f1-407">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="6c4f1-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6c4f1-408">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="6c4f1-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6c4f1-409">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="6c4f1-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6c4f1-410">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6c4f1-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6c4f1-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6c4f1-411">AzureRM.Relay</span></span>
* <span data-ttu-id="6c4f1-412">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c4f1-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c4f1-413">AzureRM.Resources</span></span>
* <span data-ttu-id="6c4f1-414">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6c4f1-415">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6c4f1-416">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6c4f1-417">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6c4f1-418">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="6c4f1-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c4f1-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c4f1-420">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6c4f1-421">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6c4f1-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c4f1-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c4f1-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c4f1-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c4f1-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c4f1-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c4f1-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c4f1-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c4f1-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c4f1-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6c4f1-427">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="6c4f1-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6c4f1-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c4f1-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6c4f1-429">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="6c4f1-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c4f1-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c4f1-430">AzureRM.Sql</span></span>
* <span data-ttu-id="6c4f1-431">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6c4f1-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6c4f1-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6c4f1-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6c4f1-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c4f1-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c4f1-434">AzureRM.Websites</span></span>
* <span data-ttu-id="6c4f1-435">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6c4f1-436">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="6c4f1-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6c4f1-437">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="6c4f1-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6c4f1-438">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="6c4f1-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c4f1-439">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="6c4f1-439">General</span></span>
* <span data-ttu-id="6c4f1-440">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-441">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-442">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-443">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-444">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="6c4f1-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6c4f1-445">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6c4f1-446">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6c4f1-447">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="6c4f1-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6c4f1-448">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6c4f1-449">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="6c4f1-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6c4f1-450">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6c4f1-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6c4f1-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6c4f1-452">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6c4f1-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c4f1-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6c4f1-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c4f1-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6c4f1-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c4f1-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c4f1-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c4f1-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c4f1-457">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6c4f1-458">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6c4f1-459">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6c4f1-460">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c4f1-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c4f1-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c4f1-462">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="6c4f1-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6c4f1-463">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6c4f1-464">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6c4f1-465">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c4f1-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c4f1-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c4f1-467">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="6c4f1-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-468">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-469">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6c4f1-470">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="6c4f1-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6c4f1-471">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6c4f1-472">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6c4f1-473">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6c4f1-474">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6c4f1-475">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6c4f1-476">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6c4f1-477">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6c4f1-478">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6c4f1-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6c4f1-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6c4f1-480">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6c4f1-481">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6c4f1-482">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c4f1-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c4f1-483">AzureRM.Resources</span></span>
* <span data-ttu-id="6c4f1-484">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6c4f1-485">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6c4f1-486">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="6c4f1-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6c4f1-487">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6c4f1-488">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6c4f1-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6c4f1-489">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="6c4f1-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6c4f1-490">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="6c4f1-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6c4f1-491">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="6c4f1-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6c4f1-492">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="6c4f1-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6c4f1-493">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="6c4f1-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6c4f1-494">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6c4f1-495">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="6c4f1-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6c4f1-496">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6c4f1-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c4f1-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c4f1-498">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c4f1-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c4f1-499">AzureRM.Sql</span></span>
* <span data-ttu-id="6c4f1-500">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="6c4f1-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6c4f1-501">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6c4f1-502">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="6c4f1-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-503">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-504">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="6c4f1-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6c4f1-505">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="6c4f1-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6c4f1-506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c4f1-506">Azure.Storage</span></span>
* <span data-ttu-id="6c4f1-507">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-508">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-509">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="6c4f1-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6c4f1-510">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="6c4f1-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6c4f1-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6c4f1-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6c4f1-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6c4f1-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6c4f1-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6c4f1-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6c4f1-514">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6c4f1-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c4f1-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6c4f1-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c4f1-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6c4f1-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c4f1-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6c4f1-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c4f1-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6c4f1-519">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c4f1-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6c4f1-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c4f1-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6c4f1-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6c4f1-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6c4f1-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6c4f1-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6c4f1-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c4f1-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6c4f1-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c4f1-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6c4f1-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c4f1-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6c4f1-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c4f1-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6c4f1-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6c4f1-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6c4f1-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6c4f1-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6c4f1-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c4f1-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6c4f1-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6c4f1-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6c4f1-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6c4f1-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6c4f1-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6c4f1-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6c4f1-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c4f1-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6c4f1-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c4f1-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6c4f1-535">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c4f1-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c4f1-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c4f1-537">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="6c4f1-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6c4f1-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c4f1-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6c4f1-539">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6c4f1-540">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="6c4f1-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6c4f1-541">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6c4f1-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6c4f1-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6c4f1-543">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6c4f1-544">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c4f1-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c4f1-545">AzureRM.Sql</span></span>
* <span data-ttu-id="6c4f1-546">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="6c4f1-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c4f1-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c4f1-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c4f1-548">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="6c4f1-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c4f1-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c4f1-549">AzureRM.Websites</span></span>
* <span data-ttu-id="6c4f1-550">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="6c4f1-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6c4f1-551">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="6c4f1-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6c4f1-552">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="6c4f1-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6c4f1-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c4f1-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6c4f1-554">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="6c4f1-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6c4f1-555">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="6c4f1-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-556">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-557">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="6c4f1-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c4f1-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c4f1-558">AzureRM.Compute</span></span>
* <span data-ttu-id="6c4f1-559">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="6c4f1-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6c4f1-560">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="6c4f1-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6c4f1-561">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6c4f1-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6c4f1-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6c4f1-563">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6c4f1-564">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="6c4f1-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6c4f1-565">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6c4f1-566">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="6c4f1-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6c4f1-567">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="6c4f1-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6c4f1-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c4f1-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c4f1-569">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="6c4f1-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-570">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-571">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="6c4f1-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c4f1-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c4f1-572">AzureRM.Resources</span></span>
* <span data-ttu-id="6c4f1-573">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="6c4f1-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6c4f1-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6c4f1-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6c4f1-575">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="6c4f1-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6c4f1-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c4f1-576">AzureRM.Sql</span></span>
* <span data-ttu-id="6c4f1-577">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="6c4f1-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6c4f1-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c4f1-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6c4f1-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6c4f1-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6c4f1-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6c4f1-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6c4f1-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6c4f1-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6c4f1-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c4f1-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c4f1-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c4f1-583">AzureRM.Websites</span></span>
* <span data-ttu-id="6c4f1-584">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6c4f1-585">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="6c4f1-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c4f1-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6c4f1-586">AzureRM.Profile</span></span>
* <span data-ttu-id="6c4f1-587">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="6c4f1-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6c4f1-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c4f1-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6c4f1-589">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c4f1-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c4f1-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c4f1-591">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="6c4f1-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6c4f1-592">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="6c4f1-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6c4f1-593">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="6c4f1-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6c4f1-594">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6c4f1-595">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="6c4f1-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6c4f1-596">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="6c4f1-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6c4f1-597">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="6c4f1-597">Added support for MSI identity</span></span>
* <span data-ttu-id="6c4f1-598">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="6c4f1-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6c4f1-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6c4f1-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6c4f1-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c4f1-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6c4f1-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6c4f1-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6c4f1-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6c4f1-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6c4f1-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6c4f1-603">AzureRM.Batch</span></span>
* <span data-ttu-id="6c4f1-604">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6c4f1-605">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6c4f1-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6c4f1-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="6c4f1-607">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="6c4f1-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c4f1-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c4f1-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c4f1-609">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6c4f1-610">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6c4f1-611">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="6c4f1-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6c4f1-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c4f1-612">AzureRM.Network</span></span>
* <span data-ttu-id="6c4f1-613">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="6c4f1-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6c4f1-614">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6c4f1-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6c4f1-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c4f1-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6c4f1-616">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6c4f1-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c4f1-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6c4f1-618">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6c4f1-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c4f1-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6c4f1-620">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="6c4f1-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6c4f1-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c4f1-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6c4f1-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c4f1-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6c4f1-623">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="6c4f1-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c4f1-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c4f1-624">AzureRM.Sql</span></span>
* <span data-ttu-id="6c4f1-625">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="6c4f1-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6c4f1-626">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6c4f1-627">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6c4f1-628">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6c4f1-629">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="6c4f1-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6c4f1-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c4f1-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6c4f1-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6c4f1-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6c4f1-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6c4f1-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6c4f1-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6c4f1-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6c4f1-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c4f1-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c4f1-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c4f1-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c4f1-636">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="6c4f1-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
