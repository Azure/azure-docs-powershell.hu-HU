---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: a9751806760a8e2265737e72d726fb491191fa5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500516"
---
# <span data-ttu-id="14e67-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14e67-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="14e67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14e67-102">SYNOPSIS</span></span>
<span data-ttu-id="14e67-103">Egy Application Gatewayt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="14e67-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14e67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14e67-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-EnableHttp2] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14e67-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14e67-105">DESCRIPTION</span></span>
<span data-ttu-id="14e67-106">A **New-AzureRmApplicationGateway** parancsmag egy Azure Application Gatewayt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="14e67-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="14e67-107">Az alkalmazás-átjáró a következőket igényli:</span><span class="sxs-lookup"><span data-stu-id="14e67-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="14e67-108">Egy erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="14e67-108">A resource group.</span></span>
- <span data-ttu-id="14e67-109">Virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="14e67-109">A virtual network.</span></span>
- <span data-ttu-id="14e67-110">A back-end Server Pool a back-end-kiszolgálók IP-címeivel.</span><span class="sxs-lookup"><span data-stu-id="14e67-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="14e67-111">A back-end Server-készlet beállításai.</span><span class="sxs-lookup"><span data-stu-id="14e67-111">Back-end server pool settings.</span></span> <span data-ttu-id="14e67-112">Mindegyik készlethez tartozik egy beállítás, például a port, a protokoll és a cookie-alapú affinitás, amelyek a készleten belül minden kiszolgálón érvényesek.</span><span class="sxs-lookup"><span data-stu-id="14e67-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="14e67-113">Az előtér IP-címei, amelyek az alkalmazás-átjárón megnyitott IP-címek.</span><span class="sxs-lookup"><span data-stu-id="14e67-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="14e67-114">Az előtér IP-címe lehet nyilvános IP-cím vagy belső IP-cím.</span><span class="sxs-lookup"><span data-stu-id="14e67-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="14e67-115">Előtér-portok, amelyek az alkalmazás-átjárón megnyitott nyilvános portok.</span><span class="sxs-lookup"><span data-stu-id="14e67-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="14e67-116">Az ilyen portokat tartalmazó forgalom átirányítása a back-end-kiszolgálókra</span><span class="sxs-lookup"><span data-stu-id="14e67-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="14e67-117">Egy olyan Request útválasztási szabály, amely köti a figyelőt és a back-end Server-készletet.</span><span class="sxs-lookup"><span data-stu-id="14e67-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="14e67-118">A szabály meghatározza, hogy melyik back-end Server-készlet a forgalomra irányuljon, amikor egy adott figyelőt üt.</span><span class="sxs-lookup"><span data-stu-id="14e67-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="14e67-119">A figyelőhöz tartozik egy előtér-végpont, egy előtér-IP-cím, egy protokoll (HTTP vagy HTTPS) és a Secure Sockets Layer (SSL) tanúsítvány neve (ha az SSL tehermentesítése beállítással).</span><span class="sxs-lookup"><span data-stu-id="14e67-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="14e67-120">Példák</span><span class="sxs-lookup"><span data-stu-id="14e67-120">EXAMPLES</span></span>

### <span data-ttu-id="14e67-121">1. példa: alkalmazás-átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="14e67-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="14e67-122">Az alábbi példa létrehoz egy Application Gatewayt, ha először létrehoz egy erőforráscsoportot és egy virtuális hálózatot, valamint az alábbiakat:</span><span class="sxs-lookup"><span data-stu-id="14e67-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="14e67-123">Egy back-end Server-készlet</span><span class="sxs-lookup"><span data-stu-id="14e67-123">A back-end server pool</span></span>
- <span data-ttu-id="14e67-124">A kiszolgálói készlet back-end beállításai</span><span class="sxs-lookup"><span data-stu-id="14e67-124">Back-end server pool settings</span></span>
- <span data-ttu-id="14e67-125">Előtér-portok</span><span class="sxs-lookup"><span data-stu-id="14e67-125">Front-end ports</span></span>
- <span data-ttu-id="14e67-126">Előtér IP-címei</span><span class="sxs-lookup"><span data-stu-id="14e67-126">Front-end IP addresses</span></span>
- <span data-ttu-id="14e67-127">A kérés útválasztási szabálya</span><span class="sxs-lookup"><span data-stu-id="14e67-127">A request routing rule</span></span>

