---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495050"
---
# <span data-ttu-id="99189-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99189-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="99189-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99189-102">SYNOPSIS</span></span>
<span data-ttu-id="99189-103">Egy Application Gatewayt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99189-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99189-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99189-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
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
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99189-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99189-105">DESCRIPTION</span></span>
<span data-ttu-id="99189-106">A **New-AzureRmApplicationGateway** parancsmag egy Azure Application Gatewayt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99189-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="99189-107">Az alkalmazás-átjáró a következőket igényli:</span><span class="sxs-lookup"><span data-stu-id="99189-107">An application gateway requires the following:</span></span>
- <span data-ttu-id="99189-108">Egy erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="99189-108">A resource group.</span></span>
- <span data-ttu-id="99189-109">Virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="99189-109">A virtual network.</span></span>
- <span data-ttu-id="99189-110">A back-end Server Pool a back-end-kiszolgálók IP-címeivel.</span><span class="sxs-lookup"><span data-stu-id="99189-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="99189-111">A back-end Server-készlet beállításai.</span><span class="sxs-lookup"><span data-stu-id="99189-111">Back-end server pool settings.</span></span> <span data-ttu-id="99189-112">Mindegyik készlethez tartozik egy beállítás, például a port, a protokoll és a cookie-alapú affinitás, amelyek a készleten belül minden kiszolgálón érvényesek.</span><span class="sxs-lookup"><span data-stu-id="99189-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="99189-113">Az előtér IP-címei, amelyek az alkalmazás-átjárón megnyitott IP-címek.</span><span class="sxs-lookup"><span data-stu-id="99189-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="99189-114">Az előtér IP-címe lehet nyilvános IP-cím vagy belső IP-cím.</span><span class="sxs-lookup"><span data-stu-id="99189-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="99189-115">Előtér-portok, amelyek az alkalmazás-átjárón megnyitott nyilvános portok.</span><span class="sxs-lookup"><span data-stu-id="99189-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="99189-116">Az ilyen portokat tartalmazó forgalom átirányítása a back-end-kiszolgálókra</span><span class="sxs-lookup"><span data-stu-id="99189-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="99189-117">Egy olyan Request útválasztási szabály, amely köti a figyelőt és a back-end Server-készletet.</span><span class="sxs-lookup"><span data-stu-id="99189-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="99189-118">A szabály meghatározza, hogy melyik back-end Server-készlet a forgalomra irányuljon, amikor egy adott figyelőt üt.</span><span class="sxs-lookup"><span data-stu-id="99189-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="99189-119">A figyelőhöz tartozik egy előtér-végpont, egy előtér-IP-cím, egy protokoll (HTTP vagy HTTPS) és a Secure Sockets Layer (SSL) tanúsítvány neve (ha az SSL tehermentesítése beállítással).</span><span class="sxs-lookup"><span data-stu-id="99189-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="99189-120">Példák</span><span class="sxs-lookup"><span data-stu-id="99189-120">EXAMPLES</span></span>

