---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 3c30f7a341615b7e12843f3cd745cd691fa205aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013233"
---
# <span data-ttu-id="bbb06-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bbb06-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="bbb06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbb06-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb06-103">Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="bbb06-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="bbb06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbb06-104">SYNTAX</span></span>

### <span data-ttu-id="bbb06-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bbb06-105">Default (Default)</span></span>
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

### <span data-ttu-id="bbb06-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbb06-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="bbb06-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbb06-107">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="bbb06-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbb06-108">DESCRIPTION</span></span>
<span data-ttu-id="bbb06-109">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bbb06-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="bbb06-110">A **New-AzVirtualNetworkGateway** parancsmag a név, az erőforráscsoport neve, a hely és az IP-konfiguráció alapján hozza létre az átjáró objektumát az Azure-ban, valamint az átjáró típusát és a ha VPN-t, a VPN-típust.</span><span class="sxs-lookup"><span data-stu-id="bbb06-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="bbb06-111">Azt is megteheti, hogy az átjáró SKU nevet adja.</span><span class="sxs-lookup"><span data-stu-id="bbb06-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="bbb06-112">Ha ezt az átjárót használják a helyközi kapcsolatokhoz, azt is meg kell jelenítenie a VPN-ügyfél címkészlet címét, amelyből címeket rendelhet a kapcsolódó ügyfelekhez, és az átjáróhoz csatlakozó VPN-ügyfelek hitelesítéséhez használt VPN-ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="bbb06-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="bbb06-113">Azt is megteheti, hogy más funkciókat is tartalmaz, például a BGP-t és az aktív aktív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bbb06-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="bbb06-114">Példák</span><span class="sxs-lookup"><span data-stu-id="bbb06-114">EXAMPLES</span></span>

### <span data-ttu-id="bbb06-115">1: virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="bbb06-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="bbb06-116">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bbb06-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="bbb06-117">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="bbb06-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="bbb06-118">2: virtuális hálózati átjáró létrehozása külső RADIUS-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="bbb06-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="bbb06-119">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bbb06-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="bbb06-120">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="bbb06-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="bbb06-121">Egy külső RADIUS-kiszolgálót is felvesz a "TestRadiusServer" címmel.</span><span class="sxs-lookup"><span data-stu-id="bbb06-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="bbb06-122">Azt is megadhatja, hogy milyen egyéni útvonalakat ad meg az ügyfelek az átjárón.</span><span class="sxs-lookup"><span data-stu-id="bbb06-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="bbb06-123">3: virtuális hálózati átjáró létrehozása a P2S beállításokkal</span><span class="sxs-lookup"><span data-stu-id="bbb06-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
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

<span data-ttu-id="bbb06-124">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre a P2S-beállításokkal (például VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy stb.) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bbb06-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="bbb06-125">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN" (VPN típusa "RouteBased") és a "VpnGw1" (SKU) "".</span><span class="sxs-lookup"><span data-stu-id="bbb06-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="bbb06-126">A virtuális magánhálózati beállítások a következő átjárón jelennek meg: Ikev2, VpnClientAddressPool: "201.169.0.0/16", az VpnClientRootCertificate a következőképpen van beállítva: a clientRootCertName és az egyéni virtuális magánhálózati IPSec-házirend a következő objektumra lett átadva: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="bbb06-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="bbb06-127">Azt is megadhatja, hogy milyen egyéni útvonalakat ad meg az ügyfelek az átjárón.</span><span class="sxs-lookup"><span data-stu-id="bbb06-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="bbb06-128">4: virtuális hálózati átjáró létrehozása AAD-hitelesítési konfigurációval a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="bbb06-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="bbb06-129">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bbb06-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="bbb06-130">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="bbb06-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="bbb06-131">A AAD hitelesítési konfigurációit is beállítja: AadTenantUri, AadIssuerUri és AadAudienceId a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="bbb06-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="bbb06-132">5: virtuális hálózati átjáró létrehozása a VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="bbb06-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="bbb06-133">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bbb06-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="bbb06-134">Az átjáró a "vnet" nevű erőforráscsoport "myNGW" nevű erőforráscsoporthoz fog szerepelni az "Egyesült Királyság nyugati" helyén, a korábban létrehozott IP-konfigurációknál a "ngwIPConfig" változó "", a "VPN" vagy a "RouteBased" (""), a SKU "VpnGw4" és a VpnGatewayGeneration Generation2 engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="bbb06-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="bbb06-135">6: virtuális hálózati átjáró létrehozása a IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="bbb06-135">6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```
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

