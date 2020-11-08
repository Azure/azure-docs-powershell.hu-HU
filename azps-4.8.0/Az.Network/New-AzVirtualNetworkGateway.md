---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184354"
---
# <span data-ttu-id="4d347-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4d347-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="4d347-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d347-102">SYNOPSIS</span></span>
<span data-ttu-id="4d347-103">Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d347-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="4d347-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d347-104">SYNTAX</span></span>

### <span data-ttu-id="4d347-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d347-105">Default (Default)</span></span>
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

### <span data-ttu-id="4d347-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d347-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="4d347-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d347-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="4d347-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d347-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="4d347-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d347-109">DESCRIPTION</span></span>
<span data-ttu-id="4d347-110">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4d347-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="4d347-111">A **New-AzVirtualNetworkGateway** parancsmag a név, az erőforráscsoport neve, a hely és az IP-konfiguráció alapján hozza létre az átjáró objektumát az Azure-ban, valamint az átjáró típusát és a ha VPN-t, a VPN-típust.</span><span class="sxs-lookup"><span data-stu-id="4d347-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="4d347-112">Azt is megteheti, hogy az átjáró SKU nevet adja.</span><span class="sxs-lookup"><span data-stu-id="4d347-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="4d347-113">Ha ezt az átjárót használják a helyközi kapcsolatokhoz, azt is meg kell jelenítenie a VPN-ügyfél címkészlet címét, amelyből címeket rendelhet a kapcsolódó ügyfelekhez, és az átjáróhoz csatlakozó VPN-ügyfelek hitelesítéséhez használt VPN-ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="4d347-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="4d347-114">Azt is megteheti, hogy más funkciókat is tartalmaz, például a BGP-t és az aktív aktív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="4d347-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="4d347-115">Példák</span><span class="sxs-lookup"><span data-stu-id="4d347-115">EXAMPLES</span></span>

### <span data-ttu-id="4d347-116">Példa 1: virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="4d347-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="4d347-117">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4d347-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="4d347-118">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="4d347-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="4d347-119">2. példa: virtuális hálózati átjáró létrehozása külső RADIUS-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="4d347-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="4d347-120">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4d347-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="4d347-121">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="4d347-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="4d347-122">Egy külső RADIUS-kiszolgálót is felvesz a "TestRadiusServer" címmel.</span><span class="sxs-lookup"><span data-stu-id="4d347-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="4d347-123">Azt is megadhatja, hogy milyen egyéni útvonalakat ad meg az ügyfelek az átjárón.</span><span class="sxs-lookup"><span data-stu-id="4d347-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="4d347-124">3. példa: virtuális hálózati átjáró létrehozása P2S beállításokkal</span><span class="sxs-lookup"><span data-stu-id="4d347-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="4d347-125">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre a P2S-beállításokkal (például VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy stb.) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4d347-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="4d347-126">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN" (VPN típusa "RouteBased") és a "VpnGw1" (SKU) "".</span><span class="sxs-lookup"><span data-stu-id="4d347-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="4d347-127">A virtuális magánhálózati beállítások a következő átjárón jelennek meg: Ikev2, VpnClientAddressPool: "201.169.0.0/16", az VpnClientRootCertificate a következőképpen van beállítva: a clientRootCertName és az egyéni virtuális magánhálózati IPSec-házirend a következő objektumra lett átadva: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="4d347-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="4d347-128">Azt is megadhatja, hogy milyen egyéni útvonalakat ad meg az ügyfelek az átjárón.</span><span class="sxs-lookup"><span data-stu-id="4d347-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="4d347-129">Példa 4: virtuális hálózati átjáró létrehozása AAD-hitelesítési konfigurációval a VpnClient virtuális hálózati átjárójában.</span><span class="sxs-lookup"><span data-stu-id="4d347-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="4d347-130">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4d347-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="4d347-131">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="4d347-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="4d347-132">A AAD hitelesítési konfigurációit is beállítja: AadTenantUri, AadIssuerUri és AadAudienceId a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="4d347-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="4d347-133">Példa 5: virtuális hálózati átjáró létrehozása a VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="4d347-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="4d347-134">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4d347-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="4d347-135">Az átjáró a "vnet" nevű erőforráscsoport "myNGW" nevű erőforráscsoporthoz fog szerepelni az "Egyesült Királyság nyugati" helyén, a korábban létrehozott IP-konfigurációknál a "ngwIPConfig" változó "", a "VPN" vagy a "RouteBased" (""), a SKU "VpnGw4" és a VpnGatewayGeneration Generation2 engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4d347-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="4d347-136">6. példa: virtuális hálózati átjáró létrehozása a IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="4d347-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="4d347-137">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="4d347-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="4d347-138">a ngwipconfig-ban létrehozott és mentett ipconfigurationId1 ipconfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d347-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="4d347-139">Az átjáró neve "gateway1" lesz az "resourcegroup1resourcegroup1" erőforráscsoport "" nevű erőforráscsoporthoz az "Egyesült Királyság nyugati részén", a korábban létrehozott IP-konfigurációk Bgppeering a "gw1ipconfBgp1" változó "", a "VPN" vagy a "RouteBased" VPN-típus "VpnGw4", a SKU "VpnGatewayGeneration" és a Generation2 engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4d347-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="4d347-140">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d347-140">PARAMETERS</span></span>

