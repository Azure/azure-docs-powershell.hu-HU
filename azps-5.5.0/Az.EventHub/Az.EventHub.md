---
Module Name: Az.EventHub
Module Guid: 5728d353-7ad5-42d8-b00a-46aaecf07b91
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.eventhub
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
ms.openlocfilehash: 55b29c8e78039c97b867ae39556b5d9a2383bd71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147963"
---
# <span data-ttu-id="fc0d5-101">Az.EventHub modul</span><span class="sxs-lookup"><span data-stu-id="fc0d5-101">Az.EventHub Module</span></span>
## <span data-ttu-id="fc0d5-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc0d5-102">Description</span></span>
<span data-ttu-id="fc0d5-103">Ez a témakör az Azure Event Hub PowerShell-erőforrás-kezelő parancsmagokkal kapcsolatos súgóját mutatja be.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-103">This topic displays help for the Azure Event Hub PowerShell resource manager cmdlets.</span></span>

## <span data-ttu-id="fc0d5-104">Az.EventHub parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fc0d5-104">Az.EventHub Cmdlets</span></span>
### [<span data-ttu-id="fc0d5-105">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-105">Add-AzEventHubIPRule</span></span>](Add-AzEventHubIPRule.md)
<span data-ttu-id="fc0d5-106">Egyetlen IP-szabály hozzáadása a megadott Namespace NetworkRuleSet-hez</span><span class="sxs-lookup"><span data-stu-id="fc0d5-106">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

### [<span data-ttu-id="fc0d5-107">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-107">Add-AzEventHubVirtualNetworkRule</span></span>](Add-AzEventHubVirtualNetworkRule.md)
<span data-ttu-id="fc0d5-108">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSethez a megadott Namespace névtérhez</span><span class="sxs-lookup"><span data-stu-id="fc0d5-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

### [<span data-ttu-id="fc0d5-109">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="fc0d5-109">Get-AzEventHub</span></span>](Get-AzEventHub.md)
<span data-ttu-id="fc0d5-110">Lekérte egyetlen eseményközpont adatait, vagy lekérte az Eseményközpontok listáját.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-110">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

### [<span data-ttu-id="fc0d5-111">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-111">Get-AzEventHubAuthorizationRule</span></span>](Get-AzEventHubAuthorizationRule.md)
<span data-ttu-id="fc0d5-112">Lekérte egy engedélyezési szabály részleteit, vagy lekérte az engedélyezési szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-112">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

### [<span data-ttu-id="fc0d5-113">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="fc0d5-113">Get-AzEventHubCluster</span></span>](Get-AzEventHubCluster.md)
<span data-ttu-id="fc0d5-114">Lekérte egyetlen dedikált eseményközpont-fürt adatait, vagy lekérte a dedikált eseményközpont-fürtök listáját az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-114">Gets the details of a single Dedicated Event Hub Cluster, or gets a list of Dedicated Event Hub Clusters in given Resourcegroup.</span></span>

### [<span data-ttu-id="fc0d5-115">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="fc0d5-115">Get-AzEventHubClustersAvailableRegion</span></span>](Get-AzEventHubClustersAvailableRegion.md)
<span data-ttu-id="fc0d5-116">Azon régiók listájának lekérte, ahol rendelkezésre állnak dedikált eseményközpont-fürtök</span><span class="sxs-lookup"><span data-stu-id="fc0d5-116">Gets the list of regions where Dedicated Event Hub Clusters are available</span></span>

### [<span data-ttu-id="fc0d5-117">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fc0d5-117">Get-AzEventHubConsumerGroup</span></span>](Get-AzEventHubConsumerGroup.md)
<span data-ttu-id="fc0d5-118">Lekérte egy adott Eseményközpont fogyasztói csoportjának adatait, vagy lekérte egy fogyasztói csoportok listáját az Eseményközpontban.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-118">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

### [<span data-ttu-id="fc0d5-119">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc0d5-119">Get-AzEventHubGeoDRConfiguration</span></span>](Get-AzEventHubGeoDRConfiguration.md)
<span data-ttu-id="fc0d5-120">Beolvassa az alias(katasztrófa-helyreállítási konfiguráció) beállítást az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="fc0d5-120">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

### [<span data-ttu-id="fc0d5-121">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="fc0d5-121">Get-AzEventHubKey</span></span>](Get-AzEventHubKey.md)
<span data-ttu-id="fc0d5-122">Lekérte a megadott Eseményközpontok engedélyezési szabályának elsődleges kulcsának adatait.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-122">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

### [<span data-ttu-id="fc0d5-123">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fc0d5-123">Get-AzEventHubNamespace</span></span>](Get-AzEventHubNamespace.md)
<span data-ttu-id="fc0d5-124">Lekérte egy Eseményközpont névterének adatait, vagy lekérte az aktuális Azure-előfizetés összes Event Hubs névterét.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-124">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

