---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 189b360f8825b7de93b67b0b2cbe670d00187327
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241355"
---
# <a name="release-notes"></a><span data-ttu-id="b945e-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="b945e-103">Release notes</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="b945e-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="b945e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="b945e-105">6.13.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="b945e-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-106">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-107">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b945e-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b945e-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b945e-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b945e-109">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b945e-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b945e-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b945e-110">AzureRM.Automation</span></span>
* <span data-ttu-id="b945e-111">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="b945e-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b945e-112">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b945e-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b945e-113">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b945e-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b945e-114">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="b945e-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b945e-115">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="b945e-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-116">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-117">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="b945e-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b945e-118">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b945e-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="b945e-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b945e-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="b945e-120">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b945e-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="b945e-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b945e-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="b945e-122">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="b945e-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-123">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-124">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="b945e-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b945e-125">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="b945e-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b945e-126">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="b945e-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="b945e-127">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="b945e-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b945e-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b945e-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b945e-129">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="b945e-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b945e-130">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="b945e-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b945e-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b945e-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b945e-132">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="b945e-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b945e-133">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="b945e-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b945e-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b945e-134">AzureRM.Relay</span></span>
* <span data-ttu-id="b945e-135">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="b945e-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-136">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-137">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="b945e-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b945e-138">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="b945e-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b945e-139">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="b945e-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b945e-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b945e-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b945e-141">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b945e-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-142">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-143">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="b945e-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b945e-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b945e-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b945e-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b945e-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b945e-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b945e-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b945e-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b945e-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b945e-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b945e-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b945e-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b945e-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b945e-152">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="b945e-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b945e-153">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="b945e-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b945e-154">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="b945e-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b945e-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b945e-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b945e-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b945e-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b945e-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b945e-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b945e-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b945e-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b945e-159">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="b945e-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="b945e-160">6.12.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="b945e-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-161">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-162">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b945e-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b945e-163">A TenantId paraméter a Connect-AzureRmAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="b945e-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b945e-164">Frissítve lett a TenantId leírása a Connect-AzureRmAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="b945e-165">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="b945e-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b945e-166">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="b945e-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b945e-167">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="b945e-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b945e-168">Javítva lett az a probléma, amely miatt a „Disconnect-AzureRmAccount” jelenik meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="b945e-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="b945e-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b945e-169">AzureRM.Automation</span></span>
* <span data-ttu-id="b945e-170">A parancsmag DLL-fájlja át lett nevezve a következőre: Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="b945e-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="b945e-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b945e-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="b945e-172">Hozzá lett adva a Get-AzureRmCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="b945e-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-173">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-174">Hozzá lett adva az Add-AzureRmVmssVMDataDisk és a Remove-AzureRmVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="b945e-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b945e-175">A Get-AzureRmVMImage megjeleníti a következőt: AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b945e-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b945e-176">Javítva lett az a probléma, amely miatt a SetAzureRmVMChefExtension -BootstrapOptions és -JsonAttribute beállítások értékei nem json formátumban lettek beállítva.</span><span class="sxs-lookup"><span data-stu-id="b945e-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b945e-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b945e-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b945e-178">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="b945e-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b945e-179">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="b945e-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b945e-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b945e-180">AzureRM.Insights</span></span>
* <span data-ttu-id="b945e-181">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="b945e-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b945e-182">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="b945e-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b945e-183">Javítva lett a 7513-as hiba [Insights] A Set-AzureRmDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="b945e-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b945e-184">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="b945e-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-185">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-186">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="b945e-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b945e-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b945e-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b945e-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b945e-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b945e-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b945e-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b945e-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b945e-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b945e-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b945e-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b945e-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b945e-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b945e-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b945e-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b945e-194">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b945e-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b945e-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b945e-196">Hozzá lett adva az Azure-fájlmegosztások támogatása a Recovery Servicesben.</span><span class="sxs-lookup"><span data-stu-id="b945e-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-197">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-198">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="b945e-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b945e-199">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzureRmResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="b945e-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-201">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="b945e-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b945e-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b945e-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b945e-203">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="b945e-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b945e-204">Javítva lett az Add-AzureRmServiceFabricClusterCertificate parancsmag</span><span class="sxs-lookup"><span data-stu-id="b945e-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b945e-205">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b945e-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b945e-206">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b945e-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b945e-207">Javítva lett az Update-AzureRmServiceFabricDurability parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="b945e-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="b945e-208">6.11.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="b945e-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-209">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-210">Ki lett javítva a Get-AzureRmSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="b945e-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="b945e-211">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="b945e-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="b945e-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="b945e-212">AzureRM.Backup</span></span>
* <span data-ttu-id="b945e-213">Elavult Azure Backup-parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="b945e-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-214">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-215">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a New-AzureRmVm parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="b945e-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="b945e-216">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b945e-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b945e-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b945e-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b945e-218">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="b945e-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b945e-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="b945e-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b945e-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b945e-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="b945e-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b945e-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="b945e-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-223">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-224">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="b945e-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b945e-225">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="b945e-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-226">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-227">Egy értelmezhető kivétel forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat eseteket, amelyekben a Get-AzureRMRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="b945e-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b945e-228">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="b945e-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="b945e-229">6.10.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="b945e-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b945e-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-230">Azure.Storage</span></span>
* <span data-ttu-id="b945e-231">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="b945e-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b945e-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b945e-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b945e-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b945e-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="b945e-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b945e-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="b945e-235">A Get-AzureRmCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="b945e-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-236">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-237">Ki lett javítva a Get-AzureRmVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon</span><span class="sxs-lookup"><span data-stu-id="b945e-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b945e-238">A SimpleParameterSet egy példája hozzá lett adva a New-AzureRmVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="b945e-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="b945e-239">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="b945e-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b945e-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b945e-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b945e-241">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="b945e-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-242">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-243">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="b945e-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b945e-244">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-244">new cmdlets added</span></span>
    - <span data-ttu-id="b945e-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b945e-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b945e-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b945e-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b945e-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b945e-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b945e-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b945e-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b945e-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="b945e-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b945e-251">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="b945e-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b945e-252">Hozzá lett adva a New-AzureRmVirtualNetworkTap, a Get-AzureRmVirtualNetworkTap, a Set-AzureRmVirtualNetworkTap és a Remove-AzureRmVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="b945e-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="b945e-253">Hozzá lett adva a Set-AzureRmNEtworkInterfaceTapConfig, a Get-AzureRmNEtworkInterfaceTapConfig és a Remove-AzureRmNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="b945e-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b945e-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b945e-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b945e-255">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="b945e-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b945e-256">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="b945e-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-257">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-258">A hiányzó -Mode paraméter hozzá lett adva a Set-AzureRmPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="b945e-259">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzureRmProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="b945e-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b945e-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-260">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-261">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="b945e-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b945e-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-262">AzureRM.Storage</span></span>
