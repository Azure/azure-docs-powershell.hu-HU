---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9b8ee02cbe28784ff1fd5789881dd62add62d674
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670261"
---
# <span data-ttu-id="62f85-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="62f85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62f85-102">SYNOPSIS</span></span>
<span data-ttu-id="62f85-103">Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="62f85-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="62f85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62f85-104">SYNTAX</span></span>

### <span data-ttu-id="62f85-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62f85-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62f85-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="62f85-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62f85-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="62f85-107">DESCRIPTION</span></span>
<span data-ttu-id="62f85-108">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="62f85-108">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="62f85-109">A **New-AzVirtualNetworkGateway** parancsmag a név, az erőforráscsoport neve, a hely és az IP-konfiguráció alapján hozza létre az átjáró objektumát az Azure-ban, valamint az átjáró típusát és a ha VPN-t, a VPN-típust.</span><span class="sxs-lookup"><span data-stu-id="62f85-109">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="62f85-110">Azt is megteheti, hogy az átjáró SKU nevet adja.</span><span class="sxs-lookup"><span data-stu-id="62f85-110">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="62f85-111">Ha ezt az átjárót használják a helyközi kapcsolatokhoz, azt is meg kell jelenítenie a VPN-ügyfél címkészlet címét, amelyből címeket rendelhet a kapcsolódó ügyfelekhez, és az átjáróhoz csatlakozó VPN-ügyfelek hitelesítéséhez használt VPN-ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="62f85-111">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="62f85-112">Azt is megteheti, hogy más funkciókat is tartalmaz, például a BGP-t és az aktív aktív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="62f85-112">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="62f85-113">Példák</span><span class="sxs-lookup"><span data-stu-id="62f85-113">EXAMPLES</span></span>

### <span data-ttu-id="62f85-114">1: virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="62f85-114">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="62f85-115">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="62f85-115">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="62f85-116">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="62f85-116">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="62f85-117">2: virtuális hálózati átjáró létrehozása külső RADIUS-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="62f85-117">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="62f85-118">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="62f85-118">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="62f85-119">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="62f85-119">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="62f85-120">Egy külső RADIUS-kiszolgálót is felvesz a "TestRadiusServer" címmel.</span><span class="sxs-lookup"><span data-stu-id="62f85-120">It also adds an external radius server with address "TestRadiusServer"</span></span>

### <span data-ttu-id="62f85-121">1: virtuális hálózati átjáró létrehozása a P2S beállításokkal</span><span class="sxs-lookup"><span data-stu-id="62f85-121">1: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="62f85-122">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre a P2S-beállításokkal (például VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy stb.) az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="62f85-122">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="62f85-123">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN" (VPN típusa "RouteBased") és a "VpnGw1" (SKU) "".</span><span class="sxs-lookup"><span data-stu-id="62f85-123">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="62f85-124">A virtuális magánhálózati beállítások a következő átjárón jelennek meg: Ikev2, VpnClientAddressPool: "201.169.0.0/16", az VpnClientRootCertificate a következőképpen van beállítva: a clientRootCertName és az egyéni virtuális magánhálózati IPSec-házirend a következő objektumra lett átadva: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="62f85-124">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  

## <span data-ttu-id="62f85-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62f85-125">PARAMETERS</span></span>

### <span data-ttu-id="62f85-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62f85-126">-AsJob</span></span>
<span data-ttu-id="62f85-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="62f85-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62f85-128">-ASN</span><span class="sxs-lookup"><span data-stu-id="62f85-128">-Asn</span></span>

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

### <span data-ttu-id="62f85-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f85-129">-DefaultProfile</span></span>
<span data-ttu-id="62f85-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62f85-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62f85-131">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="62f85-131">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="62f85-132">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="62f85-132">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="62f85-133">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="62f85-133">-EnableBgp</span></span>

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

### <span data-ttu-id="62f85-134">-Force</span><span class="sxs-lookup"><span data-stu-id="62f85-134">-Force</span></span>
<span data-ttu-id="62f85-135">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="62f85-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62f85-136">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="62f85-136">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="62f85-137">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="62f85-137">-GatewaySku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f85-138">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="62f85-138">-GatewayType</span></span>

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

### <span data-ttu-id="62f85-139">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="62f85-139">-IpConfigurations</span></span>

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

### <span data-ttu-id="62f85-140">-Hely</span><span class="sxs-lookup"><span data-stu-id="62f85-140">-Location</span></span>

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

### <span data-ttu-id="62f85-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62f85-141">-Name</span></span>

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

### <span data-ttu-id="62f85-142">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="62f85-142">-PeerWeight</span></span>

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

### <span data-ttu-id="62f85-143">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="62f85-143">-RadiusServerAddress</span></span>
<span data-ttu-id="62f85-144">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="62f85-144">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="62f85-145">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="62f85-145">-RadiusServerSecret</span></span>
<span data-ttu-id="62f85-146">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="62f85-146">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="62f85-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f85-147">-ResourceGroupName</span></span>

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

### <span data-ttu-id="62f85-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="62f85-148">-Tag</span></span>
<span data-ttu-id="62f85-149">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="62f85-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="62f85-150">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="62f85-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="62f85-151">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="62f85-151">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="62f85-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="62f85-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="62f85-153">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="62f85-153">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="62f85-154">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="62f85-154">-VpnClientProtocol</span></span>
<span data-ttu-id="62f85-155">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="62f85-155">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="62f85-156">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="62f85-156">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="62f85-157">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="62f85-157">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="62f85-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="62f85-158">-VpnType</span></span>

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

### <span data-ttu-id="62f85-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62f85-159">-Confirm</span></span>
<span data-ttu-id="62f85-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62f85-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62f85-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f85-161">-WhatIf</span></span>
<span data-ttu-id="62f85-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62f85-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f85-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62f85-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62f85-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f85-164">CommonParameters</span></span>
<span data-ttu-id="62f85-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62f85-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f85-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f85-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f85-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62f85-167">INPUTS</span></span>

### <span data-ttu-id="62f85-168">System. String</span><span class="sxs-lookup"><span data-stu-id="62f85-168">System.String</span></span>

### <span data-ttu-id="62f85-169">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="62f85-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="62f85-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62f85-170">System.Boolean</span></span>

### <span data-ttu-id="62f85-171">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-171">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="62f85-172">System. string []</span><span class="sxs-lookup"><span data-stu-id="62f85-172">System.String[]</span></span>

### <span data-ttu-id="62f85-173">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="62f85-173">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="62f85-174">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="62f85-174">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="62f85-175">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="62f85-175">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="62f85-176">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="62f85-176">System.UInt32</span></span>

### <span data-ttu-id="62f85-177">System. Int32</span><span class="sxs-lookup"><span data-stu-id="62f85-177">System.Int32</span></span>

### <span data-ttu-id="62f85-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62f85-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="62f85-179">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="62f85-179">System.Security.SecureString</span></span>

## <span data-ttu-id="62f85-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62f85-180">OUTPUTS</span></span>

### <span data-ttu-id="62f85-181">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="62f85-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62f85-182">NOTES</span></span>

## <span data-ttu-id="62f85-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62f85-183">RELATED LINKS</span></span>

[<span data-ttu-id="62f85-184">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-184">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="62f85-185">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-185">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="62f85-186">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-186">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="62f85-187">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-187">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="62f85-188">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="62f85-188">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