### <span data-ttu-id="99189-121">1. példa: alkalmazás-átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="99189-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="99189-122">Az alábbi példa létrehoz egy Application Gatewayt, ha először létrehoz egy erőforráscsoportot és egy virtuális hálózatot, valamint az alábbiakat:</span><span class="sxs-lookup"><span data-stu-id="99189-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="99189-123">Egy back-end Server-készlet</span><span class="sxs-lookup"><span data-stu-id="99189-123">A back-end server pool</span></span>
- <span data-ttu-id="99189-124">A kiszolgálói készlet back-end beállításai</span><span class="sxs-lookup"><span data-stu-id="99189-124">Back-end server pool settings</span></span>
- <span data-ttu-id="99189-125">Előtér-portok</span><span class="sxs-lookup"><span data-stu-id="99189-125">Front-end ports</span></span>
- <span data-ttu-id="99189-126">Előtér IP-címei</span><span class="sxs-lookup"><span data-stu-id="99189-126">Front-end IP addresses</span></span>
- <span data-ttu-id="99189-127">A kérések útválasztási szabálya az alábbi négy parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99189-127">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="99189-128">Az első parancs alhálózati konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99189-128">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="99189-129">A második parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99189-129">The second command creates a virtual network.</span></span>
<span data-ttu-id="99189-130">A harmadik parancs ellenőrzi az alhálózati konfigurációt, és a negyedik parancs ellenőrzi, hogy a virtuális hálózat sikeresen létrejön-e.</span><span class="sxs-lookup"><span data-stu-id="99189-130">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="99189-131">Az alábbi parancsok létrehozzák az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="99189-131">The following commands create the application gateway.</span></span>
<span data-ttu-id="99189-132">Az első parancs létrehoz egy GatewayIp01 nevű IP-konfigurációt a korábban létrehozott alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="99189-132">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="99189-133">A második parancs létrehoz egy Pool01 nevű back-end Server-készletet a back-end IP-címek listájával, és a készletet a $Pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="99189-133">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="99189-134">A harmadik parancs létrehozza a back-end Server-készlet beállításait, és a $PoolSetting változóban tárolja a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="99189-134">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="99189-135">A Forth parancs létrehoz egy előtér-portot a 80-on, megnevezi a FrontEndPort01-ot, és a $FrontEndPort változóban tárolja a portot.</span><span class="sxs-lookup"><span data-stu-id="99189-135">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="99189-136">Az ötödik parancs az új AzureRmPublicIpAddress segítségével nyilvános IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99189-136">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="99189-137">A hatodik parancs létrehozza az előtér IP-konfigurációját a $PublicIp, a FrontEndPortConfig01, és a $FrontEndIpConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="99189-137">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="99189-138">A hetedik parancs egy figyelőt hoz létre a korábban létrehozott $FrontEndIpConfig $FrontEndPort segítségével.</span><span class="sxs-lookup"><span data-stu-id="99189-138">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="99189-139">A nyolcadik parancs létrehoz egy szabályt a figyelőhöz.</span><span class="sxs-lookup"><span data-stu-id="99189-139">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="99189-140">A kilencedik parancs a SKU-ot állítja be.</span><span class="sxs-lookup"><span data-stu-id="99189-140">The ninth command sets the SKU.</span></span>
<span data-ttu-id="99189-141">A tizedik parancs az átjárót az előző parancsok által beállított objektumokkal hozza létre.</span><span class="sxs-lookup"><span data-stu-id="99189-141">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="99189-142">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99189-142">PARAMETERS</span></span>

### <span data-ttu-id="99189-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99189-143">-AsJob</span></span>
<span data-ttu-id="99189-144">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99189-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99189-145">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="99189-145">-AuthenticationCertificates</span></span>
<span data-ttu-id="99189-146">Az Application Gateway hitelesítési tanúsítványait adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-146">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="99189-147">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="99189-147">-AutoscaleConfiguration</span></span>
<span data-ttu-id="99189-148">Automatikus méretezés beállítása</span><span class="sxs-lookup"><span data-stu-id="99189-148">Autoscale Configuration</span></span>

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

### <span data-ttu-id="99189-149">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="99189-149">-BackendAddressPools</span></span>
<span data-ttu-id="99189-150">Az alkalmazás-átjáróhoz tartozó back-end-címkészlet listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-150">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="99189-151">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="99189-151">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="99189-152">Itt adhatja meg az alkalmazás átjárójának back-end HTTP-beállításainak listáját.</span><span class="sxs-lookup"><span data-stu-id="99189-152">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="99189-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99189-153">-DefaultProfile</span></span>
<span data-ttu-id="99189-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99189-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99189-155">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="99189-155">-EnableFIPS</span></span>
<span data-ttu-id="99189-156">Engedélyezve van-e a FIPS.</span><span class="sxs-lookup"><span data-stu-id="99189-156">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="99189-157">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="99189-157">-EnableHttp2</span></span>
<span data-ttu-id="99189-158">Hogy engedélyezve van-e a HTTP2.</span><span class="sxs-lookup"><span data-stu-id="99189-158">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="99189-159">-Force</span><span class="sxs-lookup"><span data-stu-id="99189-159">-Force</span></span>
<span data-ttu-id="99189-160">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="99189-160">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99189-161">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="99189-161">-FrontendIPConfigurations</span></span>
<span data-ttu-id="99189-162">Az alkalmazás átjárójának előtér IP-konfigurációinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-162">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="99189-163">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="99189-163">-FrontendPorts</span></span>
<span data-ttu-id="99189-164">Az alkalmazás-átjáróhoz tartozó előtér-portok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-164">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="99189-165">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="99189-165">-GatewayIPConfigurations</span></span>
<span data-ttu-id="99189-166">Az Application Gateway IP-konfigurációinak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-166">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="99189-167">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="99189-167">-HttpListeners</span></span>
<span data-ttu-id="99189-168">Az alkalmazás-átjáróhoz tartozó HTTP-figyelők listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-168">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="99189-169">-Hely</span><span class="sxs-lookup"><span data-stu-id="99189-169">-Location</span></span>
<span data-ttu-id="99189-170">Azt a régiót adja meg, amelybe az alkalmazás-átjárót létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="99189-170">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="99189-171">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99189-171">-Name</span></span>
<span data-ttu-id="99189-172">Az alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-172">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="99189-173">– Szondák</span><span class="sxs-lookup"><span data-stu-id="99189-173">-Probes</span></span>
<span data-ttu-id="99189-174">Az Application Gateway szondáit adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-174">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="99189-175">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="99189-175">-RedirectConfigurations</span></span>
<span data-ttu-id="99189-176">Az átirányítási konfiguráció listája</span><span class="sxs-lookup"><span data-stu-id="99189-176">The list of redirect configuration</span></span>

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