<span data-ttu-id="bbb06-136">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bbb06-136">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="bbb06-137">a ngwipconfig-ban létrehozott és mentett ipconfigurationId1 ipconfiguration.</span><span class="sxs-lookup"><span data-stu-id="bbb06-137">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="bbb06-138">Az átjáró neve "gateway1" lesz az "resourcegroup1resourcegroup1" erőforráscsoport "" nevű erőforráscsoporthoz az "Egyesült Királyság nyugati részén", a korábban létrehozott IP-konfigurációk Bgppeering a "gw1ipconfBgp1" változó "", a "VPN" vagy a "RouteBased" VPN-típus "VpnGw4", a SKU "VpnGatewayGeneration" és a Generation2 engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="bbb06-138">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="bbb06-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbb06-139">PARAMETERS</span></span>

### <span data-ttu-id="bbb06-140">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="bbb06-140">-AadAudienceId</span></span>
<span data-ttu-id="bbb06-141">P2S AAD hitelesítési beállítás: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="bbb06-141">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="bbb06-142">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="bbb06-142">-AadIssuerUri</span></span>
<span data-ttu-id="bbb06-143">P2S AAD hitelesítési beállítás: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="bbb06-143">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="bbb06-144">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="bbb06-144">-AadTenantUri</span></span>
<span data-ttu-id="bbb06-145">P2S AAD hitelesítési beállítás: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="bbb06-145">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="bbb06-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbb06-146">-AsJob</span></span>
<span data-ttu-id="bbb06-147">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bbb06-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbb06-148">-ASN</span><span class="sxs-lookup"><span data-stu-id="bbb06-148">-Asn</span></span>
<span data-ttu-id="bbb06-149">A virtuális hálózat átjárójának ASN a BGP-en keresztüli virtuális magánhálózaton</span><span class="sxs-lookup"><span data-stu-id="bbb06-149">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="bbb06-150">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="bbb06-150">-CustomRoute</span></span>
<span data-ttu-id="bbb06-151">Az egyéni útvonalak az ügyfél által megadott AddressPool</span><span class="sxs-lookup"><span data-stu-id="bbb06-151">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="bbb06-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb06-152">-DefaultProfile</span></span>
<span data-ttu-id="bbb06-153">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbb06-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbb06-154">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bbb06-154">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="bbb06-155">Megjelölés az aktív aktív funkció engedélyezéséhez a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="bbb06-155">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="bbb06-156">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="bbb06-156">-EnableBgp</span></span>
<span data-ttu-id="bbb06-157">EnableBgp jelölő</span><span class="sxs-lookup"><span data-stu-id="bbb06-157">EnableBgp Flag</span></span>

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

### <span data-ttu-id="bbb06-158">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbb06-158">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="bbb06-159">Megjelölés a magánhálózati IP-elérés engedélyezésére a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="bbb06-159">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="bbb06-160">-Force</span><span class="sxs-lookup"><span data-stu-id="bbb06-160">-Force</span></span>
<span data-ttu-id="bbb06-161">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbb06-161">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bbb06-162">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bbb06-162">-GatewayDefaultSite</span></span>
<span data-ttu-id="bbb06-163">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bbb06-163">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="bbb06-164">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="bbb06-164">-GatewaySku</span></span>
<span data-ttu-id="bbb06-165">Az átjáró SKU-rétege</span><span class="sxs-lookup"><span data-stu-id="bbb06-165">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="bbb06-166">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="bbb06-166">-GatewayType</span></span>
<span data-ttu-id="bbb06-167">A virtuális hálózati átjáró típusa: VPN, ExoressRoute</span><span class="sxs-lookup"><span data-stu-id="bbb06-167">The type of this virtual network gateway: Vpn, ExoressRoute</span></span>

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

### <span data-ttu-id="bbb06-168">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="bbb06-168">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="bbb06-169">A virtuális hálózati átjáró bgpsettings BgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="bbb06-169">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="bbb06-170">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="bbb06-170">-IpConfigurations</span></span>
<span data-ttu-id="bbb06-171">A virtuális hálózati átjáró IpConfigurations.</span><span class="sxs-lookup"><span data-stu-id="bbb06-171">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="bbb06-172">-Hely</span><span class="sxs-lookup"><span data-stu-id="bbb06-172">-Location</span></span>
<span data-ttu-id="bbb06-173">helyre.</span><span class="sxs-lookup"><span data-stu-id="bbb06-173">location.</span></span>

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

