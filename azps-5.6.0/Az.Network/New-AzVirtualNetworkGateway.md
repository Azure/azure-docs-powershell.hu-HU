---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c9729dd81dc5ff287ab032fdce6ad937c282e1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931554"
---
# <span data-ttu-id="40d85-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40d85-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="40d85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d85-102">SYNOPSIS</span></span>
<span data-ttu-id="40d85-103">Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="40d85-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="40d85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40d85-104">SYNTAX</span></span>

### <span data-ttu-id="40d85-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40d85-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d85-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="40d85-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d85-107">ServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="40d85-107">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40d85-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="40d85-108">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40d85-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40d85-109">DESCRIPTION</span></span>
<span data-ttu-id="40d85-110">A virtuális hálózati átjáró az azure-beli átjárót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="40d85-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="40d85-111">A **New-AzVirtualNetworkGateway** parancsmag létrehozza az átjáró objektumát az Azure-ban a név, az erőforráscsoport neve, a hely és az IP-konfiguráció, valamint az átjáró típusa, illetve ha VPN, a VPN-típus alapján.</span><span class="sxs-lookup"><span data-stu-id="40d85-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="40d85-112">Az átjáró termékváltozatát is meg is nevezheti.</span><span class="sxs-lookup"><span data-stu-id="40d85-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="40d85-113">Ha ezt az átjárót a "Point-to-Site" kapcsolatokhoz használja, akkor azt a VPN-ügyfélcímkészletet is fel kell használnia, amelyből címeket szeretne hozzárendelni a csatlakozó ügyfélalkalmazáshoz, valamint az átjáróhoz csatlakozó VPN-ügyfélalkalmazások hitelesítéséhez használt VPN-ügyféltanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="40d85-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="40d85-114">Azt is választhatja, hogy más szolgáltatásokat is tartalmaz, például a BGP-t és az Aktív-aktív funkciót.</span><span class="sxs-lookup"><span data-stu-id="40d85-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="40d85-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40d85-115">EXAMPLES</span></span>

