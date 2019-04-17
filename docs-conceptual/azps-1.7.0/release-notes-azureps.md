---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364134"
---
## <a name="170---april-2019"></a><span data-ttu-id="fec36-101">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="fec36-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fec36-102">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="fec36-102">Highlights since the last major release</span></span>
* <span data-ttu-id="fec36-103">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="fec36-103">General availability of `Az` module</span></span>
* <span data-ttu-id="fec36-104">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fec36-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fec36-105">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fec36-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fec36-106">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fec36-107">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fec36-108">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fec36-109">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fec36-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-110">Az.Accounts</span></span>
* <span data-ttu-id="fec36-111">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="fec36-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fec36-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fec36-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="fec36-113">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fec36-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="fec36-114">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="fec36-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fec36-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fec36-115">Az.Automation</span></span>
* <span data-ttu-id="fec36-116">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="fec36-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="fec36-117">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="fec36-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="fec36-118">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-119">Az.Compute</span></span>
* <span data-ttu-id="fec36-120">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fec36-121">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="fec36-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="fec36-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fec36-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="fec36-123">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="fec36-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fec36-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fec36-124">Az.DataFactory</span></span>
* <span data-ttu-id="fec36-125">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="fec36-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="fec36-126">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="fec36-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-127">Az.Resources</span></span>
* <span data-ttu-id="fec36-128">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="fec36-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="fec36-129">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="fec36-130">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="fec36-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="fec36-131">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fec36-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="fec36-132">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="fec36-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="fec36-133">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fec36-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-134">Az.Sql</span></span>
* <span data-ttu-id="fec36-135">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="fec36-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fec36-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-136">Az.Storage</span></span>
* <span data-ttu-id="fec36-137">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="fec36-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="fec36-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fec36-138">New-AzStorageContext</span></span>
* <span data-ttu-id="fec36-139">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="fec36-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="fec36-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fec36-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fec36-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fec36-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fec36-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fec36-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="fec36-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fec36-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="fec36-144">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="fec36-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="fec36-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fec36-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fec36-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fec36-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fec36-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fec36-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="fec36-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fec36-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="fec36-149">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="fec36-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fec36-150">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="fec36-150">Highlights since the last major release</span></span>
* <span data-ttu-id="fec36-151">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="fec36-151">General availability of `Az` module</span></span>
* <span data-ttu-id="fec36-152">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fec36-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fec36-153">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fec36-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fec36-154">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fec36-155">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fec36-156">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fec36-157">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fec36-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fec36-158">Az.Automation</span></span>
* <span data-ttu-id="fec36-159">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="fec36-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="fec36-160">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="fec36-160">Dynamic grouping</span></span>
    * <span data-ttu-id="fec36-161">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="fec36-161">Pre-Post script</span></span>
    * <span data-ttu-id="fec36-162">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="fec36-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-163">Az.Compute</span></span>
