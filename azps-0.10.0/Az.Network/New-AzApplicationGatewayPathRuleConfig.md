---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841409"
---
# <span data-ttu-id="61a43-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61a43-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="61a43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61a43-102">SYNOPSIS</span></span>
<span data-ttu-id="61a43-103">Az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="61a43-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="61a43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61a43-104">SYNTAX</span></span>

### <span data-ttu-id="61a43-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="61a43-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61a43-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="61a43-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61a43-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="61a43-107">DESCRIPTION</span></span>
<span data-ttu-id="61a43-108">A **New-AzApplicationGatewayPathRuleConfig** parancsmag az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="61a43-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="61a43-109">Az e parancsmaggal létrehozott szabályok hozzáadhatók az URL-elérésiút-Térkép konfigurációs beállításainak gyűjteményéhez, majd a hozzájuk rendelt átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="61a43-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="61a43-110">Az elérésiút-Térkép konfigurációs beállításait az Application Gateway terheléselosztási funkciói használja.</span><span class="sxs-lookup"><span data-stu-id="61a43-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="61a43-111">Példák</span><span class="sxs-lookup"><span data-stu-id="61a43-111">EXAMPLES</span></span>

### <span data-ttu-id="61a43-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="61a43-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="61a43-113">Ezekkel a parancsokkal új alkalmazás-átjáró elérésiút-szabályt hozhat létre, majd az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmaggal társíthatja ezt a szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="61a43-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="61a43-114">Ehhez az első parancs objektumra mutató hivatkozást hoz létre az átjáró ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="61a43-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="61a43-115">Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="61a43-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="61a43-116">A következő két parancs a backend-címkészletet és a backend-alapú HTTP-beállítások objektumot hozza létre; Ezek az objektumok (a változók $AddressPool és a $HttpSettings) szükségesek az elérésiút-szabály objektum létrehozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="61a43-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="61a43-117">A negyedik parancs a Path Rule objektumot hozza létre, és a $PathRuleConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="61a43-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="61a43-118">Az ötödik parancs az **Add-AzApplicationGatewayUrlPathMapConfig** használatával hozzáadja a konfigurációs beállításokat és az új elérésiút-szabályt a beállítások között a ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="61a43-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="61a43-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61a43-119">PARAMETERS</span></span>

### <span data-ttu-id="61a43-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61a43-120">-BackendAddressPool</span></span>
<span data-ttu-id="61a43-121">Itt adhatja meg a backend-címkészlet beállításai között az objektum hivatkozását, amelyet az átjáró elérési útjának konfigurációs beállításaihoz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="61a43-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="61a43-122">Az objektum hivatkozását az New-AzApplicationGatewayBackendAddressPool parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="61a43-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="61a43-123">Az előző parancs két IP-címet (192.16.1.1 és 192.168.1.2) ad hozzá a címkészlet számára.</span><span class="sxs-lookup"><span data-stu-id="61a43-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="61a43-124">Ügyeljen arra, hogy az IP-cím idézőjelek közé van írva, és vesszőkkel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="61a43-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="61a43-125">Az eredményül kapott változó ($AddressPool) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="61a43-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="61a43-126">A backend Address Pool a backend-kiszolgálók IP-címét jelöli.</span><span class="sxs-lookup"><span data-stu-id="61a43-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="61a43-127">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="61a43-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="61a43-128">Ha ezt a paramétert használja, a *DefaultBackendAddressPoolId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="61a43-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="61a43-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="61a43-130">Annak a meglévő backend-címkészlet az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="61a43-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="61a43-131">A címkészlet-azonosítók az Get-AzApplicationGatewayBackendAddressPool parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="61a43-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="61a43-132">Miután megtörtént az azonosító, a *DefaultBackendAddressPoolId* paramétert használhatja a *DefaultBackendAddressPool* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="61a43-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="61a43-133">Például:</span><span class="sxs-lookup"><span data-stu-id="61a43-133">For instance:</span></span>

