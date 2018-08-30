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
ms.openlocfilehash: 340c1d2d28e1b97cdd2ec98033361eb00b4302da
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018981"
---
# <a name="release-notes"></a><span data-ttu-id="618d4-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="618d4-103">Release notes</span></span>

<span data-ttu-id="618d4-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="618d4-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="618d4-105">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="618d4-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="618d4-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="618d4-106">General</span></span>
* <span data-ttu-id="618d4-107">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="618d4-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="618d4-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="618d4-108">AzureRM.Profile</span></span>
* <span data-ttu-id="618d4-109">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="618d4-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="618d4-110">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="618d4-110">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="618d4-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="618d4-111">Azure.Storage</span></span>
* <span data-ttu-id="618d4-112">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="618d4-112">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="618d4-113">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="618d4-113">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="618d4-114">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="618d4-114">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="618d4-115">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="618d4-115">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="618d4-116">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="618d4-116">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="618d4-117">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="618d4-117">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="618d4-118">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="618d4-118">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="618d4-119">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="618d4-119">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="618d4-120">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="618d4-120">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="618d4-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="618d4-121">AzureRM.Compute</span></span>
* <span data-ttu-id="618d4-122">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="618d4-122">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="618d4-123">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="618d4-123">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="618d4-124">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="618d4-124">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="618d4-125">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="618d4-125">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="618d4-126">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="618d4-126">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="618d4-127">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="618d4-127">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="618d4-128">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="618d4-128">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="618d4-129">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="618d4-129">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="618d4-130">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="618d4-130">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="618d4-131">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="618d4-131">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="618d4-132">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="618d4-132">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="618d4-133">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="618d4-133">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="618d4-134">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="618d4-134">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="618d4-135">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="618d4-135">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="618d4-136">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="618d4-136">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="618d4-137">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="618d4-137">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="618d4-138">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="618d4-138">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="618d4-139">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="618d4-139">AzureRM.EventHub</span></span>
* <span data-ttu-id="618d4-140">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="618d4-140">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="618d4-141">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="618d4-141">AzureRM.Insights</span></span>
* <span data-ttu-id="618d4-142">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="618d4-142">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="618d4-143">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="618d4-143">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="618d4-144">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="618d4-144">AzureRM.KeyVault</span></span>
* <span data-ttu-id="618d4-145">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="618d4-145">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="618d4-146">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="618d4-146">AzureRM.Network</span></span>
* <span data-ttu-id="618d4-147">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="618d4-147">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="618d4-148">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="618d4-148">AzureRM.Resources</span></span>
* <span data-ttu-id="618d4-149">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="618d4-149">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="618d4-150">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="618d4-150">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="618d4-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="618d4-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="618d4-152">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="618d4-152">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="618d4-153">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="618d4-153">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="618d4-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="618d4-154">AzureRM.Sql</span></span>
* <span data-ttu-id="618d4-155">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="618d4-155">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="618d4-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="618d4-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="618d4-157">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="618d4-157">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="618d4-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="618d4-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="618d4-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="618d4-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="618d4-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="618d4-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="618d4-161">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="618d4-161">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="618d4-162">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="618d4-162">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="618d4-163">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="618d4-163">AzureRM.Storage</span></span>
* <span data-ttu-id="618d4-164">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="618d4-164">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="618d4-165">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="618d4-165">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="618d4-166">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="618d4-166">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="618d4-167">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="618d4-167">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="618d4-168">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="618d4-168">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="618d4-169">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="618d4-169">AzureRM.Tags</span></span>
* <span data-ttu-id="618d4-170">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="618d4-170">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="618d4-171">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="618d4-171">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="618d4-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="618d4-172">AzureRM.Profile</span></span>
* <span data-ttu-id="618d4-173">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="618d4-173">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="618d4-174">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="618d4-174">Azure.Storage</span></span>
* <span data-ttu-id="618d4-175">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="618d4-175">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="618d4-176">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="618d4-176">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="618d4-177">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="618d4-177">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="618d4-178">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="618d4-178">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="618d4-179">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="618d4-179">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="618d4-180">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="618d4-180">AzureRM.Automation</span></span>
* <span data-ttu-id="618d4-181">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="618d4-181">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="618d4-182">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="618d4-182">AzureRM.Compute</span></span>
* <span data-ttu-id="618d4-183">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="618d4-183">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="618d4-184">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="618d4-184">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="618d4-185">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="618d4-185">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="618d4-186">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="618d4-186">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="618d4-187">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="618d4-187">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="618d4-188">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="618d4-188">AzureRM.EventHub</span></span>
* <span data-ttu-id="618d4-189">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="618d4-189">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="618d4-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="618d4-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="618d4-191">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="618d4-191">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="618d4-192">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="618d4-192">AzureRM.LogicApp</span></span>
* <span data-ttu-id="618d4-193">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="618d4-193">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="618d4-194">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="618d4-194">AzureRM.Network</span></span>
* <span data-ttu-id="618d4-195">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="618d4-195">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="618d4-196">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="618d4-196">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="618d4-197">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="618d4-197">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="618d4-198">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="618d4-198">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="618d4-199">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="618d4-199">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="618d4-200">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="618d4-200">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="618d4-201">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="618d4-201">AzureRM.Relay</span></span>
* <span data-ttu-id="618d4-202">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="618d4-202">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="618d4-203">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="618d4-203">AzureRM.Resources</span></span>
* <span data-ttu-id="618d4-204">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="618d4-204">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="618d4-205">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="618d4-205">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="618d4-206">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="618d4-206">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="618d4-207">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="618d4-207">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="618d4-208">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="618d4-208">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="618d4-209">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="618d4-209">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="618d4-210">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="618d4-210">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="618d4-211">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="618d4-211">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="618d4-212">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="618d4-212">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="618d4-213">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="618d4-213">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="618d4-214">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="618d4-214">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="618d4-215">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="618d4-215">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="618d4-216">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="618d4-216">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="618d4-217">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="618d4-217">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="618d4-218">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="618d4-218">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="618d4-219">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="618d4-219">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="618d4-220">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="618d4-220">AzureRM.Sql</span></span>
* <span data-ttu-id="618d4-221">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="618d4-221">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="618d4-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="618d4-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="618d4-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="618d4-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="618d4-224">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="618d4-224">AzureRM.Websites</span></span>
* <span data-ttu-id="618d4-225">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="618d4-225">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="618d4-226">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="618d4-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="618d4-227">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="618d4-227">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="618d4-228">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="618d4-228">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="618d4-229">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="618d4-229">General</span></span>
* <span data-ttu-id="618d4-230">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="618d4-230">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="618d4-231">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="618d4-231">AzureRM.Profile</span></span>
* <span data-ttu-id="618d4-232">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="618d4-232">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="618d4-233">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="618d4-233">AzureRM.Compute</span></span>
* <span data-ttu-id="618d4-234">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="618d4-234">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="618d4-235">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-235">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="618d4-236">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="618d4-236">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="618d4-237">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="618d4-237">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="618d4-238">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="618d4-238">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="618d4-239">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="618d4-239">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="618d4-240">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="618d4-240">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="618d4-241">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="618d4-241">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="618d4-242">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="618d4-242">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="618d4-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="618d4-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="618d4-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="618d4-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="618d4-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="618d4-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="618d4-246">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="618d4-246">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="618d4-247">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="618d4-247">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="618d4-248">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="618d4-248">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="618d4-249">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="618d4-249">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="618d4-250">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="618d4-250">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="618d4-251">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="618d4-251">AzureRM.EventHub</span></span>
* <span data-ttu-id="618d4-252">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="618d4-252">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="618d4-253">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="618d4-253">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="618d4-254">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="618d4-254">Provided Default Parameter set.</span></span>
* <span data-ttu-id="618d4-255">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="618d4-255">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="618d4-256">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="618d4-256">AzureRM.KeyVault</span></span>
* <span data-ttu-id="618d4-257">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="618d4-257">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="618d4-258">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="618d4-258">AzureRM.Network</span></span>
* <span data-ttu-id="618d4-259">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="618d4-259">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="618d4-260">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="618d4-260">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="618d4-261">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-261">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="618d4-262">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-262">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="618d4-263">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-263">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="618d4-264">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-264">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="618d4-265">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-265">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="618d4-266">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-266">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="618d4-267">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-267">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="618d4-268">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="618d4-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="618d4-269">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="618d4-269">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="618d4-270">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="618d4-270">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="618d4-271">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="618d4-271">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="618d4-272">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="618d4-272">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="618d4-273">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="618d4-273">AzureRM.Resources</span></span>
* <span data-ttu-id="618d4-274">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="618d4-274">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="618d4-275">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="618d4-275">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="618d4-276">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="618d4-276">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="618d4-277">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="618d4-277">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="618d4-278">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="618d4-278">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="618d4-279">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="618d4-279">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="618d4-280">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="618d4-280">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="618d4-281">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="618d4-281">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="618d4-282">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="618d4-282">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="618d4-283">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="618d4-283">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="618d4-284">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="618d4-284">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="618d4-285">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="618d4-285">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="618d4-286">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="618d4-286">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="618d4-287">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="618d4-287">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="618d4-288">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="618d4-288">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="618d4-289">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="618d4-289">AzureRM.Sql</span></span>
* <span data-ttu-id="618d4-290">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="618d4-290">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="618d4-291">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="618d4-291">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="618d4-292">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="618d4-292">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="618d4-293">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="618d4-293">AzureRM.Profile</span></span>
* <span data-ttu-id="618d4-294">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="618d4-294">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="618d4-295">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="618d4-295">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="618d4-296">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="618d4-296">Azure.Storage</span></span>
* <span data-ttu-id="618d4-297">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="618d4-297">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="618d4-298">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="618d4-298">AzureRM.Compute</span></span>
* <span data-ttu-id="618d4-299">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="618d4-299">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="618d4-300">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="618d4-300">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="618d4-301">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="618d4-301">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="618d4-302">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="618d4-302">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="618d4-303">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="618d4-303">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="618d4-304">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="618d4-304">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="618d4-305">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="618d4-305">Start-AzureRmVM</span></span>
    - <span data-ttu-id="618d4-306">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="618d4-306">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="618d4-307">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="618d4-307">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="618d4-308">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="618d4-308">Set-AzureRmVM</span></span>
    - <span data-ttu-id="618d4-309">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="618d4-309">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="618d4-310">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="618d4-310">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="618d4-311">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="618d4-311">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="618d4-312">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="618d4-312">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="618d4-313">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="618d4-313">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="618d4-314">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="618d4-314">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="618d4-315">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="618d4-315">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="618d4-316">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="618d4-316">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="618d4-317">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="618d4-317">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="618d4-318">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="618d4-318">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="618d4-319">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="618d4-319">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="618d4-320">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="618d4-320">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="618d4-321">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="618d4-321">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="618d4-322">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="618d4-322">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="618d4-323">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="618d4-323">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="618d4-324">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="618d4-324">AzureRM.EventGrid</span></span>
