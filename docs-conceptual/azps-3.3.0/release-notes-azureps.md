---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: fb934ed0f8bef5e2aff715debe5d406d54abf24f
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/07/2020
ms.locfileid: "75718984"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="bf015-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="bf015-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="bf015-104">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="bf015-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-105">Az.Accounts</span></span>
* <span data-ttu-id="bf015-106">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="bf015-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf015-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf015-107">Az.Cdn</span></span>
* <span data-ttu-id="bf015-108">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-108">Display error response deatil in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-109">Az.Compute</span></span>
* <span data-ttu-id="bf015-110">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="bf015-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="bf015-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="bf015-112">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="bf015-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="bf015-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="bf015-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="bf015-114">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bf015-115">Az Edge tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="bf015-115">Get the Edge Stroage Container</span></span>
* <span data-ttu-id="bf015-116">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bf015-117">Új Edge tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf015-117">Create new Edge Stroage Container</span></span>
* <span data-ttu-id="bf015-118">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bf015-119">Az Edge tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-119">Remove the Edge Stroage Container</span></span>
* <span data-ttu-id="bf015-120">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bf015-121">Meghívási művelet az Edge tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-121">Invoke action to refresh data on Edge Stroage Container</span></span>
* <span data-ttu-id="bf015-122">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="bf015-123">Az Edge tárfiók lekérése</span><span class="sxs-lookup"><span data-stu-id="bf015-123">Get the Edge Stroage Account</span></span>
* <span data-ttu-id="bf015-124">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="bf015-125">Új Edge tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf015-125">Create new Edge Stroage Account</span></span>
* <span data-ttu-id="bf015-126">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="bf015-127">Az Edge tárfiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-127">Remove the Edge Stroage Account</span></span>
* <span data-ttu-id="bf015-128">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="bf015-129">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="bf015-130">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="bf015-131">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="bf015-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-132">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-133">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="bf015-134">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="bf015-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="bf015-135">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="bf015-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="bf015-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="bf015-137">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="bf015-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf015-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf015-138">Az.EventHub</span></span>
* <span data-ttu-id="bf015-139">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bf015-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bf015-140">Az.HDInsight</span></span>
* <span data-ttu-id="bf015-141">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="bf015-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="bf015-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bf015-142">Az.MachineLearning</span></span>
* <span data-ttu-id="bf015-143">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="bf015-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="bf015-144">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bf015-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="bf015-145">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="bf015-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="bf015-146">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bf015-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="bf015-147">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bf015-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="bf015-148">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bf015-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="bf015-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="bf015-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="bf015-150">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="bf015-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-151">Az.Network</span></span>
* <span data-ttu-id="bf015-152">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="bf015-152">Upgrade dependancy of Microsoft.Azure.Management.Sql from 1.36-preivew to 1.37-preivew</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-154">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="bf015-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="bf015-155">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="bf015-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="bf015-156">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="bf015-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="bf015-157">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="bf015-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-158">Az.Resources</span></span>
* <span data-ttu-id="bf015-159">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="bf015-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-160">Az.Sql</span></span>
* <span data-ttu-id="bf015-161">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="bf015-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="bf015-162">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="bf015-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bf015-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="bf015-164">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="bf015-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-165">Az.Storage</span></span>
* <span data-ttu-id="bf015-166">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="bf015-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="bf015-167">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf015-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="bf015-168">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="bf015-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="bf015-169">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="bf015-170">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="bf015-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="bf015-171">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="bf015-171">General</span></span>
* <span data-ttu-id="bf015-172">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="bf015-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf015-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-173">Az.Accounts</span></span>
* <span data-ttu-id="bf015-174">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="bf015-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="bf015-175">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="bf015-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bf015-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf015-176">Az.Batch</span></span>
* <span data-ttu-id="bf015-177">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="bf015-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-178">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-179">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bf015-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf015-180">Az.FrontDoor</span></span>
* <span data-ttu-id="bf015-181">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="bf015-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="bf015-182">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="bf015-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="bf015-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="bf015-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="bf015-184">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="bf015-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf015-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf015-185">Az.KeyVault</span></span>
* <span data-ttu-id="bf015-186">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="bf015-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="bf015-187">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="bf015-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="bf015-188">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf015-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-189">Az.Monitor</span></span>
* <span data-ttu-id="bf015-190">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="bf015-191">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="bf015-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="bf015-192">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="bf015-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-193">Az.Network</span></span>
* <span data-ttu-id="bf015-194">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-195">Az.Resources</span></span>
* <span data-ttu-id="bf015-196">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="bf015-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="bf015-197">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="bf015-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-198">Az.Sql</span></span>
* <span data-ttu-id="bf015-199">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="bf015-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-200">Az.Storage</span></span>
* <span data-ttu-id="bf015-201">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="bf015-202">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="bf015-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="bf015-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bf015-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="bf015-204">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="bf015-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="bf015-205">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="bf015-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="bf015-206">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="bf015-207">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="bf015-208">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf015-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="bf015-209">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf015-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="bf015-210">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="bf015-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="bf015-211">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="bf015-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="bf015-212">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="bf015-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="bf015-213">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="bf015-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="bf015-214">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="bf015-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bf015-215">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="bf015-215">Highlights since the last major release</span></span>
* <span data-ttu-id="bf015-216">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="bf015-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="bf015-217">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="bf015-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-218">Az.Compute</span></span>
* <span data-ttu-id="bf015-219">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="bf015-219">VM Reapply feature</span></span>
    - <span data-ttu-id="bf015-220">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="bf015-221">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="bf015-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="bf015-222">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="bf015-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="bf015-223">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="bf015-224">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="bf015-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="bf015-225">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="bf015-226">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="bf015-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="bf015-227">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="bf015-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="bf015-228">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="bf015-229">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="bf015-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="bf015-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="bf015-231">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="bf015-232">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="bf015-232">Get the Order</span></span>
* <span data-ttu-id="bf015-233">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="bf015-234">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf015-234">Create new Order</span></span>
* <span data-ttu-id="bf015-235">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="bf015-236">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-236">Remove the Order</span></span>
* <span data-ttu-id="bf015-237">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="bf015-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="bf015-238">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="bf015-238">Now creates Local Share</span></span>
* <span data-ttu-id="bf015-239">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="bf015-240">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="bf015-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="bf015-241">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="bf015-242">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="bf015-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="bf015-243">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="bf015-244">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="bf015-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="bf015-245">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="bf015-246">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="bf015-246">Create new Triggers</span></span>
* <span data-ttu-id="bf015-247">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="bf015-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="bf015-248">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-249">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-250">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="bf015-251">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-253">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf015-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf015-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf015-254">Az.EventHub</span></span>
* <span data-ttu-id="bf015-255">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bf015-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf015-256">Az.FrontDoor</span></span>
* <span data-ttu-id="bf015-257">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="bf015-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="bf015-258">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="bf015-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="bf015-259">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="bf015-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="bf015-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="bf015-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-261">Az.Network</span></span>
* <span data-ttu-id="bf015-262">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="bf015-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="bf015-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="bf015-263">Az.PrivateDns</span></span>
* <span data-ttu-id="bf015-264">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="bf015-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-266">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="bf015-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="bf015-267">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="bf015-268">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="bf015-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bf015-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bf015-269">Az.RedisCache</span></span>
* <span data-ttu-id="bf015-270">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="bf015-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="bf015-271">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="bf015-272">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-273">Az.Resources</span></span>
- <span data-ttu-id="bf015-274">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="bf015-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="bf015-275">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="bf015-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="bf015-276">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="bf015-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="bf015-277">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="bf015-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="bf015-278">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="bf015-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-279">Az.Sql</span></span>
* <span data-ttu-id="bf015-280">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="bf015-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="bf015-281">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="bf015-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="bf015-282">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="bf015-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="bf015-283">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="bf015-283">General</span></span>
* <span data-ttu-id="bf015-284">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="bf015-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf015-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-285">Az.Accounts</span></span>
* <span data-ttu-id="bf015-286">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="bf015-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="bf015-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bf015-287">Az.Advisor</span></span>
* <span data-ttu-id="bf015-288">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bf015-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf015-289">Az.Batch</span></span>
* <span data-ttu-id="bf015-290">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="bf015-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="bf015-291">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="bf015-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="bf015-292">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="bf015-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="bf015-293">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="bf015-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="bf015-294">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="bf015-295">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="bf015-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="bf015-296">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="bf015-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="bf015-297">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="bf015-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="bf015-298">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="bf015-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="bf015-299">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="bf015-300">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="bf015-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="bf015-301">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="bf015-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="bf015-302">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="bf015-303">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="bf015-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="bf015-304">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="bf015-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="bf015-305">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="bf015-306">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="bf015-307">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="bf015-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="bf015-308">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="bf015-309">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="bf015-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="bf015-310">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="bf015-311">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="bf015-312">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="bf015-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="bf015-313">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="bf015-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="bf015-314">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="bf015-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="bf015-315">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="bf015-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="bf015-316">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="bf015-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="bf015-317">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="bf015-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="bf015-318">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="bf015-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="bf015-319">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="bf015-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="bf015-320">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="bf015-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="bf015-321">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="bf015-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="bf015-322">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="bf015-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="bf015-323">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="bf015-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="bf015-324">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="bf015-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="bf015-325">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="bf015-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf015-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf015-326">Az.Cdn</span></span>
* <span data-ttu-id="bf015-327">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="bf015-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="bf015-328">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="bf015-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-329">Az.Compute</span></span>
* <span data-ttu-id="bf015-330">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="bf015-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="bf015-331">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="bf015-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="bf015-332">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bf015-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="bf015-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="bf015-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="bf015-334">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bf015-335">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="bf015-336">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="bf015-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="bf015-337">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="bf015-338">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="bf015-338">Breaking changes</span></span>
    - <span data-ttu-id="bf015-339">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="bf015-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="bf015-340">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="bf015-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-341">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-342">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-344">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="bf015-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="bf015-345">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="bf015-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="bf015-346">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="bf015-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="bf015-347">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="bf015-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="bf015-348">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="bf015-349">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bf015-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf015-350">Az.FrontDoor</span></span>
