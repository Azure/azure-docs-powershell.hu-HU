---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 5f91f333cf7983d50ba2984fcf01845a6c555e83
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184882"
---
# <span data-ttu-id="63a55-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63a55-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="63a55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63a55-102">SYNOPSIS</span></span>
<span data-ttu-id="63a55-103">Egy Application Gatewayt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a55-103">Creates an application gateway.</span></span>

## <span data-ttu-id="63a55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63a55-104">SYNTAX</span></span>

### <span data-ttu-id="63a55-105">IdentityByUserAssignedIdentityId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63a55-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a55-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63a55-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a55-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="63a55-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a55-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="63a55-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63a55-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="63a55-109">DESCRIPTION</span></span>
<span data-ttu-id="63a55-110">A **New-AzApplicationGateway** parancsmag egy Azure Application Gatewayt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a55-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="63a55-111">Az alkalmazás-átjáró a következőket igényli:</span><span class="sxs-lookup"><span data-stu-id="63a55-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="63a55-112">Egy erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="63a55-112">A resource group.</span></span>
- <span data-ttu-id="63a55-113">Virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="63a55-113">A virtual network.</span></span>
- <span data-ttu-id="63a55-114">A back-end Server Pool a back-end-kiszolgálók IP-címeivel.</span><span class="sxs-lookup"><span data-stu-id="63a55-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="63a55-115">A back-end Server-készlet beállításai.</span><span class="sxs-lookup"><span data-stu-id="63a55-115">Back-end server pool settings.</span></span> <span data-ttu-id="63a55-116">Mindegyik készlethez tartozik egy beállítás, például a port, a protokoll és a cookie-alapú affinitás, amelyek a készleten belül minden kiszolgálón érvényesek.</span><span class="sxs-lookup"><span data-stu-id="63a55-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="63a55-117">Az előtér IP-címei, amelyek az alkalmazás-átjárón megnyitott IP-címek.</span><span class="sxs-lookup"><span data-stu-id="63a55-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="63a55-118">Az előtér IP-címe lehet nyilvános IP-cím vagy belső IP-cím.</span><span class="sxs-lookup"><span data-stu-id="63a55-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="63a55-119">Előtér-portok, amelyek az alkalmazás-átjárón megnyitott nyilvános portok.</span><span class="sxs-lookup"><span data-stu-id="63a55-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="63a55-120">Az ilyen portokat tartalmazó forgalom átirányítása a back-end-kiszolgálókra</span><span class="sxs-lookup"><span data-stu-id="63a55-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="63a55-121">Egy olyan Request útválasztási szabály, amely köti a figyelőt és a back-end Server-készletet.</span><span class="sxs-lookup"><span data-stu-id="63a55-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="63a55-122">A szabály meghatározza, hogy melyik back-end Server-készlet a forgalomra irányuljon, amikor egy adott figyelőt üt.</span><span class="sxs-lookup"><span data-stu-id="63a55-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="63a55-123">A figyelőhöz tartozik egy előtér-végpont, egy előtér-IP-cím, egy protokoll (HTTP vagy HTTPS) és a Secure Sockets Layer (SSL) tanúsítvány neve (ha az SSL tehermentesítése beállítással).</span><span class="sxs-lookup"><span data-stu-id="63a55-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="63a55-124">Példák</span><span class="sxs-lookup"><span data-stu-id="63a55-124">EXAMPLES</span></span>

