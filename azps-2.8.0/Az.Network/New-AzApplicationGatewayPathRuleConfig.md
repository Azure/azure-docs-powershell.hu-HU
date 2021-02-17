---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 6592f79291c069ade40b30277461f5e0e218b937
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407046"
---
# <span data-ttu-id="475eb-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="475eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475eb-102">SYNOPSIS</span></span>
<span data-ttu-id="475eb-103">Létrehoz egy alkalmazás-átjáró elérési útját szabályt.</span><span class="sxs-lookup"><span data-stu-id="475eb-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="475eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="475eb-104">SYNTAX</span></span>

### <span data-ttu-id="475eb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="475eb-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="475eb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="475eb-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="475eb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="475eb-107">DESCRIPTION</span></span>
<span data-ttu-id="475eb-108">A **New-AzApplicationGatewayPathRuleConfig** parancsmag létrehoz egy alkalmazás-átjáró elérési útját szabályt.</span><span class="sxs-lookup"><span data-stu-id="475eb-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="475eb-109">A parancsmag által létrehozott szabályok hozzáadhatóak az URL-útvonal-leképezés konfigurációs beállításainak gyűjteményéhez, majd hozzárendelhető egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="475eb-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="475eb-110">Az útvonal-leképezés konfigurációs beállításait az alkalmazás átjáró terheléselosztási beállításai használják.</span><span class="sxs-lookup"><span data-stu-id="475eb-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="475eb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="475eb-111">EXAMPLES</span></span>

### <span data-ttu-id="475eb-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="475eb-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="475eb-113">Ezek a parancsok új alkalmazás-átjáró elérésiút-szabályt hoznak létre, majd az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmaggal hozzárendelik a szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="475eb-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="475eb-114">Ehhez az első parancs létrehoz egy objektumhivatkozást a ContosoApplicationGateway átjáróra.</span><span class="sxs-lookup"><span data-stu-id="475eb-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="475eb-115">Ezt az objektumhivatkozást egy $Gateway.</span><span class="sxs-lookup"><span data-stu-id="475eb-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="475eb-116">A következő két parancs létrehoz egy háttércímkészletet és egy háttér-HTTP-beállításobjektumot; Ezek az objektumok (amelyek a változókban $AddressPool és $HttpSettings) szükségesek az elérésiút-szabály objektumának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="475eb-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="475eb-117">A negyedik parancs létrehozza az elérésiút-szabályobjektumot, és egy másik, "$PathRuleConfig" nevű változóban $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="475eb-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="475eb-118">Az ötödik parancs **az Add-AzApplicationGatewayUrlPathMapConfig** paranccsal adja hozzá a beállításokban szereplő konfigurációs beállításokat és az új elérésiút-szabályt a ContosoApplicationGatewayhez.</span><span class="sxs-lookup"><span data-stu-id="475eb-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="475eb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="475eb-119">PARAMETERS</span></span>