* <span data-ttu-id="bf015-351">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="bf015-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bf015-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bf015-352">Az.HDInsight</span></span>
* <span data-ttu-id="bf015-353">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="bf015-354">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="bf015-355">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="bf015-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="bf015-356">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="bf015-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="bf015-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bf015-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bf015-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bf015-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bf015-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bf015-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bf015-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf015-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="bf015-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf015-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="bf015-362">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="bf015-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="bf015-363">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="bf015-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="bf015-364">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="bf015-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="bf015-365">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="bf015-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="bf015-366">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="bf015-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="bf015-367">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="bf015-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="bf015-368">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="bf015-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="bf015-369">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="bf015-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="bf015-370">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="bf015-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="bf015-371">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="bf015-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="bf015-372">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="bf015-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="bf015-373">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="bf015-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="bf015-374">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="bf015-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf015-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf015-375">Az.IotHub</span></span>
* <span data-ttu-id="bf015-376">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="bf015-376">Breaking changes:</span></span>
    - <span data-ttu-id="bf015-377">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bf015-378">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bf015-379">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bf015-380">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bf015-381">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="bf015-382">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="bf015-383">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="bf015-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="bf015-384">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="bf015-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="bf015-385">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bf015-386">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bf015-387">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bf015-388">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-390">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="bf015-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="bf015-391">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="bf015-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="bf015-392">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="bf015-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="bf015-393">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="bf015-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="bf015-394">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="bf015-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="bf015-395">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="bf015-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="bf015-396">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="bf015-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="bf015-397">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="bf015-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="bf015-398">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="bf015-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-399">Az.Resources</span></span>
* <span data-ttu-id="bf015-400">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="bf015-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-401">Az.Network</span></span>
* <span data-ttu-id="bf015-402">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="bf015-403">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="bf015-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="bf015-404">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-405">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-406">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-407">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="bf015-409">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="bf015-410">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="bf015-410">New cmdlet:</span></span>
        - <span data-ttu-id="bf015-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="bf015-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="bf015-412">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="bf015-413">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="bf015-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="bf015-414">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="bf015-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="bf015-415">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="bf015-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="bf015-416">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="bf015-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="bf015-417">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="bf015-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="bf015-418">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="bf015-419">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-419">New cmdlets added:</span></span>
        - <span data-ttu-id="bf015-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="bf015-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="bf015-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf015-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bf015-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf015-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bf015-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf015-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bf015-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bf015-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="bf015-425">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="bf015-426">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bf015-427">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="bf015-428">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="bf015-429">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="bf015-430">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="bf015-431">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="bf015-432">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-432">New cmdlets added:</span></span>
        - <span data-ttu-id="bf015-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="bf015-434">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bf015-435">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bf015-436">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bf015-437">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bf015-438">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bf015-439">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="bf015-440">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="bf015-441">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-441">New cmdlets added:</span></span>
        - <span data-ttu-id="bf015-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="bf015-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="bf015-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="bf015-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="bf015-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bf015-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="bf015-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bf015-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="bf015-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="bf015-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="bf015-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf015-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="bf015-448">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bf015-449">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="bf015-450">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="bf015-451">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="bf015-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="bf015-452">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="bf015-453">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bf015-454">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="bf015-455">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="bf015-456">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="bf015-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="bf015-457">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="bf015-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="bf015-458">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="bf015-459">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-459">New cmdlets added:</span></span>
        - <span data-ttu-id="bf015-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bf015-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="bf015-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bf015-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="bf015-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bf015-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="bf015-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bf015-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf015-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-465">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="bf015-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-466">Az.Sql</span></span>
* <span data-ttu-id="bf015-467">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="bf015-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="bf015-468">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="bf015-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="bf015-469">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="bf015-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="bf015-470">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="bf015-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="bf015-471">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="bf015-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="bf015-472">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="bf015-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="bf015-473">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="bf015-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="bf015-474">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="bf015-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="bf015-475">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="bf015-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-476">Az.Storage</span></span>
* <span data-ttu-id="bf015-477">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="bf015-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="bf015-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="bf015-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="bf015-480">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="bf015-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="bf015-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bf015-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="bf015-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bf015-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="bf015-483">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="bf015-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="bf015-484">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="bf015-484">General</span></span>
* <span data-ttu-id="bf015-485">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="bf015-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf015-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-486">Az.Accounts</span></span>
* <span data-ttu-id="bf015-487">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="bf015-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bf015-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf015-488">Az.ApiManagement</span></span>
* <span data-ttu-id="bf015-489">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf015-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="bf015-490">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="bf015-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-491">Az.Automation</span></span>
* <span data-ttu-id="bf015-492">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="bf015-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="bf015-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf015-493">Az.Batch</span></span>
* <span data-ttu-id="bf015-494">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="bf015-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-495">Az.Compute</span></span>
* <span data-ttu-id="bf015-496">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="bf015-497">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="bf015-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="bf015-498">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="bf015-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="bf015-499">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="bf015-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-500">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-501">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="bf015-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="bf015-502">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="bf015-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="bf015-503">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-505">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="bf015-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="bf015-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="bf015-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="bf015-507">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="bf015-508">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="bf015-509">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="bf015-510">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="bf015-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf015-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf015-511">Az.IotHub</span></span>
* <span data-ttu-id="bf015-512">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="bf015-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="bf015-513">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf015-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="bf015-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-514">Az.Monitor</span></span>
* <span data-ttu-id="bf015-515">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="bf015-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="bf015-516">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="bf015-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="bf015-517">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="bf015-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="bf015-518">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="bf015-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-519">Az.Network</span></span>
* <span data-ttu-id="bf015-520">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="bf015-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="bf015-521">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="bf015-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="bf015-522">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-522">New cmdlets added:</span></span>
        - <span data-ttu-id="bf015-523">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="bf015-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="bf015-524">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bf015-525">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="bf015-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="bf015-526">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="bf015-527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bf015-528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bf015-529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="bf015-530">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="bf015-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="bf015-531">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="bf015-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="bf015-532">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="bf015-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="bf015-533">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="bf015-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bf015-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bf015-534">Az.RedisCache</span></span>