### <span data-ttu-id="63a55-125">1. példa: alkalmazás-átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="63a55-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="63a55-126">Az alábbi példa létrehoz egy Application Gatewayt, ha először létrehoz egy erőforráscsoportot és egy virtuális hálózatot, valamint az alábbiakat:</span><span class="sxs-lookup"><span data-stu-id="63a55-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="63a55-127">Egy back-end Server-készlet</span><span class="sxs-lookup"><span data-stu-id="63a55-127">A back-end server pool</span></span>
- <span data-ttu-id="63a55-128">A kiszolgálói készlet back-end beállításai</span><span class="sxs-lookup"><span data-stu-id="63a55-128">Back-end server pool settings</span></span>
- <span data-ttu-id="63a55-129">Előtér-portok</span><span class="sxs-lookup"><span data-stu-id="63a55-129">Front-end ports</span></span>
- <span data-ttu-id="63a55-130">Előtér IP-címei</span><span class="sxs-lookup"><span data-stu-id="63a55-130">Front-end IP addresses</span></span>
- <span data-ttu-id="63a55-131">A kérések útválasztási szabálya az alábbi négy parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a55-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="63a55-132">Az első parancs alhálózati konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a55-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="63a55-133">A második parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a55-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="63a55-134">A harmadik parancs ellenőrzi az alhálózati konfigurációt, és a negyedik parancs ellenőrzi, hogy a virtuális hálózat sikeresen létrejön-e.</span><span class="sxs-lookup"><span data-stu-id="63a55-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="63a55-135">Az alábbi parancsok létrehozzák az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="63a55-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="63a55-136">Az első parancs létrehoz egy GatewayIp01 nevű IP-konfigurációt a korábban létrehozott alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="63a55-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="63a55-137">A második parancs létrehoz egy Pool01 nevű back-end Server-készletet a back-end IP-címek listájával, és a készletet a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="63a55-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="63a55-138">A harmadik parancs létrehozza a back-end Server-készlet beállításait, és a $PoolSetting változóban tárolja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="63a55-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="63a55-139">A Forth parancs létrehoz egy előtér-portot a 80-on, megnevezi a FrontEndPort01-ot, és a $FrontEndPort változóban tárolja a portot.</span><span class="sxs-lookup"><span data-stu-id="63a55-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="63a55-140">Az ötödik parancs az új AzPublicIpAddress segítségével nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a55-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="63a55-141">A hatodik parancs létrehozza az előtér IP-konfigurációját a $PublicIp, a FrontEndPortConfig01, és a $FrontEndIpConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="63a55-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="63a55-142">A hetedik parancs egy figyelőt hoz létre a korábban létrehozott $FrontEndIpConfig $FrontEndPort segítségével.</span><span class="sxs-lookup"><span data-stu-id="63a55-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="63a55-143">A nyolcadik parancs létrehoz egy szabályt a figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="63a55-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="63a55-144">A kilencedik parancs a SKU-ot állítja be.</span><span class="sxs-lookup"><span data-stu-id="63a55-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="63a55-145">A tizedik parancs az átjárót az előző parancsok által beállított objektumokkal hozza létre.</span><span class="sxs-lookup"><span data-stu-id="63a55-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="63a55-146">2. példa: UserAssigned-identitással rendelkező alkalmazásobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="63a55-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="63a55-147">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63a55-147">PARAMETERS</span></span>

### <span data-ttu-id="63a55-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63a55-148">-AsJob</span></span>
<span data-ttu-id="63a55-149">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="63a55-149">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="63a55-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="63a55-151">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a55-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="63a55-153">Automatikus méretezés beállítása</span><span class="sxs-lookup"><span data-stu-id="63a55-153">Autoscale Configuration</span></span>

