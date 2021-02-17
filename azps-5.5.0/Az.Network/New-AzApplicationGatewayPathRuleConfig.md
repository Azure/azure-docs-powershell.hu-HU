---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206839"
---
# <span data-ttu-id="2acf2-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2acf2-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="2acf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2acf2-102">SYNOPSIS</span></span>
<span data-ttu-id="2acf2-103">Létrehoz egy alkalmazás-átjáró elérési útját szabályt.</span><span class="sxs-lookup"><span data-stu-id="2acf2-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="2acf2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2acf2-104">SYNTAX</span></span>

### <span data-ttu-id="2acf2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2acf2-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2acf2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2acf2-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2acf2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2acf2-107">DESCRIPTION</span></span>
<span data-ttu-id="2acf2-108">A **New-AzApplicationGatewayPathRuleConfig** parancsmag létrehoz egy alkalmazás-átjáró elérési útját szabályt.</span><span class="sxs-lookup"><span data-stu-id="2acf2-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="2acf2-109">A parancsmag által létrehozott szabályok hozzáadhatóak az URL-útvonal-leképezés konfigurációs beállításainak gyűjteményéhez, majd hozzárendelhető egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="2acf2-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="2acf2-110">Az útvonal-leképezés konfigurációs beállításait az alkalmazás átjáró terheléselosztási beállításai használják.</span><span class="sxs-lookup"><span data-stu-id="2acf2-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="2acf2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2acf2-111">EXAMPLES</span></span>

### <span data-ttu-id="2acf2-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2acf2-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="2acf2-113">Ezek a parancsok új alkalmazás-átjáró elérésiút-szabályt hoznak létre, majd az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmaggal hozzárendelik a szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="2acf2-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="2acf2-114">Ehhez az első parancs létrehoz egy objektumhivatkozást a ContosoApplicationGateway átjáróra.</span><span class="sxs-lookup"><span data-stu-id="2acf2-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="2acf2-115">Ezt az objektumhivatkozást egy $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2acf2-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="2acf2-116">A következő két parancs létrehoz egy háttércímkészletet és egy háttér-HTTP-beállításobjektumot; Ezek az objektumok (amelyek a változókban $AddressPool és $HttpSettings) szükségesek az elérésiút-szabály objektumának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="2acf2-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="2acf2-117">A negyedik parancs létrehozza az elérésiút-szabályobjektumot, és egy másik, "$PathRuleConfig" nevű változóban $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2acf2-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="2acf2-118">Az ötödik parancs **az Add-AzApplicationGatewayUrlPathMapConfig** paranccsal adja hozzá a beállításokban szereplő konfigurációs beállításokat és az új elérésiút-szabályt a ContosoApplicationGatewayhez.</span><span class="sxs-lookup"><span data-stu-id="2acf2-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="2acf2-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="2acf2-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="2acf2-120">Ezek a parancsok olyan elérési utat hoznak létre, amelynél a Név mint "alap", "/base" elérési utak, a BackendAddressPool mint $AddressPool, a BackendHttpSettings mint $HttpSettings és a FirewallPolicy mint $firewallPolicy.ngs, valamint a ContosoApplicationGateway beállításaiban található új elérésiút-szabály szerepel.</span><span class="sxs-lookup"><span data-stu-id="2acf2-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="2acf2-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2acf2-121">PARAMETERS</span></span>

