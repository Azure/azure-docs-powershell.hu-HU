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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399059"
---
# <a name="release-notes"></a><span data-ttu-id="de67b-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="de67b-103">Release notes</span></span>

<span data-ttu-id="de67b-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="de67b-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="de67b-105">6.10.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="de67b-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="de67b-106">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-106">Azure.Storage</span></span>
* <span data-ttu-id="de67b-107">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="de67b-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="de67b-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="de67b-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="de67b-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="de67b-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="de67b-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="de67b-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="de67b-111">A Get-AzureRmCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="de67b-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-112">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-113">Ki lett javítva a Get-AzureRmVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon</span><span class="sxs-lookup"><span data-stu-id="de67b-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="de67b-114">A SimpleParameterSet egy példája hozzá lett adva a New-AzureRmVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="de67b-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="de67b-115">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="de67b-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="de67b-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="de67b-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="de67b-117">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="de67b-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-118">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-119">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="de67b-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="de67b-120">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-120">new cmdlets added</span></span>
    - <span data-ttu-id="de67b-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="de67b-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="de67b-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="de67b-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="de67b-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="de67b-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="de67b-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="de67b-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="de67b-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="de67b-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="de67b-127">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="de67b-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="de67b-128">Hozzá lett adva a New-AzureRmVirtualNetworkTap, a Get-AzureRmVirtualNetworkTap, a Set-AzureRmVirtualNetworkTap és a Remove-AzureRmVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="de67b-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="de67b-129">Hozzá lett adva a Set-AzureRmNEtworkInterfaceTapConfig, a Get-AzureRmNEtworkInterfaceTapConfig és a Remove-AzureRmNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="de67b-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="de67b-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="de67b-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="de67b-131">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="de67b-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="de67b-132">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="de67b-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-133">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-134">A hiányzó -Mode paraméter hozzá lett adva a Set-AzureRmPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="de67b-135">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzureRmProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="de67b-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="de67b-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-136">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-137">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="de67b-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="de67b-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-138">AzureRM.Storage</span></span>