* <span data-ttu-id="bf015-535">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="bf015-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-536">Az.Sql</span></span>
* <span data-ttu-id="bf015-537">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-538">Az.Storage</span></span>
* <span data-ttu-id="bf015-539">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="bf015-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="bf015-540">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="bf015-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="bf015-541">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bf015-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="bf015-542">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="bf015-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="bf015-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bf015-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bf015-544">Az.StorageSync</span></span>
* <span data-ttu-id="bf015-545">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="bf015-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-546">Az.Websites</span></span>
* <span data-ttu-id="bf015-547">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="bf015-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="bf015-548">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="bf015-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="bf015-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf015-549">Az.ApiManagement</span></span>
* <span data-ttu-id="bf015-550">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="bf015-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="bf015-551">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="bf015-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="bf015-552">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="bf015-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-553">Az.Automation</span></span>
* <span data-ttu-id="bf015-554">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="bf015-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="bf015-555">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="bf015-556">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="bf015-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-557">Az.Compute</span></span>
* <span data-ttu-id="bf015-558">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="bf015-559">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bf015-560">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="bf015-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="bf015-561">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="bf015-562">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="bf015-563">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="bf015-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="bf015-564">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="bf015-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="bf015-565">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="bf015-566">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-567">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-568">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="bf015-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="bf015-569">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bf015-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bf015-570">Az.HDInsight</span></span>
* <span data-ttu-id="bf015-571">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="bf015-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf015-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf015-572">Az.IotHub</span></span>
* <span data-ttu-id="bf015-573">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="bf015-574">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="bf015-575">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="bf015-575">New cmdlets are:</span></span>
    - <span data-ttu-id="bf015-576">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bf015-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bf015-577">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bf015-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bf015-578">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bf015-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bf015-579">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bf015-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf015-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-580">Az.Monitor</span></span>
* <span data-ttu-id="bf015-581">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="bf015-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="bf015-582">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="bf015-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="bf015-583">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="bf015-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="bf015-584">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="bf015-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="bf015-585">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="bf015-586">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="bf015-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="bf015-587">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="bf015-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="bf015-588">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="bf015-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="bf015-589">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="bf015-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="bf015-590">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="bf015-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="bf015-591">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="bf015-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="bf015-592">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="bf015-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="bf015-593">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="bf015-594">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="bf015-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="bf015-595">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="bf015-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="bf015-596">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="bf015-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="bf015-597">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="bf015-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="bf015-598">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="bf015-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="bf015-599">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="bf015-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="bf015-600">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="bf015-600">Overall improved help files</span></span>
* <span data-ttu-id="bf015-601">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="bf015-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-602">Az.Network</span></span>
* <span data-ttu-id="bf015-603">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="bf015-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="bf015-604">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="bf015-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="bf015-605">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="bf015-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="bf015-606">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="bf015-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="bf015-607">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="bf015-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="bf015-608">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="bf015-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="bf015-609">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="bf015-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="bf015-610">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="bf015-611">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="bf015-612">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="bf015-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="bf015-613">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="bf015-614">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="bf015-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="bf015-615">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-615">New cmdlets</span></span>
        - <span data-ttu-id="bf015-616">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="bf015-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="bf015-617">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="bf015-618">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="bf015-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="bf015-619">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="bf015-619">New-VpnSite</span></span>
        - <span data-ttu-id="bf015-620">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="bf015-620">Update-VpnSite</span></span>
        - <span data-ttu-id="bf015-621">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-621">New-VpnConnection</span></span>
        - <span data-ttu-id="bf015-622">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-622">Update-VpnConnection</span></span>
* <span data-ttu-id="bf015-623">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="bf015-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-625">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="bf015-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="bf015-626">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="bf015-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-627">Az.Resources</span></span>
* <span data-ttu-id="bf015-628">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="bf015-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf015-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-630">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="bf015-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="bf015-631">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="bf015-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="bf015-632">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bf015-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bf015-633">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bf015-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bf015-634">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bf015-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bf015-635">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bf015-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="bf015-636">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bf015-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bf015-637">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bf015-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bf015-638">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bf015-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bf015-639">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bf015-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bf015-640">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bf015-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="bf015-641">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bf015-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bf015-642">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bf015-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bf015-643">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bf015-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bf015-644">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="bf015-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="bf015-645">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="bf015-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bf015-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bf015-646">Az.SignalR</span></span>
* <span data-ttu-id="bf015-647">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-648">Az.Sql</span></span>
* <span data-ttu-id="bf015-649">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="bf015-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="bf015-650">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="bf015-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="bf015-651">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="bf015-652">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="bf015-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="bf015-653">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="bf015-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-654">Az.Storage</span></span>
* <span data-ttu-id="bf015-655">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="bf015-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="bf015-656">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="bf015-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bf015-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="bf015-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bf015-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="bf015-659">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="bf015-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf015-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="bf015-661">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="bf015-662">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf015-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bf015-663">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf015-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bf015-664">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf015-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bf015-665">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf015-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-666">Az.Websites</span></span>
* <span data-ttu-id="bf015-667">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="bf015-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="bf015-668">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="bf015-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="bf015-669">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="bf015-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="bf015-670">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="bf015-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="bf015-671">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="bf015-671">General</span></span>
* <span data-ttu-id="bf015-672">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="bf015-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf015-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-673">Az.Accounts</span></span>
* <span data-ttu-id="bf015-674">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="bf015-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="bf015-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bf015-675">Az.Aks</span></span>
* <span data-ttu-id="bf015-676">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="bf015-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="bf015-677">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="bf015-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bf015-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf015-678">Az.ApiManagement</span></span>
* <span data-ttu-id="bf015-679">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="bf015-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="bf015-680">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="bf015-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="bf015-681">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="bf015-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="bf015-682">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="bf015-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="bf015-683">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="bf015-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bf015-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf015-684">Az.Batch</span></span>
* <span data-ttu-id="bf015-685">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="bf015-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf015-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf015-686">Az.Cdn</span></span>
* <span data-ttu-id="bf015-687">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="bf015-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-688">Az.Compute</span></span>
* <span data-ttu-id="bf015-689">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="bf015-690">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="bf015-691">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="bf015-692">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="bf015-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="bf015-693">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="bf015-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="bf015-694">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="bf015-695">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="bf015-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="bf015-696">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="bf015-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-697">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-698">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="bf015-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="bf015-699">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="bf015-700">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="bf015-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="bf015-701">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="bf015-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-703">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="bf015-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf015-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf015-704">Az.EventHub</span></span>
* <span data-ttu-id="bf015-705">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="bf015-706">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="bf015-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="bf015-707">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="bf015-708">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="bf015-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="bf015-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bf015-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bf015-710">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="bf015-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf015-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-711">Az.Monitor</span></span>
* <span data-ttu-id="bf015-712">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="bf015-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-713">Az.Network</span></span>
* <span data-ttu-id="bf015-714">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="bf015-715">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="bf015-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="bf015-716">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="bf015-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="bf015-717">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="bf015-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="bf015-718">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="bf015-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="bf015-719">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="bf015-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="bf015-720">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="bf015-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf015-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf015-722">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf015-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="bf015-723">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-723">Added example</span></span>
    - <span data-ttu-id="bf015-724">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="bf015-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="bf015-725">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="bf015-726">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="bf015-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-728">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="bf015-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-729">Az.Resources</span></span>