### <span data-ttu-id="bbb06-174">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bbb06-174">-Name</span></span>
<span data-ttu-id="bbb06-175">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bbb06-175">The resource name.</span></span>

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

### <span data-ttu-id="bbb06-176">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="bbb06-176">-PeerWeight</span></span>
<span data-ttu-id="bbb06-177">A virtuális hálózati átjárótól a BGP-től kapott értékekhez hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="bbb06-177">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="bbb06-178">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="bbb06-178">-RadiusServerAddress</span></span>
<span data-ttu-id="bbb06-179">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="bbb06-179">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="bbb06-180">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="bbb06-180">-RadiusServerSecret</span></span>
<span data-ttu-id="bbb06-181">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="bbb06-181">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="bbb06-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb06-182">-ResourceGroupName</span></span>
<span data-ttu-id="bbb06-183">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bbb06-183">The resource group name.</span></span>

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

### <span data-ttu-id="bbb06-184">-Címke</span><span class="sxs-lookup"><span data-stu-id="bbb06-184">-Tag</span></span>
<span data-ttu-id="bbb06-185">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bbb06-185">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bbb06-186">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbb06-186">-VpnClientAddressPool</span></span>
<span data-ttu-id="bbb06-187">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="bbb06-187">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="bbb06-188">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bbb06-188">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="bbb06-189">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="bbb06-189">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="bbb06-190">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="bbb06-190">-VpnClientProtocol</span></span>
<span data-ttu-id="bbb06-191">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="bbb06-191">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="bbb06-192">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="bbb06-192">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="bbb06-193">A visszavonni kívánt VpnClientCertificates listája.</span><span class="sxs-lookup"><span data-stu-id="bbb06-193">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="bbb06-194">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="bbb06-194">-VpnClientRootCertificates</span></span>
<span data-ttu-id="bbb06-195">A felvenni kívánt VpnClientRootCertificates listája.</span><span class="sxs-lookup"><span data-stu-id="bbb06-195">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="bbb06-196">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="bbb06-196">-VpnGatewayGeneration</span></span>
<span data-ttu-id="bbb06-197">A VirtualNetwork VPN-átjáró generációja.</span><span class="sxs-lookup"><span data-stu-id="bbb06-197">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="bbb06-198">Csak akkor lehet, ha a GatewayType nem VPN.</span><span class="sxs-lookup"><span data-stu-id="bbb06-198">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="bbb06-199">-VpnType</span><span class="sxs-lookup"><span data-stu-id="bbb06-199">-VpnType</span></span>
<span data-ttu-id="bbb06-200">A virtuális magánhálózat típusa: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="bbb06-200">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="bbb06-201">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbb06-201">-Confirm</span></span>
<span data-ttu-id="bbb06-202">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbb06-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb06-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb06-203">-WhatIf</span></span>
<span data-ttu-id="bbb06-204">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbb06-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb06-205">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbb06-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb06-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb06-206">CommonParameters</span></span>
<span data-ttu-id="bbb06-207">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbb06-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb06-208">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bbb06-208">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb06-209">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbb06-209">INPUTS</span></span>

### <span data-ttu-id="bbb06-210">System. String</span><span class="sxs-lookup"><span data-stu-id="bbb06-210">System.String</span></span>

### <span data-ttu-id="bbb06-211">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="bbb06-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="bbb06-212">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbb06-212">System.Boolean</span></span>

### <span data-ttu-id="bbb06-213">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bbb06-213">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="bbb06-214">System. string []</span><span class="sxs-lookup"><span data-stu-id="bbb06-214">System.String[]</span></span>

### <span data-ttu-id="bbb06-215">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="bbb06-215">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="bbb06-216">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="bbb06-216">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="bbb06-217">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="bbb06-217">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="bbb06-218">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="bbb06-218">System.UInt32</span></span>

### <span data-ttu-id="bbb06-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bbb06-219">System.Int32</span></span>

### <span data-ttu-id="bbb06-220">Microsoft. Azure. commands. Network. models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="bbb06-220">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="bbb06-221">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bbb06-221">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bbb06-222">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bbb06-222">System.Security.SecureString</span></span>

## <span data-ttu-id="bbb06-223">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbb06-223">OUTPUTS</span></span>

### <span data-ttu-id="bbb06-224">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bbb06-224">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bbb06-225">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbb06-225">NOTES</span></span>

## <span data-ttu-id="bbb06-226">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbb06-226">RELATED LINKS</span></span>
