---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 0f3d65c629218fc903035cb9df669f1c3dc7a50c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379552"
---
# <span data-ttu-id="fbe4b-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbe4b-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="fbe4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe4b-103">Alkalmazás-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-103">Creates an application gateway.</span></span>

## <span data-ttu-id="fbe4b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbe4b-104">SYNTAX</span></span>

### <span data-ttu-id="fbe4b-105">IdentityByUserAssignedIdentityId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbe4b-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="fbe4b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbe4b-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="fbe4b-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fbe4b-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

### <span data-ttu-id="fbe4b-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="fbe4b-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
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

## <span data-ttu-id="fbe4b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbe4b-109">DESCRIPTION</span></span>
<span data-ttu-id="fbe4b-110">A **New-AzApplicationGateway** parancsmag létrehoz egy Azure-alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="fbe4b-111">Az alkalmazás-átjárókhoz az alábbiakra van szükség:</span><span class="sxs-lookup"><span data-stu-id="fbe4b-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="fbe4b-112">Erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-112">A resource group.</span></span>
- <span data-ttu-id="fbe4b-113">Egy virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-113">A virtual network.</span></span>
- <span data-ttu-id="fbe4b-114">Egy háttérkiszolgáló-készlet, amely a háttérkiszolgálók IP-címét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="fbe4b-115">A háttérkiszolgáló készletének beállításai.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-115">Back-end server pool settings.</span></span> <span data-ttu-id="fbe4b-116">Minden készletnek vannak olyan beállításai, mint a port, a protokoll és a cookie-alapú affinitás, amely a készleten belül minden kiszolgálóra érvényes.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="fbe4b-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="fbe4b-118">Az előlapi IP-címek nyilvános IP-címek vagy belső IP-címek is lehetek.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="fbe4b-119">Előlapi portok, amelyek az alkalmazás-átjárón megnyitott nyilvános portok.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="fbe4b-120">Az ilyen portokat át lehet irányítani a háttérkiszolgálókra.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="fbe4b-121">Egy kéréstovábbító szabály, amely összeköti a figyelőt és a háttérkiszolgáló-készletet.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="fbe4b-122">A szabály azt határozza meg, hogy melyik háttérkiszolgáló készletbe kell irányítani a forgalmat, amikor egy adott hallgatóhoz ér.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="fbe4b-123">A hallgató rendelkezik előlapi porttal, előlapi IP-címmel, protokollal (HTTP vagy HTTPS) és SSL-tanúsítványnévvel (ha konfigurálja az SSL-t a betöltéskor).</span><span class="sxs-lookup"><span data-stu-id="fbe4b-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="fbe4b-124">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbe4b-124">EXAMPLES</span></span>

### <span data-ttu-id="fbe4b-125">1. példa: Alkalmazás-átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbe4b-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="fbe4b-126">Az alábbi példa először létrehoz egy alkalmazás-átjárót egy erőforráscsoport és egy virtuális hálózat létrehozásával, valamint az alábbiakkal:</span><span class="sxs-lookup"><span data-stu-id="fbe4b-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="fbe4b-127">Háttérkiszolgáló-készlet</span><span class="sxs-lookup"><span data-stu-id="fbe4b-127">A back-end server pool</span></span>
- <span data-ttu-id="fbe4b-128">Back-end server pool settings</span><span class="sxs-lookup"><span data-stu-id="fbe4b-128">Back-end server pool settings</span></span>
- <span data-ttu-id="fbe4b-129">Előlapi portok</span><span class="sxs-lookup"><span data-stu-id="fbe4b-129">Front-end ports</span></span>
- <span data-ttu-id="fbe4b-130">Előlapi IP-címek</span><span class="sxs-lookup"><span data-stu-id="fbe4b-130">Front-end IP addresses</span></span>
- <span data-ttu-id="fbe4b-131">Kéréstovábbítási szabály Ez a négy parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="fbe4b-132">Az első parancs létrehoz egy alhálózati konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="fbe4b-133">A második parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="fbe4b-134">A harmadik parancs ellenőrzi az alhálózat konfigurációját, a negyedik pedig ellenőrzi, hogy a virtuális hálózat létrehozása sikerült-e.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="fbe4b-135">Az alábbi parancsokkal hozhatja létre az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="fbe4b-136">Az első parancs létrehoz egy GatewayIp01 nevű IP-konfigurációt a korábban létrehozott alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="fbe4b-137">A második parancs létrehoz egy Pool01 nevű háttérkiszolgáló-készletet a háttér-IP-címek listájával, és a készletet a $Pool tárolja.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="fbe4b-138">A harmadik parancs létrehozza a háttérkiszolgáló-készlet beállításait, és a beállításokat a $PoolSetting tárolja.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="fbe4b-139">A oda parancs előtűnő portot hoz létre a 80-as porton, frontEndPort01 névvel, és a portot a $FrontEndPort változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="fbe4b-140">Az ötödik parancs nyilvános IP-címet hoz létre a New-AzPublicIpAddress paranccsal.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="fbe4b-141">A hatodik parancs előlapi IP-konfigurációt hoz létre a $PublicIp segítségével, frontEndPortConfig01 nevet ad neki, és a $FrontEndIpConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="fbe4b-142">A hetedik parancs létrehoz egy hallgatót a korábban létrehozott $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="fbe4b-143">A nyolcadik parancs létrehoz egy szabályt a hallgató számára.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="fbe4b-144">A kilencedik parancs beállítja a termékváltozatot.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="fbe4b-145">A tízedik parancs az előző parancsok által beállított objektumok használatával hozza létre az átjárót.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="fbe4b-146">2. példa: Alkalmazás-átjáró létrehozása UserAssigned Identity azonosítóval</span><span class="sxs-lookup"><span data-stu-id="fbe4b-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="fbe4b-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbe4b-147">PARAMETERS</span></span>

