---
Module Name: Az.FrontDoor
Module Guid: 91832aaa-dc11-4583-8239-adb7df531604
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Az.FrontDoor.md
ms.openlocfilehash: 669a982811a61c3cdd4522ff7eee7515deede672
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93665538"
---
# <span data-ttu-id="546e9-101">Az. FrontDoor modul</span><span class="sxs-lookup"><span data-stu-id="546e9-101">Az.FrontDoor Module</span></span>
## <span data-ttu-id="546e9-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="546e9-102">Description</span></span>
<span data-ttu-id="546e9-103">Az ebben a szakaszban szereplő témakörök az Azure-alapú bejárati ajtó szolgáltatás Azure PowerShell-parancsmagjai az Azure Resource Manager (ARM) keretrendszerben című témakörben olvashatók.</span><span class="sxs-lookup"><span data-stu-id="546e9-103">The topics in this section document the Azure PowerShell cmdlets for Azure Front Door Service in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="546e9-104">A parancsmagok a Microsoft. Azure. commands. FrontDoor névtérben találhatók.</span><span class="sxs-lookup"><span data-stu-id="546e9-104">The cmdlets exist in the Microsoft.Azure.Commands.FrontDoor namespace.</span></span>

## <span data-ttu-id="546e9-105">Az. FrontDoor parancsmagok</span><span class="sxs-lookup"><span data-stu-id="546e9-105">Az.FrontDoor Cmdlets</span></span>
### [<span data-ttu-id="546e9-106">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="546e9-106">Disable-AzFrontDoorCustomDomainHttps</span></span>](Disable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="546e9-107">HTTPS letiltása egyéni tartományhoz</span><span class="sxs-lookup"><span data-stu-id="546e9-107">Disable HTTPS for a custom domain</span></span>

### [<span data-ttu-id="546e9-108">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="546e9-108">Enable-AzFrontDoorCustomDomainHttps</span></span>](Enable-AzFrontDoorCustomDomainHttps.md)
<span data-ttu-id="546e9-109">Engedélyezze a HTTPS protokollt egy egyéni tartományhoz az első ajtó által felügyelt tanúsítvány segítségével, vagy használja az Azure Key Vault saját tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="546e9-109">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

### [<span data-ttu-id="546e9-110">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="546e9-110">Get-AzFrontDoor</span></span>](Get-AzFrontDoor.md)
<span data-ttu-id="546e9-111">A bejárati ajtó betöltője</span><span class="sxs-lookup"><span data-stu-id="546e9-111">Get Front Door load balancer</span></span>

### [<span data-ttu-id="546e9-112">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="546e9-112">Get-AzFrontDoorFrontendEndpoint</span></span>](Get-AzFrontDoorFrontendEndpoint.md)
<span data-ttu-id="546e9-113">Első ajtós felület végpontjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="546e9-113">Get a front door frontend endpoint.</span></span>

### [<span data-ttu-id="546e9-114">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="546e9-114">Get-AzFrontDoorWafPolicy</span></span>](Get-AzFrontDoorWafPolicy.md)
<span data-ttu-id="546e9-115">A WAF házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="546e9-115">Get WAF policy</span></span>

### [<span data-ttu-id="546e9-116">Új – AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="546e9-116">New-AzFrontDoor</span></span>](New-AzFrontDoor.md)
<span data-ttu-id="546e9-117">Új Azure bejárati ajtó kiegyenlítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="546e9-117">Create a new Azure Front Door load balancer</span></span>

### [<span data-ttu-id="546e9-118">Új – AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="546e9-118">New-AzFrontDoorBackendObject</span></span>](New-AzFrontDoorBackendObject.md)
<span data-ttu-id="546e9-119">PSBackend objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="546e9-119">Create a PSBackend object</span></span>

### [<span data-ttu-id="546e9-120">Új – AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="546e9-120">New-AzFrontDoorBackendPoolObject</span></span>](New-AzFrontDoorBackendPoolObject.md)
<span data-ttu-id="546e9-121">PSBackendPool objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="546e9-121">Create a PSBackendPool object for Front Door creation</span></span>

### [<span data-ttu-id="546e9-122">Új – AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="546e9-122">New-AzFrontDoorFrontendEndpointObject</span></span>](New-AzFrontDoorFrontendEndpointObject.md)
<span data-ttu-id="546e9-123">PSFrontendEndpoint objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="546e9-123">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

