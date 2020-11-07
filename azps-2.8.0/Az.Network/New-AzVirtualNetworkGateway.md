---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 75857d2c97ace9b06e3f7cdd7f672ac35a6fe34e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837156"
---
# <span data-ttu-id="e4413-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="e4413-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4413-102">SYNOPSIS</span></span>
<span data-ttu-id="e4413-103">Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="e4413-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="e4413-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4413-104">SYNTAX</span></span>

### <span data-ttu-id="e4413-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4413-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4413-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4413-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4413-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4413-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4413-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4413-108">DESCRIPTION</span></span>
<span data-ttu-id="e4413-109">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e4413-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="e4413-110">A **New-AzVirtualNetworkGateway** parancsmag a név, az erőforráscsoport neve, a hely és az IP-konfiguráció alapján hozza létre az átjáró objektumát az Azure-ban, valamint az átjáró típusát és a ha VPN-t, a VPN-típust.</span><span class="sxs-lookup"><span data-stu-id="e4413-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="e4413-111">Azt is megteheti, hogy az átjáró SKU nevet adja.</span><span class="sxs-lookup"><span data-stu-id="e4413-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="e4413-112">Ha ezt az átjárót használják a helyközi kapcsolatokhoz, azt is meg kell jelenítenie a VPN-ügyfél címkészlet címét, amelyből címeket rendelhet a kapcsolódó ügyfelekhez, és az átjáróhoz csatlakozó VPN-ügyfelek hitelesítéséhez használt VPN-ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="e4413-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="e4413-113">Azt is megteheti, hogy más funkciókat is tartalmaz, például a BGP-t és az aktív aktív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e4413-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="e4413-114">Példák</span><span class="sxs-lookup"><span data-stu-id="e4413-114">EXAMPLES</span></span>

### <span data-ttu-id="e4413-115">1: virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="e4413-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="e4413-116">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e4413-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="e4413-117">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="e4413-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="e4413-118">2: virtuális hálózati átjáró létrehozása külső RADIUS-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="e4413-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="e4413-119">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e4413-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="e4413-120">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="e4413-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="e4413-121">Egy külső RADIUS-kiszolgálót is felvesz a "TestRadiusServer" címmel.</span><span class="sxs-lookup"><span data-stu-id="e4413-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="e4413-122">Azt is megadhatja, hogy milyen egyéni útvonalakat ad meg az ügyfelek az átjárón.</span><span class="sxs-lookup"><span data-stu-id="e4413-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="e4413-123">3: virtuális hálózati átjáró létrehozása a P2S beállításokkal</span><span class="sxs-lookup"><span data-stu-id="e4413-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="e4413-124">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre a P2S-beállításokkal (például VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy stb.) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e4413-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="e4413-125">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN" (VPN típusa "RouteBased") és a "VpnGw1" (SKU) "".</span><span class="sxs-lookup"><span data-stu-id="e4413-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="e4413-126">A virtuális magánhálózati beállítások a következő átjárón jelennek meg: Ikev2, VpnClientAddressPool: "201.169.0.0/16", az VpnClientRootCertificate a következőképpen van beállítva: a clientRootCertName és az egyéni virtuális magánhálózati IPSec-házirend a következő objektumra lett átadva: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="e4413-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="e4413-127">Azt is megadhatja, hogy milyen egyéni útvonalakat ad meg az ügyfelek az átjárón.</span><span class="sxs-lookup"><span data-stu-id="e4413-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="e4413-128">4: virtuális hálózati átjáró létrehozása AAD-hitelesítési konfigurációval a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="e4413-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="e4413-129">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e4413-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="e4413-130">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="e4413-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="e4413-131">A AAD hitelesítési konfigurációit is beállítja: AadTenantUri, AadIssuerUri és AadAudienceId a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="e4413-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="e4413-132">5: virtuális hálózati átjáró létrehozása a VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="e4413-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="e4413-133">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e4413-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="e4413-134">Az átjáró a "vnet" nevű erőforráscsoport "myNGW" nevű erőforráscsoporthoz fog szerepelni az "Egyesült Királyság nyugati" helyén, a korábban létrehozott IP-konfigurációknál a "ngwIPConfig" változó "", a "VPN" vagy a "RouteBased" (""), a SKU "VpnGw4" és a VpnGatewayGeneration Generation2 engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e4413-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="e4413-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4413-135">PARAMETERS</span></span>

### <span data-ttu-id="e4413-136">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="e4413-136">-AadAudienceId</span></span>
<span data-ttu-id="e4413-137">P2S AAD hitelesítési beállítás: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="e4413-137">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="e4413-138">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="e4413-138">-AadIssuerUri</span></span>
<span data-ttu-id="e4413-139">P2S AAD hitelesítési beállítás: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="e4413-139">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="e4413-140">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="e4413-140">-AadTenantUri</span></span>
<span data-ttu-id="e4413-141">P2S AAD hitelesítési beállítás: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="e4413-141">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="e4413-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4413-142">-AsJob</span></span>
<span data-ttu-id="e4413-143">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e4413-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4413-144">-ASN</span><span class="sxs-lookup"><span data-stu-id="e4413-144">-Asn</span></span>

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

