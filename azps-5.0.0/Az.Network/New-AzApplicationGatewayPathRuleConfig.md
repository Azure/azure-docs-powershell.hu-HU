---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195384"
---
# <span data-ttu-id="0f09a-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f09a-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="0f09a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f09a-102">SYNOPSIS</span></span>
<span data-ttu-id="0f09a-103">Az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0f09a-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="0f09a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f09a-104">SYNTAX</span></span>

### <span data-ttu-id="0f09a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f09a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f09a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0f09a-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f09a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f09a-107">DESCRIPTION</span></span>
<span data-ttu-id="0f09a-108">A **New-AzApplicationGatewayPathRuleConfig** parancsmag az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0f09a-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="0f09a-109">Az e parancsmaggal létrehozott szabályok hozzáadhatók az URL-elérésiút-Térkép konfigurációs beállításainak gyűjteményéhez, majd a hozzájuk rendelt átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0f09a-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="0f09a-110">Az elérésiút-Térkép konfigurációs beállításait az Application Gateway terheléselosztási funkciói használja.</span><span class="sxs-lookup"><span data-stu-id="0f09a-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="0f09a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0f09a-111">EXAMPLES</span></span>

### <span data-ttu-id="0f09a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0f09a-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="0f09a-113">Ezekkel a parancsokkal új alkalmazás-átjáró elérésiút-szabályt hozhat létre, majd az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmaggal társíthatja ezt a szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0f09a-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="0f09a-114">Ehhez az első parancs objektumra mutató hivatkozást hoz létre az átjáró ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="0f09a-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="0f09a-115">Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="0f09a-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="0f09a-116">A következő két parancs a backend-címkészletet és a backend-alapú HTTP-beállítások objektumot hozza létre; Ezek az objektumok (a változók $AddressPool és a $HttpSettings) szükségesek az elérésiút-szabály objektum létrehozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="0f09a-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="0f09a-117">A negyedik parancs a Path Rule objektumot hozza létre, és a $PathRuleConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0f09a-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="0f09a-118">Az ötödik parancs az **Add-AzApplicationGatewayUrlPathMapConfig** használatával hozzáadja a konfigurációs beállításokat és az új elérésiút-szabályt a beállítások között a ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="0f09a-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="0f09a-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="0f09a-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="0f09a-120">A parancs létrehoz egy elérésiút-szabályt a "bázis" néven, az elérési utakat "/Base", BackendAddressPool mint $AddressPool, BackendHttpSettings mint $HttpSettings és FirewallPolicy, mint $firewallPolicy. NGS és az új elérésiút-szabály a beállítások között a ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="0f09a-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="0f09a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f09a-121">PARAMETERS</span></span>