### [<span data-ttu-id="fc0d5-125">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc0d5-125">Get-AzEventHubNetworkRuleSet</span></span>](Get-AzEventHubNetworkRuleSet.md)
<span data-ttu-id="fc0d5-126">Az aktuális Azure-előfizetés névterének Eseményközpontok NetworkruleSet-ének adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-126">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

### [<span data-ttu-id="fc0d5-127">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="fc0d5-127">New-AzEventHub</span></span>](New-AzEventHub.md)
<span data-ttu-id="fc0d5-128">Létrehoz egy új eseményközpontot.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-128">Creates a new Event Hub.</span></span>

### [<span data-ttu-id="fc0d5-129">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-129">New-AzEventHubAuthorizationRule</span></span>](New-AzEventHubAuthorizationRule.md)
<span data-ttu-id="fc0d5-130">Létrehoz egy új Eseményközpontok engedélyezési szabályt a namespace vagy az eventhub számára.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-130">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

### [<span data-ttu-id="fc0d5-131">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="fc0d5-131">New-AzEventHubAuthorizationRuleSASToken</span></span>](New-AzEventHubAuthorizationRuleSASToken.md)
<span data-ttu-id="fc0d5-132">A namespace/eventhub AZURE eventhub engedélyezési szabályának SAS-tolen-ét generálja.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-132">Generates a SAS tolen for Azure eventhub authorization rule of namespace/eventhub.</span></span>

### [<span data-ttu-id="fc0d5-133">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="fc0d5-133">New-AzEventHubCluster</span></span>](New-AzEventHubCluster.md)
<span data-ttu-id="fc0d5-134">Létrehoz egy új dedikált Eventhub-fürtöt a megadott erőforráscsoportban és helyen</span><span class="sxs-lookup"><span data-stu-id="fc0d5-134">Creates a new Dedicated Eventhub cluster in the given Resource Group and location</span></span>

### [<span data-ttu-id="fc0d5-135">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fc0d5-135">New-AzEventHubConsumerGroup</span></span>](New-AzEventHubConsumerGroup.md)
<span data-ttu-id="fc0d5-136">Létrehoz egy új fogyasztói csoportot a megadott Eseményközponthoz.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-136">Creates a new consumer group for the specified Event Hub.</span></span>

