---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475260"
---
## <a name="160---march-2019"></a><span data-ttu-id="b6f01-101">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="b6f01-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b6f01-102">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="b6f01-102">Highlights since the last major release</span></span>
* <span data-ttu-id="b6f01-103">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="b6f01-103">General availability of `Az` module</span></span>
* <span data-ttu-id="b6f01-104">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b6f01-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b6f01-105">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b6f01-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b6f01-106">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b6f01-107">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b6f01-108">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b6f01-109">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6f01-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6f01-110">Az.Automation</span></span>
* <span data-ttu-id="b6f01-111">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="b6f01-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b6f01-112">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="b6f01-112">Dynamic grouping</span></span>
    * <span data-ttu-id="b6f01-113">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="b6f01-113">Pre-Post script</span></span>
    * <span data-ttu-id="b6f01-114">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="b6f01-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-115">Az.Compute</span></span>
* <span data-ttu-id="b6f01-116">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b6f01-117">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="b6f01-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6f01-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f01-118">Az.KeyVault</span></span>
* <span data-ttu-id="b6f01-119">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6f01-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-120">Az.Network</span></span>
* <span data-ttu-id="b6f01-121">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b6f01-122">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b6f01-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6f01-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6f01-124">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="b6f01-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b6f01-125">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-126">Az.Resources</span></span>
* <span data-ttu-id="b6f01-127">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b6f01-128">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="b6f01-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6f01-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-129">Az.Sql</span></span>
* <span data-ttu-id="b6f01-130">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="b6f01-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6f01-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6f01-131">Az.Storage</span></span>
* <span data-ttu-id="b6f01-132">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="b6f01-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b6f01-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f01-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b6f01-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f01-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b6f01-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b6f01-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b6f01-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b6f01-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b6f01-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b6f01-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b6f01-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b6f01-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6f01-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6f01-139">Az.Websites</span></span>
* <span data-ttu-id="b6f01-140">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="b6f01-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="b6f01-141">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="b6f01-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6f01-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6f01-142">Az.Accounts</span></span>
* <span data-ttu-id="b6f01-143">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="b6f01-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b6f01-144">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="b6f01-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6f01-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6f01-145">Az.Automation</span></span>
* <span data-ttu-id="b6f01-146">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b6f01-147">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="b6f01-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b6f01-148">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="b6f01-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6f01-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6f01-149">Az.Cdn</span></span>
* <span data-ttu-id="b6f01-150">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="b6f01-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-151">Az.Compute</span></span>
* <span data-ttu-id="b6f01-152">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6f01-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6f01-153">Az.DataFactory</span></span>
* <span data-ttu-id="b6f01-154">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="b6f01-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b6f01-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b6f01-155">Az.LogicApp</span></span>
* <span data-ttu-id="b6f01-156">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="b6f01-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6f01-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-157">Az.Network</span></span>
* <span data-ttu-id="b6f01-158">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6f01-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6f01-160">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b6f01-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b6f01-161">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="b6f01-161">SDK Update</span></span>
* <span data-ttu-id="b6f01-162">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="b6f01-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b6f01-163">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-164">Az.Resources</span></span>
* <span data-ttu-id="b6f01-165">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b6f01-166">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b6f01-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b6f01-167">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="b6f01-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b6f01-168">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b6f01-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b6f01-169">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="b6f01-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b6f01-170">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b6f01-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6f01-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-171">Az.Sql</span></span>
* <span data-ttu-id="b6f01-172">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="b6f01-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b6f01-173">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="b6f01-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6f01-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6f01-174">Az.Storage</span></span>
* <span data-ttu-id="b6f01-175">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6f01-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b6f01-176">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="b6f01-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b6f01-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="b6f01-178">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="b6f01-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6f01-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6f01-179">Az.Automation</span></span>
* <span data-ttu-id="b6f01-180">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b6f01-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b6f01-181">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b6f01-182">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6f01-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6f01-184">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="b6f01-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-185">Az.Compute</span></span>
* <span data-ttu-id="b6f01-186">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="b6f01-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b6f01-187">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="b6f01-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b6f01-188">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b6f01-189">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="b6f01-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6f01-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6f01-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6f01-191">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="b6f01-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b6f01-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b6f01-192">Az.EventHub</span></span>
* <span data-ttu-id="b6f01-193">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="b6f01-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="b6f01-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f01-194">Az.KeyVault</span></span>
* <span data-ttu-id="b6f01-195">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="b6f01-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b6f01-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b6f01-196">Az.LogicApp</span></span>
* <span data-ttu-id="b6f01-197">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="b6f01-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b6f01-198">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="b6f01-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b6f01-199">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="b6f01-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b6f01-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6f01-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b6f01-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6f01-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b6f01-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6f01-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b6f01-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b6f01-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b6f01-204">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="b6f01-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b6f01-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f01-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b6f01-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f01-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b6f01-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f01-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b6f01-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f01-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b6f01-209">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="b6f01-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b6f01-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6f01-210">Az.Monitor</span></span>
* <span data-ttu-id="b6f01-211">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b6f01-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6f01-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-212">Az.Network</span></span>
* <span data-ttu-id="b6f01-213">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="b6f01-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b6f01-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6f01-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="b6f01-215">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="b6f01-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b6f01-216">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="b6f01-217">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="b6f01-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="b6f01-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-218">Az.Resources</span></span>
* <span data-ttu-id="b6f01-219">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b6f01-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b6f01-220">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b6f01-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b6f01-221">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="b6f01-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b6f01-222">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="b6f01-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6f01-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-223">Az.Sql</span></span>
* <span data-ttu-id="b6f01-224">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b6f01-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b6f01-225">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="b6f01-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6f01-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6f01-226">Az.Websites</span></span>
* <span data-ttu-id="b6f01-227">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="b6f01-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b6f01-228">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="b6f01-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6f01-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6f01-229">Az.Accounts</span></span>
* <span data-ttu-id="b6f01-230">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="b6f01-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b6f01-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-231">Az.AnalysisServices</span></span>
<span data-ttu-id="b6f01-232">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="b6f01-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-233">Az.Compute</span></span>
* <span data-ttu-id="b6f01-234">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="b6f01-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b6f01-235">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="b6f01-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b6f01-236">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="b6f01-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6f01-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-237">Az.RecoveryServices</span></span>
<span data-ttu-id="b6f01-238">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="b6f01-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-239">Az.Resources</span></span>
* <span data-ttu-id="b6f01-240">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="b6f01-241">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b6f01-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b6f01-242">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="b6f01-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="b6f01-243">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b6f01-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6f01-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-244">Az.Sql</span></span>
* <span data-ttu-id="b6f01-245">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b6f01-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b6f01-246">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="b6f01-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b6f01-247">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="b6f01-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b6f01-248">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="b6f01-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6f01-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6f01-249">Az.Accounts</span></span>
* <span data-ttu-id="b6f01-250">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="b6f01-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b6f01-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="b6f01-252">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="b6f01-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b6f01-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="b6f01-254">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="b6f01-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b6f01-255">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="b6f01-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6f01-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6f01-256">Az.Accounts</span></span>
* <span data-ttu-id="b6f01-257">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b6f01-258">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6f01-259">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="b6f01-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b6f01-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b6f01-260">Az.Aks</span></span>
* <span data-ttu-id="b6f01-261">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b6f01-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6f01-262">Az.Automation</span></span>
* <span data-ttu-id="b6f01-263">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="b6f01-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b6f01-264">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b6f01-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b6f01-265">Az.Cdn</span></span>
* <span data-ttu-id="b6f01-266">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-267">Az.Compute</span></span>
* <span data-ttu-id="b6f01-268">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b6f01-269">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b6f01-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b6f01-270">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b6f01-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b6f01-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b6f01-272">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b6f01-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6f01-273">Az.DataFactory</span></span>
* <span data-ttu-id="b6f01-274">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="b6f01-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6f01-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6f01-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6f01-276">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="b6f01-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b6f01-277">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b6f01-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b6f01-278">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6f01-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6f01-279">Az.IotHub</span></span>
* <span data-ttu-id="b6f01-280">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b6f01-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b6f01-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f01-281">Az.KeyVault</span></span>
* <span data-ttu-id="b6f01-282">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6f01-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-283">Az.Network</span></span>
* <span data-ttu-id="b6f01-284">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-285">Az.Resources</span></span>
* <span data-ttu-id="b6f01-286">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="b6f01-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b6f01-287">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="b6f01-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b6f01-288">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b6f01-289">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="b6f01-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b6f01-290">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="b6f01-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b6f01-291">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b6f01-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b6f01-292">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b6f01-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6f01-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6f01-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6f01-294">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="b6f01-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b6f01-295">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-295">Fix some error messages.</span></span>
* <span data-ttu-id="b6f01-296">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="b6f01-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b6f01-297">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="b6f01-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b6f01-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b6f01-298">Az.SignalR</span></span>
* <span data-ttu-id="b6f01-299">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6f01-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-300">Az.Sql</span></span>
* <span data-ttu-id="b6f01-301">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6f01-302">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="b6f01-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b6f01-303">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="b6f01-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b6f01-304">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="b6f01-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6f01-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6f01-305">Az.Storage</span></span>
* <span data-ttu-id="b6f01-306">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6f01-307">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="b6f01-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b6f01-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b6f01-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b6f01-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b6f01-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b6f01-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b6f01-310">Az.TrafficManager</span></span>
* <span data-ttu-id="b6f01-311">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6f01-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6f01-312">Az.Websites</span></span>
* <span data-ttu-id="b6f01-313">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="b6f01-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b6f01-314">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="b6f01-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b6f01-315">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="b6f01-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b6f01-316">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="b6f01-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b6f01-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6f01-317">Az.Accounts</span></span>
* <span data-ttu-id="b6f01-318">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-319">Az.Compute</span></span>
* <span data-ttu-id="b6f01-320">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="b6f01-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b6f01-321">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="b6f01-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b6f01-322">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="b6f01-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6f01-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6f01-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6f01-324">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="b6f01-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b6f01-325">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="b6f01-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b6f01-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b6f01-326">Az.EventGrid</span></span>
* <span data-ttu-id="b6f01-327">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="b6f01-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b6f01-328">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="b6f01-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b6f01-329">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="b6f01-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b6f01-330">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="b6f01-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b6f01-331">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="b6f01-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b6f01-332">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="b6f01-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b6f01-333">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="b6f01-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b6f01-334">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="b6f01-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b6f01-335">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="b6f01-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b6f01-336">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="b6f01-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="b6f01-337">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b6f01-338">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="b6f01-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b6f01-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b6f01-339">Az.IotHub</span></span>
* <span data-ttu-id="b6f01-340">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="b6f01-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b6f01-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b6f01-341">Az.LogicApp</span></span>
* <span data-ttu-id="b6f01-342">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="b6f01-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-343">Az.Resources</span></span>
* <span data-ttu-id="b6f01-344">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="b6f01-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b6f01-345">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b6f01-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b6f01-346">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="b6f01-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b6f01-347">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="b6f01-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b6f01-348">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b6f01-349">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b6f01-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b6f01-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b6f01-350">Az.SignalR</span></span>
* <span data-ttu-id="b6f01-351">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="b6f01-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6f01-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-352">Az.Sql</span></span>
* <span data-ttu-id="b6f01-353">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="b6f01-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b6f01-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6f01-354">Az.Storage</span></span>
* <span data-ttu-id="b6f01-355">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="b6f01-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b6f01-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6f01-356">New-AzStorageContext</span></span>
* <span data-ttu-id="b6f01-357">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="b6f01-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b6f01-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b6f01-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6f01-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6f01-359">Az.Websites</span></span>
* <span data-ttu-id="b6f01-360">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b6f01-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b6f01-361">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="b6f01-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b6f01-362">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="b6f01-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b6f01-363">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b6f01-363">General</span></span>

