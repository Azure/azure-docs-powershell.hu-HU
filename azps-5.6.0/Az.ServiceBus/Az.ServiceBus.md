---
Module Name: Az.ServiceBus
Module Guid: cc69c625-e961-43f4-8b50-0061eba6e4b6
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicebus
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
ms.openlocfilehash: 7f5c2658b32b0bf713dc131474eca30e57955187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007606"
---
# <span data-ttu-id="27e2d-101">Az.ServiceBus modul</span><span class="sxs-lookup"><span data-stu-id="27e2d-101">Az.ServiceBus Module</span></span>
## <span data-ttu-id="27e2d-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="27e2d-102">Description</span></span>
<span data-ttu-id="27e2d-103">Ez a témakör az Azure Service Bus parancsmagok súgótémakörét mutatja be.</span><span class="sxs-lookup"><span data-stu-id="27e2d-103">This topic displays help topics for the Azure Service Bus cmdlets.</span></span>

## <span data-ttu-id="27e2d-104">Az.ServiceBus-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="27e2d-104">Az.ServiceBus Cmdlets</span></span>
### [<span data-ttu-id="27e2d-105">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="27e2d-105">Complete-AzServiceBusMigration</span></span>](Complete-AzServiceBusMigration.md)
<span data-ttu-id="27e2d-106">A parancsmagok az Áttelepítés standardról prémium névtérre teljesként, a normál névtér kapcsolati karakterláncai pedig a Prémium névtérre mutatnak</span><span class="sxs-lookup"><span data-stu-id="27e2d-106">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

### [<span data-ttu-id="27e2d-107">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-107">Get-AzServiceBusAuthorizationRule</span></span>](Get-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="27e2d-108">Egy adott névtérhez, várólistához, témakörhez vagy aliashoz (GeoDR-konfigurációk) megadott engedélyezési szabály leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="27e2d-108">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

### [<span data-ttu-id="27e2d-109">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="27e2d-109">Get-AzServiceBusGeoDRConfiguration</span></span>](Get-AzServiceBusGeoDRConfiguration.md)
<span data-ttu-id="27e2d-110">Beolvassa az alias(katasztrófa-helyreállítási konfiguráció) beállítást az elsődleges vagy másodlagos névtérhez</span><span class="sxs-lookup"><span data-stu-id="27e2d-110">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