* <span data-ttu-id="bf015-730">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="bf015-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="bf015-731">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="bf015-732">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="bf015-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="bf015-733">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf015-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf015-734">Az.ServiceBus</span></span>
* <span data-ttu-id="bf015-735">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="bf015-736">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="bf015-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="bf015-737">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="bf015-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="bf015-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-739">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="bf015-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="bf015-740">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="bf015-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="bf015-741">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="bf015-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="bf015-742">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="bf015-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="bf015-743">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="bf015-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="bf015-744">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="bf015-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-745">Az.Sql</span></span>
* <span data-ttu-id="bf015-746">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="bf015-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-747">Az.Storage</span></span>
* <span data-ttu-id="bf015-748">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="bf015-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="bf015-749">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="bf015-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="bf015-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf015-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="bf015-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf015-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="bf015-752">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="bf015-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="bf015-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf015-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-754">Az.Websites</span></span>
* <span data-ttu-id="bf015-755">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="bf015-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="bf015-756">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="bf015-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-757">Az.Accounts</span></span>
* <span data-ttu-id="bf015-758">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="bf015-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="bf015-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="bf015-760">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="bf015-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-761">Az.Automation</span></span>
* <span data-ttu-id="bf015-762">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf015-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf015-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf015-764">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="bf015-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-765">Az.Compute</span></span>
* <span data-ttu-id="bf015-766">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="bf015-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bf015-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf015-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bf015-768">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="bf015-769">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="bf015-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-770">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-771">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="bf015-772">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf015-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf015-773">Az.EventHub</span></span>
* <span data-ttu-id="bf015-774">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bf015-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bf015-775">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="bf015-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf015-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf015-776">Az.KeyVault</span></span>
* <span data-ttu-id="bf015-777">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf015-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf015-778">Az.LogicApp</span></span>
* <span data-ttu-id="bf015-779">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="bf015-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="bf015-780">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="bf015-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="bf015-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bf015-781">Az.ManagedServices</span></span>
* <span data-ttu-id="bf015-782">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-783">Az.Network</span></span>
* <span data-ttu-id="bf015-784">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="bf015-785">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-785">New cmdlets</span></span>
        - <span data-ttu-id="bf015-786">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf015-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf015-787">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf015-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bf015-788">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-789">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-790">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-791">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bf015-792">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="bf015-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="bf015-793">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf015-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="bf015-794">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="bf015-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="bf015-795">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="bf015-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="bf015-796">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="bf015-797">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="bf015-798">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="bf015-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="bf015-799">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="bf015-800">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-800">Updated cmdlets</span></span>
        - <span data-ttu-id="bf015-801">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bf015-802">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bf015-803">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="bf015-804">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="bf015-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bf015-805">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="bf015-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="bf015-806">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="bf015-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="bf015-807">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bf015-808">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bf015-809">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="bf015-810">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="bf015-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="bf015-811">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="bf015-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="bf015-812">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="bf015-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf015-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf015-814">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="bf015-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="bf015-815">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="bf015-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-817">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bf015-818">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="bf015-819">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="bf015-820">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bf015-821">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="bf015-822">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bf015-823">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="bf015-824">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bf015-825">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="bf015-826">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-827">Az.Resources</span></span>
- <span data-ttu-id="bf015-828">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="bf015-829">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="bf015-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf015-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf015-830">Az.ServiceBus</span></span>
* <span data-ttu-id="bf015-831">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bf015-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bf015-832">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="bf015-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-833">Az.Sql</span></span>
* <span data-ttu-id="bf015-834">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="bf015-835">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="bf015-836">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="bf015-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-837">Az.Storage</span></span>
* <span data-ttu-id="bf015-838">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="bf015-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bf015-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bf015-839">Az.StorageSync</span></span>
* <span data-ttu-id="bf015-840">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="bf015-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="bf015-841">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="bf015-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-842">Az.Websites</span></span>
* <span data-ttu-id="bf015-843">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="bf015-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="bf015-844">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="bf015-845">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="bf015-846">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="bf015-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-847">Az.Accounts</span></span>
* <span data-ttu-id="bf015-848">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="bf015-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="bf015-849">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="bf015-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="bf015-850">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="bf015-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="bf015-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bf015-851">Az.Advisor</span></span>
* <span data-ttu-id="bf015-852">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="bf015-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="bf015-853">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="bf015-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bf015-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf015-854">Az.ApiManagement</span></span>
* <span data-ttu-id="bf015-855">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="bf015-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="bf015-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="bf015-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="bf015-857">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="bf015-858">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="bf015-859">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="bf015-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="bf015-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="bf015-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="bf015-861">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="bf015-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-862">Az.Automation</span></span>
* <span data-ttu-id="bf015-863">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="bf015-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-864">Az.Compute</span></span>
* <span data-ttu-id="bf015-865">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-866">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-867">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf015-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf015-868">Az.EventGrid</span></span>
* <span data-ttu-id="bf015-869">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="bf015-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf015-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf015-870">Az.IotHub</span></span>
* <span data-ttu-id="bf015-871">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="bf015-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-872">Az.Network</span></span>
* <span data-ttu-id="bf015-873">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="bf015-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="bf015-874">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="bf015-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf015-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf015-876">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="bf015-877">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="bf015-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf015-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf015-879">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="bf015-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-881">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-882">Az.Resources</span></span>
    - <span data-ttu-id="bf015-883">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="bf015-884">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="bf015-885">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="bf015-886">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf015-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf015-887">Az.ServiceBus</span></span>
* <span data-ttu-id="bf015-888">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="bf015-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-889">Az.Sql</span></span>
* <span data-ttu-id="bf015-890">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="bf015-891">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="bf015-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="bf015-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bf015-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bf015-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bf015-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bf015-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bf015-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bf015-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bf015-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bf015-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bf015-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bf015-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bf015-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="bf015-898">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="bf015-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-899">Az.Storage</span></span>
* <span data-ttu-id="bf015-900">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="bf015-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="bf015-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bf015-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="bf015-902">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="bf015-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="bf015-903">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="bf015-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="bf015-904">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="bf015-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="bf015-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="bf015-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="bf015-907">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="bf015-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="bf015-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bf015-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="bf015-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bf015-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bf015-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bf015-910">Az.StorageSync</span></span>
* <span data-ttu-id="bf015-911">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="bf015-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="bf015-912">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="bf015-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-913">Az.Accounts</span></span>
* <span data-ttu-id="bf015-914">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="bf015-915">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="bf015-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="bf015-916">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="bf015-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bf015-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="bf015-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="bf015-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-919">Az.Compute</span></span>
* <span data-ttu-id="bf015-920">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="bf015-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="bf015-921">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="bf015-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="bf015-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bf015-922">Az.Dns</span></span>
* <span data-ttu-id="bf015-923">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="bf015-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf015-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf015-924">Az.EventGrid</span></span>
* <span data-ttu-id="bf015-925">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="bf015-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="bf015-926">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-926">New cmdlets:</span></span>
    - <span data-ttu-id="bf015-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bf015-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bf015-928">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="bf015-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bf015-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bf015-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bf015-930">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="bf015-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="bf015-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bf015-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bf015-932">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="bf015-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bf015-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bf015-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bf015-934">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bf015-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bf015-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bf015-936">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="bf015-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="bf015-937">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bf015-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bf015-938">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bf015-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="bf015-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="bf015-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="bf015-940">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="bf015-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="bf015-941">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bf015-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bf015-942">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="bf015-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="bf015-943">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="bf015-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bf015-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="bf015-945">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="bf015-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bf015-946">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="bf015-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bf015-947">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="bf015-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="bf015-948">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="bf015-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="bf015-949">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="bf015-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="bf015-950">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="bf015-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="bf015-951">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="bf015-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="bf015-952">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="bf015-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="bf015-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bf015-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="bf015-954">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="bf015-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="bf015-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="bf015-956">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="bf015-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="bf015-957">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="bf015-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bf015-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf015-958">Az.FrontDoor</span></span>
* <span data-ttu-id="bf015-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="bf015-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="bf015-960">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="bf015-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="bf015-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="bf015-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="bf015-962">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="bf015-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-963">Az.Network</span></span>
* <span data-ttu-id="bf015-964">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="bf015-965">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-965">New cmdlets</span></span>
        - <span data-ttu-id="bf015-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="bf015-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="bf015-967">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="bf015-968">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-968">New cmdlets</span></span> 
        - <span data-ttu-id="bf015-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="bf015-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="bf015-970">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="bf015-971">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-971">New cmdlets</span></span> 
        - <span data-ttu-id="bf015-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf015-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="bf015-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf015-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bf015-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bf015-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bf015-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="bf015-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="bf015-977">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="bf015-978">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-978">New cmdlets</span></span>
        - <span data-ttu-id="bf015-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf015-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf015-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf015-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf015-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf015-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bf015-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="bf015-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="bf015-983">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="bf015-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="bf015-984">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="bf015-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="bf015-985">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="bf015-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="bf015-986">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="bf015-987">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="bf015-988">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="bf015-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="bf015-989">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="bf015-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="bf015-990">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="bf015-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="bf015-991">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="bf015-992">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="bf015-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="bf015-993">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="bf015-994">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="bf015-995">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="bf015-996">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="bf015-997">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="bf015-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="bf015-998">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="bf015-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="bf015-999">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="bf015-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="bf015-1000">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="bf015-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="bf015-1001">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="bf015-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="bf015-1002">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="bf015-1003">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bf015-1004">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bf015-1005">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf015-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf015-1007">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1008">Az.Resources</span></span>