```yaml
Type: PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="63a55-154">-BackendAddressPools</span></span>
<span data-ttu-id="63a55-155">Az alkalmazás-átjáróhoz tartozó back-end-címkészlet listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="63a55-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="63a55-157">Itt adhatja meg az alkalmazás átjárójának back-end HTTP-beállításainak listáját.</span><span class="sxs-lookup"><span data-stu-id="63a55-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a55-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="63a55-159">Az alkalmazás-átjáró ügyfél-hibája</span><span class="sxs-lookup"><span data-stu-id="63a55-159">Customer error of an application gateway</span></span>

```yaml
Type: PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a55-160">-DefaultProfile</span></span>
<span data-ttu-id="63a55-161">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63a55-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="63a55-162">-EnableFIPS</span></span>
<span data-ttu-id="63a55-163">Engedélyezve van-e a FIPS.</span><span class="sxs-lookup"><span data-stu-id="63a55-163">Whether FIPS is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="63a55-164">-EnableHttp2</span></span>
<span data-ttu-id="63a55-165">Hogy engedélyezve van-e a HTTP2.</span><span class="sxs-lookup"><span data-stu-id="63a55-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="63a55-166">-FirewallPolicy</span></span>
<span data-ttu-id="63a55-167">Tűzfal-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="63a55-167">Firewall configuration</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="63a55-168">-FirewallPolicyId</span></span>
<span data-ttu-id="63a55-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="63a55-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="63a55-170">-Force</span><span class="sxs-lookup"><span data-stu-id="63a55-170">-Force</span></span>
<span data-ttu-id="63a55-171">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="63a55-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="63a55-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="63a55-173">A kényszerített firewallPolicy társítás engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="63a55-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="63a55-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="63a55-175">Az alkalmazás átjárójának előtér IP-konfigurációinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="63a55-176">-FrontendPorts</span></span>
<span data-ttu-id="63a55-177">Az alkalmazás-átjáróhoz tartozó előtér-portok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="63a55-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="63a55-179">Az Application Gateway IP-konfigurációinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="63a55-180">-HttpListeners</span></span>
<span data-ttu-id="63a55-181">Az alkalmazás-átjáróhoz tartozó HTTP-figyelők listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-182">– Identitás</span><span class="sxs-lookup"><span data-stu-id="63a55-182">-Identity</span></span>
<span data-ttu-id="63a55-183">Az alkalmazás-átjáróhoz hozzárendelt alkalmazásobjektum-identitás.</span><span class="sxs-lookup"><span data-stu-id="63a55-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-184">-Hely</span><span class="sxs-lookup"><span data-stu-id="63a55-184">-Location</span></span>
<span data-ttu-id="63a55-185">Azt a régiót adja meg, amelybe az alkalmazás-átjárót létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="63a55-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-186">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63a55-186">-Name</span></span>
<span data-ttu-id="63a55-187">Az alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-187">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a55-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="63a55-189">A privateLink konfigurációjának listája</span><span class="sxs-lookup"><span data-stu-id="63a55-189">The list of privateLink Configuration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-190">– Szondák</span><span class="sxs-lookup"><span data-stu-id="63a55-190">-Probes</span></span>
<span data-ttu-id="63a55-191">Az Application Gateway szondáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="63a55-192">-RedirectConfigurations</span></span>
<span data-ttu-id="63a55-193">Az átirányítási konfiguráció listája</span><span class="sxs-lookup"><span data-stu-id="63a55-193">The list of redirect configuration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="63a55-194">-RequestRoutingRules</span></span>
<span data-ttu-id="63a55-195">A kérések útválasztási szabályainak listáját adja meg az alkalmazás átjárójában.</span><span class="sxs-lookup"><span data-stu-id="63a55-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a55-196">-ResourceGroupName</span></span>
<span data-ttu-id="63a55-197">Annak az erőforrás-csoportnak a nevét adja meg, amelyben létre szeretné hozni az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="63a55-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63a55-198">-RewriteRuleSet</span></span>
<span data-ttu-id="63a55-199">A RewriteRuleSet listája</span><span class="sxs-lookup"><span data-stu-id="63a55-199">The list of RewriteRuleSet</span></span>