* <span data-ttu-id="b945e-263">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="b945e-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b945e-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b945e-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b945e-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b945e-265">AzureRM.Websites</span></span>
* <span data-ttu-id="b945e-266">Új Get-AzureRMWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhook URL-címét</span><span class="sxs-lookup"><span data-stu-id="b945e-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b945e-267">Új New-AzureRMWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="b945e-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="b945e-268">6.9.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="b945e-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b945e-269">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b945e-269">General</span></span>
* <span data-ttu-id="b945e-270">Az AzureRM.SignalR hozzáadva az AzureRM összesített modulhoz</span><span class="sxs-lookup"><span data-stu-id="b945e-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b945e-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-271">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-272">Kisebb módosítások a tárolók általános kódjában</span><span class="sxs-lookup"><span data-stu-id="b945e-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="b945e-273">Teljes paramétertípusokkal frissült súgófájlok</span><span class="sxs-lookup"><span data-stu-id="b945e-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="b945e-274">A -ServicePrincipal módosítása nem kötelezőre a ServicePrincipalCertificateWithSubscriptionId paraméterkészletben</span><span class="sxs-lookup"><span data-stu-id="b945e-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b945e-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-275">Azure.Storage</span></span>
* <span data-ttu-id="b945e-276">Storage-környezet létrehozásának támogatása OAuth használatával.</span><span class="sxs-lookup"><span data-stu-id="b945e-276">Support create Storage Context with OAuth.</span></span>
    - <span data-ttu-id="b945e-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b945e-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="b945e-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="b945e-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="b945e-279">Standard_Microsoft hozzáadva a CDN-díjszabási termékváltozatban.</span><span class="sxs-lookup"><span data-stu-id="b945e-279">Added Standard_Microsoft in Cdn pricing sku.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-280">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-281">A Key Vault és a Storage függőségeinek áthelyezése az általános függőségekhez</span><span class="sxs-lookup"><span data-stu-id="b945e-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="b945e-282">További virtuálisgép-méretek támogatása hozzáadva az AEM-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b945e-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="b945e-283">A PublicIPPrefix paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b945e-284">A ResourceId paraméter hozzáadva az Invoke-AzureRmVMRunCommand parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="b945e-285">Az Invoke-AzureRmVmssVMRunCommand parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="b945e-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b945e-286">AzureRM.Dns</span></span>