### [<span data-ttu-id="546e9-124">Új – AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="546e9-124">New-AzFrontDoorHealthProbeSettingObject</span></span>](New-AzFrontDoorHealthProbeSettingObject.md)
<span data-ttu-id="546e9-125">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="546e9-125">Create a PSHealthProbeSetting object for Front Door creation</span></span>

### [<span data-ttu-id="546e9-126">Új – AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="546e9-126">New-AzFrontDoorLoadBalancingSettingObject</span></span>](New-AzFrontDoorLoadBalancingSettingObject.md)
<span data-ttu-id="546e9-127">PSLoadBalancingSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="546e9-127">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

### [<span data-ttu-id="546e9-128">Új – AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="546e9-128">New-AzFrontDoorRoutingRuleObject</span></span>](New-AzFrontDoorRoutingRuleObject.md)
<span data-ttu-id="546e9-129">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="546e9-129">Create a PSRoutingRuleObject for Front Door creation</span></span>

### [<span data-ttu-id="546e9-130">Új – AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="546e9-130">New-AzFrontDoorWafCustomRuleObject</span></span>](New-AzFrontDoorWafCustomRuleObject.md)
<span data-ttu-id="546e9-131">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="546e9-131">Create CustomRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="546e9-132">Új – AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="546e9-132">New-AzFrontDoorWafManagedRuleObject</span></span>](New-AzFrontDoorWafManagedRuleObject.md)
<span data-ttu-id="546e9-133">ManagedRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="546e9-133">Create ManagedRule Object for WAF policy creation</span></span>

### [<span data-ttu-id="546e9-134">Új – AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="546e9-134">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>](New-AzFrontDoorWafManagedRuleOverrideObject.md)
<span data-ttu-id="546e9-135">Felügyelt szabály létrehozása objektum felülírása</span><span class="sxs-lookup"><span data-stu-id="546e9-135">Create managed rule override object</span></span>

### [<span data-ttu-id="546e9-136">Új – AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="546e9-136">New-AzFrontDoorWafMatchConditionObject</span></span>](New-AzFrontDoorWafMatchConditionObject.md)
<span data-ttu-id="546e9-137">MatchCondition objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="546e9-137">Create MatchCondition Object for WAF policy creation</span></span>

### [<span data-ttu-id="546e9-138">Új – AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="546e9-138">New-AzFrontDoorWafPolicy</span></span>](New-AzFrontDoorWafPolicy.md)
<span data-ttu-id="546e9-139">WAF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="546e9-139">Create WAF policy</span></span>

### [<span data-ttu-id="546e9-140">Új – AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="546e9-140">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](New-AzFrontDoorWafRuleGroupOverrideObject.md)
<span data-ttu-id="546e9-141">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="546e9-141">Create RuleGroupOverride Object for WAF policy creation</span></span>

### [<span data-ttu-id="546e9-142">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="546e9-142">Remove-AzFrontDoor</span></span>](Remove-AzFrontDoor.md)
<span data-ttu-id="546e9-143">A bejárati ajtó kiegyenlítő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="546e9-143">Remove Front Door load balancer</span></span>

### [<span data-ttu-id="546e9-144">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="546e9-144">Remove-AzFrontDoorContent</span></span>](Remove-AzFrontDoorContent.md)
<span data-ttu-id="546e9-145">Tartalom eltávolítása a bejárati ajtón</span><span class="sxs-lookup"><span data-stu-id="546e9-145">Remove contents in Front Door</span></span>

### [<span data-ttu-id="546e9-146">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="546e9-146">Remove-AzFrontDoorWafPolicy</span></span>](Remove-AzFrontDoorWafPolicy.md)
<span data-ttu-id="546e9-147">A WAF házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="546e9-147">Remove WAF policy</span></span>

### [<span data-ttu-id="546e9-148">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="546e9-148">Set-AzFrontDoor</span></span>](Set-AzFrontDoor.md)
<span data-ttu-id="546e9-149">Első ajtós terheléselosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="546e9-149">Update a Front Door load balancer</span></span>

### [<span data-ttu-id="546e9-150">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="546e9-150">Update-AzFrontDoorWafPolicy</span></span>](Update-AzFrontDoorWafPolicy.md)
<span data-ttu-id="546e9-151">A WAF házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="546e9-151">Update WAF policy</span></span>