```yaml
Type: PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="63a55-200">-Sku</span></span>
<span data-ttu-id="63a55-201">Az alkalmazás-átjáró készletezési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="63a55-202">-SslCertificates</span></span>
<span data-ttu-id="63a55-203">Az Application Gateway SSL-tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="63a55-204">-SslPolicy</span></span>
<span data-ttu-id="63a55-205">Az alkalmazás-átjáró SSL-házirendjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-206">-Címke</span><span class="sxs-lookup"><span data-stu-id="63a55-206">-Tag</span></span>
<span data-ttu-id="63a55-207">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="63a55-207">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="63a55-208">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="63a55-208">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-209">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="63a55-209">-TrustedRootCertificate</span></span>
<span data-ttu-id="63a55-210">A megbízható legfelső szintű tanúsítványok listája</span><span class="sxs-lookup"><span data-stu-id="63a55-210">The list of trusted root certificates</span></span>

```yaml
Type: PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-211">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="63a55-211">-UrlPathMaps</span></span>
<span data-ttu-id="63a55-212">Az URL-cím elérési útvonalát adja meg az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="63a55-212">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-213">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="63a55-213">-UserAssignedIdentityId</span></span>
<span data-ttu-id="63a55-214">Az ResourceId hozzárendelendő felhasználó által hozzárendelt identitás.</span><span class="sxs-lookup"><span data-stu-id="63a55-214">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-215">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a55-215">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="63a55-216">Egy webalkalmazás-tűzfal (WAF) konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63a55-216">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="63a55-217">A WAF a Get-AzApplicationGatewayWebApplicationFirewallConfiguration parancsmaggal is elérheti.</span><span class="sxs-lookup"><span data-stu-id="63a55-217">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-218">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="63a55-218">-Zone</span></span>
<span data-ttu-id="63a55-219">Az elérhetőségi zónák listája, amely azt jelzi, hogy az alkalmazás átjárójának honnan kell származnia.</span><span class="sxs-lookup"><span data-stu-id="63a55-219">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-220">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63a55-220">-Confirm</span></span>
<span data-ttu-id="63a55-221">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63a55-221">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a55-222">-WhatIf</span></span>
<span data-ttu-id="63a55-223">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63a55-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a55-224">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63a55-224">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a55-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a55-225">CommonParameters</span></span>
<span data-ttu-id="63a55-226">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63a55-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a55-227">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="63a55-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a55-228">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63a55-228">INPUTS</span></span>

### <span data-ttu-id="63a55-229">System. String</span><span class="sxs-lookup"><span data-stu-id="63a55-229">System.String</span></span>

### <span data-ttu-id="63a55-230">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="63a55-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="63a55-231">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="63a55-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="63a55-232">Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="63a55-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="63a55-233">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="63a55-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="63a55-234">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="63a55-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="63a55-235">Microsoft. Azure. commands. Network. models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="63a55-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="63a55-236">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="63a55-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="63a55-237">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="63a55-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="63a55-238">Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="63a55-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="63a55-239">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="63a55-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="63a55-240">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="63a55-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="63a55-241">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="63a55-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="63a55-242">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="63a55-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="63a55-243">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="63a55-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="63a55-244">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="63a55-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="63a55-245">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="63a55-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="63a55-246">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a55-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="63a55-247">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a55-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="63a55-248">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63a55-248">System.Collections.Hashtable</span></span>

### <span data-ttu-id="63a55-249">Microsoft. Azure. commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="63a55-249">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="63a55-250">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63a55-250">OUTPUTS</span></span>

### <span data-ttu-id="63a55-251">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63a55-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63a55-252">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63a55-252">NOTES</span></span>

## <span data-ttu-id="63a55-253">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63a55-253">RELATED LINKS</span></span>

[<span data-ttu-id="63a55-254">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63a55-254">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63a55-255">Új – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="63a55-255">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="63a55-256">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="63a55-256">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="63a55-257">Új – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="63a55-257">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="63a55-258">Új – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="63a55-258">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="63a55-259">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a55-259">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="63a55-260">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="63a55-260">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="63a55-261">Új – AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="63a55-261">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="63a55-262">Új – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="63a55-262">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="63a55-263">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="63a55-263">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