### <span data-ttu-id="40d85-116">1. példa: Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="40d85-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="40d85-117">A fentiekkel létrehozhat egy erőforráscsoportot, nyilvános IP-címet kérhet, virtuális hálózatot és alhálózatot hozhat létre, és virtuális hálózati átjárót hozhat létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40d85-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="40d85-118">Az átjáró neve "myNGW" lesz a "vnet-gateway" erőforráscsoportban az "UK West" helyen, a korábban létrehozott IP-konfigurációkat az "ngwIPConfig" változóban, az átjáró típusát "VPN", a vpn-típust "RouteBased" és az "Egyszerű" termékváltozatot.</span><span class="sxs-lookup"><span data-stu-id="40d85-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="40d85-119">2. példa: Virtuális hálózati átjáró létrehozása külső sugarú konfigurációval</span><span class="sxs-lookup"><span data-stu-id="40d85-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="40d85-120">A fentiekkel létrehozhat egy erőforráscsoportot, nyilvános IP-címet kérhet, virtuális hálózatot és alhálózatot hozhat létre, és virtuális hálózati átjárót hozhat létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40d85-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="40d85-121">Az átjáró neve "myNGW" lesz a "vnet-gateway" erőforráscsoportban az "UK West" helyen, a korábban létrehozott IP-konfigurációkat az "ngwIPConfig" változóban, az átjáró típusát "VPN", a vpn-típust "RouteBased" és az "Egyszerű" termékváltozatot.</span><span class="sxs-lookup"><span data-stu-id="40d85-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="40d85-122">Emellett felvesz egy külső sugárkiszolgálót is a "TestRadiusServer" címmel.</span><span class="sxs-lookup"><span data-stu-id="40d85-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="40d85-123">Emellett az átjáró ügyfelei által megadott egyéni útvonalakat is be fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="40d85-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="40d85-124">3. példa: Virtuális hálózati átjáró létrehozása P2S-beállításokkal</span><span class="sxs-lookup"><span data-stu-id="40d85-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="40d85-125">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és létrehoz egy virtuális hálózati átjárót P2S-beállításokkal(pl. VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy stb.) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40d85-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="40d85-126">Az átjáró neve "myNGW" lesz a "vnet-gateway" erőforráscsoporton belül az "UK West" helyen, ahol a korábban létrehozott IP-konfigurációkat az "ngwIPConfig" változóba mentette, a "VPN" átjárótípust, a VPN-t a "RouteBased" típust és a "VpnGw1" termékváltozatot.</span><span class="sxs-lookup"><span data-stu-id="40d85-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="40d85-127">A Vpn-beállítások az átjáróban lesznek beállítva, például az Ikev2-ként beállított VpnProtocol, a VpnClientAddressPool mint "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName és custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="40d85-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="40d85-128">Emellett az átjáró ügyfelei által megadott egyéni útvonalakat is be fogja állítani.</span><span class="sxs-lookup"><span data-stu-id="40d85-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="40d85-129">4. példa: Virtuális hálózati átjáró létrehozása AAD-hitelesítési konfigurációval a virtuális hálózati átjáró VpnClient szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="40d85-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="40d85-130">A fentiekkel létrehozhat egy erőforráscsoportot, nyilvános IP-címet kérhet, virtuális hálózatot és alhálózatot hozhat létre, és virtuális hálózati átjárót hozhat létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40d85-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="40d85-131">Az átjáró neve "myNGW" lesz a "vnet-gateway" erőforráscsoportban az "UK West" helyen, a korábban létrehozott IP-konfigurációkat az "ngwIPConfig" változóban, az átjáró típusát "VPN", a vpn-típust "RouteBased" és az "Egyszerű" termékváltozatot.</span><span class="sxs-lookup"><span data-stu-id="40d85-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="40d85-132">Emellett konfigurálja az AAD-hitelesítési konfigurációkat is: AadTenantUri, AadIssuerUri és AadAudienceId a virtuális hálózati átjáró VpnClient szolgáltatásához.</span><span class="sxs-lookup"><span data-stu-id="40d85-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="40d85-133">5. példa: Virtuális hálózati átjáró létrehozása VpnGatewayGenerációval</span><span class="sxs-lookup"><span data-stu-id="40d85-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="40d85-134">A fentiekkel létrehozhat egy erőforráscsoportot, nyilvános IP-címet kérhet, virtuális hálózatot és alhálózatot hozhat létre, és virtuális hálózati átjárót hozhat létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40d85-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="40d85-135">Az átjáró neve "myNGW" lesz a "vnet-gateway" erőforráscsoporton belül az "UK West" helyen, ahol a korábban létrehozott IP-konfigurációk az "ngwIPConfig" változóban vannak mentve, a VPN átjárótípus, a vpn típusa "RouteBased", a "VpnGw4" és a VpnGateway Generation2 engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="40d85-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="40d85-136">6. példa: Virtuális hálózati átjáró létrehozása ipConfigurationBgpPeeringAddresses segítségével</span><span class="sxs-lookup"><span data-stu-id="40d85-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="40d85-137">A fentiekkel létrehozhat egy erőforráscsoportot, nyilvános IP-címet kérhet, virtuális hálózatot és alhálózatot hozhat létre, és virtuális hálózati átjárót hozhat létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40d85-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="40d85-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="40d85-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="40d85-139">Az átjáró neve "átjáró1" lesz az "resourcegroup1resourcegroup1" erőforráscsoportban az "UK West" helyen, ahol a korábban létrehozott Bgppeering IP-konfigurációkat a "gw1ipconfBgp1" változóba mentette, a VPN átjárótípusát, az "RouteBased" vpn-típust, a "VpnGw4" és a VpnGateway Generation2 engedélyezett termékváltozatot.</span><span class="sxs-lookup"><span data-stu-id="40d85-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="40d85-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40d85-140">PARAMETERS</span></span>