* <span data-ttu-id="de67b-139">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="de67b-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="de67b-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="de67b-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="de67b-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="de67b-141">AzureRM.Websites</span></span>
* <span data-ttu-id="de67b-142">Új Get-AzureRMWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhook URL-címét</span><span class="sxs-lookup"><span data-stu-id="de67b-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="de67b-143">Új New-AzureRMWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="de67b-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="de67b-144">6.9.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="de67b-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="de67b-145">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="de67b-145">General</span></span>
* <span data-ttu-id="de67b-146">Az AzureRM.SignalR hozzáadva az AzureRM összesített modulhoz</span><span class="sxs-lookup"><span data-stu-id="de67b-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="de67b-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-147">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-148">Kisebb módosítások a tárolók általános kódjában</span><span class="sxs-lookup"><span data-stu-id="de67b-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="de67b-149">Teljes paramétertípusokkal frissült súgófájlok</span><span class="sxs-lookup"><span data-stu-id="de67b-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="de67b-150">A -ServicePrincipal módosítása nem kötelezőre a ServicePrincipalCertificateWithSubscriptionId paraméterkészletben</span><span class="sxs-lookup"><span data-stu-id="de67b-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="de67b-151">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-151">Azure.Storage</span></span>
* <span data-ttu-id="de67b-152">Storage-környezet létrehozásának támogatása OAuth használatával.</span><span class="sxs-lookup"><span data-stu-id="de67b-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="de67b-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="de67b-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="de67b-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="de67b-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="de67b-155">Standard_Microsoft hozzáadva a CDN-díjszabási termékváltozatban.</span><span class="sxs-lookup"><span data-stu-id="de67b-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-156">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-157">A Key Vault és a Storage függőségeinek áthelyezése az általános függőségekhez</span><span class="sxs-lookup"><span data-stu-id="de67b-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="de67b-158">További virtuálisgép-méretek támogatása hozzáadva az AEM-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="de67b-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="de67b-159">A PublicIPPrefix paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="de67b-160">A ResourceId paraméter hozzáadva az Invoke-AzureRmVMRunCommand parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="de67b-161">Az Invoke-AzureRmVmssVMRunCommand parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="de67b-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="de67b-162">AzureRM.Dns</span></span>
* <span data-ttu-id="de67b-163">Aliasrekord támogatása hozzáadva DNS-rekord létrehozása során</span><span class="sxs-lookup"><span data-stu-id="de67b-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="de67b-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="de67b-164">AzureRM.Insights</span></span>
* <span data-ttu-id="de67b-165">A 6833-as és a 7102-es hiba kijavítva (Diagnosztikai beállítások területe)</span><span class="sxs-lookup"><span data-stu-id="de67b-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="de67b-166">Az alapértelmezett név, például a „service” hibái a diagnosztikai beállítások megadása és listázása/lekérése során</span><span class="sxs-lookup"><span data-stu-id="de67b-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="de67b-167">Diagnosztikai beállítások kategóriákkal történő létrehozásának hibái</span><span class="sxs-lookup"><span data-stu-id="de67b-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="de67b-168">Elavulási üzenetek hozzáadva a metrikák időfelbontási szintjeinek paramétereihez</span><span class="sxs-lookup"><span data-stu-id="de67b-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="de67b-169">Az időfelbontási szintek paramétereit még elfogadja a rendszer (ez nem egy kompatibilitástörő változás), viszont figyelmen kívül hagyja a háttérrendszerben, mivel csak a PT1M érvényes</span><span class="sxs-lookup"><span data-stu-id="de67b-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-170">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-171">A LoadBalancer parancsmagokat érintő változások</span><span class="sxs-lookup"><span data-stu-id="de67b-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="de67b-172">LoadBalancerInboundNatPoolConfig: az IdleTimeoutInMinutes, az EnableFloatingIp és az EnableTcpReset paraméterek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="de67b-173">LoadBalancerInboundNatRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="de67b-174">LoadBalancerRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="de67b-175">LoadBalancerProbeConfig: a Protocol paraméterhez tartozó „Https” érték támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="de67b-176">Új parancsok hozzáadva a LoadBalancer új, OutboundRule nevű alerőforrásához</span><span class="sxs-lookup"><span data-stu-id="de67b-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="de67b-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="de67b-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="de67b-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="de67b-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="de67b-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="de67b-182">Új HostedWorkloads tulajdonság hozzáadva a PSNetworkInterface-hez</span><span class="sxs-lookup"><span data-stu-id="de67b-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="de67b-183">Új parancsmagok hozzáadva a következő szolgáltatáshoz: Azure Firewall ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="de67b-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="de67b-184">Get-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="de67b-185">Set-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="de67b-186">New-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="de67b-187">Remove-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="de67b-188">New-AzureRmFirewallApplicationRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="de67b-189">New-AzureRmFirewallApplicationRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="de67b-190">New-AzureRmFirewallNatRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="de67b-191">New-AzureRmFirewallNatRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="de67b-192">New-AzureRmFirewallNetworkRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="de67b-193">New-AzureRmFirewallNetworkRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="de67b-194">Támogatás hozzáadva a megbízható főtanúsítványokhoz és az automatikus skálázás konfigurálásához az Application Gatewayben</span><span class="sxs-lookup"><span data-stu-id="de67b-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="de67b-195">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="de67b-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="de67b-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="de67b-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="de67b-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="de67b-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="de67b-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="de67b-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="de67b-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="de67b-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="de67b-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="de67b-205">Parancsmagok frissítve a -TrustedRootCertificate nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="de67b-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="de67b-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de67b-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="de67b-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de67b-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="de67b-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="de67b-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="de67b-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="de67b-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="de67b-210">Parancsmagok frissítve az -AutoscaleConfiguration nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="de67b-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="de67b-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de67b-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="de67b-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de67b-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="de67b-213">A Get-AzureInterfaceEndpoint parancsmag hozzáadva a felhasználói felület végpontjához</span><span class="sxs-lookup"><span data-stu-id="de67b-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="de67b-214">Támogatás hozzáadva több címelőtaghoz egy alhálózaton belül</span><span class="sxs-lookup"><span data-stu-id="de67b-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="de67b-215">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="de67b-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="de67b-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="de67b-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="de67b-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="de67b-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="de67b-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="de67b-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="de67b-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="de67b-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="de67b-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="de67b-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="de67b-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="de67b-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="de67b-228">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="de67b-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="de67b-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="de67b-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="de67b-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="de67b-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="de67b-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de67b-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="de67b-235">Alhálózat-delegálási parancsmagok hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="de67b-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="de67b-236">New-AzureRmDelegation: Létrehoz egy új delegálást, amelyet hozzá lehet adni egy alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="de67b-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="de67b-237">Remove-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott delegálási nevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="de67b-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="de67b-238">Add-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott szolgáltatásnevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="de67b-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="de67b-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="de67b-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="de67b-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="de67b-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="de67b-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="de67b-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="de67b-242">A felügyelt lemezek támogatása</span><span class="sxs-lookup"><span data-stu-id="de67b-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="de67b-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="de67b-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="de67b-244">Insights-függőség frissítve</span><span class="sxs-lookup"><span data-stu-id="de67b-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-245">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-246">A New-AzureRmResourceGroupDeployment frissítve az új RollbackAction paraméterrel</span><span class="sxs-lookup"><span data-stu-id="de67b-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="de67b-247">Az OnErrorDeployment támogatása az új paraméterrel</span><span class="sxs-lookup"><span data-stu-id="de67b-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="de67b-248">A felügyelt identitás támogatása a szabályzat-hozzárendeléseknél</span><span class="sxs-lookup"><span data-stu-id="de67b-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="de67b-249">Az alapértelmezett értékekkel rendelkező paraméterek már nem szükségesek a szabályzatok a New-AzureRmPolicyAssignmenttel történő hozzárendelésekor</span><span class="sxs-lookup"><span data-stu-id="de67b-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="de67b-250">Az új Get-AzureRmPolicyAlias parancsmag hozzáadva a szabályzataliasok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="de67b-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="de67b-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de67b-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="de67b-252">A 7161-es hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="de67b-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="de67b-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="de67b-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="de67b-254">Termékváltozatnevek frissítve Free_F1-re és Standard_S1-re</span><span class="sxs-lookup"><span data-stu-id="de67b-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="de67b-255">Verzió mező hozzáadva a PSSignalRResource objektumhoz, és kapcsolati sztring hozzáadva a PSSignalRKeys objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="de67b-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-256">AzureRM.Storage</span></span>
* <span data-ttu-id="de67b-257">Módosíthatatlansági szabályzat támogatva az AzureRM.Storage-ban</span><span class="sxs-lookup"><span data-stu-id="de67b-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="de67b-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="de67b-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="de67b-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="de67b-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="de67b-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="de67b-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="de67b-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="de67b-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="de67b-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="de67b-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="de67b-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="de67b-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="de67b-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="de67b-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="de67b-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="de67b-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="de67b-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="de67b-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="de67b-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="de67b-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="de67b-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="de67b-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="de67b-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="de67b-269">AzureRM.Websites</span></span>
* <span data-ttu-id="de67b-270">Két új parancsmag hozzáadva: Get-AzureRmDeletedWebApp és Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="de67b-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="de67b-271">A New-AzureRmAppServicePlan -HyperV kapcsoló hozzáadva App Service-csomag létrehozásához Windows-tárolóval</span><span class="sxs-lookup"><span data-stu-id="de67b-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="de67b-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot – Új paraméterek (–ContainerRegistryUser sztring -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) hozzáadva Windows-tárolóalkalmazás létrehozásához és felügyeletéhez</span><span class="sxs-lookup"><span data-stu-id="de67b-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="de67b-273">6.8.1 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="de67b-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="de67b-274">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="de67b-274">General</span></span>
* <span data-ttu-id="de67b-275">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="de67b-276">Frissített közös futtatókörnyezeti szerelvények</span><span class="sxs-lookup"><span data-stu-id="de67b-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="de67b-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="de67b-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="de67b-278">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="de67b-279">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="de67b-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="de67b-280">Az Import-AzureRmApiManagementApi és az \*-AzureRmApiManagementCertificate parancsmagok már tudják kezelni a relatív elérési utakat</span><span class="sxs-lookup"><span data-stu-id="de67b-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="de67b-281">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="de67b-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="de67b-282">A CertificateInformation egy beállítható tulajdonság, amely a Set-AzureRmApiManagement parancsmag megfelelő működését biztosítja.</span><span class="sxs-lookup"><span data-stu-id="de67b-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="de67b-283">Javítva a nuget 4.0.4-es előzetes verziójára való frissítéssel</span><span class="sxs-lookup"><span data-stu-id="de67b-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="de67b-284">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="de67b-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="de67b-285">A termékben való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="de67b-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="de67b-286">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="de67b-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="de67b-287">Az API-ban való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="de67b-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="de67b-288">Az AzureMonitor támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="de67b-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-289">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-290">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="de67b-291">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="de67b-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="de67b-292">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="de67b-293">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="de67b-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-294">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-295">A parancsmagkimenetek alapértelmezett ábrázolása táblanézetre módosítva</span><span class="sxs-lookup"><span data-stu-id="de67b-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="de67b-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="de67b-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="de67b-297">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="de67b-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="de67b-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-298">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-299">Ki lett javítva a felügyelt alkalmazások Marketplace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="de67b-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de67b-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="de67b-301">Hibák kijavítva:</span><span class="sxs-lookup"><span data-stu-id="de67b-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="de67b-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="de67b-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="de67b-303">A MultiValue útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="de67b-304">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="de67b-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="de67b-305">Az alhálózati útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="de67b-306">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="de67b-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="de67b-307">Egyéni fejlécek profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="de67b-308">Várt állapotkód-tartományok profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="de67b-309">Egyéni fejlécek végpontokon való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="de67b-310">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="de67b-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="de67b-311">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="de67b-311">General</span></span>
* <span data-ttu-id="de67b-312">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="de67b-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-313">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-314">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="de67b-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-315">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-316">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="de67b-317">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="de67b-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="de67b-318">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="de67b-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="de67b-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="de67b-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="de67b-320">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="de67b-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-321">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-322">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="de67b-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="de67b-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="de67b-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="de67b-324">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="de67b-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-325">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-326">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="de67b-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de67b-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="de67b-328">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="de67b-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="de67b-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="de67b-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="de67b-330">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="de67b-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="de67b-331">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="de67b-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="de67b-332">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="de67b-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="de67b-333">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="de67b-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="de67b-334">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="de67b-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="de67b-335">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="de67b-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="de67b-336">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="de67b-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="de67b-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="de67b-337">AzureRM.Websites</span></span>
* <span data-ttu-id="de67b-338">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="de67b-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="de67b-339">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="de67b-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="de67b-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-340">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-341">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="de67b-342">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="de67b-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="de67b-343">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="de67b-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="de67b-344">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="de67b-345">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-345">Azure.Storage</span></span>
* <span data-ttu-id="de67b-346">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="de67b-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="de67b-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="de67b-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="de67b-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="de67b-349">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="de67b-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="de67b-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="de67b-351">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="de67b-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="de67b-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="de67b-353">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="de67b-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="de67b-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="de67b-355">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="de67b-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="de67b-356">AzureRM.Automation</span></span>
* <span data-ttu-id="de67b-357">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="de67b-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="de67b-358">AzureRM.Backup</span></span>
* <span data-ttu-id="de67b-359">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="de67b-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="de67b-360">AzureRM.Batch</span></span>
* <span data-ttu-id="de67b-361">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="de67b-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="de67b-362">AzureRM.Billing</span></span>
* <span data-ttu-id="de67b-363">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="de67b-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="de67b-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="de67b-365">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="de67b-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="de67b-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="de67b-367">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-368">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-369">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="de67b-370">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="de67b-371">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="de67b-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="de67b-372">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="de67b-373">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="de67b-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="de67b-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="de67b-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="de67b-375">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="de67b-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="de67b-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="de67b-377">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="de67b-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="de67b-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="de67b-379">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="de67b-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="de67b-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="de67b-381">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="de67b-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="de67b-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="de67b-383">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="de67b-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="de67b-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="de67b-385">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="de67b-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="de67b-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="de67b-387">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="de67b-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="de67b-388">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="de67b-389">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="de67b-390">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="de67b-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="de67b-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="de67b-392">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="de67b-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="de67b-393">AzureRM.Dns</span></span>
* <span data-ttu-id="de67b-394">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="de67b-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="de67b-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="de67b-396">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="de67b-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="de67b-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="de67b-398">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="de67b-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="de67b-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="de67b-400">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="de67b-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="de67b-401">AzureRM.Insights</span></span>
* <span data-ttu-id="de67b-402">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="de67b-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="de67b-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="de67b-404">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="de67b-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="de67b-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="de67b-406">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="de67b-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="de67b-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="de67b-408">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="de67b-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="de67b-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="de67b-410">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="de67b-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="de67b-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="de67b-412">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="de67b-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="de67b-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="de67b-414">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="de67b-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="de67b-415">AzureRM.Media</span></span>
* <span data-ttu-id="de67b-416">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-417">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-418">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="de67b-419">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="de67b-420">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="de67b-421">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="de67b-422">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="de67b-423">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="de67b-424">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="de67b-425">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="de67b-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="de67b-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="de67b-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="de67b-427">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="de67b-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="de67b-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="de67b-429">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="de67b-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="de67b-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="de67b-431">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="de67b-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="de67b-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="de67b-433">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="de67b-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="de67b-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="de67b-435">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="de67b-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="de67b-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="de67b-437">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="de67b-438">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="de67b-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="de67b-439">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="de67b-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="de67b-440">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="de67b-441">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="de67b-442">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="de67b-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="de67b-443">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="de67b-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="de67b-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="de67b-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="de67b-445">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="de67b-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="de67b-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="de67b-447">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="de67b-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="de67b-448">AzureRM.Relay</span></span>
* <span data-ttu-id="de67b-449">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-450">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-451">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="de67b-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="de67b-452">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="de67b-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="de67b-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="de67b-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="de67b-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="de67b-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="de67b-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="de67b-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="de67b-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="de67b-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="de67b-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="de67b-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="de67b-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="de67b-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="de67b-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="de67b-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="de67b-460">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="de67b-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="de67b-461">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="de67b-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="de67b-462">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="de67b-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="de67b-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="de67b-464">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="de67b-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de67b-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="de67b-466">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="de67b-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="de67b-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="de67b-468">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="de67b-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-469">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-470">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="de67b-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-471">AzureRM.Storage</span></span>
* <span data-ttu-id="de67b-472">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="de67b-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="de67b-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="de67b-474">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="de67b-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="de67b-475">AzureRM.Tags</span></span>
* <span data-ttu-id="de67b-476">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="de67b-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="de67b-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="de67b-478">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="de67b-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="de67b-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="de67b-480">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="de67b-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="de67b-481">AzureRM.Websites</span></span>
* <span data-ttu-id="de67b-482">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="de67b-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="de67b-483">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="de67b-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="de67b-484">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="de67b-484">General</span></span>
* <span data-ttu-id="de67b-485">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="de67b-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="de67b-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-486">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-487">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="de67b-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="de67b-488">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="de67b-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="de67b-489">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-489">Azure.Storage</span></span>
* <span data-ttu-id="de67b-490">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="de67b-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="de67b-491">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="de67b-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="de67b-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="de67b-493">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="de67b-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="de67b-494">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="de67b-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="de67b-495">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="de67b-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="de67b-496">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="de67b-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="de67b-497">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="de67b-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="de67b-498">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="de67b-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-499">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-500">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="de67b-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="de67b-501">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="de67b-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="de67b-502">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="de67b-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="de67b-503">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="de67b-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="de67b-504">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="de67b-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="de67b-505">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="de67b-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="de67b-506">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="de67b-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="de67b-507">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="de67b-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="de67b-508">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="de67b-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="de67b-509">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="de67b-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="de67b-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="de67b-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="de67b-511">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="de67b-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="de67b-512">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="de67b-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="de67b-513">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="de67b-514">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="de67b-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="de67b-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="de67b-516">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="de67b-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="de67b-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="de67b-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="de67b-518">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="de67b-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="de67b-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="de67b-519">AzureRM.Insights</span></span>
* <span data-ttu-id="de67b-520">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="de67b-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="de67b-521">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="de67b-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="de67b-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="de67b-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="de67b-523">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="de67b-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-524">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-525">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-526">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-527">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="de67b-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="de67b-528">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="de67b-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="de67b-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de67b-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="de67b-530">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="de67b-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="de67b-531">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="de67b-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="de67b-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-532">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-533">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="de67b-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="de67b-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="de67b-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="de67b-535">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="de67b-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="de67b-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="de67b-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="de67b-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="de67b-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="de67b-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="de67b-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="de67b-539">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="de67b-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="de67b-540">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="de67b-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="de67b-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-541">AzureRM.Storage</span></span>
* <span data-ttu-id="de67b-542">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="de67b-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="de67b-543">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="de67b-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="de67b-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de67b-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="de67b-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de67b-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="de67b-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de67b-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="de67b-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="de67b-547">AzureRM.Tags</span></span>
* <span data-ttu-id="de67b-548">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="de67b-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="de67b-549">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="de67b-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="de67b-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-550">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-551">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="de67b-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="de67b-552">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-552">Azure.Storage</span></span>
* <span data-ttu-id="de67b-553">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="de67b-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="de67b-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="de67b-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="de67b-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="de67b-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="de67b-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="de67b-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="de67b-557">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="de67b-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="de67b-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="de67b-558">AzureRM.Automation</span></span>
* <span data-ttu-id="de67b-559">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="de67b-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-560">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-561">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="de67b-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="de67b-562">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="de67b-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="de67b-563">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="de67b-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="de67b-564">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="de67b-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="de67b-565">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="de67b-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="de67b-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="de67b-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="de67b-567">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="de67b-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="de67b-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="de67b-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="de67b-569">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="de67b-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="de67b-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="de67b-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="de67b-571">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="de67b-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-572">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-573">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="de67b-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="de67b-574">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="de67b-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="de67b-575">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="de67b-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="de67b-576">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="de67b-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="de67b-577">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="de67b-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="de67b-578">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="de67b-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="de67b-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="de67b-579">AzureRM.Relay</span></span>
* <span data-ttu-id="de67b-580">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="de67b-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-581">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-582">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="de67b-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="de67b-583">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="de67b-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="de67b-584">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="de67b-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="de67b-585">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="de67b-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="de67b-586">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="de67b-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="de67b-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de67b-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="de67b-588">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="de67b-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="de67b-589">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="de67b-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="de67b-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="de67b-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="de67b-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="de67b-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="de67b-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="de67b-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="de67b-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="de67b-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="de67b-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="de67b-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="de67b-595">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="de67b-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="de67b-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="de67b-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="de67b-597">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="de67b-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="de67b-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-598">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-599">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="de67b-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="de67b-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="de67b-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="de67b-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="de67b-602">AzureRM.Websites</span></span>
* <span data-ttu-id="de67b-603">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="de67b-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="de67b-604">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="de67b-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="de67b-605">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="de67b-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="de67b-606">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="de67b-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="de67b-607">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="de67b-607">General</span></span>
* <span data-ttu-id="de67b-608">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="de67b-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="de67b-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-609">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-610">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="de67b-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-611">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-612">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="de67b-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="de67b-613">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="de67b-614">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="de67b-615">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="de67b-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="de67b-616">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="de67b-617">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="de67b-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="de67b-618">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="de67b-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="de67b-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="de67b-620">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="de67b-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="de67b-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="de67b-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="de67b-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="de67b-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="de67b-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="de67b-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="de67b-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="de67b-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="de67b-625">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="de67b-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="de67b-626">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="de67b-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="de67b-627">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="de67b-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="de67b-628">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="de67b-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="de67b-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="de67b-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="de67b-630">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="de67b-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="de67b-631">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="de67b-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="de67b-632">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="de67b-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="de67b-633">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="de67b-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="de67b-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="de67b-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="de67b-635">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="de67b-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-636">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-637">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="de67b-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="de67b-638">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="de67b-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="de67b-639">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="de67b-640">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="de67b-641">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="de67b-642">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="de67b-643">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="de67b-644">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="de67b-645">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="de67b-646">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="de67b-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="de67b-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="de67b-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="de67b-648">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="de67b-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="de67b-649">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="de67b-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="de67b-650">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="de67b-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-651">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-652">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="de67b-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="de67b-653">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="de67b-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="de67b-654">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="de67b-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="de67b-655">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="de67b-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="de67b-656">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="de67b-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="de67b-657">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="de67b-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="de67b-658">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="de67b-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="de67b-659">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="de67b-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="de67b-660">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="de67b-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="de67b-661">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="de67b-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="de67b-662">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="de67b-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="de67b-663">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="de67b-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="de67b-664">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="de67b-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="de67b-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de67b-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="de67b-666">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="de67b-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="de67b-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-667">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-668">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="de67b-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="de67b-669">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="de67b-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="de67b-670">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="de67b-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="de67b-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-671">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-672">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="de67b-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="de67b-673">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="de67b-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="de67b-674">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="de67b-674">Azure.Storage</span></span>
* <span data-ttu-id="de67b-675">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="de67b-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-676">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-677">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="de67b-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="de67b-678">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="de67b-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="de67b-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="de67b-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="de67b-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="de67b-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="de67b-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="de67b-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="de67b-682">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="de67b-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="de67b-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="de67b-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="de67b-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="de67b-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="de67b-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="de67b-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="de67b-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="de67b-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="de67b-687">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="de67b-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="de67b-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de67b-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="de67b-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="de67b-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="de67b-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="de67b-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="de67b-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de67b-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="de67b-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de67b-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="de67b-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de67b-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="de67b-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de67b-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="de67b-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="de67b-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="de67b-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="de67b-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="de67b-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="de67b-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="de67b-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="de67b-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="de67b-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="de67b-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="de67b-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="de67b-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="de67b-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="de67b-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="de67b-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="de67b-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="de67b-703">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="de67b-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="de67b-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="de67b-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="de67b-705">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="de67b-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="de67b-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="de67b-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="de67b-707">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="de67b-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="de67b-708">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="de67b-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="de67b-709">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="de67b-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="de67b-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="de67b-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="de67b-711">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="de67b-712">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="de67b-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="de67b-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-713">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-714">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="de67b-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="de67b-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="de67b-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="de67b-716">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="de67b-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="de67b-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="de67b-717">AzureRM.Websites</span></span>
* <span data-ttu-id="de67b-718">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="de67b-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="de67b-719">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="de67b-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="de67b-720">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="de67b-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="de67b-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="de67b-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="de67b-722">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="de67b-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="de67b-723">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="de67b-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="de67b-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-724">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-725">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="de67b-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="de67b-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="de67b-726">AzureRM.Compute</span></span>
* <span data-ttu-id="de67b-727">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="de67b-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="de67b-728">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="de67b-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="de67b-729">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="de67b-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="de67b-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="de67b-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="de67b-731">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="de67b-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="de67b-732">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="de67b-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="de67b-733">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="de67b-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="de67b-734">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="de67b-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="de67b-735">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="de67b-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="de67b-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="de67b-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="de67b-737">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="de67b-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="de67b-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-738">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-739">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="de67b-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="de67b-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="de67b-740">AzureRM.Resources</span></span>
* <span data-ttu-id="de67b-741">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="de67b-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="de67b-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="de67b-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="de67b-743">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="de67b-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="de67b-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-744">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-745">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="de67b-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="de67b-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="de67b-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="de67b-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="de67b-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="de67b-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="de67b-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="de67b-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="de67b-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="de67b-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="de67b-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="de67b-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="de67b-751">AzureRM.Websites</span></span>
* <span data-ttu-id="de67b-752">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="de67b-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="de67b-753">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="de67b-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="de67b-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="de67b-754">AzureRM.Profile</span></span>
* <span data-ttu-id="de67b-755">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="de67b-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="de67b-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="de67b-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="de67b-757">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="de67b-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="de67b-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="de67b-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="de67b-759">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="de67b-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="de67b-760">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="de67b-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="de67b-761">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="de67b-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="de67b-762">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="de67b-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="de67b-763">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="de67b-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="de67b-764">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="de67b-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="de67b-765">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="de67b-765">Added support for MSI identity</span></span>
* <span data-ttu-id="de67b-766">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="de67b-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="de67b-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="de67b-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="de67b-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="de67b-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="de67b-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="de67b-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="de67b-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="de67b-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="de67b-771">AzureRM.Batch</span></span>
* <span data-ttu-id="de67b-772">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="de67b-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="de67b-773">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="de67b-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="de67b-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="de67b-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="de67b-775">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="de67b-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="de67b-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="de67b-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="de67b-777">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="de67b-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="de67b-778">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="de67b-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="de67b-779">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="de67b-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="de67b-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="de67b-780">AzureRM.Network</span></span>
* <span data-ttu-id="de67b-781">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="de67b-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="de67b-782">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="de67b-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="de67b-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="de67b-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="de67b-784">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="de67b-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="de67b-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="de67b-786">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="de67b-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="de67b-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="de67b-788">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="de67b-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="de67b-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="de67b-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="de67b-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="de67b-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="de67b-791">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="de67b-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="de67b-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="de67b-792">AzureRM.Sql</span></span>
* <span data-ttu-id="de67b-793">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="de67b-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="de67b-794">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="de67b-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="de67b-795">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="de67b-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="de67b-796">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="de67b-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="de67b-797">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="de67b-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="de67b-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="de67b-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="de67b-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="de67b-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="de67b-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="de67b-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="de67b-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="de67b-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="de67b-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="de67b-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="de67b-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="de67b-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="de67b-804">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="de67b-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