<span data-ttu-id="61a43-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="61a43-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="61a43-135">A backend Address Pool a backend-kiszolgálók IP-címét jelöli.</span><span class="sxs-lookup"><span data-stu-id="61a43-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="61a43-136">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="61a43-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="61a43-137">-BackendHttpSettings</span></span>
<span data-ttu-id="61a43-138">Az átjáró elérési útjának konfigurációs beállításaihoz hozzáadott backend-HTTP-beállításokra mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="61a43-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="61a43-139">Az objektum hivatkozását az New-AzApplicationGatewayBackendHttpSetting parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="61a43-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="61a43-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting név "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "disabled"</span><span class="sxs-lookup"><span data-stu-id="61a43-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="61a43-141">Az eredményül kapott változó ($HttpSettings) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet:</span><span class="sxs-lookup"><span data-stu-id="61a43-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="61a43-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="61a43-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="61a43-143">A backend HTTP-beállításai olyan tulajdonságokat (például portot, protokollt és cookie-alapú affinitást) konfigurálnak, amelyek a backend-készletekhez használhatók.</span><span class="sxs-lookup"><span data-stu-id="61a43-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="61a43-144">Ha ezt a paramétert használja, a *DefaultBackendHttpSettingsId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="61a43-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="61a43-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="61a43-146">Annak a meglévő backend-adatgyűjteménynek az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="61a43-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="61a43-147">A HTTP-beállítás azonosítói az Get-AzApplicationGatewayBackendHttpSetting parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="61a43-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="61a43-148">Miután megtörtént az azonosító, a *DefaultBackendHttpSettingsId* paramétert használhatja a *DefaultBackendHttpSettings* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="61a43-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="61a43-149">Például:</span><span class="sxs-lookup"><span data-stu-id="61a43-149">For instance:</span></span>

<span data-ttu-id="61a43-150">-DefaultBackendSettings-azonosító "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="61a43-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="61a43-151">A backend HTTP-beállításai olyan tulajdonságokat (például portot, protokollt és cookie-alapú affinitást) konfigurálnak, amelyek a backend-készletekhez használhatók.</span><span class="sxs-lookup"><span data-stu-id="61a43-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="61a43-152">Ha ezt a paramétert használja, a *DefaultBackendHttpSettings* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="61a43-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a43-153">-DefaultProfile</span></span>
<span data-ttu-id="61a43-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61a43-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-155">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61a43-155">-Name</span></span>
<span data-ttu-id="61a43-156">A parancsmag által létrehozott elérésiút-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61a43-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-157">-Paths</span><span class="sxs-lookup"><span data-stu-id="61a43-157">-Paths</span></span>
<span data-ttu-id="61a43-158">Egy vagy több alkalmazásobjektum-elérésiút-szabályt ad meg.</span><span class="sxs-lookup"><span data-stu-id="61a43-158">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="61a43-159">-RedirectConfiguration</span></span>
<span data-ttu-id="61a43-160">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="61a43-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="61a43-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="61a43-162">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="61a43-162">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a43-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a43-163">CommonParameters</span></span>
<span data-ttu-id="61a43-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61a43-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a43-165">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a43-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a43-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61a43-166">INPUTS</span></span>

###  
<span data-ttu-id="61a43-167">A **New-AzApplicationGatewayPathRuleConfig** nem fogadja el a csővezetékes bevitelt.</span><span class="sxs-lookup"><span data-stu-id="61a43-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="61a43-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61a43-168">OUTPUTS</span></span>

###  
<span data-ttu-id="61a43-169">A **New-AzApplicationGatewayPathRuleConfig** a **Microsoft. Azure. commands. Network. models. PSApplicationGatewayPathRule** objektum új példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="61a43-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="61a43-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61a43-170">NOTES</span></span>

## <span data-ttu-id="61a43-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61a43-171">RELATED LINKS</span></span>

[<span data-ttu-id="61a43-172">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="61a43-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="61a43-173">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61a43-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="61a43-174">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="61a43-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="61a43-175">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61a43-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="61a43-176">Új – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="61a43-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="61a43-177">Új – AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61a43-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="61a43-178">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="61a43-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="61a43-179">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="61a43-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="61a43-180">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="61a43-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