### [<span data-ttu-id="27e2d-111">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="27e2d-111">Get-AzServiceBusKey</span></span>](Get-AzServiceBusKey.md)
<span data-ttu-id="27e2d-112">A megadott Névtér, Várólista vagy Témakör vagy Alias (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="27e2d-112">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

### [<span data-ttu-id="27e2d-113">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="27e2d-113">Get-AzServiceBusMigration</span></span>](Get-AzServiceBusMigration.md)
<span data-ttu-id="27e2d-114">Beolvassa a MigrationConfiguration nevet a névtérhez</span><span class="sxs-lookup"><span data-stu-id="27e2d-114">Retrieves MigrationConfiguration for the namespace</span></span>

### [<span data-ttu-id="27e2d-115">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="27e2d-115">Get-AzServiceBusNamespace</span></span>](Get-AzServiceBusNamespace.md)
<span data-ttu-id="27e2d-116">Az erőforráscsoporton belül a szolgáltatás-busz névterének leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="27e2d-116">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

### [<span data-ttu-id="27e2d-117">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="27e2d-117">Get-AzServiceBusOperation</span></span>](Get-AzServiceBusOperation.md)
<span data-ttu-id="27e2d-118">Támogatott ServiceBus-műveletek listája</span><span class="sxs-lookup"><span data-stu-id="27e2d-118">List supported ServiceBus Operations</span></span>

### [<span data-ttu-id="27e2d-119">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="27e2d-119">Get-AzServiceBusQueue</span></span>](Get-AzServiceBusQueue.md)
<span data-ttu-id="27e2d-120">A megadott szolgáltatásbusz-várólistához ad leírást.</span><span class="sxs-lookup"><span data-stu-id="27e2d-120">Returns a description for the specified Service Bus queue.</span></span>

### [<span data-ttu-id="27e2d-121">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-121">Get-AzServiceBusRule</span></span>](Get-AzServiceBusRule.md)
<span data-ttu-id="27e2d-122">Új szabályt hoz létre egy adott témakör-előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="27e2d-122">Creates a new rule for a given Subscription of Topic.</span></span> 

### [<span data-ttu-id="27e2d-123">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="27e2d-123">Get-AzServiceBusSubscription</span></span>](Get-AzServiceBusSubscription.md)
<span data-ttu-id="27e2d-124">A megadott témakör előfizetési leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="27e2d-124">Returns a subscription description for the specified topic.</span></span>

### [<span data-ttu-id="27e2d-125">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="27e2d-125">Get-AzServiceBusTopic</span></span>](Get-AzServiceBusTopic.md)
<span data-ttu-id="27e2d-126">A megadott Service Bus-témakör leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="27e2d-126">Returns a description for the specified Service Bus topic.</span></span>

### [<span data-ttu-id="27e2d-127">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-127">New-AzServiceBusAuthorizationRule</span></span>](New-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="27e2d-128">Új engedélyezési szabályt hoz létre a megadott Service Bus névterhez, várólistához vagy témakörhez.</span><span class="sxs-lookup"><span data-stu-id="27e2d-128">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

### [<span data-ttu-id="27e2d-129">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="27e2d-129">New-AzServiceBusAuthorizationRuleSASToken</span></span>](New-AzServiceBusAuthorizationRuleSASToken.md)
<span data-ttu-id="27e2d-130">Egy SAS-tolen-t hoz létre a névtér/várólista/témakör Azure serviucebus engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="27e2d-130">Generates a SAS tolen for Azure serviucebus authorization rule of namespace/queue/topic.</span></span> 

### [<span data-ttu-id="27e2d-131">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="27e2d-131">New-AzServiceBusGeoDRConfiguration</span></span>](New-AzServiceBusGeoDRConfiguration.md)
<span data-ttu-id="27e2d-132">Létrehoz egy új aliast(katasztrófa-helyreállítási konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="27e2d-132">Creates an new Alias(Disaster Recovery configuration)</span></span>

### [<span data-ttu-id="27e2d-133">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="27e2d-133">New-AzServiceBusKey</span></span>](New-AzServiceBusKey.md)
<span data-ttu-id="27e2d-134">A Szolgáltatásbusz névterében, illetve várólistában vagy témakörben található elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="27e2d-134">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

### [<span data-ttu-id="27e2d-135">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="27e2d-135">New-AzServiceBusNamespace</span></span>](New-AzServiceBusNamespace.md)
<span data-ttu-id="27e2d-136">Új Service Bus névteret hoz létre.</span><span class="sxs-lookup"><span data-stu-id="27e2d-136">Creates a new Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-137">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="27e2d-137">New-AzServiceBusQueue</span></span>](New-AzServiceBusQueue.md)
<span data-ttu-id="27e2d-138">Szolgáltatásbusz-várólistát hoz létre a szolgáltatásbusz névterében.</span><span class="sxs-lookup"><span data-stu-id="27e2d-138">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-139">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-139">New-AzServiceBusRule</span></span>](New-AzServiceBusRule.md)
<span data-ttu-id="27e2d-140">Új szabályt hoz létre egy adott témakör-előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="27e2d-140">Creates a new rule for a given Subscription of Topic.</span></span> 

### [<span data-ttu-id="27e2d-141">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="27e2d-141">New-AzServiceBusSubscription</span></span>](New-AzServiceBusSubscription.md)
<span data-ttu-id="27e2d-142">Létrehoz egy előfizetést a megadott Service Bus témához.</span><span class="sxs-lookup"><span data-stu-id="27e2d-142">Creates a subscription to the specified Service Bus topic.</span></span>

### [<span data-ttu-id="27e2d-143">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="27e2d-143">New-AzServiceBusTopic</span></span>](New-AzServiceBusTopic.md)
<span data-ttu-id="27e2d-144">Létrehoz egy új Service Bus-témakört a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="27e2d-144">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-145">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-145">Remove-AzServiceBusAuthorizationRule</span></span>](Remove-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="27e2d-146">Eltávolítja egy szolgáltatásbusz névterének vagy várólistájának vagy témájának engedélyezési szabályát a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="27e2d-146">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

### [<span data-ttu-id="27e2d-147">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="27e2d-147">Remove-AzServiceBusGeoDRConfiguration</span></span>](Remove-AzServiceBusGeoDRConfiguration.md)
<span data-ttu-id="27e2d-148">Alias törlése(Katasztrófa-helyreállítás konfiguráció)</span><span class="sxs-lookup"><span data-stu-id="27e2d-148">Deletes an Alias(Disaster Recovery configuration)</span></span>

### [<span data-ttu-id="27e2d-149">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="27e2d-149">Remove-AzServiceBusMigration</span></span>](Remove-AzServiceBusMigration.md)
<span data-ttu-id="27e2d-150">Parancsmag törli a Standard–Premium névterek áttelepítési konfigurációját</span><span class="sxs-lookup"><span data-stu-id="27e2d-150">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

### [<span data-ttu-id="27e2d-151">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="27e2d-151">Remove-AzServiceBusNamespace</span></span>](Remove-AzServiceBusNamespace.md)
<span data-ttu-id="27e2d-152">Eltávolítja a névteret a megadott erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="27e2d-152">Removes the namespace from the specified resource group.</span></span> 

### [<span data-ttu-id="27e2d-153">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="27e2d-153">Remove-AzServiceBusQueue</span></span>](Remove-AzServiceBusQueue.md)
<span data-ttu-id="27e2d-154">Eltávolítja a várólistát a szolgáltatásbusz megadott névterében.</span><span class="sxs-lookup"><span data-stu-id="27e2d-154">Removes the queue from the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-155">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-155">Remove-AzServiceBusRule</span></span>](Remove-AzServiceBusRule.md)
<span data-ttu-id="27e2d-156">Egy adott előfizetés megadott szabályának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="27e2d-156">Removes the specified rule of a given subscription .</span></span>