* <span data-ttu-id="618d4-325">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="618d4-325">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="618d4-326">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="618d4-326">AzureRM.KeyVault</span></span>
* <span data-ttu-id="618d4-327">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="618d4-327">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="618d4-328">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="618d4-328">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="618d4-329">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="618d4-329">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="618d4-330">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="618d4-330">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="618d4-331">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="618d4-331">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="618d4-332">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="618d4-332">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="618d4-333">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="618d4-333">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="618d4-334">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="618d4-334">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="618d4-335">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="618d4-335">AzureRM.Sql</span></span>
* <span data-ttu-id="618d4-336">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="618d4-336">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="618d4-337">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="618d4-337">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="618d4-338">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="618d4-338">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="618d4-339">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="618d4-339">AzureRM.Websites</span></span>
* <span data-ttu-id="618d4-340">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="618d4-340">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="618d4-341">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="618d4-341">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="618d4-342">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="618d4-342">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="618d4-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="618d4-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="618d4-344">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="618d4-344">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="618d4-345">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="618d4-345">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="618d4-346">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="618d4-346">AzureRM.Profile</span></span>
* <span data-ttu-id="618d4-347">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="618d4-347">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="618d4-348">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="618d4-348">AzureRM.Compute</span></span>
* <span data-ttu-id="618d4-349">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="618d4-349">VMSS VM Update feature</span></span>
    - <span data-ttu-id="618d4-350">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="618d4-350">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="618d4-351">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="618d4-351">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="618d4-352">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="618d4-352">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="618d4-353">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="618d4-353">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="618d4-354">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="618d4-354">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="618d4-355">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="618d4-355">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="618d4-356">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="618d4-356">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="618d4-357">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="618d4-357">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="618d4-358">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="618d4-358">AzureRM.KeyVault</span></span>