* <span data-ttu-id="fec36-164">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="fec36-165">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="fec36-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fec36-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fec36-166">Az.KeyVault</span></span>
* <span data-ttu-id="fec36-167">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fec36-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-168">Az.Network</span></span>
* <span data-ttu-id="fec36-169">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="fec36-170">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fec36-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fec36-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fec36-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="fec36-172">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="fec36-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="fec36-173">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-174">Az.Resources</span></span>
* <span data-ttu-id="fec36-175">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="fec36-176">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="fec36-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-177">Az.Sql</span></span>
* <span data-ttu-id="fec36-178">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="fec36-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fec36-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-179">Az.Storage</span></span>
* <span data-ttu-id="fec36-180">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="fec36-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="fec36-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fec36-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fec36-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fec36-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fec36-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fec36-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fec36-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="fec36-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="fec36-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="fec36-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="fec36-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="fec36-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fec36-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fec36-187">Az.Websites</span></span>
* <span data-ttu-id="fec36-188">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="fec36-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="fec36-189">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="fec36-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fec36-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-190">Az.Accounts</span></span>
* <span data-ttu-id="fec36-191">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="fec36-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="fec36-192">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="fec36-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fec36-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fec36-193">Az.Automation</span></span>
* <span data-ttu-id="fec36-194">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="fec36-195">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="fec36-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="fec36-196">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="fec36-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fec36-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fec36-197">Az.Cdn</span></span>
* <span data-ttu-id="fec36-198">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="fec36-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-199">Az.Compute</span></span>
* <span data-ttu-id="fec36-200">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fec36-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fec36-201">Az.DataFactory</span></span>
* <span data-ttu-id="fec36-202">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="fec36-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fec36-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fec36-203">Az.LogicApp</span></span>
* <span data-ttu-id="fec36-204">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="fec36-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fec36-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-205">Az.Network</span></span>
* <span data-ttu-id="fec36-206">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fec36-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fec36-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="fec36-208">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fec36-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="fec36-209">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="fec36-209">SDK Update</span></span>
* <span data-ttu-id="fec36-210">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="fec36-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="fec36-211">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fec36-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-212">Az.Resources</span></span>
* <span data-ttu-id="fec36-213">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="fec36-214">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="fec36-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="fec36-215">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a `Get-AzResource` eredménye át lett irányítva a következőbe:</span><span class="sxs-lookup"><span data-stu-id="fec36-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="fec36-216">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="fec36-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="fec36-217">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a következő futtatásakor jelentkezett:</span><span class="sxs-lookup"><span data-stu-id="fec36-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="fec36-218">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="fec36-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-219">Az.Sql</span></span>
* <span data-ttu-id="fec36-220">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="fec36-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="fec36-221">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="fec36-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fec36-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-222">Az.Storage</span></span>
* <span data-ttu-id="fec36-223">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fec36-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="fec36-224">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="fec36-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="fec36-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fec36-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="fec36-226">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="fec36-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fec36-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fec36-227">Az.Automation</span></span>
* <span data-ttu-id="fec36-228">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="fec36-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="fec36-229">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fec36-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="fec36-230">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fec36-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fec36-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="fec36-232">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="fec36-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-233">Az.Compute</span></span>
* <span data-ttu-id="fec36-234">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="fec36-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="fec36-235">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="fec36-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="fec36-236">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fec36-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="fec36-237">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="fec36-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fec36-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fec36-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="fec36-239">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="fec36-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fec36-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fec36-240">Az.EventHub</span></span>
* <span data-ttu-id="fec36-241">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="fec36-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="fec36-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fec36-242">Az.KeyVault</span></span>
* <span data-ttu-id="fec36-243">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="fec36-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fec36-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fec36-244">Az.LogicApp</span></span>
* <span data-ttu-id="fec36-245">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="fec36-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="fec36-246">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="fec36-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="fec36-247">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="fec36-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="fec36-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fec36-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fec36-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fec36-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fec36-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fec36-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fec36-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fec36-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="fec36-252">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="fec36-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="fec36-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fec36-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fec36-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fec36-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fec36-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fec36-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fec36-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fec36-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="fec36-257">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="fec36-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fec36-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fec36-258">Az.Monitor</span></span>
* <span data-ttu-id="fec36-259">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="fec36-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fec36-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-260">Az.Network</span></span>
* <span data-ttu-id="fec36-261">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="fec36-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fec36-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fec36-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="fec36-263">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="fec36-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="fec36-264">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fec36-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="fec36-265">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="fec36-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="fec36-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-266">Az.Resources</span></span>
* <span data-ttu-id="fec36-267">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fec36-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fec36-268">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fec36-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="fec36-269">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="fec36-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="fec36-270">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="fec36-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-271">Az.Sql</span></span>
* <span data-ttu-id="fec36-272">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fec36-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="fec36-273">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="fec36-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fec36-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fec36-274">Az.Websites</span></span>
* <span data-ttu-id="fec36-275">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="fec36-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="fec36-276">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="fec36-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fec36-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-277">Az.Accounts</span></span>
* <span data-ttu-id="fec36-278">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="fec36-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fec36-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fec36-279">Az.AnalysisServices</span></span>
<span data-ttu-id="fec36-280">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="fec36-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-281">Az.Compute</span></span>
* <span data-ttu-id="fec36-282">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="fec36-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="fec36-283">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="fec36-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="fec36-284">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="fec36-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fec36-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fec36-285">Az.RecoveryServices</span></span>
<span data-ttu-id="fec36-286">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="fec36-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-287">Az.Resources</span></span>
* <span data-ttu-id="fec36-288">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="fec36-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="fec36-289">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fec36-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fec36-290">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="fec36-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="fec36-291">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fec36-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-292">Az.Sql</span></span>
* <span data-ttu-id="fec36-293">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fec36-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="fec36-294">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="fec36-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="fec36-295">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="fec36-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="fec36-296">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="fec36-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fec36-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-297">Az.Accounts</span></span>
* <span data-ttu-id="fec36-298">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="fec36-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fec36-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fec36-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="fec36-300">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="fec36-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fec36-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fec36-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="fec36-302">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="fec36-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="fec36-303">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="fec36-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fec36-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-304">Az.Accounts</span></span>
* <span data-ttu-id="fec36-305">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fec36-306">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fec36-307">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="fec36-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="fec36-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fec36-308">Az.Aks</span></span>
* <span data-ttu-id="fec36-309">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fec36-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fec36-310">Az.Automation</span></span>
* <span data-ttu-id="fec36-311">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="fec36-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="fec36-312">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fec36-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fec36-313">Az.Cdn</span></span>
* <span data-ttu-id="fec36-314">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-315">Az.Compute</span></span>
* <span data-ttu-id="fec36-316">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="fec36-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="fec36-317">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fec36-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="fec36-318">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="fec36-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="fec36-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fec36-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="fec36-320">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fec36-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fec36-321">Az.DataFactory</span></span>
* <span data-ttu-id="fec36-322">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="fec36-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fec36-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fec36-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="fec36-324">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="fec36-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="fec36-325">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="fec36-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="fec36-326">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fec36-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fec36-327">Az.IotHub</span></span>
* <span data-ttu-id="fec36-328">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fec36-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fec36-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fec36-329">Az.KeyVault</span></span>
* <span data-ttu-id="fec36-330">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fec36-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-331">Az.Network</span></span>
* <span data-ttu-id="fec36-332">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-333">Az.Resources</span></span>
* <span data-ttu-id="fec36-334">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="fec36-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="fec36-335">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="fec36-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="fec36-336">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="fec36-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="fec36-337">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="fec36-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="fec36-338">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="fec36-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="fec36-339">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="fec36-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="fec36-340">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="fec36-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fec36-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fec36-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="fec36-342">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="fec36-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="fec36-343">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="fec36-343">Fix some error messages.</span></span>
* <span data-ttu-id="fec36-344">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="fec36-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="fec36-345">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="fec36-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fec36-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fec36-346">Az.SignalR</span></span>
* <span data-ttu-id="fec36-347">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-348">Az.Sql</span></span>
* <span data-ttu-id="fec36-349">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fec36-350">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="fec36-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="fec36-351">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="fec36-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="fec36-352">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="fec36-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fec36-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-353">Az.Storage</span></span>
* <span data-ttu-id="fec36-354">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fec36-355">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="fec36-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="fec36-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="fec36-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="fec36-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fec36-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="fec36-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fec36-358">Az.TrafficManager</span></span>
* <span data-ttu-id="fec36-359">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fec36-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fec36-360">Az.Websites</span></span>
* <span data-ttu-id="fec36-361">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fec36-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fec36-362">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="fec36-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="fec36-363">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="fec36-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="fec36-364">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="fec36-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fec36-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-365">Az.Accounts</span></span>
* <span data-ttu-id="fec36-366">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="fec36-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-367">Az.Compute</span></span>
* <span data-ttu-id="fec36-368">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="fec36-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="fec36-369">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="fec36-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="fec36-370">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="fec36-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fec36-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fec36-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="fec36-372">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="fec36-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="fec36-373">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="fec36-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fec36-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fec36-374">Az.EventGrid</span></span>
* <span data-ttu-id="fec36-375">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="fec36-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="fec36-376">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="fec36-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="fec36-377">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="fec36-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fec36-378">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="fec36-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fec36-379">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="fec36-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fec36-380">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="fec36-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="fec36-381">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="fec36-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fec36-382">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="fec36-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fec36-383">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="fec36-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fec36-384">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="fec36-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="fec36-385">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="fec36-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="fec36-386">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="fec36-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fec36-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fec36-387">Az.IotHub</span></span>
* <span data-ttu-id="fec36-388">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="fec36-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fec36-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fec36-389">Az.LogicApp</span></span>
* <span data-ttu-id="fec36-390">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="fec36-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-391">Az.Resources</span></span>
* <span data-ttu-id="fec36-392">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="fec36-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="fec36-393">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="fec36-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="fec36-394">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="fec36-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fec36-395">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fec36-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="fec36-396">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="fec36-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="fec36-397">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="fec36-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fec36-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fec36-398">Az.SignalR</span></span>
* <span data-ttu-id="fec36-399">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="fec36-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-400">Az.Sql</span></span>
* <span data-ttu-id="fec36-401">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="fec36-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fec36-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-402">Az.Storage</span></span>
* <span data-ttu-id="fec36-403">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="fec36-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="fec36-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fec36-404">New-AzStorageContext</span></span>
* <span data-ttu-id="fec36-405">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="fec36-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="fec36-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fec36-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fec36-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fec36-407">Az.Websites</span></span>
* <span data-ttu-id="fec36-408">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fec36-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="fec36-409">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="fec36-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="fec36-410">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="fec36-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="fec36-411">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fec36-411">General</span></span>