### <span data-ttu-id="2acf2-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2acf2-122">-BackendAddressPool</span></span>
<span data-ttu-id="2acf2-123">Egy objektumhivatkozást ad meg a háttércímkészlet azon beállításainak gyűjteményére, amelyek hozzáadva lesznek az átjáró elérési útvonalának beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="2acf2-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="2acf2-124">Ezt az objektumhivatkozást a következő New-AzApplicationGatewayBackendAddressPool szintaxissal hozhatja létre: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="2acf2-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="2acf2-125">Az előző parancs két IP-címet (192.16.1.1 és 192.168.1.2) ad a címkészlethez.</span><span class="sxs-lookup"><span data-stu-id="2acf2-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="2acf2-126">Ne feledje, hogy az IP-cím idézőjelek közé van zárva, és vesszővel vannak elválasztva egymástól.</span><span class="sxs-lookup"><span data-stu-id="2acf2-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="2acf2-127">Az eredményül kapott $AddressPool a *DefaultBackendAddressPool* paraméter paraméterértékeként.</span><span class="sxs-lookup"><span data-stu-id="2acf2-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="2acf2-128">A háttérkiszolgálói címkészlet a háttérkiszolgálók IP-címeit képviseli.</span><span class="sxs-lookup"><span data-stu-id="2acf2-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="2acf2-129">Ezeknek az IP-címeknek vagy a virtuális hálózat alhálózatához kell tartozni, vagy nyilvános IP-címeknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2acf2-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="2acf2-130">Ha ezt a paramétert használja, nem használhatja ugyanabban a parancsban a *DefaultBackendAddressPoolId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2acf2-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="2acf2-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2acf2-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="2acf2-132">Megadja egy meglévő háttércímkészlet azonosítóját, amely hozzáadható az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="2acf2-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2acf2-133">A címkészlet-címek az Get-AzApplicationGatewayBackendAddressPool parancsmag használatával térnek vissza.</span><span class="sxs-lookup"><span data-stu-id="2acf2-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="2acf2-134">Az azonosító megadása után használhatja a *DefaultBackendAddressPoolId* paramétert a *DefaultBackendAddressPool paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="2acf2-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="2acf2-135">Például: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" A háttérkiszolgálói címkészlet a háttérkiszolgálók IP-címét képviseli.</span><span class="sxs-lookup"><span data-stu-id="2acf2-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="2acf2-136">Ezeknek az IP-címeknek vagy a virtuális hálózat alhálózatához kell tartozni, vagy nyilvános IP-címeknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2acf2-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="2acf2-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2acf2-137">-BackendHttpSettings</span></span>
<span data-ttu-id="2acf2-138">Objektumhivatkozást ad meg az átjáró elérésiút-szabály konfigurációs beállításaihoz hozzáadható háttérhálózati HTTP-beállítások gyűjteményére.</span><span class="sxs-lookup"><span data-stu-id="2acf2-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2acf2-139">Ezt az objektumhivatkozást a következőhöz hasonló New-AzApplicationGatewayBackendHttpSettings parancsmaggal és szintaxissal hozhatja létre: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Az eredményül kapott változó, $HttpSettings a *DefaultBackendAddressPool* paraméter paraméterértékeként használhatók: -DefaultBackendHttpSettings $HttpSettings A háttéralapú HTTP-beállítások konfigurálják a tulajdonságokat, például a portot, a protokollt és a cookie-alapú affinitást a háttérkészlethez.</span><span class="sxs-lookup"><span data-stu-id="2acf2-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="2acf2-140">Ha ezt a paramétert használja, nem használhatja ugyanabban a parancsban a *DefaultBackendHttpSettingsId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2acf2-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="2acf2-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2acf2-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2acf2-142">Egy meglévő háttérhálózati HTTP-beállításcsoport azonosítóját adja meg, amely hozzáadható az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="2acf2-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2acf2-143">A HTTP-beállítási címek visszaadhatóak a Get-AzApplicationGatewayBackendHttpSettings parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="2acf2-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="2acf2-144">Az azonosító megadása után a *DefaultBackendHttpSettingsId* paramétert használhatja a *DefaultBackendHttpSettings paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="2acf2-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="2acf2-145">Például: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" A háttérbeli HTTP-beállítások olyan tulajdonságokat konfigurálnak, mint a port, a protokoll, és cookie-alapú affinitás egy háttérkészlethez.</span><span class="sxs-lookup"><span data-stu-id="2acf2-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="2acf2-146">Ha ezt a paramétert használja, nem használhatja ugyanabban a parancsban a *DefaultBackendHttpSettings* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2acf2-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="2acf2-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2acf2-147">-FirewallPolicy</span></span>
<span data-ttu-id="2acf2-148">Egy legfelső szintű tűzfal-házirend objektumhivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2acf2-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="2acf2-149">Az objektumhivatkozást egy parancsmag használatával New-AzApplicationGatewayWebApplicationFirewallPolicy létrehozni.</span><span class="sxs-lookup"><span data-stu-id="2acf2-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="2acf2-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A fenti parancsmag használatával létrehozott tűzfalházi házirendre elérésiút-szabályszinten hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="2acf2-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="2acf2-151">he above command would create a default policy settings and managed rules.</span><span class="sxs-lookup"><span data-stu-id="2acf2-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="2acf2-152">Az alapértelmezett értékek helyett a felhasználók megadhatják a PolicySettings és a ManagedRules beállítást a New-AzApplicationGatewayFirewallPolicySettings és New-AzApplicationGatewayFirewallPolicyManagedRules meg.</span><span class="sxs-lookup"><span data-stu-id="2acf2-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf2-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="2acf2-153">-FirewallPolicyId</span></span>
<span data-ttu-id="2acf2-154">Egy meglévő legfelső szintű webalkalmazás tűzfalerőforrásának azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2acf2-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="2acf2-155">A tűzfalháziaktár-okat a parancsmag Get-AzApplicationGatewayWebApplicationFirewallPolicy vissza.</span><span class="sxs-lookup"><span data-stu-id="2acf2-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="2acf2-156">Az azonosító megadása után a *FirewallPolicyId* paramétert használhatja a *FirewallPolicy paraméter helyett.*</span><span class="sxs-lookup"><span data-stu-id="2acf2-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="2acf2-157">Például: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="2acf2-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2acf2-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acf2-158">-DefaultProfile</span></span>
<span data-ttu-id="2acf2-159">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2acf2-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2acf2-160">-Name</span><span class="sxs-lookup"><span data-stu-id="2acf2-160">-Name</span></span>
<span data-ttu-id="2acf2-161">A parancsmag által létrehozott útvonalszabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2acf2-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2acf2-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="2acf2-162">-Paths</span></span>
<span data-ttu-id="2acf2-163">Egy vagy több alkalmazás-átjáró elérési útvonalának szabályait adja meg.</span><span class="sxs-lookup"><span data-stu-id="2acf2-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="2acf2-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2acf2-164">-RedirectConfiguration</span></span>
<span data-ttu-id="2acf2-165">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2acf2-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2acf2-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2acf2-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="2acf2-167">A RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="2acf2-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2acf2-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2acf2-168">-RewriteRuleSet</span></span>
<span data-ttu-id="2acf2-169">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2acf2-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2acf2-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2acf2-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="2acf2-171">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="2acf2-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2acf2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acf2-172">CommonParameters</span></span>
<span data-ttu-id="2acf2-173">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acf2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acf2-174">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2acf2-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acf2-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2acf2-175">INPUTS</span></span>

### <span data-ttu-id="2acf2-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="2acf2-176">None</span></span>

## <span data-ttu-id="2acf2-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2acf2-177">OUTPUTS</span></span>

### <span data-ttu-id="2acf2-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="2acf2-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="2acf2-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2acf2-179">NOTES</span></span>

## <span data-ttu-id="2acf2-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2acf2-180">RELATED LINKS</span></span>

[<span data-ttu-id="2acf2-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2acf2-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2acf2-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2acf2-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2acf2-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2acf2-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2acf2-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2acf2-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2acf2-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2acf2-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2acf2-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2acf2-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="2acf2-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2acf2-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2acf2-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2acf2-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2acf2-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2acf2-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