### <span data-ttu-id="40d85-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="40d85-141">-AadAudienceId</span></span>
<span data-ttu-id="40d85-142">P2S AAD authentication option:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="40d85-142">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="40d85-143">-AadIssuerUri</span></span>
<span data-ttu-id="40d85-144">P2S AAD authentication option:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="40d85-144">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="40d85-145">-AadTenantUri</span></span>
<span data-ttu-id="40d85-146">P2S AAD authentication option:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="40d85-146">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40d85-147">-AsJob</span></span>
<span data-ttu-id="40d85-148">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="40d85-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40d85-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="40d85-149">-Asn</span></span>
<span data-ttu-id="40d85-150">A virtuális hálózati átjáró ASN-ja a VPN-en keresztüli BGP-hez</span><span class="sxs-lookup"><span data-stu-id="40d85-150">The virtual network gateway's ASN for BGP over VPN</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="40d85-151">-CustomRoute</span></span>
<span data-ttu-id="40d85-152">Custom routes AddressPool specified by customer</span><span class="sxs-lookup"><span data-stu-id="40d85-152">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d85-153">-DefaultProfile</span></span>
<span data-ttu-id="40d85-154">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40d85-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d85-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="40d85-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="40d85-156">Flag to enable Active Active feature on virtual network gateway</span><span class="sxs-lookup"><span data-stu-id="40d85-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="40d85-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="40d85-157">-EnableBgp</span></span>
<span data-ttu-id="40d85-158">EnableBgp Flag</span><span class="sxs-lookup"><span data-stu-id="40d85-158">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="40d85-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="40d85-160">Flag to enable private IPAddress on virtual network gateway</span><span class="sxs-lookup"><span data-stu-id="40d85-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="40d85-161">-Force</span><span class="sxs-lookup"><span data-stu-id="40d85-161">-Force</span></span>
<span data-ttu-id="40d85-162">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="40d85-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="40d85-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="40d85-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="40d85-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="40d85-164">GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="40d85-165">-GatewaySku</span></span>
<span data-ttu-id="40d85-166">Az átjáró termékváltozatának rétege</span><span class="sxs-lookup"><span data-stu-id="40d85-166">The Gateway Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="40d85-167">-GatewayType</span></span>
<span data-ttu-id="40d85-168">A virtuális hálózati átjáró típusa: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="40d85-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="40d85-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="40d85-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="40d85-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="40d85-171">-IpConfigurations</span></span>
<span data-ttu-id="40d85-172">A virtuális hálózati átjáró IpConfigurations szolgáltatása.</span><span class="sxs-lookup"><span data-stu-id="40d85-172">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-173">-Location</span><span class="sxs-lookup"><span data-stu-id="40d85-173">-Location</span></span>
<span data-ttu-id="40d85-174">helyére.</span><span class="sxs-lookup"><span data-stu-id="40d85-174">location.</span></span>

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

### <span data-ttu-id="40d85-175">-Name</span><span class="sxs-lookup"><span data-stu-id="40d85-175">-Name</span></span>
<span data-ttu-id="40d85-176">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="40d85-176">The resource name.</span></span>

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

### <span data-ttu-id="40d85-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="40d85-177">-PeerWeight</span></span>
<span data-ttu-id="40d85-178">A BGP-hálózaton keresztül ebből a virtuális hálózati átjáróból megtanult útvonalak súlyozása</span><span class="sxs-lookup"><span data-stu-id="40d85-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-179">-ServerAddress</span><span class="sxs-lookup"><span data-stu-id="40d85-179">-RadiusServerAddress</span></span>
<span data-ttu-id="40d85-180">A P2S külső sugarú kiszolgálójának címe.</span><span class="sxs-lookup"><span data-stu-id="40d85-180">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-181">-Sugárkiszolgáló-lista</span><span class="sxs-lookup"><span data-stu-id="40d85-181">-RadiusServerList</span></span>
<span data-ttu-id="40d85-182">P2S több külső sugárkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="40d85-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-183">-ServerSecret</span><span class="sxs-lookup"><span data-stu-id="40d85-183">-RadiusServerSecret</span></span>
<span data-ttu-id="40d85-184">P2S Külső sugár kiszolgálói titkos.</span><span class="sxs-lookup"><span data-stu-id="40d85-184">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d85-185">-ResourceGroupName</span></span>
<span data-ttu-id="40d85-186">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40d85-186">The resource group name.</span></span>

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