- <span data-ttu-id="fec36-412">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="fec36-412">General Availability of Az Module</span></span>
- <span data-ttu-id="fec36-413">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-413">Online help for each module</span></span>
- <span data-ttu-id="fec36-414">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="fec36-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="fec36-415">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="fec36-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-416">Az.Accounts</span></span>
- <span data-ttu-id="fec36-417">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="fec36-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="fec36-418">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fec36-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fec36-419">Az.ApiManagement</span></span>
- <span data-ttu-id="fec36-420">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="fec36-420">Fixes for #7002</span></span>
- <span data-ttu-id="fec36-421">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="fec36-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fec36-422">Az.Batch</span></span>
- <span data-ttu-id="fec36-423">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="fec36-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="fec36-424">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="fec36-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="fec36-425">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="fec36-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="fec36-426">Az.Billing</span></span>
- <span data-ttu-id="fec36-427">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="fec36-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="fec36-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="fec36-428">Az.CognitivServices</span></span>
- <span data-ttu-id="fec36-429">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="fec36-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="fec36-430">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="fec36-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fec36-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fec36-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="fec36-432">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="fec36-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="fec36-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fec36-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="fec36-434">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fec36-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fec36-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="fec36-436">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="fec36-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fec36-437">Az.Monitor</span></span>
- <span data-ttu-id="fec36-438">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="fec36-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fec36-439">Az.KeyVault</span></span>
- <span data-ttu-id="fec36-440">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fec36-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="fec36-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fec36-441">Az.MachineLearning</span></span>
- <span data-ttu-id="fec36-442">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="fec36-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="fec36-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fec36-443">Az.Media</span></span>
- <span data-ttu-id="fec36-444">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="fec36-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fec36-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-445">Az.Network</span></span>
<span data-ttu-id="fec36-446">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="fec36-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="fec36-447">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fec36-447">New cmdlets added:</span></span>
        - <span data-ttu-id="fec36-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fec36-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fec36-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fec36-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fec36-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fec36-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fec36-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fec36-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fec36-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fec36-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fec36-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fec36-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="fec36-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fec36-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="fec36-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="fec36-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="fec36-456">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fec36-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="fec36-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fec36-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="fec36-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fec36-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fec36-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fec36-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fec36-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fec36-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="fec36-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fec36-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="fec36-462">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="fec36-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="fec36-463">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fec36-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="fec36-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fec36-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fec36-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fec36-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fec36-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fec36-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="fec36-467">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="fec36-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="fec36-468">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="fec36-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fec36-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="fec36-470">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="fec36-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fec36-471">Az.Profile</span></span>