### <span data-ttu-id="4d347-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="4d347-141">-AadAudienceId</span></span>
<span data-ttu-id="4d347-142">P2S AAD hitelesítési beállítás: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="4d347-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="4d347-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="4d347-143">-AadIssuerUri</span></span>
<span data-ttu-id="4d347-144">P2S AAD hitelesítési beállítás: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="4d347-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="4d347-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="4d347-145">-AadTenantUri</span></span>
<span data-ttu-id="4d347-146">P2S AAD hitelesítési beállítás: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="4d347-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="4d347-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d347-147">-AsJob</span></span>
<span data-ttu-id="4d347-148">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4d347-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d347-149">-ASN</span><span class="sxs-lookup"><span data-stu-id="4d347-149">-Asn</span></span>
<span data-ttu-id="4d347-150">A virtuális hálózat átjárójának ASN a BGP-en keresztüli virtuális magánhálózaton</span><span class="sxs-lookup"><span data-stu-id="4d347-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="4d347-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="4d347-151">-CustomRoute</span></span>
<span data-ttu-id="4d347-152">Az egyéni útvonalak az ügyfél által megadott AddressPool</span><span class="sxs-lookup"><span data-stu-id="4d347-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="4d347-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d347-153">-DefaultProfile</span></span>
<span data-ttu-id="4d347-154">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d347-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d347-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="4d347-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="4d347-156">Megjelölés az aktív aktív funkció engedélyezéséhez a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="4d347-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="4d347-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="4d347-157">-EnableBgp</span></span>
<span data-ttu-id="4d347-158">EnableBgp jelölő</span><span class="sxs-lookup"><span data-stu-id="4d347-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="4d347-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d347-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="4d347-160">Megjelölés a magánhálózati IP-elérés engedélyezésére a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="4d347-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="4d347-161">-Force</span><span class="sxs-lookup"><span data-stu-id="4d347-161">-Force</span></span>
<span data-ttu-id="4d347-162">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d347-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4d347-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="4d347-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="4d347-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="4d347-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="4d347-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="4d347-165">-GatewaySku</span></span>
<span data-ttu-id="4d347-166">Az átjáró SKU-rétege</span><span class="sxs-lookup"><span data-stu-id="4d347-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="4d347-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="4d347-167">-GatewayType</span></span>
<span data-ttu-id="4d347-168">A virtuális hálózati átjáró típusa: VPN, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4d347-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="4d347-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="4d347-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="4d347-170">A virtuális hálózati átjáró bgpsettings BgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="4d347-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="4d347-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="4d347-171">-IpConfigurations</span></span>
<span data-ttu-id="4d347-172">A virtuális hálózati átjáró IpConfigurations.</span><span class="sxs-lookup"><span data-stu-id="4d347-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="4d347-173">-Hely</span><span class="sxs-lookup"><span data-stu-id="4d347-173">-Location</span></span>
<span data-ttu-id="4d347-174">helyre.</span><span class="sxs-lookup"><span data-stu-id="4d347-174">location.</span></span>

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