### <span data-ttu-id="99189-177">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="99189-177">-RequestRoutingRules</span></span>
<span data-ttu-id="99189-178">A kérések útválasztási szabályainak listáját adja meg az alkalmazás átjárójában.</span><span class="sxs-lookup"><span data-stu-id="99189-178">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="99189-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99189-179">-ResourceGroupName</span></span>
<span data-ttu-id="99189-180">Annak az erőforrás-csoportnak a nevét adja meg, amelyben létre szeretné hozni az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="99189-180">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="99189-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="99189-181">-Sku</span></span>
<span data-ttu-id="99189-182">Az alkalmazás-átjáró készletezési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-182">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="99189-183">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="99189-183">-SslCertificates</span></span>
<span data-ttu-id="99189-184">Az Application Gateway SSL-tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-184">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="99189-185">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="99189-185">-SslPolicy</span></span>
<span data-ttu-id="99189-186">Az alkalmazás-átjáró SSL-házirendjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-186">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="99189-187">-Címke</span><span class="sxs-lookup"><span data-stu-id="99189-187">-Tag</span></span>
<span data-ttu-id="99189-188">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="99189-188">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="99189-189">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="99189-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="99189-190">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="99189-190">-TrustedRootCertificate</span></span>
<span data-ttu-id="99189-191">A megbízható legfelső szintű tanúsítványok listája</span><span class="sxs-lookup"><span data-stu-id="99189-191">The list of trusted root certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99189-192">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="99189-192">-UrlPathMaps</span></span>
<span data-ttu-id="99189-193">Az URL-cím elérési útvonalát adja meg az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="99189-193">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="99189-194">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="99189-194">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="99189-195">Egy webalkalmazás-tűzfal (WAF) konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99189-195">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="99189-196">A WAF a Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration parancsmaggal is elérheti.</span><span class="sxs-lookup"><span data-stu-id="99189-196">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="99189-197">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="99189-197">-Zone</span></span>
<span data-ttu-id="99189-198">Az elérhetőségi zónák listája, amely azt jelzi, hogy az alkalmazás átjárójának honnan kell származnia.</span><span class="sxs-lookup"><span data-stu-id="99189-198">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99189-199">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99189-199">-Confirm</span></span>
<span data-ttu-id="99189-200">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99189-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99189-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99189-201">-WhatIf</span></span>
<span data-ttu-id="99189-202">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99189-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99189-203">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99189-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99189-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99189-204">CommonParameters</span></span>
<span data-ttu-id="99189-205">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99189-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99189-206">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99189-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99189-207">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99189-207">INPUTS</span></span>

### <span data-ttu-id="99189-208">System. String</span><span class="sxs-lookup"><span data-stu-id="99189-208">System.String</span></span>

### <span data-ttu-id="99189-209">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="99189-209">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="99189-210">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="99189-210">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="99189-211">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-211">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-212">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-212">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-213">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayAuthenticationCertificate, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-213">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-214">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendIPConfiguration, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-214">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-215">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-215">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-216">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayProbe, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-216">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-217">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-217">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-218">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendHttpSettings, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-218">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-219">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-219">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-220">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-220">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-221">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-221">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-222">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99189-222">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="99189-223">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="99189-223">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="99189-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="99189-224">System.Collections.Hashtable</span></span>

## <span data-ttu-id="99189-225">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99189-225">OUTPUTS</span></span>

### <span data-ttu-id="99189-226">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99189-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99189-227">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99189-227">NOTES</span></span>

## <span data-ttu-id="99189-228">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99189-228">RELATED LINKS</span></span>

[<span data-ttu-id="99189-229">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="99189-229">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="99189-230">Új – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="99189-230">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="99189-231">Új – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="99189-231">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="99189-232">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="99189-232">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="99189-233">Új – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="99189-233">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="99189-234">Új – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="99189-234">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="99189-235">Új – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="99189-235">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="99189-236">Új – AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="99189-236">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="99189-237">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99189-237">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="99189-238">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="99189-238">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