* <span data-ttu-id="bf015-1009">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="bf015-1010">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bf015-1011">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bf015-1012">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf015-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-1014">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="bf015-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1015">Az.Sql</span></span>
* <span data-ttu-id="bf015-1016">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="bf015-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="bf015-1017">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="bf015-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="bf015-1018">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="bf015-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf015-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bf015-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf015-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bf015-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bf015-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bf015-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bf015-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="bf015-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bf015-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1024">Az.Storage</span></span>
* <span data-ttu-id="bf015-1025">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="bf015-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="bf015-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="bf015-1027">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="bf015-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="bf015-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bf015-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1029">Az.Websites</span></span>
* <span data-ttu-id="bf015-1030">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="bf015-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="bf015-1031">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="bf015-1032">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="bf015-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="bf015-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf015-1033">Az.Cdn</span></span>
* <span data-ttu-id="bf015-1034">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="bf015-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1035">Az.Compute</span></span>
* <span data-ttu-id="bf015-1036">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="bf015-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="bf015-1037">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf015-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf015-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf015-1038">Az.EventHub</span></span>
* <span data-ttu-id="bf015-1039">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="bf015-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="bf015-1040">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="bf015-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1041">Az.Network</span></span>
* <span data-ttu-id="bf015-1042">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="bf015-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="bf015-1043">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="bf015-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf015-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf015-1045">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-1047">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="bf015-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf015-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf015-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="bf015-1049">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="bf015-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf015-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-1051">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="bf015-1052">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="bf015-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1053">Az.Sql</span></span>
* <span data-ttu-id="bf015-1054">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="bf015-1055">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="bf015-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="bf015-1056">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="bf015-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="bf015-1057">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="bf015-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1058">Az.Websites</span></span>
* <span data-ttu-id="bf015-1059">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="bf015-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="bf015-1060">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="bf015-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="bf015-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf015-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="bf015-1062">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="bf015-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="bf015-1063">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="bf015-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="bf015-1064">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="bf015-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="bf015-1065">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="bf015-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="bf015-1066">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="bf015-1067">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="bf015-1068">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="bf015-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="bf015-1069">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="bf015-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="bf015-1070">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="bf015-1071">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="bf015-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="bf015-1072">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="bf015-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="bf015-1073">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="bf015-1074">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="bf015-1075">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="bf015-1076">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="bf015-1077">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="bf015-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="bf015-1078">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="bf015-1079">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="bf015-1080">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="bf015-1081">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="bf015-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="bf015-1082">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="bf015-1083">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="bf015-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="bf015-1084">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="bf015-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="bf015-1085">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="bf015-1086">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="bf015-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="bf015-1087">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="bf015-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="bf015-1088">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="bf015-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="bf015-1089">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="bf015-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="bf015-1090">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="bf015-1091">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="bf015-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="bf015-1092">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="bf015-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="bf015-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="bf015-1094">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="bf015-1095">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bf015-1096">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="bf015-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="bf015-1097">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="bf015-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="bf015-1098">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="bf015-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="bf015-1099">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="bf015-1100">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="bf015-1101">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="bf015-1102">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bf015-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bf015-1103">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="bf015-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="bf015-1104">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="bf015-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="bf015-1105">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="bf015-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="bf015-1106">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bf015-1107">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bf015-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bf015-1108">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="bf015-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="bf015-1109">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="bf015-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="bf015-1110">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="bf015-1111">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="bf015-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="bf015-1112">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="bf015-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="bf015-1113">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="bf015-1114">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="bf015-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="bf015-1115">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="bf015-1116">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="bf015-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="bf015-1117">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="bf015-1118">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bf015-1119">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bf015-1120">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bf015-1121">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bf015-1122">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bf015-1123">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bf015-1124">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bf015-1125">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bf015-1126">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="bf015-1127">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bf015-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="bf015-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="bf015-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="bf015-1129">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bf015-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="bf015-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="bf015-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="bf015-1131">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="bf015-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="bf015-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="bf015-1133">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bf015-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="bf015-1134">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bf015-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="bf015-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="bf015-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="bf015-1136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bf015-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="bf015-1137">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="bf015-1138">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bf015-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-1139">Az.Automation</span></span>
* <span data-ttu-id="bf015-1140">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="bf015-1141">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="bf015-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="bf015-1142">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="bf015-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="bf015-1143">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="bf015-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="bf015-1144">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="bf015-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="bf015-1145">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="bf015-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="bf015-1146">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="bf015-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1147">Az.Compute</span></span>
* <span data-ttu-id="bf015-1148">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="bf015-1149">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="bf015-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-1151">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="bf015-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf015-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-1152">Az.Monitor</span></span>
* <span data-ttu-id="bf015-1153">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="bf015-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1154">Az.Network</span></span>
* <span data-ttu-id="bf015-1155">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="bf015-1156">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="bf015-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="bf015-1157">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf015-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="bf015-1158">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="bf015-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1159">Az.Resources</span></span>
* <span data-ttu-id="bf015-1160">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1161">Az.Sql</span></span>
* <span data-ttu-id="bf015-1162">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="bf015-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="bf015-1163">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="bf015-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1164">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1165">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="bf015-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf015-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf015-1167">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="bf015-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="bf015-1168">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1169">Az.Compute</span></span>
* <span data-ttu-id="bf015-1170">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="bf015-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="bf015-1171">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bf015-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="bf015-1172">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="bf015-1173">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="bf015-1174">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="bf015-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="bf015-1175">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="bf015-1176">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="bf015-1176">Breaking changes</span></span>
    - <span data-ttu-id="bf015-1177">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="bf015-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="bf015-1178">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="bf015-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="bf015-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="bf015-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="bf015-1180">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="bf015-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="bf015-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bf015-1181">Az.Dns</span></span>
* <span data-ttu-id="bf015-1182">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="bf015-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="bf015-1183">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="bf015-1184">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="bf015-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bf015-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf015-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="bf015-1186">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="bf015-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="bf015-1187">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="bf015-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="bf015-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bf015-1188">Az.HDInsight</span></span>
* <span data-ttu-id="bf015-1189">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="bf015-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="bf015-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf015-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="bf015-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf015-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bf015-1192">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="bf015-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bf015-1193">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="bf015-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="bf015-1194">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="bf015-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="bf015-1195">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="bf015-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf015-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-1196">Az.Monitor</span></span>
* <span data-ttu-id="bf015-1197">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="bf015-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="bf015-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bf015-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="bf015-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="bf015-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="bf015-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="bf015-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="bf015-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="bf015-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="bf015-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="bf015-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="bf015-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="bf015-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="bf015-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf015-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf015-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf015-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf015-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bf015-1209">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="bf015-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="bf015-1210">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="bf015-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1211">Az.Network</span></span>
* <span data-ttu-id="bf015-1212">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="bf015-1213">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-1213">New cmdlets</span></span>
        - <span data-ttu-id="bf015-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf015-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="bf015-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf015-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="bf015-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf015-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="bf015-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bf015-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="bf015-1218">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="bf015-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bf015-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="bf015-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bf015-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="bf015-1221">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="bf015-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="bf015-1222">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="bf015-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="bf015-1223">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="bf015-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf015-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf015-1225">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="bf015-1226">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="bf015-1227">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-1229">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="bf015-1230">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="bf015-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="bf015-1231">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="bf015-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="bf015-1232">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="bf015-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="bf015-1233">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="bf015-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="bf015-1234">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="bf015-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="bf015-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bf015-1235">Az.Relay</span></span>