- <span data-ttu-id="b6f01-364">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="b6f01-364">General Availability of Az Module</span></span>
- <span data-ttu-id="b6f01-365">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-365">Online help for each module</span></span>
- <span data-ttu-id="b6f01-366">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="b6f01-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b6f01-367">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b6f01-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6f01-368">Az.Accounts</span></span>
- <span data-ttu-id="b6f01-369">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="b6f01-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="b6f01-370">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b6f01-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6f01-371">Az.ApiManagement</span></span>
- <span data-ttu-id="b6f01-372">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="b6f01-372">Fixes for #7002</span></span>
- <span data-ttu-id="b6f01-373">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b6f01-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b6f01-374">Az.Batch</span></span>
- <span data-ttu-id="b6f01-375">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="b6f01-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b6f01-376">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="b6f01-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b6f01-377">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b6f01-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b6f01-378">Az.Billing</span></span>
- <span data-ttu-id="b6f01-379">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="b6f01-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b6f01-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-380">Az.CognitivServices</span></span>
- <span data-ttu-id="b6f01-381">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="b6f01-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b6f01-382">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="b6f01-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b6f01-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b6f01-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="b6f01-384">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="b6f01-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b6f01-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b6f01-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b6f01-386">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b6f01-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6f01-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="b6f01-388">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b6f01-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b6f01-389">Az.Monitor</span></span>
- <span data-ttu-id="b6f01-390">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b6f01-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f01-391">Az.KeyVault</span></span>
- <span data-ttu-id="b6f01-392">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b6f01-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b6f01-393">Az.MachineLearning</span></span>
- <span data-ttu-id="b6f01-394">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="b6f01-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b6f01-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b6f01-395">Az.Media</span></span>
- <span data-ttu-id="b6f01-396">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="b6f01-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b6f01-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-397">Az.Network</span></span>
<span data-ttu-id="b6f01-398">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="b6f01-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b6f01-399">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b6f01-399">New cmdlets added:</span></span>
        - <span data-ttu-id="b6f01-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f01-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6f01-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f01-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6f01-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f01-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6f01-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f01-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6f01-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6f01-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b6f01-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b6f01-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b6f01-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b6f01-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b6f01-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f01-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b6f01-408">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b6f01-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b6f01-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6f01-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b6f01-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6f01-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b6f01-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6f01-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b6f01-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6f01-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b6f01-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b6f01-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b6f01-414">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="b6f01-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b6f01-415">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b6f01-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b6f01-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6f01-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b6f01-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6f01-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b6f01-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6f01-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b6f01-419">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b6f01-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b6f01-420">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b6f01-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b6f01-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="b6f01-422">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b6f01-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b6f01-423">Az.Profile</span></span>