### <span data-ttu-id="475eb-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="475eb-120">-BackendAddressPool</span></span>
<span data-ttu-id="475eb-121">Egy objektumhivatkozást ad meg a háttércímkészlet azon beállításainak gyűjteményére, amelyek hozzáadva lesznek az átjáró elérési útvonalának beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="475eb-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="475eb-122">Ezt az objektumhivatkozást a következő New-AzApplicationGatewayBackendAddressPool szintaxissal hozhatja létre: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="475eb-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="475eb-123">Az előző parancs két IP-címet (192.16.1.1 és 192.168.1.2) ad a címkészlethez.</span><span class="sxs-lookup"><span data-stu-id="475eb-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="475eb-124">Ne feledje, hogy az IP-cím idézőjelek közé van zárva, és vesszővel vannak elválasztva egymástól.</span><span class="sxs-lookup"><span data-stu-id="475eb-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="475eb-125">Az eredményül kapott $AddressPool a *DefaultBackendAddressPool* paraméter paraméterértékeként.</span><span class="sxs-lookup"><span data-stu-id="475eb-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="475eb-126">A háttérkiszolgálói címkészlet a háttérkiszolgálók IP-címét képviseli.</span><span class="sxs-lookup"><span data-stu-id="475eb-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="475eb-127">Ezeknek az IP-címeknek vagy a virtuális hálózat alhálózatához kell tartozni, vagy nyilvános IP-címeknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="475eb-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="475eb-128">Ha ezt a paramétert használja, nem használhatja ugyanabban a parancsban a *DefaultBackendAddressPoolId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="475eb-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="475eb-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="475eb-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="475eb-130">Egy meglévő háttércímkészlet azonosítója, amely hozzáadható az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="475eb-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="475eb-131">A címkészlet-címek az Get-AzApplicationGatewayBackendAddressPool parancsmag használatával térnek vissza.</span><span class="sxs-lookup"><span data-stu-id="475eb-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="475eb-132">Az azonosító megadása után használhatja a *DefaultBackendAddressPoolId* paramétert a *DefaultBackendAddressPool paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="475eb-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="475eb-133">Például: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" A háttérkiszolgálói címkészlet a háttérkiszolgálók IP-címét képviseli.</span><span class="sxs-lookup"><span data-stu-id="475eb-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="475eb-134">Ezeknek az IP-címeknek vagy a virtuális hálózat alhálózatához kell tartozni, vagy nyilvános IP-címeknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="475eb-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="475eb-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="475eb-135">-BackendHttpSettings</span></span>
<span data-ttu-id="475eb-136">Objektumhivatkozást ad meg az átjáró elérésiút-szabály konfigurációs beállításaihoz hozzáadható háttérhálózati HTTP-beállítások gyűjteményére.</span><span class="sxs-lookup"><span data-stu-id="475eb-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="475eb-137">Ezt az objektumhivatkozást a következőhöz hasonló New-AzApplicationGatewayBackendHttpSettings parancsmaggal és szintaxissal hozhatja létre: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Az eredményül kapott változó, $HttpSettings a *DefaultBackendAddressPool* paraméter paraméterértékeként használható: -DefaultBackendHttpSettings $HttpSettings A háttéren alapuló HTTP-beállítások konfigurálják a tulajdonságokat, például a portot, a protokollt és a cookie-alapú affinitást a háttérkészlethez.</span><span class="sxs-lookup"><span data-stu-id="475eb-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="475eb-138">Ha ezt a paramétert használja, nem használhatja ugyanabban a parancsban a *DefaultBackendHttpSettingsId* paramétert.</span><span class="sxs-lookup"><span data-stu-id="475eb-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="475eb-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="475eb-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="475eb-140">Egy meglévő háttérhálózati HTTP-beállításcsoport azonosítóját adja meg, amely hozzáadható az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="475eb-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="475eb-141">A HTTP-beállításokat a parancsmag használatával Get-AzApplicationGatewayBackendHttpSettings vissza.</span><span class="sxs-lookup"><span data-stu-id="475eb-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="475eb-142">Az azonosító megadása után a *DefaultBackendHttpSettingsId* paramétert használhatja a *DefaultBackendHttpSettings paraméter* helyett.</span><span class="sxs-lookup"><span data-stu-id="475eb-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="475eb-143">Például: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" A háttérbeli HTTP-beállítások olyan tulajdonságokat konfigurálnak, mint a port, a protokoll, és cookie-alapú affinitás egy háttérkészlethez.</span><span class="sxs-lookup"><span data-stu-id="475eb-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="475eb-144">Ha ezt a paramétert használja, nem használhatja ugyanabban a parancsban a *DefaultBackendHttpSettings* paramétert.</span><span class="sxs-lookup"><span data-stu-id="475eb-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="475eb-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475eb-145">-DefaultProfile</span></span>
<span data-ttu-id="475eb-146">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="475eb-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475eb-147">-Name</span><span class="sxs-lookup"><span data-stu-id="475eb-147">-Name</span></span>
<span data-ttu-id="475eb-148">A parancsmag által létrehozott útvonalszabály-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="475eb-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="475eb-149">-Paths</span><span class="sxs-lookup"><span data-stu-id="475eb-149">-Paths</span></span>
<span data-ttu-id="475eb-150">Egy vagy több alkalmazás-átjáró elérési útvonalának szabályait adja meg.</span><span class="sxs-lookup"><span data-stu-id="475eb-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="475eb-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="475eb-151">-RedirectConfiguration</span></span>
<span data-ttu-id="475eb-152">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="475eb-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="475eb-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="475eb-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="475eb-154">A RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="475eb-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="475eb-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="475eb-155">-RewriteRuleSet</span></span>
<span data-ttu-id="475eb-156">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="475eb-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="475eb-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="475eb-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="475eb-158">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="475eb-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="475eb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475eb-159">CommonParameters</span></span>
<span data-ttu-id="475eb-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475eb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475eb-161">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475eb-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475eb-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="475eb-162">INPUTS</span></span>

### <span data-ttu-id="475eb-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="475eb-163">None</span></span>

## <span data-ttu-id="475eb-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="475eb-164">OUTPUTS</span></span>

### <span data-ttu-id="475eb-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="475eb-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="475eb-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="475eb-166">NOTES</span></span>

## <span data-ttu-id="475eb-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="475eb-167">RELATED LINKS</span></span>

[<span data-ttu-id="475eb-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="475eb-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="475eb-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="475eb-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="475eb-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="475eb-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="475eb-172">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-172">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="475eb-173">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-173">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="475eb-174">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-174">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="475eb-175">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-175">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