* <span data-ttu-id="bf015-1236">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="bf015-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf015-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf015-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="bf015-1238">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="bf015-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1239">Az.Storage</span></span>
* <span data-ttu-id="bf015-1240">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="bf015-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="bf015-1241">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="bf015-1242">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="bf015-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="bf015-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="bf015-1244">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="bf015-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="bf015-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="bf015-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="bf015-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1248">Az.Websites</span></span>
* <span data-ttu-id="bf015-1249">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="bf015-1250">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="bf015-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="bf015-1251">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="bf015-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bf015-1252">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="bf015-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="bf015-1253">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="bf015-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="bf015-1254">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="bf015-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bf015-1255">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="bf015-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bf015-1256">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bf015-1257">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf015-1258">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bf015-1259">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf015-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1260">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1261">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bf015-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf015-1262">Az.Batch</span></span>
* <span data-ttu-id="bf015-1263">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf015-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf015-1264">Az.Cdn</span></span>
* <span data-ttu-id="bf015-1265">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf015-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf015-1267">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1268">Az.Compute</span></span>
* <span data-ttu-id="bf015-1269">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="bf015-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="bf015-1270">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf015-1271">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf015-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-1272">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-1273">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="bf015-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-1275">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf015-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf015-1276">Az.EventGrid</span></span>
* <span data-ttu-id="bf015-1277">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="bf015-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf015-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf015-1278">Az.EventHub</span></span>
* <span data-ttu-id="bf015-1279">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="bf015-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="bf015-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bf015-1280">Az.HDInsight</span></span>
* <span data-ttu-id="bf015-1281">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf015-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf015-1282">Az.IotHub</span></span>
* <span data-ttu-id="bf015-1283">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf015-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf015-1284">Az.KeyVault</span></span>
* <span data-ttu-id="bf015-1285">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf015-1286">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf015-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="bf015-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bf015-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="bf015-1288">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="bf015-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bf015-1289">Az.Media</span></span>
* <span data-ttu-id="bf015-1290">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf015-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-1291">Az.Monitor</span></span>
  * <span data-ttu-id="bf015-1292">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="bf015-1293">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="bf015-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="bf015-1294">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="bf015-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="bf015-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bf015-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bf015-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bf015-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bf015-1297">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bf015-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="bf015-1298">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="bf015-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1299">Az.Network</span></span>
* <span data-ttu-id="bf015-1300">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf015-1301">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf015-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="bf015-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="bf015-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="bf015-1303">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf015-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf015-1305">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="bf015-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bf015-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="bf015-1307">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-1309">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf015-1310">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="bf015-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="bf015-1311">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="bf015-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="bf015-1312">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="bf015-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bf015-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bf015-1313">Az.RedisCache</span></span>
* <span data-ttu-id="bf015-1314">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1315">Az.Resources</span></span>
* <span data-ttu-id="bf015-1316">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf015-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1317">Az.Sql</span></span>
* <span data-ttu-id="bf015-1318">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="bf015-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="bf015-1319">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf015-1320">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="bf015-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="bf015-1321">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bf015-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="bf015-1322">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="bf015-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="bf015-1323">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="bf015-1324">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf015-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1325">Az.Websites</span></span>
* <span data-ttu-id="bf015-1326">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="bf015-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="bf015-1327">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bf015-1328">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="bf015-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="bf015-1329">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="bf015-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="bf015-1330">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="bf015-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bf015-1331">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="bf015-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="bf015-1332">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="bf015-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="bf015-1333">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="bf015-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bf015-1334">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="bf015-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bf015-1335">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bf015-1336">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf015-1337">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bf015-1338">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bf015-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1339">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1340">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bf015-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="bf015-1342">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="bf015-1343">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-1344">Az.Automation</span></span>
* <span data-ttu-id="bf015-1345">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="bf015-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="bf015-1346">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="bf015-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="bf015-1347">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1348">Az.Compute</span></span>
* <span data-ttu-id="bf015-1349">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bf015-1350">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="bf015-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="bf015-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="bf015-1352">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="bf015-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-1353">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-1354">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="bf015-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="bf015-1355">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="bf015-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1356">Az.Resources</span></span>
* <span data-ttu-id="bf015-1357">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="bf015-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="bf015-1358">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="bf015-1359">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="bf015-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="bf015-1360">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bf015-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="bf015-1361">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="bf015-1362">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bf015-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1363">Az.Sql</span></span>
* <span data-ttu-id="bf015-1364">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1365">Az.Storage</span></span>
* <span data-ttu-id="bf015-1366">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="bf015-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="bf015-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf015-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="bf015-1368">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="bf015-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="bf015-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bf015-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bf015-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bf015-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bf015-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf015-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="bf015-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf015-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="bf015-1373">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="bf015-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf015-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bf015-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bf015-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bf015-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bf015-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="bf015-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bf015-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="bf015-1378">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="bf015-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bf015-1379">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="bf015-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="bf015-1380">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="bf015-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="bf015-1381">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="bf015-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bf015-1382">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="bf015-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bf015-1383">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bf015-1384">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf015-1385">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bf015-1386">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-1387">Az.Automation</span></span>
* <span data-ttu-id="bf015-1388">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="bf015-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="bf015-1389">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="bf015-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="bf015-1390">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="bf015-1390">Pre-Post script</span></span>
    * <span data-ttu-id="bf015-1391">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="bf015-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1392">Az.Compute</span></span>