<span data-ttu-id="14e67-128">A négy parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="14e67-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="14e67-129">Az első parancs alhálózati konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="14e67-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="14e67-130">A második parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="14e67-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="14e67-131">A harmadik parancs ellenőrzi az alhálózati konfigurációt, és a negyedik parancs ellenőrzi, hogy a virtuális hálózat sikeresen létrejön-e.</span><span class="sxs-lookup"><span data-stu-id="14e67-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="14e67-132">Az alábbi parancsok létrehozzák az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="14e67-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="14e67-133">Az első parancs létrehoz egy GatewayIp01 nevű IP-konfigurációt a korábban létrehozott alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="14e67-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="14e67-134">A második parancs létrehoz egy Pool01 nevű back-end Server-készletet a back-end IP-címek listájával, és a készletet a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="14e67-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="14e67-135">A harmadik parancs létrehozza a back-end Server-készlet beállításait, és a $PoolSetting változóban tárolja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="14e67-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="14e67-136">A Forth parancs létrehoz egy előtér-portot a 80-on, megnevezi a FrontEndPort01-ot, és a $FrontEndPort változóban tárolja a portot.</span><span class="sxs-lookup"><span data-stu-id="14e67-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="14e67-137">Az ötödik parancs az új AzureRmPublicIpAddress segítségével nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="14e67-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="14e67-138">A hatodik parancs létrehozza az előtér IP-konfigurációját a $PublicIp, a FrontEndPortConfig01, és a $FrontEndIpConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="14e67-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="14e67-139">A hetedik parancs egy figyelőt hoz létre a korábban létrehozott $FrontEndIpConfig $FrontEndPort segítségével.</span><span class="sxs-lookup"><span data-stu-id="14e67-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="14e67-140">A nyolcadik parancs létrehoz egy szabályt a figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="14e67-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="14e67-141">A kilencedik parancs a SKU-ot állítja be.</span><span class="sxs-lookup"><span data-stu-id="14e67-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="14e67-142">A tizedik parancs az átjárót az előző parancsok által beállított objektumokkal hozza létre.</span><span class="sxs-lookup"><span data-stu-id="14e67-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="14e67-143">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14e67-143">PARAMETERS</span></span>

