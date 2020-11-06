---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 6f0a18211ae7c9d2fe8ffcb9c653de9952691e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501472"
---
# <span data-ttu-id="2ea8a-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ea8a-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="2ea8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ea8a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea8a-103">Virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ea8a-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ea8a-104">SYNTAX</span></span>

### <span data-ttu-id="2ea8a-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ea8a-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea8a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ea8a-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ea8a-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2ea8a-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea8a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ea8a-108">DESCRIPTION</span></span>
<span data-ttu-id="2ea8a-109">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="2ea8a-110">A **New-AzureRmVirtualNetworkGateway** parancsmag a név, az erőforráscsoport neve, a hely és az IP-konfiguráció alapján hozza létre az átjáró objektumát az Azure-ban, valamint az átjáró típusát és a ha VPN-t, a VPN-típust.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="2ea8a-111">Azt is megteheti, hogy az átjáró SKU nevet adja.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="2ea8a-112">Ha ezt az átjárót használják a helyközi kapcsolatokhoz, azt is meg kell jelenítenie a VPN-ügyfél címkészlet címét, amelyből címeket rendelhet a kapcsolódó ügyfelekhez, és az átjáróhoz csatlakozó VPN-ügyfelek hitelesítéséhez használt VPN-ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="2ea8a-113">Azt is megteheti, hogy más funkciókat is tartalmaz, például a BGP-t és az aktív aktív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="2ea8a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="2ea8a-114">EXAMPLES</span></span>

### <span data-ttu-id="2ea8a-115">1: virtuális hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ea8a-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="2ea8a-116">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="2ea8a-117">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="2ea8a-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="2ea8a-118">2: virtuális hálózati átjáró létrehozása külső RADIUS-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="2ea8a-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="2ea8a-119">A fenti létrehoz egy erőforráscsoportot, nyilvános IP-címet kér, virtuális hálózatot és alhálózatot hoz létre, és virtuális hálózati átjárót hoz létre az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="2ea8a-120">Az átjáró neve "myNGW", az "vnet-átjáró" nevű erőforráscsoport "UK West" ("az Egyesült Királyság nyugati része"), az "ngwIPConfig" változóban a "", a "VPN", a "RouteBased" és a SKU "Basic" (VPN) típus "".</span><span class="sxs-lookup"><span data-stu-id="2ea8a-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="2ea8a-121">Egy külső RADIUS-kiszolgálót is felvesz a "TestRadiusServer" címmel.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="2ea8a-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ea8a-122">PARAMETERS</span></span>

### <span data-ttu-id="2ea8a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ea8a-123">-AsJob</span></span>
<span data-ttu-id="2ea8a-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2ea8a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ea8a-125">-ASN</span><span class="sxs-lookup"><span data-stu-id="2ea8a-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea8a-126">-DefaultProfile</span></span>
<span data-ttu-id="2ea8a-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="2ea8a-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="2ea8a-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="2ea8a-129">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-129">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="2ea8a-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2ea8a-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-131">-Force</span><span class="sxs-lookup"><span data-stu-id="2ea8a-131">-Force</span></span>
<span data-ttu-id="2ea8a-132">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ea8a-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="2ea8a-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="2ea8a-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-135">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="2ea8a-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="2ea8a-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="2ea8a-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ea8a-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2ea8a-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2ea8a-140">-RadiusServerAddress</span></span>
<span data-ttu-id="2ea8a-141">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="2ea8a-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2ea8a-142">-RadiusServerSecret</span></span>
<span data-ttu-id="2ea8a-143">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea8a-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="2ea8a-145">-Tag</span></span>
<span data-ttu-id="2ea8a-146">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ea8a-147">Példa:</span><span class="sxs-lookup"><span data-stu-id="2ea8a-147">For example:</span></span>

<span data-ttu-id="2ea8a-148">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="2ea8a-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2ea8a-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="2ea8a-149">-VpnClientAddressPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="2ea8a-150">-VpnClientProtocol</span></span>
<span data-ttu-id="2ea8a-151">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="2ea8a-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="2ea8a-152">-VpnClientRevokedCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="2ea8a-153">-VpnClientRootCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2ea8a-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea8a-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ea8a-155">-Confirm</span></span>
<span data-ttu-id="2ea8a-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea8a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea8a-157">-WhatIf</span></span>
<span data-ttu-id="2ea8a-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea8a-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea8a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea8a-160">CommonParameters</span></span>
<span data-ttu-id="2ea8a-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ea8a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea8a-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea8a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea8a-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ea8a-163">INPUTS</span></span>

### <span data-ttu-id="2ea8a-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ea8a-164">None</span></span>
<span data-ttu-id="2ea8a-165">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2ea8a-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ea8a-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ea8a-166">OUTPUTS</span></span>

### <span data-ttu-id="2ea8a-167">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ea8a-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2ea8a-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ea8a-168">NOTES</span></span>

## <span data-ttu-id="2ea8a-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ea8a-169">RELATED LINKS</span></span>

[<span data-ttu-id="2ea8a-170">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ea8a-170">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2ea8a-171">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ea8a-171">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2ea8a-172">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ea8a-172">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2ea8a-173">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ea8a-173">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2ea8a-174">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ea8a-174">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