* <span data-ttu-id="bf015-1393">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="bf015-1394">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="bf015-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf015-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf015-1395">Az.KeyVault</span></span>
* <span data-ttu-id="bf015-1396">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1397">Az.Network</span></span>
* <span data-ttu-id="bf015-1398">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="bf015-1399">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-1401">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="bf015-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="bf015-1402">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1403">Az.Resources</span></span>
* <span data-ttu-id="bf015-1404">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="bf015-1405">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1406">Az.Sql</span></span>
* <span data-ttu-id="bf015-1407">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="bf015-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1408">Az.Storage</span></span>
* <span data-ttu-id="bf015-1409">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="bf015-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bf015-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bf015-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bf015-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bf015-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bf015-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bf015-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="bf015-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="bf015-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="bf015-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="bf015-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1416">Az.Websites</span></span>
* <span data-ttu-id="bf015-1417">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="bf015-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="bf015-1418">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="bf015-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1419">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1420">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="bf015-1421">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-1422">Az.Automation</span></span>
* <span data-ttu-id="bf015-1423">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="bf015-1424">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="bf015-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="bf015-1425">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="bf015-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf015-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf015-1426">Az.Cdn</span></span>
* <span data-ttu-id="bf015-1427">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="bf015-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1428">Az.Compute</span></span>
* <span data-ttu-id="bf015-1429">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-1430">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-1431">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="bf015-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf015-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf015-1432">Az.LogicApp</span></span>
* <span data-ttu-id="bf015-1433">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="bf015-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1434">Az.Network</span></span>
* <span data-ttu-id="bf015-1435">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-1437">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="bf015-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="bf015-1438">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="bf015-1438">SDK Update</span></span>
* <span data-ttu-id="bf015-1439">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="bf015-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="bf015-1440">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1441">Az.Resources</span></span>
* <span data-ttu-id="bf015-1442">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="bf015-1443">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="bf015-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="bf015-1444">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="bf015-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="bf015-1445">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="bf015-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="bf015-1446">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="bf015-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="bf015-1447">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="bf015-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1448">Az.Sql</span></span>
* <span data-ttu-id="bf015-1449">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="bf015-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="bf015-1450">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="bf015-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1451">Az.Storage</span></span>
* <span data-ttu-id="bf015-1452">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf015-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="bf015-1453">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="bf015-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="bf015-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="bf015-1455">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="bf015-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-1456">Az.Automation</span></span>
* <span data-ttu-id="bf015-1457">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="bf015-1458">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="bf015-1459">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf015-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf015-1461">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1462">Az.Compute</span></span>
* <span data-ttu-id="bf015-1463">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="bf015-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="bf015-1464">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="bf015-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="bf015-1465">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="bf015-1466">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="bf015-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-1468">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="bf015-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bf015-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bf015-1469">Az.EventHub</span></span>
* <span data-ttu-id="bf015-1470">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="bf015-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="bf015-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf015-1471">Az.KeyVault</span></span>
* <span data-ttu-id="bf015-1472">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf015-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf015-1473">Az.LogicApp</span></span>
* <span data-ttu-id="bf015-1474">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="bf015-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="bf015-1475">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="bf015-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="bf015-1476">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="bf015-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="bf015-1477">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf015-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bf015-1478">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf015-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bf015-1479">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf015-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bf015-1480">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bf015-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="bf015-1481">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="bf015-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="bf015-1482">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf015-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bf015-1483">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf015-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bf015-1484">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf015-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bf015-1485">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf015-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="bf015-1486">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="bf015-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bf015-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-1487">Az.Monitor</span></span>
* <span data-ttu-id="bf015-1488">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1489">Az.Network</span></span>
* <span data-ttu-id="bf015-1490">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="bf015-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bf015-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="bf015-1492">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="bf015-1493">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="bf015-1494">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="bf015-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="bf015-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1495">Az.Resources</span></span>
* <span data-ttu-id="bf015-1496">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="bf015-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bf015-1497">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="bf015-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="bf015-1498">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="bf015-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="bf015-1499">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="bf015-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1500">Az.Sql</span></span>
* <span data-ttu-id="bf015-1501">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="bf015-1502">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="bf015-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1503">Az.Websites</span></span>
* <span data-ttu-id="bf015-1504">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="bf015-1505">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="bf015-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1506">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1507">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="bf015-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bf015-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="bf015-1509">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1510">Az.Compute</span></span>
* <span data-ttu-id="bf015-1511">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="bf015-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="bf015-1512">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="bf015-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="bf015-1513">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="bf015-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="bf015-1515">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="bf015-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1516">Az.Resources</span></span>
* <span data-ttu-id="bf015-1517">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="bf015-1518">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="bf015-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bf015-1519">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="bf015-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="bf015-1520">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="bf015-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1521">Az.Sql</span></span>
* <span data-ttu-id="bf015-1522">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="bf015-1523">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="bf015-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="bf015-1524">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="bf015-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="bf015-1525">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="bf015-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1526">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1527">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="bf015-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bf015-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="bf015-1529">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="bf015-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="bf015-1531">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="bf015-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="bf015-1532">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="bf015-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1533">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1534">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bf015-1535">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf015-1536">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="bf015-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="bf015-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bf015-1537">Az.Aks</span></span>
* <span data-ttu-id="bf015-1538">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bf015-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-1539">Az.Automation</span></span>
* <span data-ttu-id="bf015-1540">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="bf015-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="bf015-1541">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bf015-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bf015-1542">Az.Cdn</span></span>
* <span data-ttu-id="bf015-1543">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1544">Az.Compute</span></span>
* <span data-ttu-id="bf015-1545">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="bf015-1546">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="bf015-1547">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bf015-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf015-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bf015-1549">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bf015-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf015-1550">Az.DataFactory</span></span>
* <span data-ttu-id="bf015-1551">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="bf015-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-1553">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="bf015-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="bf015-1554">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="bf015-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="bf015-1555">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf015-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf015-1556">Az.IotHub</span></span>
* <span data-ttu-id="bf015-1557">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bf015-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf015-1558">Az.KeyVault</span></span>
* <span data-ttu-id="bf015-1559">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1560">Az.Network</span></span>
* <span data-ttu-id="bf015-1561">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1562">Az.Resources</span></span>
* <span data-ttu-id="bf015-1563">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="bf015-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="bf015-1564">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="bf015-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="bf015-1565">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="bf015-1566">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="bf015-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="bf015-1567">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="bf015-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="bf015-1568">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="bf015-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="bf015-1569">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="bf015-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf015-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-1571">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="bf015-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="bf015-1572">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1572">Fix some error messages.</span></span>
* <span data-ttu-id="bf015-1573">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="bf015-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="bf015-1574">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="bf015-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bf015-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bf015-1575">Az.SignalR</span></span>
* <span data-ttu-id="bf015-1576">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1577">Az.Sql</span></span>
* <span data-ttu-id="bf015-1578">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf015-1579">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="bf015-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="bf015-1580">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="bf015-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="bf015-1581">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="bf015-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1582">Az.Storage</span></span>
* <span data-ttu-id="bf015-1583">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf015-1584">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="bf015-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="bf015-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bf015-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="bf015-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bf015-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="bf015-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bf015-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="bf015-1588">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1589">Az.Websites</span></span>
* <span data-ttu-id="bf015-1590">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="bf015-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bf015-1591">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="bf015-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="bf015-1592">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="bf015-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="bf015-1593">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="bf015-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bf015-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1594">Az.Accounts</span></span>
* <span data-ttu-id="bf015-1595">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1596">Az.Compute</span></span>
* <span data-ttu-id="bf015-1597">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="bf015-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="bf015-1598">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="bf015-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="bf015-1599">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="bf015-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-1601">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="bf015-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="bf015-1602">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="bf015-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bf015-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bf015-1603">Az.EventGrid</span></span>
* <span data-ttu-id="bf015-1604">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="bf015-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="bf015-1605">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="bf015-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="bf015-1606">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="bf015-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bf015-1607">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="bf015-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bf015-1608">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="bf015-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bf015-1609">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="bf015-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="bf015-1610">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="bf015-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bf015-1611">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="bf015-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bf015-1612">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="bf015-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bf015-1613">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="bf015-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="bf015-1614">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="bf015-1615">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="bf015-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bf015-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bf015-1616">Az.IotHub</span></span>
* <span data-ttu-id="bf015-1617">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="bf015-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bf015-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bf015-1618">Az.LogicApp</span></span>
* <span data-ttu-id="bf015-1619">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="bf015-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1620">Az.Resources</span></span>
* <span data-ttu-id="bf015-1621">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="bf015-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="bf015-1622">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="bf015-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="bf015-1623">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="bf015-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bf015-1624">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="bf015-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="bf015-1625">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="bf015-1626">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="bf015-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bf015-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bf015-1627">Az.SignalR</span></span>
* <span data-ttu-id="bf015-1628">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="bf015-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1629">Az.Sql</span></span>
* <span data-ttu-id="bf015-1630">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="bf015-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bf015-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1631">Az.Storage</span></span>
* <span data-ttu-id="bf015-1632">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="bf015-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="bf015-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf015-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="bf015-1634">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="bf015-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="bf015-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bf015-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1636">Az.Websites</span></span>
* <span data-ttu-id="bf015-1637">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="bf015-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="bf015-1638">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="bf015-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="bf015-1639">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="bf015-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="bf015-1640">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="bf015-1640">General</span></span>

- <span data-ttu-id="bf015-1641">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="bf015-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="bf015-1642">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1642">Online help for each module</span></span>
- <span data-ttu-id="bf015-1643">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="bf015-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="bf015-1644">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="bf015-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1645">Az.Accounts</span></span>
- <span data-ttu-id="bf015-1646">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="bf015-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="bf015-1647">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bf015-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf015-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="bf015-1649">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="bf015-1649">Fixes for #7002</span></span>
- <span data-ttu-id="bf015-1650">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="bf015-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bf015-1651">Az.Batch</span></span>
- <span data-ttu-id="bf015-1652">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="bf015-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="bf015-1653">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="bf015-1654">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="bf015-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="bf015-1655">Az.Billing</span></span>
- <span data-ttu-id="bf015-1656">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="bf015-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="bf015-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="bf015-1658">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="bf015-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="bf015-1659">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="bf015-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bf015-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="bf015-1661">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="bf015-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="bf015-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="bf015-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="bf015-1663">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="bf015-1665">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="bf015-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bf015-1666">Az.Monitor</span></span>
- <span data-ttu-id="bf015-1667">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="bf015-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bf015-1668">Az.KeyVault</span></span>
- <span data-ttu-id="bf015-1669">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="bf015-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bf015-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="bf015-1671">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="bf015-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="bf015-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bf015-1672">Az.Media</span></span>
- <span data-ttu-id="bf015-1673">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="bf015-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bf015-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1674">Az.Network</span></span>
<span data-ttu-id="bf015-1675">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="bf015-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="bf015-1676">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bf015-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="bf015-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf015-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf015-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf015-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf015-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bf015-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="bf015-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bf015-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="bf015-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf015-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="bf015-1685">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="bf015-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf015-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="bf015-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bf015-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf015-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bf015-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="bf015-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="bf015-1691">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="bf015-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="bf015-1692">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf015-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="bf015-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf015-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bf015-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf015-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bf015-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf015-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="bf015-1696">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="bf015-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="bf015-1697">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="bf015-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="bf015-1699">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="bf015-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bf015-1700">Az.Profile</span></span>
- <span data-ttu-id="bf015-1701">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bf015-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="bf015-1703">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="bf015-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1704">Az.Resources</span></span>
- <span data-ttu-id="bf015-1705">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bf015-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="bf015-1707">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="bf015-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="bf015-1708">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="bf015-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="bf015-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="bf015-1710">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="bf015-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="bf015-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1711">Az.Sql</span></span>
- <span data-ttu-id="bf015-1712">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="bf015-1713">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="bf015-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="bf015-1714">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="bf015-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1715">Az.Storage</span></span>
- <span data-ttu-id="bf015-1716">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bf015-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1717">Az.Websites</span></span>
- <span data-ttu-id="bf015-1718">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bf015-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="bf015-1719">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="bf015-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="bf015-1720">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="bf015-1720">General</span></span>

