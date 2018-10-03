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
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179003"
---
# <a name="release-notes"></a><span data-ttu-id="34e7f-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="34e7f-103">Release notes</span></span>

<span data-ttu-id="34e7f-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="34e7f-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="34e7f-105">6.9.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="34e7f-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="34e7f-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="34e7f-106">General</span></span>
* <span data-ttu-id="34e7f-107">Az AzureRM.SignalR hozzáadva az AzureRM összesített modulhoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-108">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-109">Kisebb módosítások a tárolók általános kódjában</span><span class="sxs-lookup"><span data-stu-id="34e7f-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="34e7f-110">Teljes paramétertípusokkal frissült súgófájlok</span><span class="sxs-lookup"><span data-stu-id="34e7f-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="34e7f-111">A -ServicePrincipal módosítása nem kötelezőre a ServicePrincipalCertificateWithSubscriptionId paraméterkészletben</span><span class="sxs-lookup"><span data-stu-id="34e7f-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="34e7f-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-112">Azure.Storage</span></span>
* <span data-ttu-id="34e7f-113">Storage-környezet létrehozásának támogatása OAuth használatával.</span><span class="sxs-lookup"><span data-stu-id="34e7f-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="34e7f-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="34e7f-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="34e7f-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="34e7f-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="34e7f-116">Standard_Microsoft hozzáadva a CDN-díjszabási termékváltozatban.</span><span class="sxs-lookup"><span data-stu-id="34e7f-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-117">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-118">A Key Vault és a Storage függőségeinek áthelyezése az általános függőségekhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="34e7f-119">További virtuálisgép-méretek támogatása hozzáadva az AEM-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="34e7f-120">A PublicIPPrefix paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="34e7f-121">A ResourceId paraméter hozzáadva az Invoke-AzureRmVMRunCommand parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="34e7f-122">Az Invoke-AzureRmVmssVMRunCommand parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="34e7f-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="34e7f-123">AzureRM.Dns</span></span>
* <span data-ttu-id="34e7f-124">Aliasrekord támogatása hozzáadva DNS-rekord létrehozása során</span><span class="sxs-lookup"><span data-stu-id="34e7f-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="34e7f-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="34e7f-125">AzureRM.Insights</span></span>
* <span data-ttu-id="34e7f-126">A 6833-as és a 7102-es hiba kijavítva (Diagnosztikai beállítások területe)</span><span class="sxs-lookup"><span data-stu-id="34e7f-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="34e7f-127">Az alapértelmezett név, például a „service” hibái a diagnosztikai beállítások megadása és listázása/lekérése során</span><span class="sxs-lookup"><span data-stu-id="34e7f-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="34e7f-128">Diagnosztikai beállítások kategóriákkal történő létrehozásának hibái</span><span class="sxs-lookup"><span data-stu-id="34e7f-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="34e7f-129">Elavulási üzenetek hozzáadva a metrikák időfelbontási szintjeinek paramétereihez</span><span class="sxs-lookup"><span data-stu-id="34e7f-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="34e7f-130">Az időfelbontási szintek paramétereit még elfogadja a rendszer (ez nem egy kompatibilitástörő változás), viszont figyelmen kívül hagyja a háttérrendszerben, mivel csak a PT1M érvényes</span><span class="sxs-lookup"><span data-stu-id="34e7f-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-131">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-132">A LoadBalancer parancsmagokat érintő változások</span><span class="sxs-lookup"><span data-stu-id="34e7f-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="34e7f-133">LoadBalancerInboundNatPoolConfig: az IdleTimeoutInMinutes, az EnableFloatingIp és az EnableTcpReset paraméterek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="34e7f-134">LoadBalancerInboundNatRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="34e7f-135">LoadBalancerRuleConfig: az EnableTcpReset paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="34e7f-136">LoadBalancerProbeConfig: a Protocol paraméterhez tartozó „Https” érték támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="34e7f-137">Új parancsok hozzáadva a LoadBalancer új, OutboundRule nevű alerőforrásához</span><span class="sxs-lookup"><span data-stu-id="34e7f-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="34e7f-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="34e7f-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="34e7f-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="34e7f-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="34e7f-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="34e7f-143">Új HostedWorkloads tulajdonság hozzáadva a PSNetworkInterface-hez</span><span class="sxs-lookup"><span data-stu-id="34e7f-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="34e7f-144">Új parancsmagok hozzáadva a következő szolgáltatáshoz: Azure Firewall ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="34e7f-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="34e7f-145">Get-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="34e7f-146">Set-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="34e7f-147">New-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="34e7f-148">Remove-AzureRmFirewall hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="34e7f-149">New-AzureRmFirewallApplicationRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="34e7f-150">New-AzureRmFirewallApplicationRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="34e7f-151">New-AzureRmFirewallNatRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="34e7f-152">New-AzureRmFirewallNatRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="34e7f-153">New-AzureRmFirewallNetworkRuleCollection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="34e7f-154">New-AzureRmFirewallNetworkRule hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="34e7f-155">Támogatás hozzáadva a megbízható főtanúsítványokhoz és az automatikus skálázás konfigurálásához az Application Gatewayben</span><span class="sxs-lookup"><span data-stu-id="34e7f-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="34e7f-156">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="34e7f-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="34e7f-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="34e7f-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="34e7f-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="34e7f-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="34e7f-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="34e7f-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="34e7f-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="34e7f-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="34e7f-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="34e7f-166">Parancsmagok frissítve a -TrustedRootCertificate nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="34e7f-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="34e7f-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e7f-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="34e7f-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e7f-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="34e7f-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="34e7f-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="34e7f-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="34e7f-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="34e7f-171">Parancsmagok frissítve az -AutoscaleConfiguration nevű, nem kötelező paraméterrel</span><span class="sxs-lookup"><span data-stu-id="34e7f-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="34e7f-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e7f-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="34e7f-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34e7f-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="34e7f-174">A Get-AzureInterfaceEndpoint parancsmag hozzáadva a felhasználói felület végpontjához</span><span class="sxs-lookup"><span data-stu-id="34e7f-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="34e7f-175">Támogatás hozzáadva több címelőtaghoz egy alhálózaton belül</span><span class="sxs-lookup"><span data-stu-id="34e7f-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="34e7f-176">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="34e7f-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="34e7f-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="34e7f-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="34e7f-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="34e7f-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="34e7f-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="34e7f-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="34e7f-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="34e7f-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="34e7f-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="34e7f-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="34e7f-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="34e7f-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="34e7f-189">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="34e7f-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="34e7f-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="34e7f-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="34e7f-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="34e7f-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="34e7f-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="34e7f-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="34e7f-196">Alhálózat-delegálási parancsmagok hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="34e7f-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="34e7f-197">New-AzureRmDelegation: Létrehoz egy új delegálást, amelyet hozzá lehet adni egy alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="34e7f-198">Remove-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott delegálási nevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="34e7f-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="34e7f-199">Add-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott szolgáltatásnevet az adott alhálózatból</span><span class="sxs-lookup"><span data-stu-id="34e7f-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="34e7f-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="34e7f-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="34e7f-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="34e7f-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="34e7f-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="34e7f-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="34e7f-203">A felügyelt lemezek támogatása</span><span class="sxs-lookup"><span data-stu-id="34e7f-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="34e7f-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="34e7f-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="34e7f-205">Insights-függőség frissítve</span><span class="sxs-lookup"><span data-stu-id="34e7f-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="34e7f-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-206">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-207">A New-AzureRmResourceGroupDeployment frissítve az új RollbackAction paraméterrel</span><span class="sxs-lookup"><span data-stu-id="34e7f-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="34e7f-208">Az OnErrorDeployment támogatása az új paraméterrel</span><span class="sxs-lookup"><span data-stu-id="34e7f-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="34e7f-209">A felügyelt identitás támogatása a szabályzat-hozzárendeléseknél</span><span class="sxs-lookup"><span data-stu-id="34e7f-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="34e7f-210">Az alapértelmezett értékekkel rendelkező paraméterek már nem szükségesek a szabályzatok a New-AzureRmPolicyAssignmenttel történő hozzárendelésekor</span><span class="sxs-lookup"><span data-stu-id="34e7f-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="34e7f-211">Az új Get-AzureRmPolicyAlias parancsmag hozzáadva a szabályzataliasok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="34e7f-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34e7f-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="34e7f-213">A 7161-es hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="34e7f-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="34e7f-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="34e7f-215">Termékváltozatnevek frissítve Free_F1-re és Standard_S1-re</span><span class="sxs-lookup"><span data-stu-id="34e7f-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="34e7f-216">Verzió mező hozzáadva a PSSignalRResource objektumhoz, és kapcsolati sztring hozzáadva a PSSignalRKeys objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="34e7f-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-217">AzureRM.Storage</span></span>
* <span data-ttu-id="34e7f-218">Módosíthatatlansági szabályzat támogatva az AzureRM.Storage-ban</span><span class="sxs-lookup"><span data-stu-id="34e7f-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="34e7f-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="34e7f-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="34e7f-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34e7f-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="34e7f-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34e7f-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="34e7f-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34e7f-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="34e7f-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34e7f-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="34e7f-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="34e7f-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="34e7f-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="34e7f-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="34e7f-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="34e7f-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="34e7f-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="34e7f-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="34e7f-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="34e7f-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="34e7f-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="34e7f-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="34e7f-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="34e7f-230">AzureRM.Websites</span></span>
* <span data-ttu-id="34e7f-231">Két új parancsmag hozzáadva: Get-AzureRmDeletedWebApp és Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="34e7f-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="34e7f-232">A New-AzureRmAppServicePlan -HyperV kapcsoló hozzáadva App Service-csomag létrehozásához Windows-tárolóval</span><span class="sxs-lookup"><span data-stu-id="34e7f-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="34e7f-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot – Új paraméterek (–ContainerRegistryUser sztring -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) hozzáadva Windows-tárolóalkalmazás létrehozásához és felügyeletéhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="34e7f-234">6.8.1 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="34e7f-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="34e7f-235">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="34e7f-235">General</span></span>
* <span data-ttu-id="34e7f-236">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="34e7f-237">Frissített közös futtatókörnyezeti szerelvények</span><span class="sxs-lookup"><span data-stu-id="34e7f-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="34e7f-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="34e7f-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="34e7f-239">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="34e7f-240">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="34e7f-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="34e7f-241">Az Import-AzureRmApiManagementApi és az \*-AzureRmApiManagementCertificate parancsmagok már tudják kezelni a relatív elérési utakat</span><span class="sxs-lookup"><span data-stu-id="34e7f-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="34e7f-242">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="34e7f-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="34e7f-243">A CertificateInformation egy beállítható tulajdonság, amely a Set-AzureRmApiManagement parancsmag megfelelő működését biztosítja.</span><span class="sxs-lookup"><span data-stu-id="34e7f-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="34e7f-244">Javítva a nuget 4.0.4-es előzetes verziójára való frissítéssel</span><span class="sxs-lookup"><span data-stu-id="34e7f-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="34e7f-245">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="34e7f-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="34e7f-246">A termékben való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="34e7f-247">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="34e7f-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="34e7f-248">Az API-ban való név szerinti kereséshez tartozó Odata-szűrő kijavítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="34e7f-249">Az AzureMonitor támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-250">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-251">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="34e7f-252">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="34e7f-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="34e7f-253">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="34e7f-254">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="34e7f-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-255">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-256">A parancsmagkimenetek alapértelmezett ábrázolása táblanézetre módosítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="34e7f-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="34e7f-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="34e7f-258">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="34e7f-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="34e7f-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-259">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-260">Ki lett javítva a felügyelt alkalmazások Marketplace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="34e7f-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34e7f-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="34e7f-262">Hibák kijavítva:</span><span class="sxs-lookup"><span data-stu-id="34e7f-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="34e7f-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="34e7f-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="34e7f-264">A MultiValue útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="34e7f-265">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="34e7f-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="34e7f-266">Az alhálózati útválasztási módszer támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="34e7f-267">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="34e7f-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="34e7f-268">Egyéni fejlécek profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="34e7f-269">Várt állapotkód-tartományok profilokban való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="34e7f-270">Egyéni fejlécek végpontokon való támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="34e7f-271">6.8.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="34e7f-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="34e7f-272">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="34e7f-272">General</span></span>
* <span data-ttu-id="34e7f-273">Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-274">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-275">Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-276">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-277">Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="34e7f-278">Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="34e7f-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="34e7f-279">Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)</span><span class="sxs-lookup"><span data-stu-id="34e7f-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="34e7f-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="34e7f-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="34e7f-281">Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái</span><span class="sxs-lookup"><span data-stu-id="34e7f-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-282">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-283">Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre</span><span class="sxs-lookup"><span data-stu-id="34e7f-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="34e7f-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="34e7f-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="34e7f-285">Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során</span><span class="sxs-lookup"><span data-stu-id="34e7f-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="34e7f-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-286">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-287">Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="34e7f-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34e7f-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="34e7f-289">Problémák megoldása</span><span class="sxs-lookup"><span data-stu-id="34e7f-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="34e7f-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="34e7f-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="34e7f-291">A MultiValue útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="34e7f-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="34e7f-292">Új paraméter A MultiValue-útválasztáshoz: MaxReturn</span><span class="sxs-lookup"><span data-stu-id="34e7f-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="34e7f-293">A Subnet útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="34e7f-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="34e7f-294">IP-címtartományok (alhálózatok) támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="34e7f-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="34e7f-295">Egyéni fejlécek támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="34e7f-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="34e7f-296">Várt állapotkód-tartományok támogatása a profilokban</span><span class="sxs-lookup"><span data-stu-id="34e7f-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="34e7f-297">Egyéni fejlécek támogatása a végpontokon</span><span class="sxs-lookup"><span data-stu-id="34e7f-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="34e7f-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="34e7f-298">AzureRM.Websites</span></span>
* <span data-ttu-id="34e7f-299">Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="34e7f-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="34e7f-300">6.7.0 – 2018. augusztus</span><span class="sxs-lookup"><span data-stu-id="34e7f-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-301">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-302">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="34e7f-303">A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="34e7f-304">A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398</span><span class="sxs-lookup"><span data-stu-id="34e7f-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="34e7f-305">A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="34e7f-306">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-306">Azure.Storage</span></span>
* <span data-ttu-id="34e7f-307">Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="34e7f-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="34e7f-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="34e7f-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34e7f-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="34e7f-310">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="34e7f-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34e7f-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="34e7f-312">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="34e7f-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="34e7f-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="34e7f-314">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="34e7f-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="34e7f-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="34e7f-316">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="34e7f-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="34e7f-317">AzureRM.Automation</span></span>
* <span data-ttu-id="34e7f-318">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="34e7f-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="34e7f-319">AzureRM.Backup</span></span>
* <span data-ttu-id="34e7f-320">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="34e7f-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="34e7f-321">AzureRM.Batch</span></span>
* <span data-ttu-id="34e7f-322">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="34e7f-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="34e7f-323">AzureRM.Billing</span></span>
* <span data-ttu-id="34e7f-324">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="34e7f-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="34e7f-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="34e7f-326">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="34e7f-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="34e7f-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="34e7f-328">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-329">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-330">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="34e7f-331">Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="34e7f-332">Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.</span><span class="sxs-lookup"><span data-stu-id="34e7f-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="34e7f-333">A paraméter leírásának javítása a Save-AzureRmVMImage esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="34e7f-334">A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben</span><span class="sxs-lookup"><span data-stu-id="34e7f-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="34e7f-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="34e7f-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="34e7f-336">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="34e7f-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="34e7f-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="34e7f-338">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="34e7f-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="34e7f-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="34e7f-340">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="34e7f-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="34e7f-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="34e7f-342">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="34e7f-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="34e7f-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="34e7f-344">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="34e7f-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="34e7f-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="34e7f-346">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="34e7f-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34e7f-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="34e7f-348">A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="34e7f-349">Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="34e7f-350">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="34e7f-351">Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="34e7f-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="34e7f-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="34e7f-353">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="34e7f-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="34e7f-354">AzureRM.Dns</span></span>
* <span data-ttu-id="34e7f-355">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="34e7f-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="34e7f-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="34e7f-357">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="34e7f-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="34e7f-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="34e7f-359">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="34e7f-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="34e7f-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="34e7f-361">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="34e7f-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="34e7f-362">AzureRM.Insights</span></span>
* <span data-ttu-id="34e7f-363">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="34e7f-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="34e7f-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="34e7f-365">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="34e7f-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34e7f-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="34e7f-367">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="34e7f-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="34e7f-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="34e7f-369">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="34e7f-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="34e7f-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="34e7f-371">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="34e7f-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="34e7f-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="34e7f-373">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="34e7f-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="34e7f-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="34e7f-375">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="34e7f-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="34e7f-376">AzureRM.Media</span></span>
* <span data-ttu-id="34e7f-377">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-378">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-379">Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="34e7f-380">Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="34e7f-381">Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="34e7f-382">Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="34e7f-383">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="34e7f-384">Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="34e7f-385">Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="34e7f-386">Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor</span><span class="sxs-lookup"><span data-stu-id="34e7f-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="34e7f-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="34e7f-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="34e7f-388">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="34e7f-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="34e7f-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="34e7f-390">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="34e7f-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="34e7f-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="34e7f-392">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="34e7f-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="34e7f-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="34e7f-394">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="34e7f-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34e7f-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="34e7f-396">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="34e7f-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="34e7f-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="34e7f-398">Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="34e7f-399">A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.</span><span class="sxs-lookup"><span data-stu-id="34e7f-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="34e7f-400">A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.</span><span class="sxs-lookup"><span data-stu-id="34e7f-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="34e7f-401">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="34e7f-402">A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="34e7f-403">A Managed Diskek visszaállítására kijelölt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="34e7f-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="34e7f-404">Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.</span><span class="sxs-lookup"><span data-stu-id="34e7f-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="34e7f-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="34e7f-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="34e7f-406">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="34e7f-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="34e7f-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="34e7f-408">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="34e7f-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="34e7f-409">AzureRM.Relay</span></span>
* <span data-ttu-id="34e7f-410">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="34e7f-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-411">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-412">A sablonlapú üzembe helyezés támogatása előfizetési hatókörben.</span><span class="sxs-lookup"><span data-stu-id="34e7f-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="34e7f-413">Hozzáadott új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="34e7f-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="34e7f-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="34e7f-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="34e7f-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="34e7f-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="34e7f-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="34e7f-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="34e7f-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="34e7f-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="34e7f-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="34e7f-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="34e7f-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="34e7f-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="34e7f-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="34e7f-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="34e7f-421">Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak</span><span class="sxs-lookup"><span data-stu-id="34e7f-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="34e7f-422">Példa javítva a New-AzureRmResourceGroupDeployment esetén</span><span class="sxs-lookup"><span data-stu-id="34e7f-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="34e7f-423">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="34e7f-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="34e7f-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="34e7f-425">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="34e7f-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34e7f-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="34e7f-427">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="34e7f-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34e7f-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="34e7f-429">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="34e7f-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34e7f-430">AzureRM.Sql</span></span>
* <span data-ttu-id="34e7f-431">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="34e7f-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-432">AzureRM.Storage</span></span>
* <span data-ttu-id="34e7f-433">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="34e7f-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="34e7f-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="34e7f-435">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="34e7f-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="34e7f-436">AzureRM.Tags</span></span>
* <span data-ttu-id="34e7f-437">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="34e7f-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="34e7f-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="34e7f-439">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="34e7f-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="34e7f-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="34e7f-441">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="34e7f-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="34e7f-442">AzureRM.Websites</span></span>
* <span data-ttu-id="34e7f-443">Frissítve az Azure ClientRuntime legújabb verziójára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="34e7f-444">6.6.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="34e7f-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="34e7f-445">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="34e7f-445">General</span></span>
* <span data-ttu-id="34e7f-446">Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="34e7f-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-447">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-448">Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.</span><span class="sxs-lookup"><span data-stu-id="34e7f-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="34e7f-449">A Common.Storage új ps1xml-típusokkal egészült ki</span><span class="sxs-lookup"><span data-stu-id="34e7f-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="34e7f-450">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-450">Azure.Storage</span></span>
* <span data-ttu-id="34e7f-451">A Storage-környezet DefaultProfile használatával történő lekérésének támogatása</span><span class="sxs-lookup"><span data-stu-id="34e7f-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="34e7f-452">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="34e7f-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="34e7f-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="34e7f-454">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="34e7f-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="34e7f-455">Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett</span><span class="sxs-lookup"><span data-stu-id="34e7f-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="34e7f-456">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="34e7f-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="34e7f-457">Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl</span><span class="sxs-lookup"><span data-stu-id="34e7f-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="34e7f-458">Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="34e7f-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="34e7f-459">Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit</span><span class="sxs-lookup"><span data-stu-id="34e7f-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-460">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-461">Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="34e7f-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="34e7f-462">Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot</span><span class="sxs-lookup"><span data-stu-id="34e7f-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="34e7f-463">Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.</span><span class="sxs-lookup"><span data-stu-id="34e7f-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="34e7f-464">(A ResouceGroupName paraméter mostantól opcionális.)</span><span class="sxs-lookup"><span data-stu-id="34e7f-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="34e7f-465">Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="34e7f-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="34e7f-466">Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.</span><span class="sxs-lookup"><span data-stu-id="34e7f-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="34e7f-467">Frissült a New-AzureRmDisk példája</span><span class="sxs-lookup"><span data-stu-id="34e7f-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="34e7f-468">Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa</span><span class="sxs-lookup"><span data-stu-id="34e7f-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="34e7f-469">Frissült a Set-AzureRmVMOSDisk leírása</span><span class="sxs-lookup"><span data-stu-id="34e7f-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="34e7f-470">Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája.</span><span class="sxs-lookup"><span data-stu-id="34e7f-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="34e7f-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="34e7f-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="34e7f-472">Az ADF.Net SDK verziója 1.1.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="34e7f-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="34e7f-473">Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.</span><span class="sxs-lookup"><span data-stu-id="34e7f-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="34e7f-474">Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="34e7f-475">Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="34e7f-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34e7f-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="34e7f-477">A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült</span><span class="sxs-lookup"><span data-stu-id="34e7f-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="34e7f-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="34e7f-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="34e7f-479">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="34e7f-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="34e7f-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="34e7f-480">AzureRM.Insights</span></span>
* <span data-ttu-id="34e7f-481">Javítottuk az OutputType formázását a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="34e7f-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="34e7f-482">A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált</span><span class="sxs-lookup"><span data-stu-id="34e7f-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="34e7f-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34e7f-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="34e7f-484">Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját</span><span class="sxs-lookup"><span data-stu-id="34e7f-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-485">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-486">Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="34e7f-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-487">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-488">Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="34e7f-489">Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét</span><span class="sxs-lookup"><span data-stu-id="34e7f-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="34e7f-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34e7f-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="34e7f-491">Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="34e7f-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="34e7f-492">Kijavítottunk néhány hibát</span><span class="sxs-lookup"><span data-stu-id="34e7f-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="34e7f-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34e7f-493">AzureRM.Sql</span></span>
* <span data-ttu-id="34e7f-494">A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:</span><span class="sxs-lookup"><span data-stu-id="34e7f-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="34e7f-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="34e7f-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="34e7f-496">A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:</span><span class="sxs-lookup"><span data-stu-id="34e7f-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="34e7f-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="34e7f-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="34e7f-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="34e7f-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="34e7f-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="34e7f-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="34e7f-500">Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját</span><span class="sxs-lookup"><span data-stu-id="34e7f-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="34e7f-501">Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben</span><span class="sxs-lookup"><span data-stu-id="34e7f-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="34e7f-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-502">AzureRM.Storage</span></span>
* <span data-ttu-id="34e7f-503">A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="34e7f-504">A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált</span><span class="sxs-lookup"><span data-stu-id="34e7f-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="34e7f-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="34e7f-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="34e7f-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="34e7f-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="34e7f-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="34e7f-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="34e7f-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="34e7f-508">AzureRM.Tags</span></span>
* <span data-ttu-id="34e7f-509">El lett távolítva egy helytelen állítás a Tag parancsmag súgójából</span><span class="sxs-lookup"><span data-stu-id="34e7f-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="34e7f-510">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="34e7f-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-511">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-512">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="34e7f-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="34e7f-513">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-513">Azure.Storage</span></span>
* <span data-ttu-id="34e7f-514">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="34e7f-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="34e7f-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="34e7f-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="34e7f-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="34e7f-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="34e7f-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34e7f-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="34e7f-518">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="34e7f-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="34e7f-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="34e7f-519">AzureRM.Automation</span></span>
* <span data-ttu-id="34e7f-520">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="34e7f-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-521">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-522">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="34e7f-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="34e7f-523">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="34e7f-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="34e7f-524">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="34e7f-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="34e7f-525">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="34e7f-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="34e7f-526">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="34e7f-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="34e7f-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="34e7f-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="34e7f-528">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="34e7f-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="34e7f-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34e7f-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="34e7f-530">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="34e7f-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="34e7f-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="34e7f-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="34e7f-532">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="34e7f-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-533">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-534">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="34e7f-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="34e7f-535">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="34e7f-536">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="34e7f-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="34e7f-537">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="34e7f-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="34e7f-538">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="34e7f-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="34e7f-539">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="34e7f-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="34e7f-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="34e7f-540">AzureRM.Relay</span></span>
* <span data-ttu-id="34e7f-541">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="34e7f-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="34e7f-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-542">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-543">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="34e7f-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="34e7f-544">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="34e7f-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="34e7f-545">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="34e7f-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="34e7f-546">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="34e7f-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="34e7f-547">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="34e7f-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="34e7f-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34e7f-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="34e7f-549">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="34e7f-550">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="34e7f-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="34e7f-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="34e7f-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="34e7f-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="34e7f-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="34e7f-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="34e7f-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="34e7f-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="34e7f-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="34e7f-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="34e7f-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="34e7f-556">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="34e7f-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="34e7f-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34e7f-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="34e7f-558">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="34e7f-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="34e7f-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34e7f-559">AzureRM.Sql</span></span>
* <span data-ttu-id="34e7f-560">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="34e7f-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="34e7f-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="34e7f-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="34e7f-563">AzureRM.Websites</span></span>
* <span data-ttu-id="34e7f-564">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="34e7f-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="34e7f-565">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="34e7f-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="34e7f-566">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="34e7f-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="34e7f-567">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="34e7f-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="34e7f-568">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="34e7f-568">General</span></span>
* <span data-ttu-id="34e7f-569">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="34e7f-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-570">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-571">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-572">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-573">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="34e7f-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="34e7f-574">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="34e7f-575">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="34e7f-576">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="34e7f-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="34e7f-577">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="34e7f-578">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="34e7f-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="34e7f-579">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="34e7f-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="34e7f-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="34e7f-581">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="34e7f-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="34e7f-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="34e7f-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="34e7f-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="34e7f-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="34e7f-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="34e7f-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="34e7f-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34e7f-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="34e7f-586">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="34e7f-587">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="34e7f-588">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="34e7f-589">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="34e7f-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="34e7f-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="34e7f-591">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="34e7f-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="34e7f-592">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="34e7f-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="34e7f-593">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="34e7f-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="34e7f-594">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="34e7f-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="34e7f-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34e7f-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="34e7f-596">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="34e7f-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-597">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-598">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="34e7f-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="34e7f-599">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="34e7f-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="34e7f-600">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="34e7f-601">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="34e7f-602">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="34e7f-603">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="34e7f-604">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="34e7f-605">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="34e7f-606">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="34e7f-607">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="34e7f-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="34e7f-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="34e7f-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="34e7f-609">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="34e7f-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="34e7f-610">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="34e7f-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="34e7f-611">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="34e7f-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="34e7f-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-612">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-613">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="34e7f-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="34e7f-614">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="34e7f-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="34e7f-615">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="34e7f-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="34e7f-616">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="34e7f-617">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="34e7f-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="34e7f-618">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="34e7f-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="34e7f-619">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="34e7f-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="34e7f-620">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="34e7f-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="34e7f-621">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="34e7f-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="34e7f-622">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="34e7f-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="34e7f-623">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="34e7f-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="34e7f-624">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="34e7f-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="34e7f-625">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="34e7f-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34e7f-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="34e7f-627">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="34e7f-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="34e7f-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34e7f-628">AzureRM.Sql</span></span>
* <span data-ttu-id="34e7f-629">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="34e7f-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="34e7f-630">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="34e7f-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="34e7f-631">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="34e7f-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-632">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-633">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="34e7f-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="34e7f-634">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="34e7f-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="34e7f-635">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="34e7f-635">Azure.Storage</span></span>
* <span data-ttu-id="34e7f-636">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="34e7f-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-637">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-638">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="34e7f-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="34e7f-639">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="34e7f-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="34e7f-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="34e7f-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="34e7f-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="34e7f-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="34e7f-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="34e7f-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="34e7f-643">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="34e7f-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="34e7f-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34e7f-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="34e7f-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34e7f-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="34e7f-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34e7f-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="34e7f-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34e7f-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="34e7f-648">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34e7f-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="34e7f-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34e7f-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="34e7f-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="34e7f-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="34e7f-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="34e7f-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="34e7f-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34e7f-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="34e7f-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34e7f-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="34e7f-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34e7f-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="34e7f-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34e7f-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="34e7f-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="34e7f-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="34e7f-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="34e7f-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="34e7f-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="34e7f-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="34e7f-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="34e7f-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="34e7f-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="34e7f-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="34e7f-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="34e7f-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="34e7f-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="34e7f-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="34e7f-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="34e7f-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="34e7f-664">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="34e7f-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="34e7f-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34e7f-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="34e7f-666">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="34e7f-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="34e7f-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="34e7f-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="34e7f-668">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="34e7f-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="34e7f-669">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="34e7f-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="34e7f-670">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="34e7f-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="34e7f-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="34e7f-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="34e7f-672">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="34e7f-673">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="34e7f-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="34e7f-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34e7f-674">AzureRM.Sql</span></span>
* <span data-ttu-id="34e7f-675">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="34e7f-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="34e7f-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="34e7f-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="34e7f-677">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="34e7f-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="34e7f-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="34e7f-678">AzureRM.Websites</span></span>
* <span data-ttu-id="34e7f-679">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="34e7f-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="34e7f-680">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="34e7f-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="34e7f-681">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="34e7f-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="34e7f-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="34e7f-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="34e7f-683">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="34e7f-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="34e7f-684">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="34e7f-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-685">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-686">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="34e7f-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="34e7f-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="34e7f-687">AzureRM.Compute</span></span>
* <span data-ttu-id="34e7f-688">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="34e7f-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="34e7f-689">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="34e7f-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="34e7f-690">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="34e7f-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="34e7f-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="34e7f-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="34e7f-692">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="34e7f-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="34e7f-693">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="34e7f-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="34e7f-694">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="34e7f-695">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="34e7f-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="34e7f-696">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="34e7f-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="34e7f-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34e7f-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="34e7f-698">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="34e7f-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-699">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-700">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="34e7f-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="34e7f-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="34e7f-701">AzureRM.Resources</span></span>
* <span data-ttu-id="34e7f-702">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="34e7f-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="34e7f-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="34e7f-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="34e7f-704">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="34e7f-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="34e7f-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34e7f-705">AzureRM.Sql</span></span>
* <span data-ttu-id="34e7f-706">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="34e7f-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="34e7f-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="34e7f-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="34e7f-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="34e7f-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="34e7f-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="34e7f-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="34e7f-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="34e7f-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="34e7f-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="34e7f-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="34e7f-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="34e7f-712">AzureRM.Websites</span></span>
* <span data-ttu-id="34e7f-713">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="34e7f-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="34e7f-714">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="34e7f-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="34e7f-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="34e7f-715">AzureRM.Profile</span></span>
* <span data-ttu-id="34e7f-716">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="34e7f-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="34e7f-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34e7f-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="34e7f-718">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="34e7f-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="34e7f-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="34e7f-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="34e7f-720">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="34e7f-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="34e7f-721">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="34e7f-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="34e7f-722">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="34e7f-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="34e7f-723">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="34e7f-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="34e7f-724">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="34e7f-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="34e7f-725">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="34e7f-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="34e7f-726">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="34e7f-726">Added support for MSI identity</span></span>
* <span data-ttu-id="34e7f-727">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="34e7f-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="34e7f-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="34e7f-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="34e7f-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="34e7f-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="34e7f-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="34e7f-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="34e7f-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="34e7f-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="34e7f-732">AzureRM.Batch</span></span>
* <span data-ttu-id="34e7f-733">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="34e7f-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="34e7f-734">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="34e7f-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="34e7f-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="34e7f-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="34e7f-736">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="34e7f-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="34e7f-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34e7f-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="34e7f-738">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="34e7f-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="34e7f-739">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="34e7f-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="34e7f-740">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="34e7f-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="34e7f-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="34e7f-741">AzureRM.Network</span></span>
* <span data-ttu-id="34e7f-742">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="34e7f-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="34e7f-743">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="34e7f-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="34e7f-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="34e7f-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="34e7f-745">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="34e7f-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="34e7f-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="34e7f-747">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="34e7f-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="34e7f-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="34e7f-749">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="34e7f-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="34e7f-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="34e7f-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="34e7f-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34e7f-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="34e7f-752">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="34e7f-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="34e7f-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="34e7f-753">AzureRM.Sql</span></span>
* <span data-ttu-id="34e7f-754">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="34e7f-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="34e7f-755">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="34e7f-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="34e7f-756">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="34e7f-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="34e7f-757">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="34e7f-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="34e7f-758">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="34e7f-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="34e7f-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="34e7f-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="34e7f-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="34e7f-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="34e7f-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="34e7f-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="34e7f-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="34e7f-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="34e7f-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="34e7f-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="34e7f-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="34e7f-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="34e7f-765">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="34e7f-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