* <span data-ttu-id="618d4-359">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="618d4-359">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="618d4-360">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="618d4-360">AzureRM.Network</span></span>
* <span data-ttu-id="618d4-361">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="618d4-361">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="618d4-362">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="618d4-362">AzureRM.Resources</span></span>
* <span data-ttu-id="618d4-363">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="618d4-363">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="618d4-364">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="618d4-364">AzureRM.Scheduler</span></span>
* <span data-ttu-id="618d4-365">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="618d4-365">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="618d4-366">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="618d4-366">AzureRM.Sql</span></span>
* <span data-ttu-id="618d4-367">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="618d4-367">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="618d4-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="618d4-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="618d4-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="618d4-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="618d4-370">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="618d4-370">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="618d4-371">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="618d4-371">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="618d4-372">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="618d4-372">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="618d4-373">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="618d4-373">AzureRM.Websites</span></span>
* <span data-ttu-id="618d4-374">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="618d4-374">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="618d4-375">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="618d4-375">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="618d4-376">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="618d4-376">AzureRM.Profile</span></span>
* <span data-ttu-id="618d4-377">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="618d4-377">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="618d4-378">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="618d4-378">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="618d4-379">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="618d4-379">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="618d4-380">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="618d4-380">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="618d4-381">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="618d4-381">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="618d4-382">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="618d4-382">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="618d4-383">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="618d4-383">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="618d4-384">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="618d4-384">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="618d4-385">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="618d4-385">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="618d4-386">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="618d4-386">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="618d4-387">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="618d4-387">Added support for MSI identity</span></span>
* <span data-ttu-id="618d4-388">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="618d4-388">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="618d4-389">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="618d4-389">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="618d4-390">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="618d4-390">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="618d4-391">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="618d4-391">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="618d4-392">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="618d4-392">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="618d4-393">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="618d4-393">AzureRM.Batch</span></span>
* <span data-ttu-id="618d4-394">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="618d4-394">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="618d4-395">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="618d4-395">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="618d4-396">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="618d4-396">AzureRM.Consumption</span></span>
* <span data-ttu-id="618d4-397">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="618d4-397">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="618d4-398">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="618d4-398">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="618d4-399">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="618d4-399">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="618d4-400">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="618d4-400">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="618d4-401">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="618d4-401">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="618d4-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="618d4-402">AzureRM.Network</span></span>
* <span data-ttu-id="618d4-403">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="618d4-403">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="618d4-404">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="618d4-404">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="618d4-405">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="618d4-405">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="618d4-406">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="618d4-406">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="618d4-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="618d4-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="618d4-408">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="618d4-408">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="618d4-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="618d4-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="618d4-410">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="618d4-410">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="618d4-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="618d4-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="618d4-412">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="618d4-412">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="618d4-413">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="618d4-413">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="618d4-414">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="618d4-414">AzureRM.Sql</span></span>
* <span data-ttu-id="618d4-415">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="618d4-415">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="618d4-416">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="618d4-416">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="618d4-417">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="618d4-417">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="618d4-418">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="618d4-418">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="618d4-419">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="618d4-419">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="618d4-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="618d4-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="618d4-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="618d4-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="618d4-422">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="618d4-422">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="618d4-423">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="618d4-423">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="618d4-424">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="618d4-424">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="618d4-425">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="618d4-425">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="618d4-426">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="618d4-426">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