### <span data-ttu-id="4d347-175">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d347-175">-Name</span></span>
<span data-ttu-id="4d347-176">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4d347-176">The resource name.</span></span>

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

### <span data-ttu-id="4d347-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="4d347-177">-PeerWeight</span></span>
<span data-ttu-id="4d347-178">A virtuális hálózati átjárótól a BGP-től kapott értékekhez hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="4d347-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="4d347-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="4d347-179">-RadiusServerAddress</span></span>
<span data-ttu-id="4d347-180">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="4d347-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="4d347-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="4d347-181">-RadiusServerList</span></span>
<span data-ttu-id="4d347-182">P2S több külső RADIUS-kiszolgáló esetén.</span><span class="sxs-lookup"><span data-stu-id="4d347-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="4d347-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="4d347-183">-RadiusServerSecret</span></span>
<span data-ttu-id="4d347-184">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="4d347-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="4d347-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d347-185">-ResourceGroupName</span></span>
<span data-ttu-id="4d347-186">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d347-186">The resource group name.</span></span>

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

### <span data-ttu-id="4d347-187">-Címke</span><span class="sxs-lookup"><span data-stu-id="4d347-187">-Tag</span></span>
<span data-ttu-id="4d347-188">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4d347-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4d347-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d347-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="4d347-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="4d347-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="4d347-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="4d347-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="4d347-192">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="4d347-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="4d347-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="4d347-193">-VpnClientProtocol</span></span>
<span data-ttu-id="4d347-194">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="4d347-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="4d347-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="4d347-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="4d347-196">A visszavonni kívánt VpnClientCertificates listája.</span><span class="sxs-lookup"><span data-stu-id="4d347-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="4d347-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="4d347-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="4d347-198">A felvenni kívánt VpnClientRootCertificates listája.</span><span class="sxs-lookup"><span data-stu-id="4d347-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="4d347-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="4d347-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="4d347-200">A VirtualNetwork VPN-átjáró generációja.</span><span class="sxs-lookup"><span data-stu-id="4d347-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="4d347-201">Csak akkor lehet, ha a GatewayType nem VPN.</span><span class="sxs-lookup"><span data-stu-id="4d347-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="4d347-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="4d347-202">-VpnType</span></span>
<span data-ttu-id="4d347-203">A virtuális magánhálózat típusa: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="4d347-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="4d347-204">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d347-204">-Confirm</span></span>
<span data-ttu-id="4d347-205">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d347-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d347-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d347-206">-WhatIf</span></span>
<span data-ttu-id="4d347-207">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d347-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d347-208">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d347-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d347-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d347-209">CommonParameters</span></span>
<span data-ttu-id="4d347-210">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d347-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d347-211">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d347-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d347-212">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d347-212">INPUTS</span></span>

### <span data-ttu-id="4d347-213">System. String</span><span class="sxs-lookup"><span data-stu-id="4d347-213">System.String</span></span>

### <span data-ttu-id="4d347-214">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4d347-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="4d347-215">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d347-215">System.Boolean</span></span>

### <span data-ttu-id="4d347-216">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4d347-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="4d347-217">System. string []</span><span class="sxs-lookup"><span data-stu-id="4d347-217">System.String[]</span></span>

### <span data-ttu-id="4d347-218">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="4d347-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="4d347-219">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="4d347-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="4d347-220">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="4d347-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="4d347-221">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="4d347-221">System.UInt32</span></span>

### <span data-ttu-id="4d347-222">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4d347-222">System.Int32</span></span>

### <span data-ttu-id="4d347-223">Microsoft. Azure. commands. Network. models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="4d347-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="4d347-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4d347-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4d347-225">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="4d347-225">System.Security.SecureString</span></span>

## <span data-ttu-id="4d347-226">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d347-226">OUTPUTS</span></span>

### <span data-ttu-id="4d347-227">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4d347-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4d347-228">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d347-228">NOTES</span></span>

## <span data-ttu-id="4d347-229">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d347-229">RELATED LINKS</span></span>