- <span data-ttu-id="fec36-472">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fec36-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fec36-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fec36-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="fec36-474">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="fec36-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-475">Az.Resources</span></span>
- <span data-ttu-id="fec36-476">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fec36-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fec36-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="fec36-478">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="fec36-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="fec36-479">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="fec36-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="fec36-480">Az.SIgnalR</span></span>
- <span data-ttu-id="fec36-481">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="fec36-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="fec36-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-482">Az.Sql</span></span>
- <span data-ttu-id="fec36-483">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="fec36-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="fec36-484">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="fec36-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="fec36-485">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="fec36-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-486">Az.Storage</span></span>
- <span data-ttu-id="fec36-487">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fec36-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fec36-488">Az.Websites</span></span>
- <span data-ttu-id="fec36-489">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fec36-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="fec36-490">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="fec36-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="fec36-491">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fec36-491">General</span></span>

* <span data-ttu-id="fec36-492">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="fec36-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="fec36-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-493">Az.Compute</span></span>

* <span data-ttu-id="fec36-494">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="fec36-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fec36-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fec36-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="fec36-496">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="fec36-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="fec36-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fec36-497">Az.FrontDoor</span></span>

* <span data-ttu-id="fec36-498">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="fec36-498">Fixed some broken links</span></span>
    - <span data-ttu-id="fec36-499">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="fec36-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="fec36-500">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="fec36-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fec36-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fec36-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="fec36-502">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="fec36-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="fec36-503">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="fec36-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="fec36-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-504">Az.Resources</span></span>