### <span data-ttu-id="40d85-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="40d85-187">-Tag</span></span>
<span data-ttu-id="40d85-188">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="40d85-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="40d85-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="40d85-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="40d85-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="40d85-190">P2S VpnClient AddressPool</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="40d85-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="40d85-192">IPSec-házirendek listája a P2S VPN-ügyféloldali protokollokhoz.</span><span class="sxs-lookup"><span data-stu-id="40d85-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="40d85-193">-VpnClientProtocol</span></span>
<span data-ttu-id="40d85-194">A P2S VPN-ügyfélcsatorna-építési protokollok listája</span><span class="sxs-lookup"><span data-stu-id="40d85-194">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="40d85-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="40d85-196">A visszavonható VpnClientCertificates listája.</span><span class="sxs-lookup"><span data-stu-id="40d85-196">The list of VpnClientCertificates to be revoked.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="40d85-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="40d85-198">A hozzáadható VpnClientRootCertificates listája.</span><span class="sxs-lookup"><span data-stu-id="40d85-198">The list of VpnClientRootCertificates to be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-199">-VpnGatewayGeneráció</span><span class="sxs-lookup"><span data-stu-id="40d85-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="40d85-200">A VirtualNetwork VPN-átjáró generációja.</span><span class="sxs-lookup"><span data-stu-id="40d85-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="40d85-201">Nincsnek kell lennie, ha a GatewayType nem VPN.</span><span class="sxs-lookup"><span data-stu-id="40d85-201">Must be None if GatewayType is not VPN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="40d85-202">-VpnType</span></span>
<span data-ttu-id="40d85-203">A Vpn:PolicyBased/RouteBased típusa</span><span class="sxs-lookup"><span data-stu-id="40d85-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40d85-204">-Confirm</span></span>
<span data-ttu-id="40d85-205">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40d85-205">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d85-206">-WhatIf</span></span>
<span data-ttu-id="40d85-207">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40d85-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d85-208">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40d85-208">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d85-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d85-209">CommonParameters</span></span>
<span data-ttu-id="40d85-210">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d85-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d85-211">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40d85-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d85-212">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40d85-212">INPUTS</span></span>

### <span data-ttu-id="40d85-213">System.String</span><span class="sxs-lookup"><span data-stu-id="40d85-213">System.String</span></span>

### <span data-ttu-id="40d85-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="40d85-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="40d85-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40d85-215">System.Boolean</span></span>

### <span data-ttu-id="40d85-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40d85-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="40d85-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="40d85-217">System.String[]</span></span>

### <span data-ttu-id="40d85-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="40d85-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="40d85-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="40d85-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="40d85-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="40d85-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="40d85-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="40d85-221">System.UInt32</span></span>

### <span data-ttu-id="40d85-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="40d85-222">System.Int32</span></span>

### <span data-ttu-id="40d85-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="40d85-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="40d85-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="40d85-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="40d85-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="40d85-225">System.Security.SecureString</span></span>

## <span data-ttu-id="40d85-226">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40d85-226">OUTPUTS</span></span>

### <span data-ttu-id="40d85-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40d85-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="40d85-228">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40d85-228">NOTES</span></span>

## <span data-ttu-id="40d85-229">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40d85-229">RELATED LINKS</span></span>