* <span data-ttu-id="b945e-287">Aliasrekord támogatása hozzáadva DNS-rekord létrehozása során</span><span class="sxs-lookup"><span data-stu-id="b945e-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b945e-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b945e-288">AzureRM.Insights</span></span>
* <span data-ttu-id="b945e-289">A 6833-as és a 7102-es hiba kijavítva (Diagnosztikai beállítások területe)</span><span class="sxs-lookup"><span data-stu-id="b945e-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="b945e-290">Az alapértelmezett név, például a „service” hibái a diagnosztikai beállítások megadása és listázása/lekérése során</span><span class="sxs-lookup"><span data-stu-id="b945e-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="b945e-291">Diagnosztikai beállítások kategóriákkal történő létrehozásának hibái</span><span class="sxs-lookup"><span data-stu-id="b945e-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="b945e-292">Elavulási üzenetek hozzáadva a metrikák időfelbontási szintjeinek paramétereihez</span><span class="sxs-lookup"><span data-stu-id="b945e-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="b945e-293">Az időfelbontási szintek paramétereit még elfogadja a rendszer (ez nem egy kompatibilitástörő változás), viszont figyelmen kívül hagyja a háttérrendszerben, mivel csak a PT1M érvényes</span><span class="sxs-lookup"><span data-stu-id="b945e-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-294">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-295">A LoadBalancer parancsmagokat érintő változások</span><span class="sxs-lookup"><span data-stu-id="b945e-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="b945e-296">LoadBalancerInboundNatPoolConfig: az IdleTimeoutInMinutes, az EnableFloatingIp és az EnableTcpReset paraméterek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="b945e-297">LoadBalancerInboundNatRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="b945e-298">LoadBalancerRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="b945e-299">LoadBalancerProbeConfig: a Protocol paraméterhez tartozó „Https” érték támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="b945e-300">Új parancsok hozzáadva a LoadBalancer új, OutboundRule nevű alerőforrásához</span><span class="sxs-lookup"><span data-stu-id="b945e-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="b945e-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b945e-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b945e-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b945e-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b945e-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="b945e-306">Új HostedWorkloads tulajdonság hozzáadva a PSNetworkInterface-hez</span><span class="sxs-lookup"><span data-stu-id="b945e-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="b945e-307">Új parancsmagok hozzáadva a következő szolgáltatáshoz: Azure Firewall ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="b945e-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="b945e-308">Get-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="b945e-309">Set-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="b945e-310">New-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="b945e-311">Remove-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="b945e-312">New-AzureRmFirewallApplicationRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="b945e-313">New-AzureRmFirewallApplicationRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="b945e-314">New-AzureRmFirewallNatRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="b945e-315">New-AzureRmFirewallNatRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="b945e-316">New-AzureRmFirewallNetworkRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="b945e-317">New-AzureRmFirewallNetworkRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="b945e-318">Támogatás hozzáadva a megbízható főtanúsítványokhoz és az automatikus skálázás konfigurálásához az Application Gatewayben</span><span class="sxs-lookup"><span data-stu-id="b945e-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="b945e-319">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b945e-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="b945e-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b945e-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b945e-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b945e-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b945e-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b945e-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="b945e-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="b945e-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="b945e-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="b945e-329">Parancsmagok frissítve a -TrustedRootCertificate nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b945e-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="b945e-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b945e-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="b945e-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b945e-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="b945e-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b945e-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="b945e-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b945e-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="b945e-334">Parancsmagok frissítve az -AutoscaleConfiguration nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b945e-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="b945e-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b945e-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="b945e-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b945e-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="b945e-337">A Get-AzureInterfaceEndpoint parancsmag hozzáadva a felhasználói felület végpontjához</span><span class="sxs-lookup"><span data-stu-id="b945e-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="b945e-338">Támogatás hozzáadva több címelőtaghoz egy alhálózaton belül</span><span class="sxs-lookup"><span data-stu-id="b945e-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="b945e-339">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b945e-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="b945e-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b945e-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b945e-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b945e-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b945e-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="b945e-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="b945e-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="b945e-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="b945e-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="b945e-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="b945e-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="b945e-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="b945e-352">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="b945e-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="b945e-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="b945e-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="b945e-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="b945e-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="b945e-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b945e-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="b945e-359">Alhálózat-delegálási parancsmagok hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b945e-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="b945e-360">New-AzureRmDelegation: Létrehoz egy új delegálást, amelyet hozzá lehet adni egy alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="b945e-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="b945e-361">Remove-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott delegálási nevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="b945e-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="b945e-362">Add-AzureRmDelegation: Felvesz egy alhálózatot, és hozzáadja a megadott szolgáltatásnevet delegálásként az adott alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="b945e-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="b945e-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="b945e-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="b945e-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="b945e-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b945e-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b945e-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b945e-366">A felügyelt lemezek támogatása</span><span class="sxs-lookup"><span data-stu-id="b945e-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b945e-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b945e-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b945e-368">Insights-függőség frissítve</span><span class="sxs-lookup"><span data-stu-id="b945e-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-369">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-370">A New-AzureRmResourceGroupDeployment frissítve az új RollbackAction paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b945e-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="b945e-371">Az OnErrorDeployment támogatása az új paraméterrel</span><span class="sxs-lookup"><span data-stu-id="b945e-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="b945e-372">A felügyelt identitás támogatása a szabályzat-hozzárendeléseknél</span><span class="sxs-lookup"><span data-stu-id="b945e-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="b945e-373">Az alapértelmezett értékekkel rendelkező paraméterek már nem szükségesek a szabályzatok a New-AzureRmPolicyAssignmenttel történő hozzárendelésekor</span><span class="sxs-lookup"><span data-stu-id="b945e-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="b945e-374">Az új Get-AzureRmPolicyAlias parancsmag hozzáadva a szabályzataliasok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="b945e-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-376">A 7161-es hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="b945e-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="b945e-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="b945e-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="b945e-378">Termékváltozatnevek frissítve Free_F1-re és Standard_S1-re</span><span class="sxs-lookup"><span data-stu-id="b945e-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="b945e-379">Verzió mező hozzáadva a PSSignalRResource objektumhoz, és kapcsolati sztring hozzáadva a PSSignalRKeys objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b945e-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-380">AzureRM.Storage</span></span>
* <span data-ttu-id="b945e-381">Módosíthatatlansági szabályzat támogatva az AzureRM.Storage-ban</span><span class="sxs-lookup"><span data-stu-id="b945e-381">Support Immutability Policy in AzureRm.Storage</span></span>
    - <span data-ttu-id="b945e-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b945e-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="b945e-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b945e-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b945e-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b945e-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b945e-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b945e-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b945e-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b945e-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b945e-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="b945e-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="b945e-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="b945e-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="b945e-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b945e-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="b945e-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b945e-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="b945e-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b945e-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="b945e-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b945e-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b945e-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b945e-393">AzureRM.Websites</span></span>