### <span data-ttu-id="e4413-145">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="e4413-145">-CustomRoute</span></span>
<span data-ttu-id="e4413-146">Az egyéni útvonalak az ügyfél által megadott AddressPool</span><span class="sxs-lookup"><span data-stu-id="e4413-146">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="e4413-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4413-147">-DefaultProfile</span></span>
<span data-ttu-id="e4413-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4413-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4413-149">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="e4413-149">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="e4413-150">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="e4413-150">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="e4413-151">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="e4413-151">-EnableBgp</span></span>

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

### <span data-ttu-id="e4413-152">-Force</span><span class="sxs-lookup"><span data-stu-id="e4413-152">-Force</span></span>
<span data-ttu-id="e4413-153">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e4413-153">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4413-154">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e4413-154">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="e4413-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="e4413-155">-GatewaySku</span></span>

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

### <span data-ttu-id="e4413-156">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="e4413-156">-GatewayType</span></span>

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

### <span data-ttu-id="e4413-157">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="e4413-157">-IpConfigurations</span></span>

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

### <span data-ttu-id="e4413-158">-Hely</span><span class="sxs-lookup"><span data-stu-id="e4413-158">-Location</span></span>

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

### <span data-ttu-id="e4413-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4413-159">-Name</span></span>

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

### <span data-ttu-id="e4413-160">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e4413-160">-PeerWeight</span></span>

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

### <span data-ttu-id="e4413-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="e4413-161">-RadiusServerAddress</span></span>
<span data-ttu-id="e4413-162">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="e4413-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="e4413-163">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="e4413-163">-RadiusServerSecret</span></span>
<span data-ttu-id="e4413-164">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="e4413-164">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="e4413-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4413-165">-ResourceGroupName</span></span>

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

### <span data-ttu-id="e4413-166">-Címke</span><span class="sxs-lookup"><span data-stu-id="e4413-166">-Tag</span></span>
<span data-ttu-id="e4413-167">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e4413-167">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e4413-168">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e4413-168">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e4413-169">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="e4413-169">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="e4413-170">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="e4413-170">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="e4413-171">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="e4413-171">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="e4413-172">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="e4413-172">-VpnClientProtocol</span></span>
<span data-ttu-id="e4413-173">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="e4413-173">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="e4413-174">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="e4413-174">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="e4413-175">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="e4413-175">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="e4413-176">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="e4413-176">-VpnGatewayGeneration</span></span>
<span data-ttu-id="e4413-177">A VirtualNetwork VPN-átjáró generációja.</span><span class="sxs-lookup"><span data-stu-id="e4413-177">The generation for this VirtualNetwork VPN gateway.</span></span> <span data-ttu-id="e4413-178">Csak akkor lehet, ha a GatewayType nem VPN.</span><span class="sxs-lookup"><span data-stu-id="e4413-178">Must be None if GatewayType is not VPN.</span></span> <span data-ttu-id="e4413-179">A beállítás beállítása után ez a tulajdonság nem módosítható az átjáró élettartama alatt.</span><span class="sxs-lookup"><span data-stu-id="e4413-179">Once set, this property cannot be changed over the lifetime of the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, Generation1, Generation2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4413-180">-VpnType</span><span class="sxs-lookup"><span data-stu-id="e4413-180">-VpnType</span></span>

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

### <span data-ttu-id="e4413-181">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4413-181">-Confirm</span></span>
<span data-ttu-id="e4413-182">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4413-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4413-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4413-183">-WhatIf</span></span>
<span data-ttu-id="e4413-184">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4413-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4413-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4413-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4413-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4413-186">CommonParameters</span></span>
<span data-ttu-id="e4413-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4413-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4413-188">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4413-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4413-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4413-189">INPUTS</span></span>

### <span data-ttu-id="e4413-190">System. String</span><span class="sxs-lookup"><span data-stu-id="e4413-190">System.String</span></span>

### <span data-ttu-id="e4413-191">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="e4413-191">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="e4413-192">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4413-192">System.Boolean</span></span>

### <span data-ttu-id="e4413-193">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-193">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="e4413-194">System. string []</span><span class="sxs-lookup"><span data-stu-id="e4413-194">System.String[]</span></span>

### <span data-ttu-id="e4413-195">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="e4413-195">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="e4413-196">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="e4413-196">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="e4413-197">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="e4413-197">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="e4413-198">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="e4413-198">System.UInt32</span></span>

### <span data-ttu-id="e4413-199">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e4413-199">System.Int32</span></span>

### <span data-ttu-id="e4413-200">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4413-200">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e4413-201">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e4413-201">System.Security.SecureString</span></span>

## <span data-ttu-id="e4413-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4413-202">OUTPUTS</span></span>

### <span data-ttu-id="e4413-203">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-203">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e4413-204">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4413-204">NOTES</span></span>

## <span data-ttu-id="e4413-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4413-205">RELATED LINKS</span></span>

[<span data-ttu-id="e4413-206">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-206">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e4413-207">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-207">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e4413-208">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-208">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e4413-209">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-209">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e4413-210">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4413-210">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