### <span data-ttu-id="fbe4b-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbe4b-148">-AsJob</span></span>
<span data-ttu-id="fbe4b-149">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fbe4b-149">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="fbe4b-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="fbe4b-151">Az alkalmazás-átjáró hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="fbe4b-153">Automatikus méretezés beállítása</span><span class="sxs-lookup"><span data-stu-id="fbe4b-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="fbe4b-154">-BackendAddressPools</span></span>
<span data-ttu-id="fbe4b-155">Az alkalmazás-átjáró háttércímkészletek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="fbe4b-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="fbe4b-157">Az alkalmazás-átjáró háttér-HTTP-beállításainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="fbe4b-159">Ügyfélhiba egy alkalmazás-átjáróban</span><span class="sxs-lookup"><span data-stu-id="fbe4b-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe4b-160">-DefaultProfile</span></span>
<span data-ttu-id="fbe4b-161">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbe4b-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="fbe4b-162">-EnableFIPS</span></span>
<span data-ttu-id="fbe4b-163">Hogy a FIPS engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-163">Whether FIPS is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="fbe4b-164">-EnableHttp2</span></span>
<span data-ttu-id="fbe4b-165">Hogy a HTTP2 engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fbe4b-166">-FirewallPolicy</span></span>
<span data-ttu-id="fbe4b-167">Tűzfal-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="fbe4b-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="fbe4b-168">-FirewallPolicyId</span></span>
<span data-ttu-id="fbe4b-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="fbe4b-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="fbe4b-170">-Force</span><span class="sxs-lookup"><span data-stu-id="fbe4b-170">-Force</span></span>
<span data-ttu-id="fbe4b-171">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="fbe4b-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="fbe4b-173">Hogy engedélyezve van-e a Force firewallPolicy társítás.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="fbe4b-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="fbe4b-175">Az előlapi IP-konfigurációk listáját adja meg az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="fbe4b-176">-FrontendPorts</span></span>
<span data-ttu-id="fbe4b-177">Az alkalmazás átjárója előlapi portjainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="fbe4b-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="fbe4b-179">Az alkalmazás-átjáró IP-konfigurációjának listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="fbe4b-180">-HttpListeners</span></span>
<span data-ttu-id="fbe4b-181">Az alkalmazás-átjáró HTTP- hallgatóinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="fbe4b-182">-Identity</span></span>
<span data-ttu-id="fbe4b-183">Application Gateway Identity to be assigned to Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-184">-Location</span><span class="sxs-lookup"><span data-stu-id="fbe4b-184">-Location</span></span>
<span data-ttu-id="fbe4b-185">Azt a régiót adja meg, amelyben létre kell hoznia az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-186">-Name</span><span class="sxs-lookup"><span data-stu-id="fbe4b-186">-Name</span></span>
<span data-ttu-id="fbe4b-187">Az alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-187">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="fbe4b-189">The list of privateLink Configuration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-189">The list of privateLink Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-190">-Fogarasok</span><span class="sxs-lookup"><span data-stu-id="fbe4b-190">-Probes</span></span>
<span data-ttu-id="fbe4b-191">Az alkalmazás-átjárónál megadott értékeket határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="fbe4b-192">-RedirectConfigurations</span></span>
<span data-ttu-id="fbe4b-193">Az átirányítási konfiguráció listája</span><span class="sxs-lookup"><span data-stu-id="fbe4b-193">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="fbe4b-194">-RequestRoutingRules</span></span>
<span data-ttu-id="fbe4b-195">Az alkalmazás-átjáró kéréstovábbító szabályainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe4b-196">-ResourceGroupName</span></span>
<span data-ttu-id="fbe4b-197">Annak az erőforráscsoportnak a nevét adja meg, amelyben létre kell hoznia az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fbe4b-198">-RewriteRuleSet</span></span>
<span data-ttu-id="fbe4b-199">The list of RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fbe4b-199">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-200">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="fbe4b-200">-Sku</span></span>
<span data-ttu-id="fbe4b-201">Az alkalmazás-átjáró készletkészletét (SKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="fbe4b-202">-SslCertificates</span></span>
<span data-ttu-id="fbe4b-203">Az ssl-tanúsítványok listájának megadása az alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="fbe4b-204">-SslPolicy</span></span>
<span data-ttu-id="fbe4b-205">Ssl-házirendet ad meg az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-206">-SslProfiles</span><span class="sxs-lookup"><span data-stu-id="fbe4b-206">-SslProfiles</span></span>
<span data-ttu-id="fbe4b-207">Az ssl-profilok listája</span><span class="sxs-lookup"><span data-stu-id="fbe4b-207">The list of ssl profiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-208">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbe4b-208">-Tag</span></span>
<span data-ttu-id="fbe4b-209">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-209">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fbe4b-210">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="fbe4b-210">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-211">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="fbe4b-211">-TrustedClientCertificates</span></span>
<span data-ttu-id="fbe4b-212">A megbízható ügyfél-hitelesítésszolgáltatói tanúsítványláncok listája</span><span class="sxs-lookup"><span data-stu-id="fbe4b-212">The list of trusted client CA certificate chains</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-213">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbe4b-213">-TrustedRootCertificate</span></span>
<span data-ttu-id="fbe4b-214">A megbízható főtanúsítványok listája</span><span class="sxs-lookup"><span data-stu-id="fbe4b-214">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-215">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="fbe4b-215">-UrlPathMaps</span></span>
<span data-ttu-id="fbe4b-216">Az alkalmazás-átjáró URL-útvonaltérképét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-216">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-217">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="fbe4b-217">-UserAssignedIdentityId</span></span>
<span data-ttu-id="fbe4b-218">Az Alkalmazás átjáróhoz hozzárendelni szükséges felhasználó által hozzárendelt identitás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-218">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-219">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-219">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="fbe4b-220">A webalkalmazás tűzfalának (WAF) konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-220">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="fbe4b-221">A Get-AzApplicationGatewayWebApplicationFirewallConfiguration parancsmagot is használhatja.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-221">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-222">-Zone</span><span class="sxs-lookup"><span data-stu-id="fbe4b-222">-Zone</span></span>
<span data-ttu-id="fbe4b-223">A rendelkezésre állási zónák listája, amely azt sorolja fel, hogy az alkalmazás-átjárónak honnan kell átjönni.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-223">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-224">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbe4b-224">-Confirm</span></span>
<span data-ttu-id="fbe4b-225">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-225">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-226">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe4b-226">-WhatIf</span></span>
<span data-ttu-id="fbe4b-227">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-227">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe4b-228">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-228">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe4b-229">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe4b-229">CommonParameters</span></span>
<span data-ttu-id="fbe4b-230">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe4b-230">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe4b-231">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbe4b-231">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe4b-232">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbe4b-232">INPUTS</span></span>

### <span data-ttu-id="fbe4b-233">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe4b-233">System.String</span></span>

### <span data-ttu-id="fbe4b-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="fbe4b-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="fbe4b-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="fbe4b-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="fbe4b-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="fbe4b-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="fbe4b-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="fbe4b-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="fbe4b-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="fbe4b-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="fbe4b-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="fbe4b-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="fbe4b-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="fbe4b-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="fbe4b-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="fbe4b-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="fbe4b-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="fbe4b-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="fbe4b-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="fbe4b-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="fbe4b-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="fbe4b-252">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbe4b-252">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fbe4b-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="fbe4b-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="fbe4b-254">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbe4b-254">OUTPUTS</span></span>

### <span data-ttu-id="fbe4b-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbe4b-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fbe4b-256">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbe4b-256">NOTES</span></span>

## <span data-ttu-id="fbe4b-257">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbe4b-257">RELATED LINKS</span></span>

[<span data-ttu-id="fbe4b-258">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fbe4b-258">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fbe4b-259">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="fbe4b-259">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="fbe4b-260">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fbe4b-260">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fbe4b-261">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fbe4b-261">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fbe4b-262">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fbe4b-262">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fbe4b-263">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe4b-263">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="fbe4b-264">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fbe4b-264">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="fbe4b-265">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="fbe4b-265">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="fbe4b-266">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fbe4b-266">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="fbe4b-267">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fbe4b-267">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