* <span data-ttu-id="b945e-394">Két új parancsmag hozzáadva: Get-AzureRmDeletedWebApp és Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b945e-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="b945e-395">A New-AzureRmAppServicePlan -HyperV kapcsoló hozzáadva App Service-csomag létrehozásához Windows-tárolóval</span><span class="sxs-lookup"><span data-stu-id="b945e-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="b945e-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot – Új paraméterek (–ContainerRegistryUser sztring -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) hozzáadva Windows-tárolóalkalmazás létrehozásához és felügyeletéhez</span><span class="sxs-lookup"><span data-stu-id="b945e-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="b945e-397">6.8.1 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="b945e-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b945e-398">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b945e-398">General</span></span>
* <span data-ttu-id="b945e-399">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b945e-400">Frissített közös futtatókörnyezeti szerelvények</span><span class="sxs-lookup"><span data-stu-id="b945e-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b945e-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b945e-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b945e-402">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b945e-403">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="b945e-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="b945e-404">Az Import-AzureRmApiManagementApi és az \*-AzureRmApiManagementCertificate parancsmagok már tudják kezelni a relatív elérési utakat</span><span class="sxs-lookup"><span data-stu-id="b945e-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="b945e-405">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="b945e-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="b945e-406">A CertificateInformation egy beállítható tulajdonság, amely a Set-AzureRmApiManagement parancsmag megfelelő működését biztosítja.</span><span class="sxs-lookup"><span data-stu-id="b945e-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="b945e-407">Javítva a nuget 4.0.4-es előzetes verziójára való frissítéssel</span><span class="sxs-lookup"><span data-stu-id="b945e-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="b945e-408">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="b945e-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="b945e-409">A termékben való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="b945e-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="b945e-410">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="b945e-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="b945e-411">Az API-ban való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="b945e-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="b945e-412">Az AzureMonitor támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="b945e-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-413">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-414">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="b945e-415">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="b945e-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="b945e-416">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b945e-417">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="b945e-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-418">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-419">A parancsmagkimenetek alapértelmezett ábrázolása táblanézetre módosítva</span><span class="sxs-lookup"><span data-stu-id="b945e-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b945e-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b945e-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b945e-421">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="b945e-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="b945e-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-422">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-423">Ki lett javítva a felügyelt alkalmazások Marketplace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-425">Hibák kijavítva:</span><span class="sxs-lookup"><span data-stu-id="b945e-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b945e-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b945e-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b945e-427">A MultiValue útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="b945e-428">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="b945e-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="b945e-429">Az alhálózati útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="b945e-430">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="b945e-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="b945e-431">Egyéni fejlécek profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="b945e-432">Várt állapotkód-tartományok profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="b945e-433">Egyéni fejlécek végpontokon való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="b945e-434">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="b945e-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b945e-435">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b945e-435">General</span></span>
* <span data-ttu-id="b945e-436">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b945e-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-437">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-438">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="b945e-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-439">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-440">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="b945e-441">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="b945e-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="b945e-442">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="b945e-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="b945e-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b945e-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="b945e-444">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="b945e-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-445">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-446">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="b945e-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b945e-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b945e-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b945e-448">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="b945e-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-449">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-450">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-452">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="b945e-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b945e-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b945e-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b945e-454">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="b945e-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="b945e-455">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="b945e-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="b945e-456">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="b945e-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="b945e-457">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="b945e-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="b945e-458">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="b945e-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="b945e-459">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="b945e-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="b945e-460">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="b945e-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b945e-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b945e-461">AzureRM.Websites</span></span>
* <span data-ttu-id="b945e-462">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="b945e-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="b945e-463">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="b945e-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-464">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-465">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b945e-466">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="b945e-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="b945e-467">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="b945e-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="b945e-468">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="b945e-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-469">Azure.Storage</span></span>
* <span data-ttu-id="b945e-470">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="b945e-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b945e-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b945e-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b945e-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b945e-473">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="b945e-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b945e-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="b945e-475">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b945e-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b945e-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b945e-477">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="b945e-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b945e-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="b945e-479">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b945e-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b945e-480">AzureRM.Automation</span></span>
* <span data-ttu-id="b945e-481">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="b945e-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="b945e-482">AzureRM.Backup</span></span>
* <span data-ttu-id="b945e-483">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b945e-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b945e-484">AzureRM.Batch</span></span>
* <span data-ttu-id="b945e-485">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="b945e-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="b945e-486">AzureRM.Billing</span></span>
* <span data-ttu-id="b945e-487">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="b945e-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="b945e-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="b945e-489">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="b945e-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b945e-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="b945e-491">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-492">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-493">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b945e-494">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="b945e-495">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="b945e-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="b945e-496">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b945e-497">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="b945e-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b945e-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b945e-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="b945e-499">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="b945e-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b945e-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="b945e-501">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="b945e-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b945e-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="b945e-503">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="b945e-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="b945e-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="b945e-505">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b945e-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b945e-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b945e-507">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b945e-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b945e-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b945e-509">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b945e-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b945e-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b945e-511">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="b945e-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="b945e-512">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b945e-513">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b945e-514">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="b945e-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="b945e-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="b945e-516">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="b945e-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b945e-517">AzureRM.Dns</span></span>
* <span data-ttu-id="b945e-518">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b945e-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b945e-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b945e-520">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b945e-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b945e-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="b945e-522">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="b945e-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b945e-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="b945e-524">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b945e-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b945e-525">AzureRM.Insights</span></span>
* <span data-ttu-id="b945e-526">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="b945e-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b945e-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="b945e-528">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b945e-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b945e-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b945e-530">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b945e-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b945e-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b945e-532">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="b945e-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b945e-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="b945e-534">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="b945e-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b945e-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="b945e-536">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="b945e-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b945e-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="b945e-538">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="b945e-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="b945e-539">AzureRM.Media</span></span>
* <span data-ttu-id="b945e-540">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-541">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-542">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="b945e-543">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b945e-544">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="b945e-545">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b945e-546">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b945e-547">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b945e-548">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="b945e-549">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="b945e-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="b945e-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b945e-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="b945e-551">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="b945e-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b945e-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b945e-553">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b945e-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b945e-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b945e-555">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b945e-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b945e-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b945e-557">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="b945e-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b945e-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="b945e-559">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b945e-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b945e-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b945e-561">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="b945e-562">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="b945e-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="b945e-563">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="b945e-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="b945e-564">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b945e-565">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="b945e-566">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="b945e-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="b945e-567">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="b945e-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b945e-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b945e-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b945e-569">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b945e-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b945e-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b945e-571">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b945e-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b945e-572">AzureRM.Relay</span></span>
* <span data-ttu-id="b945e-573">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-574">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-575">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="b945e-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="b945e-576">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b945e-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="b945e-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b945e-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="b945e-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b945e-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="b945e-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b945e-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="b945e-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b945e-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="b945e-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b945e-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="b945e-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b945e-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="b945e-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="b945e-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="b945e-584">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="b945e-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="b945e-585">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="b945e-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="b945e-586">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b945e-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b945e-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b945e-588">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-590">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b945e-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b945e-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b945e-592">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b945e-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-593">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-594">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b945e-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-595">AzureRM.Storage</span></span>
* <span data-ttu-id="b945e-596">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="b945e-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="b945e-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="b945e-598">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b945e-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b945e-599">AzureRM.Tags</span></span>
* <span data-ttu-id="b945e-600">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b945e-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b945e-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b945e-602">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="b945e-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="b945e-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="b945e-604">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b945e-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b945e-605">AzureRM.Websites</span></span>
* <span data-ttu-id="b945e-606">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="b945e-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="b945e-607">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="b945e-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b945e-608">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b945e-608">General</span></span>
* <span data-ttu-id="b945e-609">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="b945e-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b945e-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-610">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-611">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="b945e-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="b945e-612">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="b945e-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b945e-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-613">Azure.Storage</span></span>
* <span data-ttu-id="b945e-614">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="b945e-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="b945e-615">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b945e-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b945e-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b945e-617">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="b945e-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="b945e-618">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="b945e-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="b945e-619">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="b945e-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="b945e-620">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="b945e-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="b945e-621">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="b945e-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="b945e-622">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="b945e-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-623">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-624">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="b945e-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="b945e-625">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="b945e-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="b945e-626">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="b945e-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="b945e-627">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="b945e-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="b945e-628">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="b945e-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="b945e-629">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="b945e-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="b945e-630">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="b945e-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="b945e-631">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="b945e-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="b945e-632">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="b945e-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="b945e-633">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="b945e-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b945e-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b945e-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b945e-635">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="b945e-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="b945e-636">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="b945e-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="b945e-637">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="b945e-638">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b945e-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b945e-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b945e-640">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="b945e-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b945e-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b945e-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="b945e-642">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="b945e-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b945e-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b945e-643">AzureRM.Insights</span></span>
* <span data-ttu-id="b945e-644">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="b945e-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="b945e-645">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="b945e-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b945e-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b945e-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b945e-647">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="b945e-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-648">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-649">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-650">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-651">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="b945e-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="b945e-652">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="b945e-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-654">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="b945e-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="b945e-655">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="b945e-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="b945e-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-656">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-657">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="b945e-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="b945e-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b945e-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b945e-659">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="b945e-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="b945e-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="b945e-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="b945e-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="b945e-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="b945e-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="b945e-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="b945e-663">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="b945e-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="b945e-664">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="b945e-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b945e-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-665">AzureRM.Storage</span></span>
* <span data-ttu-id="b945e-666">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="b945e-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="b945e-667">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="b945e-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="b945e-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b945e-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b945e-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b945e-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b945e-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b945e-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b945e-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b945e-671">AzureRM.Tags</span></span>
* <span data-ttu-id="b945e-672">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="b945e-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="b945e-673">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="b945e-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-674">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-675">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b945e-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b945e-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-676">Azure.Storage</span></span>
* <span data-ttu-id="b945e-677">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="b945e-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="b945e-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b945e-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="b945e-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b945e-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b945e-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b945e-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b945e-681">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="b945e-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b945e-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b945e-682">AzureRM.Automation</span></span>
* <span data-ttu-id="b945e-683">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b945e-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-684">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-685">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b945e-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="b945e-686">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b945e-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b945e-687">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="b945e-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b945e-688">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="b945e-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="b945e-689">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="b945e-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b945e-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b945e-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="b945e-691">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="b945e-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b945e-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b945e-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b945e-693">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="b945e-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b945e-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b945e-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b945e-695">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b945e-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-696">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-697">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b945e-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="b945e-698">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="b945e-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="b945e-699">New-AzureRmApplicationGateway : EnableFIPS jelző és zónatámogatás hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="b945e-700">New-AzureRmApplicationGatewaySku : Új Standard_v2 és WAF_v2 SKU-k hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="b945e-701">Set-AzureRmApplicationGatewaySku : Új Standard_v2 és WAF_v2 SKU-k hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="b945e-702">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b945e-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b945e-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b945e-703">AzureRM.Relay</span></span>
* <span data-ttu-id="b945e-704">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="b945e-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-705">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-706">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="b945e-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="b945e-707">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="b945e-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="b945e-708">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="b945e-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="b945e-709">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="b945e-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="b945e-710">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="b945e-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-712">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="b945e-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="b945e-713">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="b945e-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="b945e-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b945e-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b945e-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b945e-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b945e-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b945e-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b945e-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b945e-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b945e-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b945e-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="b945e-719">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="b945e-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b945e-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b945e-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b945e-721">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="b945e-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b945e-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-722">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-723">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="b945e-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="b945e-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="b945e-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b945e-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b945e-726">AzureRM.Websites</span></span>
* <span data-ttu-id="b945e-727">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="b945e-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="b945e-728">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="b945e-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="b945e-729">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="b945e-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="b945e-730">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="b945e-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b945e-731">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="b945e-731">General</span></span>
* <span data-ttu-id="b945e-732">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="b945e-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b945e-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-733">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-734">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="b945e-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-735">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-736">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="b945e-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="b945e-737">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="b945e-738">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b945e-739">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="b945e-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="b945e-740">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="b945e-741">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="b945e-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="b945e-742">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b945e-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b945e-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b945e-744">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="b945e-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="b945e-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b945e-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b945e-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b945e-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b945e-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b945e-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b945e-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b945e-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b945e-749">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="b945e-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b945e-750">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="b945e-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b945e-751">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="b945e-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="b945e-752">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="b945e-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b945e-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b945e-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="b945e-754">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="b945e-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="b945e-755">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="b945e-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="b945e-756">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="b945e-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="b945e-757">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="b945e-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b945e-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b945e-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b945e-759">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="b945e-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-760">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-761">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="b945e-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="b945e-762">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="b945e-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="b945e-763">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b945e-764">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b945e-765">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b945e-766">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b945e-767">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b945e-768">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b945e-769">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b945e-770">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="b945e-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b945e-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b945e-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b945e-772">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="b945e-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="b945e-773">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="b945e-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="b945e-774">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="b945e-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-775">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-776">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="b945e-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="b945e-777">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="b945e-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="b945e-778">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="b945e-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="b945e-779">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="b945e-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="b945e-780">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b945e-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="b945e-781">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="b945e-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b945e-782">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="b945e-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b945e-783">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b945e-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="b945e-784">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="b945e-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b945e-785">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="b945e-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b945e-786">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b945e-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="b945e-787">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="b945e-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="b945e-788">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="b945e-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="b945e-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b945e-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b945e-790">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="b945e-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b945e-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-791">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-792">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="b945e-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="b945e-793">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="b945e-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="b945e-794">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="b945e-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-795">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-796">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="b945e-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="b945e-797">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="b945e-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b945e-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b945e-798">Azure.Storage</span></span>
* <span data-ttu-id="b945e-799">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="b945e-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-800">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-801">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="b945e-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span>
* <span data-ttu-id="b945e-802">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="b945e-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="b945e-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b945e-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b945e-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b945e-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b945e-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b945e-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b945e-806">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="b945e-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="b945e-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b945e-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="b945e-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b945e-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="b945e-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b945e-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="b945e-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b945e-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="b945e-811">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b945e-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="b945e-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b945e-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="b945e-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b945e-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="b945e-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b945e-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="b945e-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b945e-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="b945e-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b945e-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="b945e-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b945e-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="b945e-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b945e-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="b945e-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b945e-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="b945e-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b945e-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b945e-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b945e-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="b945e-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b945e-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b945e-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b945e-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="b945e-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b945e-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="b945e-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b945e-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b945e-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b945e-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b945e-827">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="b945e-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b945e-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b945e-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b945e-829">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="b945e-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b945e-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b945e-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b945e-831">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="b945e-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="b945e-832">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="b945e-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="b945e-833">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="b945e-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b945e-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b945e-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b945e-835">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="b945e-836">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b945e-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b945e-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-837">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-838">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="b945e-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b945e-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b945e-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b945e-840">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="b945e-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b945e-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b945e-841">AzureRM.Websites</span></span>
* <span data-ttu-id="b945e-842">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="b945e-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="b945e-843">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="b945e-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="b945e-844">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="b945e-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="b945e-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b945e-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b945e-846">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="b945e-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="b945e-847">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="b945e-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-848">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-849">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="b945e-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b945e-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b945e-850">AzureRM.Compute</span></span>
* <span data-ttu-id="b945e-851">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="b945e-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="b945e-852">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="b945e-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="b945e-853">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="b945e-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b945e-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b945e-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b945e-855">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="b945e-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="b945e-856">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="b945e-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="b945e-857">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="b945e-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="b945e-858">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="b945e-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="b945e-859">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="b945e-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="b945e-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b945e-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b945e-861">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="b945e-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="b945e-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-862">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-863">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="b945e-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b945e-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b945e-864">AzureRM.Resources</span></span>
* <span data-ttu-id="b945e-865">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="b945e-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b945e-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b945e-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b945e-867">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="b945e-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="b945e-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-868">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-869">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="b945e-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="b945e-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b945e-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b945e-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b945e-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b945e-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b945e-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b945e-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b945e-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b945e-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b945e-875">AzureRM.Websites</span></span>
* <span data-ttu-id="b945e-876">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="b945e-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="b945e-877">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="b945e-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b945e-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b945e-878">AzureRM.Profile</span></span>
* <span data-ttu-id="b945e-879">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="b945e-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b945e-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b945e-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b945e-881">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="b945e-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b945e-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b945e-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b945e-883">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="b945e-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="b945e-884">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="b945e-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="b945e-885">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="b945e-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="b945e-886">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="b945e-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="b945e-887">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="b945e-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="b945e-888">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="b945e-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="b945e-889">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="b945e-889">Added support for MSI identity</span></span>
* <span data-ttu-id="b945e-890">A szabályzatok URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="b945e-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="b945e-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="b945e-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="b945e-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="b945e-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="b945e-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="b945e-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b945e-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b945e-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b945e-895">AzureRM.Batch</span></span>
* <span data-ttu-id="b945e-896">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="b945e-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="b945e-897">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="b945e-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b945e-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b945e-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="b945e-899">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="b945e-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b945e-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b945e-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b945e-901">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="b945e-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b945e-902">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="b945e-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span>
* <span data-ttu-id="b945e-903">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="b945e-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b945e-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b945e-904">AzureRM.Network</span></span>
* <span data-ttu-id="b945e-905">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="b945e-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="b945e-906">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b945e-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="b945e-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b945e-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="b945e-908">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="b945e-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="b945e-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b945e-910">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="b945e-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="b945e-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b945e-912">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="b945e-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="b945e-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b945e-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b945e-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b945e-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b945e-915">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="b945e-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b945e-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b945e-916">AzureRM.Sql</span></span>
* <span data-ttu-id="b945e-917">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="b945e-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="b945e-918">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="b945e-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="b945e-919">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="b945e-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="b945e-920">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="b945e-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="b945e-921">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="b945e-921">The updated cmdlets including:</span></span>
    - <span data-ttu-id="b945e-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b945e-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b945e-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b945e-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b945e-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b945e-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b945e-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b945e-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b945e-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b945e-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b945e-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b945e-928">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="b945e-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
