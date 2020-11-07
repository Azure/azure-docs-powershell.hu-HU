---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: a73233908f37463c591aeb2e3d6b00eeb3c511ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670400"
---
# <span data-ttu-id="74f63-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74f63-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="74f63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74f63-102">SYNOPSIS</span></span>
<span data-ttu-id="74f63-103">Az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="74f63-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="74f63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74f63-104">SYNTAX</span></span>

### <span data-ttu-id="74f63-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74f63-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74f63-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="74f63-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f63-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="74f63-107">DESCRIPTION</span></span>
<span data-ttu-id="74f63-108">A **New-AzApplicationGatewayPathRuleConfig** parancsmag az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="74f63-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="74f63-109">Az e parancsmaggal létrehozott szabályok hozzáadhatók az URL-elérésiút-Térkép konfigurációs beállításainak gyűjteményéhez, majd a hozzájuk rendelt átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="74f63-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="74f63-110">Az elérésiút-Térkép konfigurációs beállításait az Application Gateway terheléselosztási funkciói használja.</span><span class="sxs-lookup"><span data-stu-id="74f63-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="74f63-111">Példák</span><span class="sxs-lookup"><span data-stu-id="74f63-111">EXAMPLES</span></span>

### <span data-ttu-id="74f63-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74f63-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="74f63-113">Ezekkel a parancsokkal új alkalmazás-átjáró elérésiút-szabályt hozhat létre, majd az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmaggal társíthatja ezt a szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="74f63-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="74f63-114">Ehhez az első parancs objektumra mutató hivatkozást hoz létre az átjáró ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="74f63-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="74f63-115">Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="74f63-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="74f63-116">A következő két parancs a backend-címkészletet és a backend-alapú HTTP-beállítások objektumot hozza létre; Ezek az objektumok (a változók $AddressPool és a $HttpSettings) szükségesek az elérésiút-szabály objektum létrehozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="74f63-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="74f63-117">A negyedik parancs a Path Rule objektumot hozza létre, és a $PathRuleConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="74f63-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="74f63-118">Az ötödik parancs az **Add-AzApplicationGatewayUrlPathMapConfig** használatával hozzáadja a konfigurációs beállításokat és az új elérésiút-szabályt a beállítások között a ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="74f63-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="74f63-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74f63-119">PARAMETERS</span></span>

### <span data-ttu-id="74f63-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="74f63-120">-BackendAddressPool</span></span>
<span data-ttu-id="74f63-121">Itt adhatja meg a backend-címkészlet beállításai között az objektum hivatkozását, amelyet az átjáró elérési útjának konfigurációs beállításaihoz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="74f63-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="74f63-122">Az objektum hivatkozását az New-AzApplicationGatewayBackendAddressPool parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="74f63-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="74f63-123">Az előző parancs két IP-címet (192.16.1.1 és 192.168.1.2) ad hozzá a címkészlet számára.</span><span class="sxs-lookup"><span data-stu-id="74f63-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="74f63-124">Ügyeljen arra, hogy az IP-cím idézőjelek közé van írva, és vesszőkkel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="74f63-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="74f63-125">Az eredményül kapott változó ($AddressPool) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="74f63-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="74f63-126">A backend Address Pool a backend-kiszolgálók IP-címét jelöli.</span><span class="sxs-lookup"><span data-stu-id="74f63-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="74f63-127">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="74f63-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="74f63-128">Ha ezt a paramétert használja, a *DefaultBackendAddressPoolId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="74f63-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="74f63-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="74f63-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="74f63-130">Annak a meglévő backend-címkészlet az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="74f63-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="74f63-131">A címkészlet-azonosítók az Get-AzApplicationGatewayBackendAddressPool parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="74f63-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="74f63-132">Miután megtörtént az azonosító, a *DefaultBackendAddressPoolId* paramétert használhatja a *DefaultBackendAddressPool* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="74f63-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="74f63-133">Például:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool": a backend Address Pool a backend-kiszolgálók IP-címeinek felel meg.</span><span class="sxs-lookup"><span data-stu-id="74f63-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="74f63-134">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="74f63-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="74f63-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="74f63-135">-BackendHttpSettings</span></span>
<span data-ttu-id="74f63-136">Az átjáró elérési útjának konfigurációs beállításaihoz hozzáadott backend-HTTP-beállításokra mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="74f63-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="74f63-137">Az objektum hivatkozását az New-AzApplicationGatewayBackendHttpSettings parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "disabled": az eredményül kapott változó, $HttpSettings ezt követően a *DefaultBackendAddressPool* paraméter értéke lehet:-DefaultBackendHttpSettings $HttpSettings a backend http-beállításai (például a port, a Protocol és a cookie-alapú affinitás) a backend-készletekhez használhatók.</span><span class="sxs-lookup"><span data-stu-id="74f63-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="74f63-138">Ha ezt a paramétert használja, a *DefaultBackendHttpSettingsId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="74f63-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="74f63-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="74f63-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="74f63-140">Annak a meglévő backend-adatgyűjteménynek az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="74f63-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="74f63-141">A HTTP-beállítás azonosítói az Get-AzApplicationGatewayBackendHttpSettings parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="74f63-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="74f63-142">Miután megtörtént az azonosító, a *DefaultBackendHttpSettingsId* paramétert használhatja a *DefaultBackendHttpSettings* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="74f63-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="74f63-143">Például:-DefaultBackendSettings-azonosító "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings": a backend HTTP-beállításai, például a port, a Protocol és a cookie-alapú Affinitás beállítása a backend-készletben.</span><span class="sxs-lookup"><span data-stu-id="74f63-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="74f63-144">Ha ezt a paramétert használja, a *DefaultBackendHttpSettings* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="74f63-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="74f63-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f63-145">-DefaultProfile</span></span>
<span data-ttu-id="74f63-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74f63-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f63-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74f63-147">-Name</span></span>
<span data-ttu-id="74f63-148">A parancsmag által létrehozott elérésiút-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74f63-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="74f63-149">-Paths</span><span class="sxs-lookup"><span data-stu-id="74f63-149">-Paths</span></span>
<span data-ttu-id="74f63-150">Egy vagy több alkalmazásobjektum-elérésiút-szabályt ad meg.</span><span class="sxs-lookup"><span data-stu-id="74f63-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="74f63-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="74f63-151">-RedirectConfiguration</span></span>
<span data-ttu-id="74f63-152">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="74f63-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="74f63-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="74f63-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="74f63-154">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="74f63-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="74f63-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74f63-155">-RewriteRuleSet</span></span>
<span data-ttu-id="74f63-156">Az Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="74f63-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="74f63-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="74f63-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="74f63-158">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="74f63-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="74f63-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f63-159">CommonParameters</span></span>
<span data-ttu-id="74f63-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74f63-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f63-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f63-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f63-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74f63-162">INPUTS</span></span>

### <span data-ttu-id="74f63-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="74f63-163">None</span></span>

## <span data-ttu-id="74f63-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74f63-164">OUTPUTS</span></span>

### <span data-ttu-id="74f63-165">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="74f63-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="74f63-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74f63-166">NOTES</span></span>

## <span data-ttu-id="74f63-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74f63-167">RELATED LINKS</span></span>

[<span data-ttu-id="74f63-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="74f63-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="74f63-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74f63-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="74f63-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="74f63-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="74f63-171">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="74f63-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="74f63-172">Új – AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="74f63-172">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="74f63-173">Új – AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74f63-173">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="74f63-174">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="74f63-174">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="74f63-175">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="74f63-175">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="74f63-176">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="74f63-176">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