### <span data-ttu-id="14e67-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14e67-144">-AsJob</span></span>
<span data-ttu-id="14e67-145">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="14e67-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14e67-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="14e67-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="14e67-147">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-147">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="14e67-148">-BackendAddressPools</span></span>
<span data-ttu-id="14e67-149">Az alkalmazás-átjáróhoz tartozó back-end-címkészlet listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-149">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="14e67-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="14e67-151">Itt adhatja meg az alkalmazás átjárójának back-end HTTP-beállításainak listáját.</span><span class="sxs-lookup"><span data-stu-id="14e67-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e67-152">-DefaultProfile</span></span>
<span data-ttu-id="14e67-153">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14e67-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14e67-154">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="14e67-154">-EnableHttp2</span></span>
<span data-ttu-id="14e67-155">Hogy engedélyezve van-e a HTTP2.</span><span class="sxs-lookup"><span data-stu-id="14e67-155">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-156">-Force</span><span class="sxs-lookup"><span data-stu-id="14e67-156">-Force</span></span>
<span data-ttu-id="14e67-157">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="14e67-157">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14e67-158">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="14e67-158">-FrontendIPConfigurations</span></span>
<span data-ttu-id="14e67-159">Az alkalmazás átjárójának előtér IP-konfigurációinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-159">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-160">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="14e67-160">-FrontendPorts</span></span>
<span data-ttu-id="14e67-161">Az alkalmazás-átjáróhoz tartozó előtér-portok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-161">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-162">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="14e67-162">-GatewayIPConfigurations</span></span>
<span data-ttu-id="14e67-163">Az Application Gateway IP-konfigurációinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-163">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-164">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="14e67-164">-HttpListeners</span></span>
<span data-ttu-id="14e67-165">Az alkalmazás-átjáróhoz tartozó HTTP-figyelők listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-165">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-166">-Hely</span><span class="sxs-lookup"><span data-stu-id="14e67-166">-Location</span></span>
<span data-ttu-id="14e67-167">Azt a régiót adja meg, amelybe az alkalmazás-átjárót létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="14e67-167">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="14e67-168">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14e67-168">-Name</span></span>
<span data-ttu-id="14e67-169">Az alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-169">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="14e67-170">– Szondák</span><span class="sxs-lookup"><span data-stu-id="14e67-170">-Probes</span></span>
<span data-ttu-id="14e67-171">Az Application Gateway szondáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-171">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-172">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="14e67-172">-RedirectConfigurations</span></span>
<span data-ttu-id="14e67-173">Az átirányítási konfiguráció listája</span><span class="sxs-lookup"><span data-stu-id="14e67-173">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-174">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="14e67-174">-RequestRoutingRules</span></span>
<span data-ttu-id="14e67-175">A kérések útválasztási szabályainak listáját adja meg az alkalmazás átjárójában.</span><span class="sxs-lookup"><span data-stu-id="14e67-175">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e67-176">-ResourceGroupName</span></span>
<span data-ttu-id="14e67-177">Annak az erőforrás-csoportnak a nevét adja meg, amelyben létre szeretné hozni az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="14e67-177">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="14e67-178">-SKU</span><span class="sxs-lookup"><span data-stu-id="14e67-178">-Sku</span></span>
<span data-ttu-id="14e67-179">Az alkalmazás-átjáró készletezési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-179">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="14e67-180">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="14e67-180">-SslCertificates</span></span>
<span data-ttu-id="14e67-181">Az Application Gateway SSL-tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-181">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-182">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="14e67-182">-SslPolicy</span></span>
<span data-ttu-id="14e67-183">Az alkalmazás-átjáró SSL-házirendjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-183">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="14e67-184">-Címke</span><span class="sxs-lookup"><span data-stu-id="14e67-184">-Tag</span></span>
<span data-ttu-id="14e67-185">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="14e67-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="14e67-186">Példa:</span><span class="sxs-lookup"><span data-stu-id="14e67-186">For example:</span></span>

<span data-ttu-id="14e67-187">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="14e67-187">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="14e67-188">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="14e67-188">-UrlPathMaps</span></span>
<span data-ttu-id="14e67-189">Az URL-cím elérési útvonalát adja meg az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="14e67-189">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14e67-190">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="14e67-190">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="14e67-191">Egy webalkalmazás-tűzfal (WAF) konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14e67-191">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="14e67-192">A WAF a Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration parancsmaggal is elérheti.</span><span class="sxs-lookup"><span data-stu-id="14e67-192">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="14e67-193">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14e67-193">-Confirm</span></span>
<span data-ttu-id="14e67-194">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14e67-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e67-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e67-195">-WhatIf</span></span>
<span data-ttu-id="14e67-196">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14e67-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e67-197">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14e67-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e67-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e67-198">CommonParameters</span></span>
<span data-ttu-id="14e67-199">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14e67-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e67-200">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e67-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e67-201">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14e67-201">INPUTS</span></span>

### <span data-ttu-id="14e67-202">Nincs</span><span class="sxs-lookup"><span data-stu-id="14e67-202">None</span></span>
<span data-ttu-id="14e67-203">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="14e67-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14e67-204">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14e67-204">OUTPUTS</span></span>

### <span data-ttu-id="14e67-205">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14e67-205">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14e67-206">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14e67-206">NOTES</span></span>

## <span data-ttu-id="14e67-207">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14e67-207">RELATED LINKS</span></span>

[<span data-ttu-id="14e67-208">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="14e67-208">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="14e67-209">Új – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="14e67-209">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="14e67-210">Új – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="14e67-210">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="14e67-211">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="14e67-211">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="14e67-212">Új – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14e67-212">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="14e67-213">Új – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="14e67-213">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="14e67-214">Új – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="14e67-214">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="14e67-215">Új – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="14e67-215">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="14e67-216">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="14e67-216">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="14e67-217">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="14e67-217">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