* <span data-ttu-id="fec36-505">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="fec36-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="fec36-506">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="fec36-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="fec36-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-507">Az.Sql</span></span>

* <span data-ttu-id="fec36-508">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="fec36-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="fec36-509">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="fec36-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="fec36-510">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="fec36-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="fec36-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-511">Az.Storage</span></span>

* <span data-ttu-id="fec36-512">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fec36-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="fec36-513">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="fec36-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="fec36-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fec36-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fec36-515">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="fec36-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="fec36-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fec36-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="fec36-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fec36-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fec36-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fec36-518">Az.Websites</span></span>

* <span data-ttu-id="fec36-519">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fec36-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="fec36-520">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="fec36-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="fec36-521">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="fec36-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="fec36-522">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="fec36-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fec36-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fec36-523">Az.ApiManagement</span></span>
* <span data-ttu-id="fec36-524">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fec36-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="fec36-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fec36-525">Az.Automation</span></span>
* <span data-ttu-id="fec36-526">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="fec36-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="fec36-527">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fec36-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="fec36-528">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fec36-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="fec36-529">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="fec36-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="fec36-530">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="fec36-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="fec36-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-531">Az.Compute</span></span>
* <span data-ttu-id="fec36-532">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="fec36-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="fec36-533">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fec36-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fec36-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fec36-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="fec36-535">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fec36-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="fec36-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fec36-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fec36-537">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="fec36-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fec36-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-538">Az.Network</span></span>
* <span data-ttu-id="fec36-539">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="fec36-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="fec36-540">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="fec36-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="fec36-541">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="fec36-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="fec36-542">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="fec36-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="fec36-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fec36-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fec36-544">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="fec36-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="fec36-545">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="fec36-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="fec36-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fec36-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fec36-547">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="fec36-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="fec36-548">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fec36-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="fec36-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fec36-549">Az.Relay</span></span>
* <span data-ttu-id="fec36-550">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="fec36-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="fec36-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-551">Az.Resources</span></span>
* <span data-ttu-id="fec36-552">Frissült a következők erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja: `New-AzureRmPolicyAssignment` és</span><span class="sxs-lookup"><span data-stu-id="fec36-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="fec36-553">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="fec36-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="fec36-554">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="fec36-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fec36-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fec36-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="fec36-556">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="fec36-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="fec36-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-557">Az.Sql</span></span>
* <span data-ttu-id="fec36-558">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="fec36-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="fec36-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fec36-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fec36-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fec36-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fec36-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fec36-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fec36-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fec36-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fec36-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fec36-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fec36-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fec36-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fec36-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fec36-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fec36-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fec36-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="fec36-567">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="fec36-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="fec36-568">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="fec36-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="fec36-569">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="fec36-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="fec36-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fec36-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fec36-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fec36-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fec36-572">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fec36-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="fec36-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fec36-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="fec36-574">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="fec36-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="fec36-575">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="fec36-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fec36-576">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fec36-576">General</span></span>
* <span data-ttu-id="fec36-577">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="fec36-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="fec36-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fec36-578">Az.Profile</span></span>
* <span data-ttu-id="fec36-579">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="fec36-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="fec36-580">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="fec36-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="fec36-581">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="fec36-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="fec36-582">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="fec36-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="fec36-583">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="fec36-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="fec36-584">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="fec36-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="fec36-585">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="fec36-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="fec36-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fec36-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="fec36-587">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="fec36-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-588">Az.Compute</span></span>
* <span data-ttu-id="fec36-589">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="fec36-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="fec36-590">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="fec36-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="fec36-591">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="fec36-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fec36-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fec36-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="fec36-593">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="fec36-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="fec36-594">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="fec36-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="fec36-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="fec36-595">Az.Insights</span></span>
* <span data-ttu-id="fec36-596">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="fec36-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="fec36-597">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="fec36-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="fec36-598">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="fec36-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="fec36-599">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="fec36-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fec36-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-600">Az.Network</span></span>
* <span data-ttu-id="fec36-601">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="fec36-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="fec36-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fec36-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="fec36-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fec36-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="fec36-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fec36-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="fec36-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="fec36-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fec36-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fec36-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fec36-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fec36-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fec36-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fec36-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="fec36-609">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fec36-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-610">Az.Resources</span></span>
* <span data-ttu-id="fec36-611">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="fec36-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="fec36-612">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="fec36-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fec36-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fec36-613">Az.ServiceBus</span></span>
* <span data-ttu-id="fec36-614">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="fec36-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fec36-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fec36-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="fec36-616">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="fec36-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="fec36-617">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="fec36-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="fec36-618">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="fec36-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="fec36-619">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="fec36-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="fec36-620">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="fec36-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="fec36-621">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="fec36-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="fec36-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fec36-622">Az.Profile</span></span>
* <span data-ttu-id="fec36-623">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="fec36-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="fec36-624">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="fec36-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-625">Az.Compute</span></span>
* <span data-ttu-id="fec36-626">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="fec36-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="fec36-627">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="fec36-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fec36-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fec36-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="fec36-629">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="fec36-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="fec36-630">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="fec36-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="fec36-631">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="fec36-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fec36-632">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="fec36-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fec36-633">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="fec36-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fec36-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-634">Az.Network</span></span>
* <span data-ttu-id="fec36-635">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="fec36-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="fec36-636">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="fec36-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-637">Az.Resources</span></span>
* <span data-ttu-id="fec36-638">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="fec36-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="fec36-639">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="fec36-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="fec36-640">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="fec36-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="fec36-641">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fec36-641">Azure.Storage</span></span>
* <span data-ttu-id="fec36-642">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="fec36-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="fec36-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fec36-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="fec36-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fec36-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fec36-645">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="fec36-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="fec36-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="fec36-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="fec36-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fec36-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="fec36-648">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="fec36-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fec36-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fec36-649">Az.Compute</span></span>
* <span data-ttu-id="fec36-650">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="fec36-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="fec36-651">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="fec36-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="fec36-652">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="fec36-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="fec36-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fec36-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="fec36-654">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="fec36-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fec36-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fec36-655">Az.Network</span></span>
* <span data-ttu-id="fec36-656">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="fec36-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="fec36-657">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fec36-657">new cmdlets added</span></span>
    - <span data-ttu-id="fec36-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fec36-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="fec36-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fec36-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="fec36-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fec36-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="fec36-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fec36-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="fec36-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fec36-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="fec36-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fec36-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="fec36-664">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="fec36-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="fec36-665">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="fec36-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="fec36-666">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="fec36-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fec36-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fec36-667">Az.RedisCache</span></span>
* <span data-ttu-id="fec36-668">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="fec36-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="fec36-669">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="fec36-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="fec36-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fec36-670">Az.Resources</span></span>
* <span data-ttu-id="fec36-671">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fec36-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fec36-672">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="fec36-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="fec36-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fec36-673">Az.Sql</span></span>
* <span data-ttu-id="fec36-674">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="fec36-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fec36-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fec36-675">Az.Websites</span></span>
* <span data-ttu-id="fec36-676">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="fec36-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="fec36-677">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="fec36-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="fec36-678">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="fec36-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="fec36-679">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="fec36-679">Initial Release</span></span>