### [<span data-ttu-id="27e2d-157">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="27e2d-157">Remove-AzServiceBusSubscription</span></span>](Remove-AzServiceBusSubscription.md)
<span data-ttu-id="27e2d-158">Eltávolítja egy témakör előfizetését a megadott Service Bus névtérből.</span><span class="sxs-lookup"><span data-stu-id="27e2d-158">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-159">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="27e2d-159">Remove-AzServiceBusTopic</span></span>](Remove-AzServiceBusTopic.md)
<span data-ttu-id="27e2d-160">Eltávolítja a témakört a szolgáltatásbusz megadott névterében.</span><span class="sxs-lookup"><span data-stu-id="27e2d-160">Removes the topic from the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-161">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-161">Set-AzServiceBusAuthorizationRule</span></span>](Set-AzServiceBusAuthorizationRule.md)
<span data-ttu-id="27e2d-162">Frissíti a szolgáltatási-busz névterének vagy várólistájának vagy témájának engedélyezési szabályának megadott leírását.</span><span class="sxs-lookup"><span data-stu-id="27e2d-162">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

### [<span data-ttu-id="27e2d-163">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="27e2d-163">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>](Set-AzServiceBusGeoDRConfigurationBreakPair.md)
<span data-ttu-id="27e2d-164">Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.</span><span class="sxs-lookup"><span data-stu-id="27e2d-164">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

### [<span data-ttu-id="27e2d-165">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="27e2d-165">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>](Set-AzServiceBusGeoDRConfigurationFailOver.md)
<span data-ttu-id="27e2d-166">A GEO DR feladatátvételének meghívása és az alias újrakonfigurálása a másodlagos névtérre</span><span class="sxs-lookup"><span data-stu-id="27e2d-166">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

### [<span data-ttu-id="27e2d-167">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="27e2d-167">Set-AzServiceBusNamespace</span></span>](Set-AzServiceBusNamespace.md)
<span data-ttu-id="27e2d-168">Frissíti egy meglévő Szolgáltatásbusz névterének leírását.</span><span class="sxs-lookup"><span data-stu-id="27e2d-168">Updates the description of an existing Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-169">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="27e2d-169">Set-AzServiceBusQueue</span></span>](Set-AzServiceBusQueue.md)
<span data-ttu-id="27e2d-170">Frissíti a Szolgáltatásbusz várólistájának leírását a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="27e2d-170">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-171">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="27e2d-171">Set-AzServiceBusRule</span></span>](Set-AzServiceBusRule.md)
<span data-ttu-id="27e2d-172">Frissíti az adott előfizetéshez megadott szabályleírást.</span><span class="sxs-lookup"><span data-stu-id="27e2d-172">Updates the specified rule description for the given subscription.</span></span>

### [<span data-ttu-id="27e2d-173">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="27e2d-173">Set-AzServiceBusSubscription</span></span>](Set-AzServiceBusSubscription.md)
<span data-ttu-id="27e2d-174">Frissíti a Szolgáltatásbusz témakör előfizetési leírását a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="27e2d-174">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-175">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="27e2d-175">Set-AzServiceBusTopic</span></span>](Set-AzServiceBusTopic.md)
<span data-ttu-id="27e2d-176">Frissíti a Szolgáltatásbusz témakör leírását a megadott Service Bus névterében.</span><span class="sxs-lookup"><span data-stu-id="27e2d-176">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

### [<span data-ttu-id="27e2d-177">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="27e2d-177">Start-AzServiceBusMigration</span></span>](Start-AzServiceBusMigration.md)
<span data-ttu-id="27e2d-178">Új áttelepítési konfigurációt hoz létre, és megkezdi az entitások áttelepítését a Standardból a Prémium névterekbe</span><span class="sxs-lookup"><span data-stu-id="27e2d-178">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

### [<span data-ttu-id="27e2d-179">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="27e2d-179">Stop-AzServiceBusMigration</span></span>](Stop-AzServiceBusMigration.md)
<span data-ttu-id="27e2d-180">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="27e2d-180">{{Fill in the Synopsis}}</span></span>

### [<span data-ttu-id="27e2d-181">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="27e2d-181">Test-AzServiceBusName</span></span>](Test-AzServiceBusName.md)
<span data-ttu-id="27e2d-182">A megadott Névtérnév vagy Alias elérhetőségének ellenőrzése (DR konfiguráció neve)</span><span class="sxs-lookup"><span data-stu-id="27e2d-182">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