* <span data-ttu-id="bf015-1721">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="bf015-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1722">Az.Compute</span></span>

* <span data-ttu-id="bf015-1723">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="bf015-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="bf015-1725">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="bf015-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="bf015-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bf015-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="bf015-1727">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="bf015-1728">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="bf015-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="bf015-1729">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="bf015-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bf015-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="bf015-1731">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="bf015-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="bf015-1732">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="bf015-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="bf015-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1733">Az.Resources</span></span>

* <span data-ttu-id="bf015-1734">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="bf015-1735">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="bf015-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="bf015-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1736">Az.Sql</span></span>

* <span data-ttu-id="bf015-1737">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="bf015-1738">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="bf015-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="bf015-1739">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="bf015-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="bf015-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1740">Az.Storage</span></span>

* <span data-ttu-id="bf015-1741">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="bf015-1742">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="bf015-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="bf015-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bf015-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bf015-1744">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="bf015-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bf015-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="bf015-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bf015-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bf015-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1747">Az.Websites</span></span>

* <span data-ttu-id="bf015-1748">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bf015-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="bf015-1749">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="bf015-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="bf015-1750">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="bf015-1751">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="bf015-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bf015-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bf015-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="bf015-1753">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="bf015-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bf015-1754">Az.Automation</span></span>
* <span data-ttu-id="bf015-1755">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="bf015-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="bf015-1756">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="bf015-1757">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="bf015-1758">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="bf015-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="bf015-1759">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="bf015-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="bf015-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1760">Az.Compute</span></span>
* <span data-ttu-id="bf015-1761">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="bf015-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="bf015-1762">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bf015-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="bf015-1764">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="bf015-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bf015-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bf015-1766">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="bf015-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bf015-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1767">Az.Network</span></span>
* <span data-ttu-id="bf015-1768">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="bf015-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="bf015-1769">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="bf015-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="bf015-1770">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="bf015-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="bf015-1771">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="bf015-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="bf015-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bf015-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bf015-1773">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="bf015-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="bf015-1774">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="bf015-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="bf015-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="bf015-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="bf015-1776">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="bf015-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="bf015-1777">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="bf015-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bf015-1778">Az.Relay</span></span>
* <span data-ttu-id="bf015-1779">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="bf015-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1780">Az.Resources</span></span>
* <span data-ttu-id="bf015-1781">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="bf015-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="bf015-1782">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="bf015-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="bf015-1783">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="bf015-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bf015-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-1785">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="bf015-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1786">Az.Sql</span></span>
* <span data-ttu-id="bf015-1787">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="bf015-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="bf015-1788">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf015-1789">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf015-1790">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf015-1791">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bf015-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bf015-1792">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf015-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bf015-1793">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf015-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bf015-1794">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf015-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bf015-1795">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bf015-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="bf015-1796">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="bf015-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="bf015-1797">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="bf015-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="bf015-1798">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="bf015-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="bf015-1799">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="bf015-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bf015-1800">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="bf015-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bf015-1801">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="bf015-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="bf015-1802">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="bf015-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="bf015-1803">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="bf015-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="bf015-1804">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="bf015-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bf015-1805">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="bf015-1805">General</span></span>
* <span data-ttu-id="bf015-1806">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="bf015-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="bf015-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bf015-1807">Az.Profile</span></span>
* <span data-ttu-id="bf015-1808">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="bf015-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="bf015-1809">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="bf015-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="bf015-1810">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="bf015-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="bf015-1811">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="bf015-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="bf015-1812">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="bf015-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="bf015-1813">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="bf015-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="bf015-1814">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="bf015-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="bf015-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf015-1816">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="bf015-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1817">Az.Compute</span></span>
* <span data-ttu-id="bf015-1818">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="bf015-1819">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="bf015-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="bf015-1820">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-1822">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="bf015-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="bf015-1823">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="bf015-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="bf015-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="bf015-1824">Az.Insights</span></span>
* <span data-ttu-id="bf015-1825">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="bf015-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="bf015-1826">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="bf015-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="bf015-1827">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="bf015-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="bf015-1828">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="bf015-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1829">Az.Network</span></span>
* <span data-ttu-id="bf015-1830">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="bf015-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="bf015-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf015-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="bf015-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bf015-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="bf015-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bf015-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="bf015-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="bf015-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="bf015-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="bf015-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="bf015-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bf015-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bf015-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bf015-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="bf015-1838">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1839">Az.Resources</span></span>
* <span data-ttu-id="bf015-1840">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="bf015-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="bf015-1841">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="bf015-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bf015-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bf015-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="bf015-1843">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="bf015-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bf015-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bf015-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="bf015-1845">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="bf015-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="bf015-1846">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="bf015-1847">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="bf015-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="bf015-1848">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="bf015-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="bf015-1849">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="bf015-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="bf015-1850">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="bf015-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="bf015-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bf015-1851">Az.Profile</span></span>
* <span data-ttu-id="bf015-1852">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="bf015-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="bf015-1853">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="bf015-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1854">Az.Compute</span></span>
* <span data-ttu-id="bf015-1855">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="bf015-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="bf015-1856">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bf015-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf015-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="bf015-1858">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="bf015-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="bf015-1859">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="bf015-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="bf015-1860">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="bf015-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bf015-1861">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="bf015-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bf015-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="bf015-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1863">Az.Network</span></span>
* <span data-ttu-id="bf015-1864">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="bf015-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="bf015-1865">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="bf015-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1866">Az.Resources</span></span>
* <span data-ttu-id="bf015-1867">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="bf015-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="bf015-1868">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="bf015-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="bf015-1869">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="bf015-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="bf015-1870">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="bf015-1870">Azure.Storage</span></span>
* <span data-ttu-id="bf015-1871">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="bf015-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="bf015-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bf015-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="bf015-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bf015-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bf015-1874">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="bf015-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="bf015-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="bf015-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="bf015-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bf015-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="bf015-1877">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="bf015-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bf015-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bf015-1878">Az.Compute</span></span>
* <span data-ttu-id="bf015-1879">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="bf015-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="bf015-1880">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="bf015-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="bf015-1881">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="bf015-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="bf015-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bf015-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="bf015-1883">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="bf015-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bf015-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bf015-1884">Az.Network</span></span>
* <span data-ttu-id="bf015-1885">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="bf015-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="bf015-1886">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="bf015-1886">new cmdlets added</span></span>
    - <span data-ttu-id="bf015-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf015-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf015-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf015-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf015-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf015-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf015-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bf015-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="bf015-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="bf015-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf015-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="bf015-1893">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="bf015-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="bf015-1894">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="bf015-1895">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="bf015-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bf015-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bf015-1896">Az.RedisCache</span></span>
* <span data-ttu-id="bf015-1897">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="bf015-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="bf015-1898">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="bf015-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bf015-1899">Az.Resources</span></span>
* <span data-ttu-id="bf015-1900">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="bf015-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bf015-1901">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="bf015-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="bf015-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bf015-1902">Az.Sql</span></span>
* <span data-ttu-id="bf015-1903">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="bf015-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bf015-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bf015-1904">Az.Websites</span></span>
* <span data-ttu-id="bf015-1905">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="bf015-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="bf015-1906">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="bf015-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="bf015-1907">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="bf015-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="bf015-1908">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="bf015-1908">Initial Release</span></span>