- <span data-ttu-id="b6f01-424">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b6f01-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b6f01-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="b6f01-426">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b6f01-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-427">Az.Resources</span></span>
- <span data-ttu-id="b6f01-428">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b6f01-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6f01-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="b6f01-430">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="b6f01-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b6f01-431">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b6f01-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b6f01-432">Az.SIgnalR</span></span>
- <span data-ttu-id="b6f01-433">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="b6f01-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b6f01-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-434">Az.Sql</span></span>
- <span data-ttu-id="b6f01-435">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b6f01-436">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="b6f01-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b6f01-437">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b6f01-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6f01-438">Az.Storage</span></span>
- <span data-ttu-id="b6f01-439">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b6f01-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6f01-440">Az.Websites</span></span>
- <span data-ttu-id="b6f01-441">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="b6f01-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b6f01-442">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="b6f01-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b6f01-443">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b6f01-443">General</span></span>

* <span data-ttu-id="b6f01-444">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="b6f01-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b6f01-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-445">Az.Compute</span></span>

* <span data-ttu-id="b6f01-446">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="b6f01-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b6f01-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6f01-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="b6f01-448">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="b6f01-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b6f01-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b6f01-449">Az.FrontDoor</span></span>

* <span data-ttu-id="b6f01-450">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="b6f01-450">Fixed some broken links</span></span>
    - <span data-ttu-id="b6f01-451">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="b6f01-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b6f01-452">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="b6f01-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b6f01-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="b6f01-454">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="b6f01-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b6f01-455">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="b6f01-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b6f01-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-456">Az.Resources</span></span>

