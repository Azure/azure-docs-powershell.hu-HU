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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653491"
---
# <a name="release-notes"></a><span data-ttu-id="c706f-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="c706f-103">Release notes</span></span>

<span data-ttu-id="c706f-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="c706f-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="c706f-105">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="c706f-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c706f-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="c706f-106">General</span></span>
* <span data-ttu-id="c706f-107">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="c706f-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c706f-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c706f-108">AzureRM.Profile</span></span>
* <span data-ttu-id="c706f-109">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="c706f-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="c706f-110">Az alapértelmezett beállítás mindig az igaz érték, az egyéni erőforrások és az alapértelmezett érték felülírásának lehetősége.</span><span class="sxs-lookup"><span data-stu-id="c706f-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="c706f-111">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="c706f-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c706f-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c706f-112">Azure.Storage</span></span>
* <span data-ttu-id="c706f-113">Támogatott a Storage-környezet beolvasása a DefaulfProfile-ból</span><span class="sxs-lookup"><span data-stu-id="c706f-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="c706f-114">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="c706f-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c706f-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c706f-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c706f-116">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="c706f-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="c706f-117">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="c706f-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="c706f-118">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="c706f-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="c706f-119">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="c706f-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="c706f-120">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="c706f-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="c706f-121">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="c706f-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c706f-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c706f-122">AzureRM.Compute</span></span>
* <span data-ttu-id="c706f-123">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="c706f-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="c706f-124">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="c706f-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="c706f-125">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="c706f-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="c706f-126">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="c706f-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="c706f-127">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="c706f-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="c706f-128">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="c706f-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="c706f-129">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="c706f-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="c706f-130">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="c706f-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="c706f-131">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="c706f-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="c706f-132">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="c706f-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c706f-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c706f-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c706f-134">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="c706f-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="c706f-135">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="c706f-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="c706f-136">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="c706f-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="c706f-137">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="c706f-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c706f-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c706f-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c706f-139">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="c706f-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c706f-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c706f-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="c706f-141">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="c706f-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c706f-142">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c706f-142">AzureRM.Insights</span></span>
* <span data-ttu-id="c706f-143">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="c706f-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="c706f-144">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="c706f-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c706f-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c706f-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c706f-146">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="c706f-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c706f-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c706f-147">AzureRM.Network</span></span>
* <span data-ttu-id="c706f-148">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="c706f-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c706f-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c706f-149">AzureRM.Resources</span></span>
* <span data-ttu-id="c706f-150">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="c706f-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="c706f-151">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="c706f-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c706f-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c706f-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c706f-153">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="c706f-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="c706f-154">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="c706f-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="c706f-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c706f-155">AzureRM.Sql</span></span>
* <span data-ttu-id="c706f-156">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="c706f-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="c706f-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c706f-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c706f-158">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="c706f-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="c706f-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="c706f-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="c706f-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="c706f-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="c706f-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="c706f-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="c706f-162">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="c706f-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="c706f-163">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="c706f-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c706f-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c706f-164">AzureRM.Storage</span></span>
* <span data-ttu-id="c706f-165">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="c706f-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="c706f-166">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="c706f-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="c706f-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c706f-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c706f-168">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c706f-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c706f-169">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c706f-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c706f-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c706f-170">AzureRM.Tags</span></span>
* <span data-ttu-id="c706f-171">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="c706f-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="c706f-172">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="c706f-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c706f-173">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c706f-173">AzureRM.Profile</span></span>
* <span data-ttu-id="c706f-174">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="c706f-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c706f-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c706f-175">Azure.Storage</span></span>
* <span data-ttu-id="c706f-176">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="c706f-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="c706f-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c706f-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="c706f-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c706f-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c706f-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c706f-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c706f-180">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="c706f-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c706f-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c706f-181">AzureRM.Automation</span></span>
* <span data-ttu-id="c706f-182">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="c706f-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c706f-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c706f-183">AzureRM.Compute</span></span>
* <span data-ttu-id="c706f-184">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c706f-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="c706f-185">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="c706f-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c706f-186">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="c706f-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c706f-187">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="c706f-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="c706f-188">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="c706f-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c706f-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c706f-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="c706f-190">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="c706f-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c706f-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c706f-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c706f-192">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="c706f-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c706f-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c706f-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c706f-194">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c706f-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c706f-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c706f-195">AzureRM.Network</span></span>
* <span data-ttu-id="c706f-196">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c706f-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="c706f-197">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="c706f-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="c706f-198">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="c706f-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="c706f-199">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="c706f-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="c706f-200">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="c706f-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="c706f-201">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c706f-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c706f-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c706f-202">AzureRM.Relay</span></span>
* <span data-ttu-id="c706f-203">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="c706f-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c706f-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c706f-204">AzureRM.Resources</span></span>
* <span data-ttu-id="c706f-205">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="c706f-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="c706f-206">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="c706f-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="c706f-207">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="c706f-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="c706f-208">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="c706f-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="c706f-209">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="c706f-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c706f-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c706f-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c706f-211">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="c706f-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="c706f-212">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="c706f-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="c706f-213">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c706f-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c706f-214">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c706f-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c706f-215">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c706f-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c706f-216">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c706f-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c706f-217">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c706f-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="c706f-218">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="c706f-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c706f-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c706f-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c706f-220">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="c706f-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c706f-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c706f-221">AzureRM.Sql</span></span>
* <span data-ttu-id="c706f-222">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="c706f-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="c706f-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c706f-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="c706f-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c706f-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c706f-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c706f-225">AzureRM.Websites</span></span>
* <span data-ttu-id="c706f-226">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="c706f-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="c706f-227">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="c706f-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="c706f-228">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="c706f-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="c706f-229">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="c706f-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c706f-230">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="c706f-230">General</span></span>
* <span data-ttu-id="c706f-231">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="c706f-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c706f-232">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c706f-232">AzureRM.Profile</span></span>
* <span data-ttu-id="c706f-233">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="c706f-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c706f-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c706f-234">AzureRM.Compute</span></span>
* <span data-ttu-id="c706f-235">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="c706f-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="c706f-236">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="c706f-237">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c706f-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c706f-238">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="c706f-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="c706f-239">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c706f-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="c706f-240">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="c706f-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="c706f-241">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c706f-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c706f-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c706f-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c706f-243">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="c706f-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="c706f-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c706f-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c706f-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c706f-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c706f-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c706f-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c706f-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c706f-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c706f-248">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="c706f-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c706f-249">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="c706f-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c706f-250">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="c706f-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="c706f-251">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="c706f-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c706f-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c706f-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="c706f-253">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="c706f-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="c706f-254">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="c706f-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="c706f-255">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="c706f-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="c706f-256">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="c706f-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c706f-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c706f-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c706f-258">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="c706f-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c706f-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c706f-259">AzureRM.Network</span></span>
* <span data-ttu-id="c706f-260">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="c706f-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="c706f-261">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="c706f-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="c706f-262">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c706f-263">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c706f-264">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c706f-265">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c706f-266">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c706f-267">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c706f-268">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c706f-269">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="c706f-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c706f-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c706f-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c706f-271">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="c706f-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="c706f-272">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="c706f-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="c706f-273">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="c706f-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c706f-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c706f-274">AzureRM.Resources</span></span>
* <span data-ttu-id="c706f-275">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="c706f-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="c706f-276">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="c706f-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="c706f-277">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="c706f-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="c706f-278">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="c706f-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="c706f-279">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c706f-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="c706f-280">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="c706f-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c706f-281">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="c706f-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c706f-282">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c706f-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="c706f-283">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="c706f-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c706f-284">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="c706f-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c706f-285">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="c706f-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="c706f-286">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="c706f-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="c706f-287">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="c706f-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="c706f-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c706f-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c706f-289">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="c706f-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c706f-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c706f-290">AzureRM.Sql</span></span>
* <span data-ttu-id="c706f-291">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="c706f-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="c706f-292">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="c706f-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="c706f-293">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="c706f-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c706f-294">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c706f-294">AzureRM.Profile</span></span>
* <span data-ttu-id="c706f-295">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="c706f-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="c706f-296">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="c706f-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c706f-297">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c706f-297">Azure.Storage</span></span>
* <span data-ttu-id="c706f-298">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="c706f-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c706f-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c706f-299">AzureRM.Compute</span></span>
* <span data-ttu-id="c706f-300">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="c706f-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="c706f-301">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="c706f-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="c706f-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c706f-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c706f-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c706f-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c706f-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c706f-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c706f-305">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="c706f-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="c706f-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c706f-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="c706f-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c706f-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="c706f-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c706f-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="c706f-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c706f-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="c706f-310">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c706f-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="c706f-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c706f-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="c706f-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c706f-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="c706f-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c706f-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="c706f-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c706f-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="c706f-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c706f-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="c706f-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c706f-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="c706f-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c706f-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="c706f-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c706f-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="c706f-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c706f-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c706f-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c706f-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="c706f-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c706f-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c706f-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c706f-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="c706f-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c706f-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="c706f-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c706f-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c706f-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c706f-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c706f-326">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="c706f-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c706f-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c706f-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c706f-328">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="c706f-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c706f-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c706f-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c706f-330">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="c706f-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="c706f-331">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="c706f-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="c706f-332">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="c706f-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c706f-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c706f-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c706f-334">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="c706f-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="c706f-335">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c706f-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c706f-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c706f-336">AzureRM.Sql</span></span>
* <span data-ttu-id="c706f-337">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="c706f-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c706f-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c706f-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c706f-339">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="c706f-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c706f-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c706f-340">AzureRM.Websites</span></span>
* <span data-ttu-id="c706f-341">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="c706f-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="c706f-342">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="c706f-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="c706f-343">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="c706f-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="c706f-344">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c706f-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c706f-345">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="c706f-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="c706f-346">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="c706f-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c706f-347">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c706f-347">AzureRM.Profile</span></span>
* <span data-ttu-id="c706f-348">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="c706f-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c706f-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c706f-349">AzureRM.Compute</span></span>
* <span data-ttu-id="c706f-350">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="c706f-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="c706f-351">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="c706f-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="c706f-352">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="c706f-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c706f-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c706f-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c706f-354">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="c706f-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="c706f-355">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="c706f-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="c706f-356">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="c706f-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="c706f-357">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="c706f-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="c706f-358">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="c706f-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c706f-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c706f-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c706f-360">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="c706f-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c706f-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c706f-361">AzureRM.Network</span></span>
* <span data-ttu-id="c706f-362">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="c706f-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c706f-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c706f-363">AzureRM.Resources</span></span>
* <span data-ttu-id="c706f-364">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="c706f-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c706f-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c706f-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c706f-366">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="c706f-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="c706f-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c706f-367">AzureRM.Sql</span></span>
* <span data-ttu-id="c706f-368">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="c706f-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="c706f-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c706f-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c706f-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c706f-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c706f-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c706f-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c706f-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c706f-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c706f-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c706f-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c706f-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c706f-374">AzureRM.Websites</span></span>
* <span data-ttu-id="c706f-375">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="c706f-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="c706f-376">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="c706f-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c706f-377">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c706f-377">AzureRM.Profile</span></span>
* <span data-ttu-id="c706f-378">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="c706f-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c706f-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c706f-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c706f-380">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="c706f-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c706f-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c706f-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c706f-382">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="c706f-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c706f-383">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="c706f-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c706f-384">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="c706f-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c706f-385">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="c706f-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c706f-386">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="c706f-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c706f-387">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="c706f-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c706f-388">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="c706f-388">Added support for MSI identity</span></span>
* <span data-ttu-id="c706f-389">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="c706f-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c706f-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c706f-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c706f-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c706f-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c706f-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c706f-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c706f-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c706f-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c706f-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c706f-394">AzureRM.Batch</span></span>
* <span data-ttu-id="c706f-395">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="c706f-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c706f-396">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="c706f-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c706f-397">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c706f-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="c706f-398">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="c706f-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c706f-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c706f-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c706f-400">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="c706f-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c706f-401">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="c706f-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="c706f-402">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="c706f-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="c706f-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c706f-403">AzureRM.Network</span></span>
* <span data-ttu-id="c706f-404">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="c706f-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c706f-405">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="c706f-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c706f-406">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c706f-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c706f-407">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="c706f-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c706f-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c706f-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c706f-409">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="c706f-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c706f-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c706f-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c706f-411">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="c706f-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c706f-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c706f-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c706f-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c706f-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c706f-414">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="c706f-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c706f-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c706f-415">AzureRM.Sql</span></span>
* <span data-ttu-id="c706f-416">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="c706f-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c706f-417">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="c706f-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c706f-418">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="c706f-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c706f-419">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="c706f-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c706f-420">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="c706f-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="c706f-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c706f-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c706f-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c706f-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c706f-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c706f-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c706f-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c706f-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c706f-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c706f-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c706f-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c706f-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c706f-427">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="c706f-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>