### [<span data-ttu-id="fc0d5-137">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc0d5-137">New-AzEventHubGeoDRConfiguration</span></span>](New-AzEventHubGeoDRConfiguration.md)
<span data-ttu-id="fc0d5-138">Létrehoz egy új aliast(katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="fc0d5-138">Creates an new Alias(Disaster Recovery configuration)</span></span>

### [<span data-ttu-id="fc0d5-139">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="fc0d5-139">New-AzEventHubKey</span></span>](New-AzEventHubKey.md)
<span data-ttu-id="fc0d5-140">Létrehoz egy új elsődleges vagy másodlagos kulcsot a megadott Eseményközpontok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-140">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

### [<span data-ttu-id="fc0d5-141">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fc0d5-141">New-AzEventHubNamespace</span></span>](New-AzEventHubNamespace.md)
<span data-ttu-id="fc0d5-142">Létrehozza az Eseményközpontok névterét.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-142">Creates an Event Hubs namespace.</span></span>

### [<span data-ttu-id="fc0d5-143">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-143">Remove-AzEventHubIPRule</span></span>](Remove-AzEventHubIPRule.md)
<span data-ttu-id="fc0d5-144">Egyetlen IP-szabály eltávolítása a megadott Namespace NetworkRuleSet szolgáltatásba</span><span class="sxs-lookup"><span data-stu-id="fc0d5-144">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

### [<span data-ttu-id="fc0d5-145">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="fc0d5-145">Remove-AzEventHub</span></span>](Remove-AzEventHub.md)
<span data-ttu-id="fc0d5-146">A megadott eseményközpont eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-146">Removes the specified Event Hub.</span></span>

### [<span data-ttu-id="fc0d5-147">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-147">Remove-AzEventHubVirtualNetworkRule</span></span>](Remove-AzEventHubVirtualNetworkRule.md)
<span data-ttu-id="fc0d5-148">Eltávolítja a Namespace NetworkRuleSet virtualnetworkRule-ét</span><span class="sxs-lookup"><span data-stu-id="fc0d5-148">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### [<span data-ttu-id="fc0d5-149">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc0d5-149">Remove-AzEventHubNetworkRuleSet</span></span>](Remove-AzEventHubNetworkRuleSet.md)
<span data-ttu-id="fc0d5-150">A Megadott névtér NetworkRuleSet-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fc0d5-150">Removes the NetworkRuleSet for the Given Namespace</span></span>

### [<span data-ttu-id="fc0d5-151">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-151">Remove-AzEventHubAuthorizationRule</span></span>](Remove-AzEventHubAuthorizationRule.md)
<span data-ttu-id="fc0d5-152">Eltávolítja a megadott eseményközpont engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-152">Removes the specified Event Hub authorization rule.</span></span>

### [<span data-ttu-id="fc0d5-153">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="fc0d5-153">Remove-AzEventHubCluster</span></span>](Remove-AzEventHubCluster.md)
<span data-ttu-id="fc0d5-154">A megadott dedikált Eventhub-fürt törlése az Erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="fc0d5-154">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

### [<span data-ttu-id="fc0d5-155">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fc0d5-155">Remove-AzEventHubConsumerGroup</span></span>](Remove-AzEventHubConsumerGroup.md)
<span data-ttu-id="fc0d5-156">Törli a megadott Eseményközpontok fogyasztói csoportot.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-156">Deletes the specified Event Hubs consumer group.</span></span>

### [<span data-ttu-id="fc0d5-157">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc0d5-157">Remove-AzEventHubGeoDRConfiguration</span></span>](Remove-AzEventHubGeoDRConfiguration.md)
<span data-ttu-id="fc0d5-158">Alias törlése(Katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="fc0d5-158">Deletes an Alias(Disaster Recovery configuration)</span></span>

### [<span data-ttu-id="fc0d5-159">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fc0d5-159">Remove-AzEventHubNamespace</span></span>](Remove-AzEventHubNamespace.md)
<span data-ttu-id="fc0d5-160">Eltávolítja az Eseményközpontok megadott névterét.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-160">Removes the specified Event Hubs namespace.</span></span>

### [<span data-ttu-id="fc0d5-161">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="fc0d5-161">Set-AzEventHub</span></span>](Set-AzEventHub.md)
<span data-ttu-id="fc0d5-162">Frissíti a megadott eseményközpontot.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-162">Updates the specified Event Hub.</span></span>

### [<span data-ttu-id="fc0d5-163">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fc0d5-163">Set-AzEventHubAuthorizationRule</span></span>](Set-AzEventHubAuthorizationRule.md)
<span data-ttu-id="fc0d5-164">Frissíti a megadott engedélyezési szabályt egy eseményközpontban.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-164">Updates the specified authorization rule on an Event Hub.</span></span>

### [<span data-ttu-id="fc0d5-165">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="fc0d5-165">Set-AzEventHubCluster</span></span>](Set-AzEventHubCluster.md)
<span data-ttu-id="fc0d5-166">Az adott fürt címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="fc0d5-166">Updates the Tags for the given Cluster</span></span>

### [<span data-ttu-id="fc0d5-167">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fc0d5-167">Set-AzEventHubConsumerGroup</span></span>](Set-AzEventHubConsumerGroup.md)
<span data-ttu-id="fc0d5-168">Frissíti a megadott Eseményközpontok fogyasztói csoportot.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-168">Updates the specified Event Hubs consumer group.</span></span>

### [<span data-ttu-id="fc0d5-169">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="fc0d5-169">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>](Set-AzEventHubGeoDRConfigurationBreakPair.md)
<span data-ttu-id="fc0d5-170">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-170">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

### [<span data-ttu-id="fc0d5-171">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="fc0d5-171">Set-AzEventHubGeoDRConfigurationFailOver</span></span>](Set-AzEventHubGeoDRConfigurationFailOver.md)
<span data-ttu-id="fc0d5-172">A GEO DR feladatátvételének meghívása és az alias újrakonfigurálása a másodlagos névtérre</span><span class="sxs-lookup"><span data-stu-id="fc0d5-172">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

### [<span data-ttu-id="fc0d5-173">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fc0d5-173">Set-AzEventHubNamespace</span></span>](Set-AzEventHubNamespace.md)
<span data-ttu-id="fc0d5-174">Frissíti a megadott Event Hubs névteret.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-174">Updates the specified Event Hubs namespace.</span></span>

### [<span data-ttu-id="fc0d5-175">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc0d5-175">Set-AzEventHubNetworkRuleSet</span></span>](Set-AzEventHubNetworkRuleSet.md)
<span data-ttu-id="fc0d5-176">Frissítse az aktuális Azure-előfizetés adott Névterének NetworkruleSet szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="fc0d5-176">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

### [<span data-ttu-id="fc0d5-177">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="fc0d5-177">Test-AzEventHubName</span></span>](Test-AzEventHubName.md)
<span data-ttu-id="fc0d5-178">A megadott Névtérnév vagy Alias elérhetőségének ellenőrzése (DR konfiguráció neve)</span><span class="sxs-lookup"><span data-stu-id="fc0d5-178">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

