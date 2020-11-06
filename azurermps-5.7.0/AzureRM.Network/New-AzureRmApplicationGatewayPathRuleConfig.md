---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 209986a25882415a68df86611d10559612a8ec04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500507"
---
# <span data-ttu-id="7c75a-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c75a-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="7c75a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c75a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c75a-103">Az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7c75a-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c75a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c75a-104">SYNTAX</span></span>

### <span data-ttu-id="7c75a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c75a-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c75a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7c75a-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c75a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c75a-107">DESCRIPTION</span></span>
<span data-ttu-id="7c75a-108">A **New-AzureRmApplicationGatewayPathRuleConfig** parancsmag az alkalmazás-átjáró elérési útjának szabályát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7c75a-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="7c75a-109">Az e parancsmaggal létrehozott szabályok hozzáadhatók az URL-elérésiút-Térkép konfigurációs beállításainak gyűjteményéhez, majd a hozzájuk rendelt átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7c75a-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="7c75a-110">Az elérésiút-Térkép konfigurációs beállításait az Application Gateway terheléselosztási funkciói használja.</span><span class="sxs-lookup"><span data-stu-id="7c75a-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="7c75a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7c75a-111">EXAMPLES</span></span>

### <span data-ttu-id="7c75a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c75a-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="7c75a-113">Ezekkel a parancsokkal új alkalmazás-átjáró elérésiút-szabályt hozhat létre, majd az **Add-AzureRmApplicationGatewayUrlPathMapConfig** parancsmaggal társíthatja ezt a szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7c75a-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="7c75a-114">Ehhez az első parancs objektumra mutató hivatkozást hoz létre az átjáró ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="7c75a-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="7c75a-115">Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="7c75a-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="7c75a-116">A következő két parancs a backend-címkészletet és a backend-alapú HTTP-beállítások objektumot hozza létre; Ezek az objektumok (a változók $AddressPool és a $HttpSettings) szükségesek az elérésiút-szabály objektum létrehozása érdekében.</span><span class="sxs-lookup"><span data-stu-id="7c75a-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="7c75a-117">A negyedik parancs a Path Rule objektumot hozza létre, és a $PathRuleConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7c75a-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="7c75a-118">Az ötödik parancs az **Add-AzureRmApplicationGatewayUrlPathMapConfig** használatával hozzáadja a konfigurációs beállításokat és az új elérésiút-szabályt a beállítások között a ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="7c75a-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="7c75a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c75a-119">PARAMETERS</span></span>

### <span data-ttu-id="7c75a-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c75a-120">-BackendAddressPool</span></span>
<span data-ttu-id="7c75a-121">Itt adhatja meg a backend-címkészlet beállításai között az objektum hivatkozását, amelyet az átjáró elérési útjának konfigurációs beállításaihoz kell hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="7c75a-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="7c75a-122">Az objektum hivatkozását az New-AzureRmApplicationGatewayBackendAddressPool parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="7c75a-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="7c75a-123">Az előző parancs két IP-címet (192.16.1.1 és 192.168.1.2) ad hozzá a címkészlet számára.</span><span class="sxs-lookup"><span data-stu-id="7c75a-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="7c75a-124">Ügyeljen arra, hogy az IP-cím idézőjelek közé van írva, és vesszőkkel elválasztva.</span><span class="sxs-lookup"><span data-stu-id="7c75a-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="7c75a-125">Az eredményül kapott változó ($AddressPool) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="7c75a-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="7c75a-126">A backend Address Pool a backend-kiszolgálók IP-címét jelöli.</span><span class="sxs-lookup"><span data-stu-id="7c75a-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="7c75a-127">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="7c75a-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="7c75a-128">Ha ezt a paramétert használja, a *DefaultBackendAddressPoolId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="7c75a-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="7c75a-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7c75a-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="7c75a-130">Annak a meglévő backend-címkészlet az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="7c75a-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="7c75a-131">A címkészlet-azonosítók az Get-AzureRmApplicationGatewayBackendAddressPool parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="7c75a-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="7c75a-132">Miután megtörtént az azonosító, a *DefaultBackendAddressPoolId* paramétert használhatja a *DefaultBackendAddressPool* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="7c75a-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="7c75a-133">Például:</span><span class="sxs-lookup"><span data-stu-id="7c75a-133">For instance:</span></span>

