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
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237689"
---
# <a name="release-notes"></a><span data-ttu-id="49e25-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="49e25-103">Release notes</span></span>

<span data-ttu-id="49e25-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="49e25-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="49e25-105">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="49e25-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="49e25-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="49e25-106">AzureRM.Profile</span></span>
* <span data-ttu-id="49e25-107">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek.</span><span class="sxs-lookup"><span data-stu-id="49e25-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="49e25-108">Környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut.</span><span class="sxs-lookup"><span data-stu-id="49e25-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="49e25-109">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="49e25-109">Azure.Storage</span></span>
* <span data-ttu-id="49e25-110">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="49e25-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="49e25-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="49e25-111">AzureRM.Compute</span></span>
* <span data-ttu-id="49e25-112">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik.</span><span class="sxs-lookup"><span data-stu-id="49e25-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="49e25-113">A Compute ügyfélkódtár verziója frissült, a következő parancsmagok javítása érdekében:</span><span class="sxs-lookup"><span data-stu-id="49e25-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="49e25-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="49e25-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="49e25-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="49e25-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="49e25-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="49e25-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="49e25-117">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="49e25-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="49e25-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="49e25-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="49e25-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="49e25-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="49e25-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="49e25-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="49e25-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="49e25-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="49e25-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="49e25-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="49e25-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49e25-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="49e25-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="49e25-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="49e25-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="49e25-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="49e25-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49e25-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="49e25-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49e25-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="49e25-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49e25-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="49e25-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="49e25-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="49e25-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="49e25-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="49e25-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="49e25-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="49e25-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="49e25-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="49e25-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="49e25-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="49e25-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="49e25-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="49e25-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="49e25-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="49e25-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="49e25-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="49e25-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="49e25-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="49e25-138">A ValidateNotNullOrEmpty érvényesítési feltételek az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatóak.</span><span class="sxs-lookup"><span data-stu-id="49e25-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="49e25-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="49e25-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="49e25-140">Ki lett javítva az a probléma, amelyben nem lett visszaadva címke a Get-AzureRmKeyVault -Tag futtatásakor.</span><span class="sxs-lookup"><span data-stu-id="49e25-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="49e25-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="49e25-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="49e25-142">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="49e25-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="49e25-143">A 2018. 04. 04. dátumú API-verziót használják.</span><span class="sxs-lookup"><span data-stu-id="49e25-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="49e25-144">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez.</span><span class="sxs-lookup"><span data-stu-id="49e25-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="49e25-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="49e25-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="49e25-146">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="49e25-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="49e25-147">Ha át van adva, felülírja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="49e25-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="49e25-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="49e25-148">AzureRM.Sql</span></span>
* <span data-ttu-id="49e25-149">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült.</span><span class="sxs-lookup"><span data-stu-id="49e25-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="49e25-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="49e25-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="49e25-151">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült.</span><span class="sxs-lookup"><span data-stu-id="49e25-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="49e25-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="49e25-152">AzureRM.Websites</span></span>
* <span data-ttu-id="49e25-153">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor.</span><span class="sxs-lookup"><span data-stu-id="49e25-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="49e25-154">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként.</span><span class="sxs-lookup"><span data-stu-id="49e25-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="49e25-155">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="49e25-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="49e25-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="49e25-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="49e25-157">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja.</span><span class="sxs-lookup"><span data-stu-id="49e25-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="49e25-158">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="49e25-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="49e25-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="49e25-159">AzureRM.Profile</span></span>
* <span data-ttu-id="49e25-160">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="49e25-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="49e25-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="49e25-161">AzureRM.Compute</span></span>
* <span data-ttu-id="49e25-162">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="49e25-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="49e25-163">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="49e25-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="49e25-164">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="49e25-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="49e25-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="49e25-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="49e25-166">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="49e25-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="49e25-167">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="49e25-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="49e25-168">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="49e25-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="49e25-169">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="49e25-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="49e25-170">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="49e25-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="49e25-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="49e25-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="49e25-172">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="49e25-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="49e25-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="49e25-173">AzureRM.Network</span></span>
* <span data-ttu-id="49e25-174">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="49e25-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="49e25-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="49e25-175">AzureRM.Resources</span></span>
* <span data-ttu-id="49e25-176">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="49e25-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="49e25-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="49e25-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="49e25-178">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="49e25-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="49e25-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="49e25-179">AzureRM.Sql</span></span>
* <span data-ttu-id="49e25-180">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="49e25-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="49e25-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49e25-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="49e25-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49e25-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="49e25-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="49e25-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="49e25-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="49e25-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="49e25-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49e25-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="49e25-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="49e25-186">AzureRM.Websites</span></span>
* <span data-ttu-id="49e25-187">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="49e25-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="49e25-188">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="49e25-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="49e25-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="49e25-189">AzureRM.Profile</span></span>
* <span data-ttu-id="49e25-190">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="49e25-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="49e25-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="49e25-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="49e25-192">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="49e25-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="49e25-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="49e25-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="49e25-194">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="49e25-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="49e25-195">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="49e25-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="49e25-196">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="49e25-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="49e25-197">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="49e25-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="49e25-198">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="49e25-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="49e25-199">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="49e25-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="49e25-200">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="49e25-200">Added support for MSI identity</span></span>
* <span data-ttu-id="49e25-201">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="49e25-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="49e25-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="49e25-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="49e25-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="49e25-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="49e25-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="49e25-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="49e25-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="49e25-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="49e25-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="49e25-206">AzureRM.Batch</span></span>
* <span data-ttu-id="49e25-207">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="49e25-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="49e25-208">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="49e25-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="49e25-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="49e25-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="49e25-210">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="49e25-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="49e25-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="49e25-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="49e25-212">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="49e25-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="49e25-213">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="49e25-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="49e25-214">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="49e25-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="49e25-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="49e25-215">AzureRM.Network</span></span>
* <span data-ttu-id="49e25-216">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="49e25-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="49e25-217">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="49e25-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="49e25-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="49e25-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="49e25-219">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="49e25-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="49e25-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="49e25-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="49e25-221">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="49e25-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="49e25-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="49e25-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="49e25-223">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="49e25-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="49e25-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="49e25-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="49e25-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="49e25-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="49e25-226">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="49e25-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="49e25-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="49e25-227">AzureRM.Sql</span></span>
* <span data-ttu-id="49e25-228">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="49e25-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="49e25-229">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="49e25-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="49e25-230">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="49e25-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="49e25-231">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="49e25-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="49e25-232">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="49e25-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="49e25-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49e25-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="49e25-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="49e25-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="49e25-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="49e25-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="49e25-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="49e25-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="49e25-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="49e25-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="49e25-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="49e25-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="49e25-239">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="49e25-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>