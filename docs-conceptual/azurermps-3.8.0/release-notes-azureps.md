---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 2e17b6f7f62f25d8d91c4d32a4a1ae5c45b8665d
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821802"
---
# <a name="release-notes"></a><span data-ttu-id="7bebc-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="7bebc-103">Release notes</span></span>

<span data-ttu-id="7bebc-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="7bebc-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="7bebc-105">3.8.0-ás verzió</span><span class="sxs-lookup"><span data-stu-id="7bebc-105">Version 3.8.0</span></span>
* <span data-ttu-id="7bebc-106">Compute</span><span class="sxs-lookup"><span data-stu-id="7bebc-106">Compute</span></span>
  - <span data-ttu-id="7bebc-107">A Get-\* parancsmagok hibájának javítása több oldalnyi adat (több, mint 120 elem) lekérésének lehetővé tétele érdekében</span><span class="sxs-lookup"><span data-stu-id="7bebc-107">Fix bug in Get-\* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="7bebc-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7bebc-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="7bebc-109">Egyes parancsok súgójának javítása a megfelelő megfogalmazás és példák érdekében.</span><span class="sxs-lookup"><span data-stu-id="7bebc-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="7bebc-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7bebc-110">DataLakeStore</span></span>
  - <span data-ttu-id="7bebc-111">A `Get-AzureRMDataLakeStoreItemContent` parancsmag elejének és végének támogatása.</span><span class="sxs-lookup"><span data-stu-id="7bebc-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="7bebc-112">Ez lehetővé teszi az új, megjelenítendő felső N vagy utolsó N vonalakkal tagolt sor visszaadását.</span><span class="sxs-lookup"><span data-stu-id="7bebc-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="7bebc-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="7bebc-113">HDInsight</span></span>
  - <span data-ttu-id="7bebc-114">Az RServer-fürttípus támogatása</span><span class="sxs-lookup"><span data-stu-id="7bebc-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="7bebc-115">Az élcsomópontok virtuális gépeinek mérete a New-AzureRmHDInsightCluster vagy New-AzureRmHDInsightClusterConfig parancsmagokban adható meg az RServer-fürt esetében</span><span class="sxs-lookup"><span data-stu-id="7bebc-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="7bebc-116">Az RServer mostantól egy konfigurációs beállítás az Add-AzureRmHDInsightConfigValues parancsmagon belül.</span><span class="sxs-lookup"><span data-stu-id="7bebc-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="7bebc-117">Ez lehetővé teszi az RStudio-jelző beállítását, amely jelzi, hogy az R Studio telepítését el kell végezni.</span><span class="sxs-lookup"><span data-stu-id="7bebc-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="7bebc-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="7bebc-118">LogicApp</span></span>
  - <span data-ttu-id="7bebc-119">A Set-AzureRmIntegrationAccountSchema és Set-AzureRmIntegrationAccountMap parancsmagok contentlink-hibájának javítása (a content és contentlink paraméterek egyaránt meg voltak adva, amely a frissítés meghiúsulását okozta).</span><span class="sxs-lookup"><span data-stu-id="7bebc-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="7bebc-120">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="7bebc-120">Network</span></span>
  - <span data-ttu-id="7bebc-121">Új webalkalmazási tűzfalszolgáltatások támogatása az Application Gateway átjárók esetében</span><span class="sxs-lookup"><span data-stu-id="7bebc-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="7bebc-122">A New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7bebc-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="7bebc-123">A Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets) hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7bebc-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="7bebc-124">A New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration frissítése: A -RuleSetType, -RuleSetVersion és -DisabledRuleGroups paraméterek hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7bebc-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="7bebc-125">A Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration frissítése: A -RuleSetType, -RuleSetVersion és -DisabledRuleGroups paraméter hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7bebc-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="7bebc-126">IPsec-házirendek támogatása a virtuális hálózati átjárókapcsolatok esetében</span><span class="sxs-lookup"><span data-stu-id="7bebc-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="7bebc-127">A New-AzureRmIpsecPolicy parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7bebc-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="7bebc-128">A New-AzureRmVirtualNetworkGatewayConnection frissítése: Az -IpsecPolicies és -UsePolicyBasedTrafficSelectors paraméter hozzáadása</span><span class="sxs-lookup"><span data-stu-id="7bebc-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="7bebc-129">Profil</span><span class="sxs-lookup"><span data-stu-id="7bebc-129">Profile</span></span>
  - <span data-ttu-id="7bebc-130">*Elavult*: A Save-AzureRmProfile parancsmag új neve: Save-AzureRmContext. Létezik egy alias a régi parancsmag nevéhez, amely a következő kiadásban el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="7bebc-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="7bebc-131">*Elavult*: A Select-AzureRmProfile parancsmag új neve: Import-AzureRmContext. Létezik egy alias a régi parancsmag nevéhez, amely a következő kiadásban el lesz távolítva.</span><span class="sxs-lookup"><span data-stu-id="7bebc-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="7bebc-132">A profilparancsmagok PSAzureContext és PSAzureProfile kimenettípusa a következő kiadásban módosítva lesz.</span><span class="sxs-lookup"><span data-stu-id="7bebc-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="7bebc-133">A Save-AzureRmContext parancsmag nem rendelkezik majd OutputType paraméterrel a következő kiadásban.</span><span class="sxs-lookup"><span data-stu-id="7bebc-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="7bebc-134">Hiba javítása a parancsmagok általános kódjában annak érdekében, hogy azok a FIPS előírásainak megfelelő algoritmusokat használjanak az adatkivonatokhoz: https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="7bebc-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="7bebc-135">SQL</span><span class="sxs-lookup"><span data-stu-id="7bebc-135">Sql</span></span>
  - <span data-ttu-id="7bebc-136">Hibajavítások az Azure feladatátvételi csoport parancsmagjaiban</span><span class="sxs-lookup"><span data-stu-id="7bebc-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="7bebc-137">Műveletlekérdezés javítása</span><span class="sxs-lookup"><span data-stu-id="7bebc-137">Fix for operation polling</span></span>
  - <span data-ttu-id="7bebc-138">A GracePeriodWithDataLossHour érték javítása a FailoverPolicy paraméter Manual (Manuális) értékre való állításakor</span><span class="sxs-lookup"><span data-stu-id="7bebc-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="7bebc-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7bebc-139">TrafficManager</span></span>
  - <span data-ttu-id="7bebc-140">A földrajzi forgalom-útválasztási módszer támogatása</span><span class="sxs-lookup"><span data-stu-id="7bebc-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="7bebc-141">Új „Geographic” érték a New-AzureRmTrafficManagerProfile parancsmag TrafficRoutingMethod paramétere esetében</span><span class="sxs-lookup"><span data-stu-id="7bebc-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="7bebc-142">Új „GeoMapping” paraméter a New-AzureRmTrafficManagerEndpoint és Add-AzureRmTrafficManagerEndpointConfig parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="7bebc-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="7bebc-143">Az átirányítás javítása a Get-AzureRmTrafficManagerProfile parancsmag esetében profilgyűjtemény visszaadásakor</span><span class="sxs-lookup"><span data-stu-id="7bebc-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="7bebc-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="7bebc-144">ServiceManagement</span></span>
  - <span data-ttu-id="7bebc-145">Restart-AzureVM: Az InitiateMaintenance paraméter hozzáadása arra az esetre, ha a karbantartás elvégzése a virtuális gép újraindítása során történik.</span><span class="sxs-lookup"><span data-stu-id="7bebc-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="7bebc-146">Get-AzureVM: Maintenance Status (Karbantartás állapota) mező hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="7bebc-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="7bebc-147">Új parancsmagok hozzáadása a Recovery Services-tároló frissítésének támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="7bebc-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="7bebc-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="7bebc-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="7bebc-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="7bebc-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