* <span data-ttu-id="b6f01-457">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="b6f01-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b6f01-458">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="b6f01-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b6f01-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-459">Az.Sql</span></span>

* <span data-ttu-id="b6f01-460">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="b6f01-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b6f01-461">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="b6f01-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b6f01-462">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="b6f01-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b6f01-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b6f01-463">Az.Storage</span></span>

* <span data-ttu-id="b6f01-464">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b6f01-465">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="b6f01-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b6f01-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b6f01-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b6f01-467">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="b6f01-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="b6f01-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b6f01-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b6f01-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b6f01-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b6f01-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6f01-470">Az.Websites</span></span>

* <span data-ttu-id="b6f01-471">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b6f01-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b6f01-472">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="b6f01-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b6f01-473">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b6f01-474">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="b6f01-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b6f01-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b6f01-475">Az.ApiManagement</span></span>
* <span data-ttu-id="b6f01-476">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b6f01-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b6f01-477">Az.Automation</span></span>
* <span data-ttu-id="b6f01-478">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="b6f01-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b6f01-479">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b6f01-480">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b6f01-481">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="b6f01-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b6f01-482">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="b6f01-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b6f01-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-483">Az.Compute</span></span>
* <span data-ttu-id="b6f01-484">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="b6f01-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b6f01-485">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b6f01-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b6f01-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="b6f01-487">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b6f01-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b6f01-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b6f01-489">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="b6f01-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b6f01-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-490">Az.Network</span></span>
* <span data-ttu-id="b6f01-491">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="b6f01-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b6f01-492">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="b6f01-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b6f01-493">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="b6f01-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b6f01-494">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="b6f01-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b6f01-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b6f01-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b6f01-496">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="b6f01-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b6f01-497">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="b6f01-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b6f01-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b6f01-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b6f01-499">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="b6f01-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b6f01-500">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b6f01-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b6f01-501">Az.Relay</span></span>
* <span data-ttu-id="b6f01-502">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="b6f01-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b6f01-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-503">Az.Resources</span></span>
* <span data-ttu-id="b6f01-504">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="b6f01-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b6f01-505">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="b6f01-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b6f01-506">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="b6f01-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b6f01-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6f01-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6f01-508">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b6f01-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b6f01-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-509">Az.Sql</span></span>
* <span data-ttu-id="b6f01-510">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="b6f01-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b6f01-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6f01-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6f01-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6f01-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6f01-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6f01-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6f01-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b6f01-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b6f01-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6f01-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b6f01-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6f01-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b6f01-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6f01-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b6f01-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6f01-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b6f01-519">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="b6f01-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b6f01-520">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="b6f01-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b6f01-521">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="b6f01-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b6f01-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6f01-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b6f01-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6f01-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b6f01-524">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6f01-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b6f01-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b6f01-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b6f01-526">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="b6f01-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b6f01-527">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="b6f01-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b6f01-528">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b6f01-528">General</span></span>
* <span data-ttu-id="b6f01-529">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="b6f01-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b6f01-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b6f01-530">Az.Profile</span></span>
* <span data-ttu-id="b6f01-531">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b6f01-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b6f01-532">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="b6f01-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b6f01-533">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="b6f01-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b6f01-534">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="b6f01-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b6f01-535">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="b6f01-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b6f01-536">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="b6f01-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b6f01-537">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="b6f01-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b6f01-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6f01-539">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="b6f01-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-540">Az.Compute</span></span>
* <span data-ttu-id="b6f01-541">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="b6f01-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b6f01-542">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="b6f01-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b6f01-543">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6f01-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6f01-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6f01-545">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="b6f01-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b6f01-546">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="b6f01-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b6f01-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b6f01-547">Az.Insights</span></span>
* <span data-ttu-id="b6f01-548">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="b6f01-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b6f01-549">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="b6f01-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b6f01-550">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="b6f01-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b6f01-551">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="b6f01-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6f01-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-552">Az.Network</span></span>
* <span data-ttu-id="b6f01-553">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="b6f01-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b6f01-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6f01-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b6f01-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b6f01-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b6f01-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b6f01-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b6f01-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b6f01-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b6f01-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6f01-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b6f01-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b6f01-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b6f01-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b6f01-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="b6f01-561">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b6f01-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-562">Az.Resources</span></span>
* <span data-ttu-id="b6f01-563">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="b6f01-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b6f01-564">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="b6f01-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b6f01-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b6f01-565">Az.ServiceBus</span></span>
* <span data-ttu-id="b6f01-566">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="b6f01-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b6f01-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b6f01-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="b6f01-568">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="b6f01-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b6f01-569">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="b6f01-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b6f01-570">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b6f01-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b6f01-571">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b6f01-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b6f01-572">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="b6f01-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b6f01-573">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="b6f01-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b6f01-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b6f01-574">Az.Profile</span></span>
* <span data-ttu-id="b6f01-575">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="b6f01-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b6f01-576">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b6f01-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-577">Az.Compute</span></span>
* <span data-ttu-id="b6f01-578">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="b6f01-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b6f01-579">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b6f01-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b6f01-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="b6f01-581">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="b6f01-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b6f01-582">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="b6f01-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b6f01-583">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b6f01-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b6f01-584">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="b6f01-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b6f01-585">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="b6f01-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6f01-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-586">Az.Network</span></span>
* <span data-ttu-id="b6f01-587">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="b6f01-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b6f01-588">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b6f01-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-589">Az.Resources</span></span>
* <span data-ttu-id="b6f01-590">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="b6f01-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b6f01-591">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="b6f01-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b6f01-592">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="b6f01-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b6f01-593">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b6f01-593">Azure.Storage</span></span>
* <span data-ttu-id="b6f01-594">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="b6f01-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b6f01-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b6f01-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b6f01-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b6f01-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b6f01-597">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="b6f01-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b6f01-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b6f01-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b6f01-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b6f01-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="b6f01-600">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="b6f01-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b6f01-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b6f01-601">Az.Compute</span></span>
* <span data-ttu-id="b6f01-602">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="b6f01-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b6f01-603">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="b6f01-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b6f01-604">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="b6f01-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b6f01-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b6f01-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b6f01-606">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="b6f01-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b6f01-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b6f01-607">Az.Network</span></span>
* <span data-ttu-id="b6f01-608">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="b6f01-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b6f01-609">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b6f01-609">new cmdlets added</span></span>
    - <span data-ttu-id="b6f01-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6f01-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6f01-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6f01-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6f01-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6f01-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6f01-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b6f01-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b6f01-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b6f01-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b6f01-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6f01-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b6f01-616">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="b6f01-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b6f01-617">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="b6f01-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b6f01-618">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="b6f01-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b6f01-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b6f01-619">Az.RedisCache</span></span>
* <span data-ttu-id="b6f01-620">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="b6f01-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b6f01-621">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b6f01-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b6f01-622">Az.Resources</span></span>
* <span data-ttu-id="b6f01-623">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b6f01-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b6f01-624">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="b6f01-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b6f01-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b6f01-625">Az.Sql</span></span>
* <span data-ttu-id="b6f01-626">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="b6f01-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b6f01-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b6f01-627">Az.Websites</span></span>
* <span data-ttu-id="b6f01-628">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="b6f01-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b6f01-629">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="b6f01-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b6f01-630">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="b6f01-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b6f01-631">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="b6f01-631">Initial Release</span></span>