<span data-ttu-id="7c75a-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="7c75a-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="7c75a-135">A backend Address Pool a backend-kiszolgálók IP-címét jelöli.</span><span class="sxs-lookup"><span data-stu-id="7c75a-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="7c75a-136">Ezek az IP-címek vagy a virtuális hálózat alhálózatához tartoznak, vagy nyilvános IP-címnek kell lenniük.</span><span class="sxs-lookup"><span data-stu-id="7c75a-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="7c75a-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7c75a-137">-BackendHttpSettings</span></span>
<span data-ttu-id="7c75a-138">Az átjáró elérési útjának konfigurációs beállításaihoz hozzáadott backend-HTTP-beállításokra mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c75a-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="7c75a-139">Az objektum hivatkozását az New-AzureRmApplicationGatewayBackendHttpSettings parancsmag és az ehhez hasonló szintaxis használatával hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="7c75a-139">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="7c75a-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings név "ContosoHttpSetings"-port 80-Protocol "http"-CookieBasedAffinity "disabled"</span><span class="sxs-lookup"><span data-stu-id="7c75a-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="7c75a-141">Az eredményül kapott változó ($HttpSettings) a *DefaultBackendAddressPool* paraméter paraméterének értéke lehet:</span><span class="sxs-lookup"><span data-stu-id="7c75a-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="7c75a-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="7c75a-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="7c75a-143">A backend HTTP-beállításai olyan tulajdonságokat (például portot, protokollt és cookie-alapú affinitást) konfigurálnak, amelyek a backend-készletekhez használhatók.</span><span class="sxs-lookup"><span data-stu-id="7c75a-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="7c75a-144">Ha ezt a paramétert használja, a *DefaultBackendHttpSettingsId* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="7c75a-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="7c75a-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7c75a-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="7c75a-146">Annak a meglévő backend-adatgyűjteménynek az AZONOSÍTÓját adja meg, amely hozzáadódik az átjáró elérésiút-szabály konfigurációs beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="7c75a-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="7c75a-147">A HTTP-beállítás azonosítói az Get-AzureRmApplicationGatewayBackendHttpSettings parancsmag használatával adhatók vissza.</span><span class="sxs-lookup"><span data-stu-id="7c75a-147">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="7c75a-148">Miután megtörtént az azonosító, a *DefaultBackendHttpSettingsId* paramétert használhatja a *DefaultBackendHttpSettings* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="7c75a-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="7c75a-149">Például:</span><span class="sxs-lookup"><span data-stu-id="7c75a-149">For instance:</span></span>

<span data-ttu-id="7c75a-150">-DefaultBackendSettings-azonosító "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="7c75a-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="7c75a-151">A backend HTTP-beállításai olyan tulajdonságokat (például portot, protokollt és cookie-alapú affinitást) konfigurálnak, amelyek a backend-készletekhez használhatók.</span><span class="sxs-lookup"><span data-stu-id="7c75a-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="7c75a-152">Ha ezt a paramétert használja, a *DefaultBackendHttpSettings* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="7c75a-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="7c75a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c75a-153">-DefaultProfile</span></span>
<span data-ttu-id="7c75a-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c75a-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c75a-155">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c75a-155">-Name</span></span>
<span data-ttu-id="7c75a-156">A parancsmag által létrehozott elérésiút-szabály konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c75a-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7c75a-157">-Paths</span><span class="sxs-lookup"><span data-stu-id="7c75a-157">-Paths</span></span>
<span data-ttu-id="7c75a-158">Egy vagy több alkalmazásobjektum-elérésiút-szabályt ad meg.</span><span class="sxs-lookup"><span data-stu-id="7c75a-158">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="7c75a-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c75a-159">-RedirectConfiguration</span></span>
<span data-ttu-id="7c75a-160">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c75a-160">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="7c75a-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7c75a-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="7c75a-162">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="7c75a-162">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="7c75a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c75a-163">CommonParameters</span></span>
<span data-ttu-id="7c75a-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c75a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c75a-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c75a-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c75a-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c75a-166">INPUTS</span></span>

###  
<span data-ttu-id="7c75a-167">A **New-AzureRmApplicationGatewayPathRuleConfig** nem fogadja el a csővezetékes bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7c75a-167">**New-AzureRmApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="7c75a-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c75a-168">OUTPUTS</span></span>

###  
<span data-ttu-id="7c75a-169">A **New-AzureRmApplicationGatewayPathRuleConfig** a **Microsoft. Azure. commands. Network. models. PSApplicationGatewayPathRule** objektum új példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7c75a-169">**New-AzureRmApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="7c75a-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c75a-170">NOTES</span></span>

## <span data-ttu-id="7c75a-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c75a-171">RELATED LINKS</span></span>

[<span data-ttu-id="7c75a-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7c75a-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7c75a-173">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c75a-173">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="7c75a-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7c75a-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7c75a-175">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c75a-175">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7c75a-176">Új – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7c75a-176">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="7c75a-177">Új – AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c75a-177">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="7c75a-178">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7c75a-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7c75a-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7c75a-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7c75a-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7c75a-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


