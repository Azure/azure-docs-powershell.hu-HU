---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/08/2018
ms.locfileid: "33912003"
---
# <a name="release-notes"></a><span data-ttu-id="0d101-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="0d101-103">Release notes</span></span>

<span data-ttu-id="0d101-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="0d101-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="0d101-105">6.0.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="0d101-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="0d101-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0d101-106">General</span></span>
* <span data-ttu-id="0d101-107">A PowerShell 5.0 beállítása mint a modulok minimális függősége</span><span class="sxs-lookup"><span data-stu-id="0d101-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="0d101-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0d101-108">Azure.Storage</span></span>
* <span data-ttu-id="0d101-109">Az Azure Storage-blobtárolók neve alapján történő támogatás</span><span class="sxs-lookup"><span data-stu-id="0d101-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="0d101-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0d101-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="0d101-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0d101-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="0d101-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0d101-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="0d101-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0d101-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="0d101-114">Probléma kijavítása, amely során bizonyos Storage-parancsmagok hibakimenete nem tartalmazott részletes információt a hibáról</span><span class="sxs-lookup"><span data-stu-id="0d101-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="0d101-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0d101-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0d101-116">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-117">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="0d101-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="0d101-118">AzureRM.Automation</span></span>
* <span data-ttu-id="0d101-119">Elavult címkék aliasának eltávolítása a parancsmagokból</span><span class="sxs-lookup"><span data-stu-id="0d101-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="0d101-120">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d101-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="0d101-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="0d101-121">AzureRM.Batch</span></span>
* <span data-ttu-id="0d101-122">Frissült a New-AzureBatchPool dokumentációja, amelyből egy elavult példa el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="0d101-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="0d101-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="0d101-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="0d101-124">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-125">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="0d101-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0d101-126">AzureRM.Compute</span></span>
* <span data-ttu-id="0d101-127">A New-AzureRmVm és a New-AzureRmVmss támogatja a paraméterek részletes kimenetét</span><span class="sxs-lookup"><span data-stu-id="0d101-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="0d101-128">A New-AzureRmVm és a New-AzureRmVmss (egyszerű paraméterkészlet) támogatja az identitások meghatározását a virtuális gépek számára felhasználók és (vagy) rendszerek által.</span><span class="sxs-lookup"><span data-stu-id="0d101-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="0d101-129">VMSS Redeploy és PerformMaintenance funkció</span><span class="sxs-lookup"><span data-stu-id="0d101-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="0d101-130">Az új -Redeploy és -PerformMaintenance kapcsolóparaméter hozzáadása a Set-AzureRmVmss és Set-AzureRmVmssVM parancshoz</span><span class="sxs-lookup"><span data-stu-id="0d101-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="0d101-131">Az új DisableVMAgent kapcsolóparaméter hozzáadása a Set-AzureRmVMOperatingSystem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0d101-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="0d101-132">A New-AzureRmVm és a New-AzureRmVmss (egyszerű paraméterkészlet) támogatja a Windows 10-rendszerképet.</span><span class="sxs-lookup"><span data-stu-id="0d101-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="0d101-133">Új Repair-AzureRmVmssServiceFabricUpdateDomain parancsmag.</span><span class="sxs-lookup"><span data-stu-id="0d101-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="0d101-134">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-135">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="0d101-136">A Set-AzureRmVmDiskEncryptionExtension az AAD-paramétereket opcionálissá teszi</span><span class="sxs-lookup"><span data-stu-id="0d101-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="0d101-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="0d101-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="0d101-138">Elavult címkék aliasának eltávolítása a parancsmagokból</span><span class="sxs-lookup"><span data-stu-id="0d101-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="0d101-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="0d101-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0d101-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0d101-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0d101-141">Az ADF .Net SDK frissítése a 0.7.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="0d101-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="0d101-142">Új végrehajtási paraméterek és kapcsolatkezelő tulajdonságok az ExecuteSSISPackage tevékenységhez</span><span class="sxs-lookup"><span data-stu-id="0d101-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="0d101-143">A PostgreSql, MySql társított szolgáltatás frissítése teljes kapcsolati karakterlánc használatára, a kiszolgáló, adatbázis, séma, felhasználónév és jelszó használata helyett</span><span class="sxs-lookup"><span data-stu-id="0d101-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="0d101-144">A séma eltávolítása a DB2 társított szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="0d101-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="0d101-145">Sématulajdonság eltávolítása a Teradata társított szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="0d101-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="0d101-146">LinkedService, Dataset és CopySource hozzáadása a Responsyshez</span><span class="sxs-lookup"><span data-stu-id="0d101-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="0d101-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0d101-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="0d101-148">Elavult címkék aliasának eltávolítása a parancsmagokból</span><span class="sxs-lookup"><span data-stu-id="0d101-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="0d101-149">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0d101-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="0d101-150">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0d101-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="0d101-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0d101-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0d101-152">Új rekurzív Acl-módosítási funkció hozzáadása a következőkhöz: Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0d101-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="0d101-153">Új parancsmag hozzáadása a tartalomösszegzés egy címtárban történő lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="0d101-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="0d101-154">Új parancsmag hozzáadása a lemezhasználat és Acl-memóriakép lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="0d101-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="0d101-155">A Set-AzureRmDataLakeStoreItemAcl logikai érték visszatérési típusának javítása IEnumerable típusra<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="0d101-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="0d101-156">A Set-AzureRmDataLakeStoreItemAclEntry logikai érték visszatérési típusának javítása IEnumerable típusra<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="0d101-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="0d101-157">Kompatibilitástörő változások az alábbiakban: Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0d101-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="0d101-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="0d101-158">AzureRM.Dns</span></span>
* <span data-ttu-id="0d101-159">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-160">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="0d101-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0d101-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="0d101-162">A parancsmagok súgója frissítve lett a hiányzó példákkal</span><span class="sxs-lookup"><span data-stu-id="0d101-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="0d101-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0d101-163">AzureRM.Insights</span></span>
* <span data-ttu-id="0d101-164">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-165">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="0d101-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="0d101-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="0d101-167">Címkék és alapszintű termékváltozat engedélyezése az IoTHub számára</span><span class="sxs-lookup"><span data-stu-id="0d101-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="0d101-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0d101-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0d101-169">Átirányítási forgatókönyveket támogató kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="0d101-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="0d101-170">Az alábbi új parancsmagok hozzáadása: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval és Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="0d101-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="0d101-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0d101-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="0d101-172">Elavult címkék aliasának eltávolítása a parancsmagokból</span><span class="sxs-lookup"><span data-stu-id="0d101-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="0d101-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0d101-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="0d101-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="0d101-174">AzureRM.Media</span></span>
* <span data-ttu-id="0d101-175">Elavult címkék aliasának eltávolítása a parancsmagokból</span><span class="sxs-lookup"><span data-stu-id="0d101-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="0d101-176">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="0d101-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="0d101-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0d101-177">AzureRM.Network</span></span>
* <span data-ttu-id="0d101-178">A DDoS-védelem támogatása erőforrás-tervezéshez</span><span class="sxs-lookup"><span data-stu-id="0d101-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="0d101-179">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-180">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="0d101-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0d101-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="0d101-182">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-183">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="0d101-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0d101-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="0d101-185">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-186">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="0d101-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0d101-187">AzureRM.Profile</span></span>
* <span data-ttu-id="0d101-188">A környezet automatikus mentése alapértelmezés szerint engedélyezve van</span><span class="sxs-lookup"><span data-stu-id="0d101-188">Enable context autosave by default</span></span>
* <span data-ttu-id="0d101-189">A USGovernmentOperationalInsightsEndpoint és USGovernmentOperationalInsightsEndpointResourceId tulajdonság hozzáadása az USA-beli államigazgatásban használt Azure-környezethez.</span><span class="sxs-lookup"><span data-stu-id="0d101-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="0d101-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0d101-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0d101-191">A SiteRecovery-forgatókönyvek során használt hitelesítési fejléc javítása</span><span class="sxs-lookup"><span data-stu-id="0d101-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="0d101-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0d101-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="0d101-193">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-194">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="0d101-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0d101-195">AzureRM.Resources</span></span>
* <span data-ttu-id="0d101-196">Az elavult -AtScopeAndBelow paraméter eltávolítása a Get-AzureRmRoledefinition hívásából</span><span class="sxs-lookup"><span data-stu-id="0d101-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="0d101-197">Hozzárendelések hozzáadása a törölt felhasználókhoz/csoportokhoz/szolgáltatásnevekhez a Get-AzureRmRoleAssignment eredményében</span><span class="sxs-lookup"><span data-stu-id="0d101-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="0d101-198">Scope és ResourceType lapkiegészítő hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0d101-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="0d101-199">Egyszerűsített parancsmag hozzáadása szolgáltatásnevek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="0d101-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="0d101-200">A lekérési és keresési funkció egyesítése a Get-AzureRmResource esetén</span><span class="sxs-lookup"><span data-stu-id="0d101-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="0d101-201">AD-parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="0d101-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="0d101-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="0d101-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="0d101-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="0d101-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="0d101-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="0d101-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="0d101-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="0d101-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="0d101-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0d101-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="0d101-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0d101-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="0d101-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0d101-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="0d101-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0d101-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="0d101-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0d101-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0d101-211">Az alapértelmezett linuxos rendszerképverzió termékváltozatának frissítése</span><span class="sxs-lookup"><span data-stu-id="0d101-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="0d101-212">A NewAzureServiceFabricCluster.cs alapértelmezett UbuntuServer1604-termékváltozatának frissítése</span><span class="sxs-lookup"><span data-stu-id="0d101-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="0d101-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="0d101-213">AzureRM.Storage</span></span>
* <span data-ttu-id="0d101-214">Több kompatibilitástörő változás bevezetése</span><span class="sxs-lookup"><span data-stu-id="0d101-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="0d101-215">További információért tekintse meg a migrálási útmutatót</span><span class="sxs-lookup"><span data-stu-id="0d101-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="0d101-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0d101-216">AzureRM.Websites</span></span>
* <span data-ttu-id="0d101-217">Frissítés a Websites SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="0d101-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="0d101-218">Új -AssignIdentity és -Httpsonly tulajdonság a Set-AzureRmWebApp és a Set-AzureRmWebAppSlot esetén</span><span class="sxs-lookup"><span data-stu-id="0d101-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="0d101-219">Két új parancsmag hozzáadva: Get-AzureRmWebAppSnapshots és Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0d101-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