### <span data-ttu-id="0f09a-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f09a-122">-BackendAddressPool</span></span>
<span data-ttu-id="0f09a-123">Itt adhatja meg a backend-címkészlet beállításai között az objektum hivatkozását, amelyet az átjáró elérési útjának konfigurációs beállításaihoz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="0f09a-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="0f09a-124">Az objektum hivatkozását az New-AzApplicationGatewayBackendAddressPool parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="0f09a-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="0f09a-125">Az előző parancs két IP-címet (192.16.1.1 és 192.168.1.2) ad hozzá a címkészlet számára.</span><span class="sxs-lookup"><span data-stu-id="0f09a-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="0f09a-126">Ügyeljen arra, hogy az IP-cím idézőjelek közé van írva, és vesszőkkel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="0f09a-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="0f09a-127">Az eredményül kapott változó ($AddressPool) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="0f09a-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="0f09a-128">A backend Address Pool a backend-kiszolgálók IP-címét jelöli.</span><span class="sxs-lookup"><span data-stu-id="0f09a-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="0f09a-129">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="0f09a-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="0f09a-130">Ha ezt a paramétert használja, a *DefaultBackendAddressPoolId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="0f09a-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0f09a-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="0f09a-132">Annak a meglévő backend-címkészlet az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="0f09a-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0f09a-133">A címkészlet-azonosítók az Get-AzApplicationGatewayBackendAddressPool parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="0f09a-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="0f09a-134">Miután megtörtént az azonosító, a *DefaultBackendAddressPoolId* paramétert használhatja a *DefaultBackendAddressPool* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="0f09a-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="0f09a-135">Például:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool": a backend Address Pool a backend-kiszolgálók IP-címeinek felel meg.</span><span class="sxs-lookup"><span data-stu-id="0f09a-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="0f09a-136">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="0f09a-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0f09a-137">-BackendHttpSettings</span></span>
<span data-ttu-id="0f09a-138">Az átjáró elérési útjának konfigurációs beállításaihoz hozzáadott backend-HTTP-beállításokra mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f09a-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0f09a-139">Az objektum hivatkozását az New-AzApplicationGatewayBackendHttpSettings parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-port 80-Protocol "http"-CookieBasedAffinity "disabled": az eredményül kapott változó, $HttpSettings ezt követően a *DefaultBackendAddressPool* paraméter értéke lehet:-DefaultBackendHttpSettings $HttpSettings a backend http-beállításai (például a port, a Protocol és a cookie-alapú affinitás) a backend-készletekhez használhatók.</span><span class="sxs-lookup"><span data-stu-id="0f09a-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="0f09a-140">Ha ezt a paramétert használja, a *DefaultBackendHttpSettingsId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="0f09a-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0f09a-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="0f09a-142">Annak a meglévő backend-adatgyűjteménynek az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="0f09a-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0f09a-143">A HTTP-beállítás azonosítói az Get-AzApplicationGatewayBackendHttpSettings parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="0f09a-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="0f09a-144">Miután megtörtént az azonosító, a *DefaultBackendHttpSettingsId* paramétert használhatja a *DefaultBackendHttpSettings* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="0f09a-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="0f09a-145">Például:-DefaultBackendSettings-azonosító "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings": a backend HTTP-beállításai, például a port, a Protocol és a cookie-alapú Affinitás beállítása a backend-készletben.</span><span class="sxs-lookup"><span data-stu-id="0f09a-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="0f09a-146">Ha ezt a paramétert használja, a *DefaultBackendHttpSettings* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="0f09a-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0f09a-147">-FirewallPolicy</span></span>
<span data-ttu-id="0f09a-148">A legfelső szintű tűzfal-házirendre mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f09a-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="0f09a-149">Az objektum hivatkozását New-AzApplicationGatewayWebApplicationFirewallPolicy parancsmag használatával lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="0f09a-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="0f09a-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" a fenti parancsmagot létrehozott tűzfal-házirendet az elérési út szabályi szintjén lehet megtekinteni.</span><span class="sxs-lookup"><span data-stu-id="0f09a-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="0f09a-151">a parancs a fenti paranccsal létrehozta az alapértelmezett házirend-beállításokat és felügyelt szabályokat.</span><span class="sxs-lookup"><span data-stu-id="0f09a-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="0f09a-152">Az alapértelmezett értékek helyett a felhasználók megadhatják a PolicySettings, az ManagedRules és New-AzApplicationGatewayFirewallPolicySettings a New-AzApplicationGatewayFirewallPolicyManagedRulest is.</span><span class="sxs-lookup"><span data-stu-id="0f09a-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0f09a-153">-FirewallPolicyId</span></span>
<span data-ttu-id="0f09a-154">Egy meglévő, legfelső szintű webalkalmazás-tűzfal-erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f09a-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="0f09a-155">A tűzfal-házirend azonosítóit a Get-AzApplicationGatewayWebApplicationFirewallPolicy parancsmag segítségével lehet visszaadni.</span><span class="sxs-lookup"><span data-stu-id="0f09a-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="0f09a-156">Miután rendelkezünk az AZONOSÍTÓval, a *FirewallPolicy* paraméter helyett használhatja a *FirewallPolicyId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="0f09a-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="0f09a-157">Például:-FirewallPolicyId "/Subscriptions/<előfizetés-azonosító>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="0f09a-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f09a-158">-DefaultProfile</span></span>
<span data-ttu-id="0f09a-159">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f09a-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-160">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f09a-160">-Name</span></span>
<span data-ttu-id="0f09a-161">A parancsmag által létrehozott elérésiút-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f09a-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="0f09a-162">-Paths</span></span>
<span data-ttu-id="0f09a-163">Egy vagy több alkalmazásobjektum-elérésiút-szabályt ad meg.</span><span class="sxs-lookup"><span data-stu-id="0f09a-163">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f09a-164">-RedirectConfiguration</span></span>
<span data-ttu-id="0f09a-165">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f09a-165">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0f09a-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="0f09a-167">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="0f09a-167">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0f09a-168">-RewriteRuleSet</span></span>
<span data-ttu-id="0f09a-169">Az Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0f09a-169">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="0f09a-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="0f09a-171">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="0f09a-171">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f09a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f09a-172">CommonParameters</span></span>
<span data-ttu-id="0f09a-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f09a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f09a-174">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f09a-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f09a-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f09a-175">INPUTS</span></span>

### <span data-ttu-id="0f09a-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="0f09a-176">None</span></span>

## <span data-ttu-id="0f09a-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f09a-177">OUTPUTS</span></span>

### <span data-ttu-id="0f09a-178">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="0f09a-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="0f09a-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f09a-179">NOTES</span></span>

## <span data-ttu-id="0f09a-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f09a-180">RELATED LINKS</span></span>

[<span data-ttu-id="0f09a-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f09a-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f09a-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0f09a-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0f09a-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f09a-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f09a-184">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f09a-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0f09a-185">Új – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0f09a-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="0f09a-186">Új – AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f09a-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="0f09a-187">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f09a-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f09a-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f09a-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0f09a-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0f09a-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


