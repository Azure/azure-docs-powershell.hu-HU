---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: e5216d3a5727c32bd5e9f185cd48ace068a890b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010663"
---
# <span data-ttu-id="7a694-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a694-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a694-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a694-102">SYNOPSIS</span></span>
<span data-ttu-id="7a694-103">Virtuális hálózati átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="7a694-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="7a694-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a694-104">SYNTAX</span></span>

### <span data-ttu-id="7a694-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a694-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a694-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a694-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a694-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="7a694-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a694-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a694-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a694-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="7a694-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a694-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a694-110">DESCRIPTION</span></span>
<span data-ttu-id="7a694-111">A **set-AzVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="7a694-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="7a694-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7a694-112">EXAMPLES</span></span>

### <span data-ttu-id="7a694-113">Példa 1: virtuális hálózati átjáró ASN-es frissítése</span><span class="sxs-lookup"><span data-stu-id="7a694-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="7a694-114">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancs $Gateway a második parancsban frissíti a $Gateway változóban tárolt virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="7a694-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="7a694-115">A parancs az ASN-1337 is beállítja.</span><span class="sxs-lookup"><span data-stu-id="7a694-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="7a694-116">2. példa: IPsec-házirend hozzáadása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7a694-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="7a694-117">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és $Gateway a második parancsban tárolja a VPN IPSec-házirend-objektumot meghatározott IPSec-paraméterekként.</span><span class="sxs-lookup"><span data-stu-id="7a694-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="7a694-118">A harmadik parancs az $Gateway változóban tárolt virtuális hálózati átjárót frissíti.</span><span class="sxs-lookup"><span data-stu-id="7a694-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="7a694-119">A parancs a virtuális hálózati átjárón a $vpnclientipsecpolicy objektumban megadott egyéni virtuális magánhálózati IPSec-házirendet is beállítja.</span><span class="sxs-lookup"><span data-stu-id="7a694-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="7a694-120">3. példa: Címkék hozzáadása vagy frissítése meglévő virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7a694-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="7a694-121">Az első parancs egy Gateway01 nevű virtuális hálózati átjárót kap, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban $Gateway tárolja a virtuális hálózati átjáró Gateway01 a @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="7a694-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="7a694-122">4. példa: a AAD hitelesítési konfigurációjának hozzáadása/frissítése egy meglévő virtuális hálózati átjáró VpnClient</span><span class="sxs-lookup"><span data-stu-id="7a694-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="7a694-123">Az első parancs be$Gateway olvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban tárolja a virtuális hálózati átjáró Gateway01 a AAD hitelesítési konfigurációk params: aadTenantUri, aadAudienceId, aadIssuerUri, VpnClient, és.</span><span class="sxs-lookup"><span data-stu-id="7a694-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="7a694-124">A harmadik parancs eltávolítja a AAD-hitelesítés konfigurációját a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="7a694-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="7a694-125">Példa 5: IpConfigurationBgpPeeringAddresses hozzáadása és frissítése meglévő virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7a694-125">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="7a694-126">Az első parancs be$Gateway olvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban tárolja a virtuális hálózati átjáró Gateway01 IpConfiguration-azonosító értékét a változó ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="7a694-126">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="7a694-127">A harmadik parancs a címlistát a addresslist1-ba osztja.</span><span class="sxs-lookup"><span data-stu-id="7a694-127">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="7a694-128">A negyedik parancs létrehozta a PSIpConfigurationBgpPeeringAddress objektumot.</span><span class="sxs-lookup"><span data-stu-id="7a694-128">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="7a694-129">Az ötödik parancs beállítja ezt az új létrehozott PSIpConfigurationBgpPeeringAddress, hogy IpConfigurationBgpPeeringAddresses és frissítse az átjárót.</span><span class="sxs-lookup"><span data-stu-id="7a694-129">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="7a694-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a694-130">PARAMETERS</span></span>

### <span data-ttu-id="7a694-131">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="7a694-131">-AadAudienceId</span></span>
<span data-ttu-id="7a694-132">P2S AAD hitelesítési beállítás: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="7a694-132">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="7a694-133">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="7a694-133">-AadIssuerUri</span></span>
<span data-ttu-id="7a694-134">P2S AAD hitelesítési beállítás: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="7a694-134">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="7a694-135">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="7a694-135">-AadTenantUri</span></span>
<span data-ttu-id="7a694-136">P2S AAD hitelesítési beállítás: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="7a694-136">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="7a694-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a694-137">-AsJob</span></span>
<span data-ttu-id="7a694-138">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7a694-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a694-139">-ASN</span><span class="sxs-lookup"><span data-stu-id="7a694-139">-Asn</span></span>
<span data-ttu-id="7a694-140">A virtuális hálózat átjárójának ASN-je, amelyet az IPsec-alagutakon belül a BGP-munkamenetek beállításához használt.</span><span class="sxs-lookup"><span data-stu-id="7a694-140">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="7a694-141">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="7a694-141">-CustomRoute</span></span>
<span data-ttu-id="7a694-142">Az egyéni útvonalak az ügyfél által megadott AddressPool</span><span class="sxs-lookup"><span data-stu-id="7a694-142">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="7a694-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a694-143">-DefaultProfile</span></span>
<span data-ttu-id="7a694-144">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a694-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a694-145">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7a694-145">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="7a694-146">Megjelölés az aktív aktív funkció letiltására a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="7a694-146">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7a694-147">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7a694-147">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="7a694-148">Megjelölés az aktív aktív funkció engedélyezéséhez a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="7a694-148">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7a694-149">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7a694-149">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="7a694-150">Megjelölés az aktív aktív funkció engedélyezéséhez a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="7a694-150">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a694-151">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7a694-151">-GatewayDefaultSite</span></span>
<span data-ttu-id="7a694-152">Az alapértelmezett webhely, amellyel kényszerítheti a bújtatási alagút használatát.</span><span class="sxs-lookup"><span data-stu-id="7a694-152">The default site to use for force tunneling.</span></span>
<span data-ttu-id="7a694-153">Ha meg van adva egy alapértelmezett webhely, az átjáró vnet az összes internetes forgalom az adott webhelyre továbbítódik.</span><span class="sxs-lookup"><span data-stu-id="7a694-153">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="7a694-154">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7a694-154">-GatewaySku</span></span>
<span data-ttu-id="7a694-155">A virtuális hálózati átjáró SKU-je</span><span class="sxs-lookup"><span data-stu-id="7a694-155">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="7a694-156">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7a694-156">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="7a694-157">A virtuális hálózati átjáró bgpsettings BgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7a694-157">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="7a694-158">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="7a694-158">-PeerWeight</span></span>
<span data-ttu-id="7a694-159">A virtuális hálózati átjárótól a BGP-től kapott értékekhez hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="7a694-159">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="7a694-160">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="7a694-160">-RadiusServerAddress</span></span>
<span data-ttu-id="7a694-161">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="7a694-161">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a694-162">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="7a694-162">-RadiusServerSecret</span></span>
<span data-ttu-id="7a694-163">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="7a694-163">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a694-164">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="7a694-164">-RemoveAadAuthentication</span></span>
<span data-ttu-id="7a694-165">Megjelölés a P2S-ügyfél AAD-hitelesítésének eltávolításához a virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="7a694-165">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="7a694-166">-Címke</span><span class="sxs-lookup"><span data-stu-id="7a694-166">-Tag</span></span>
<span data-ttu-id="7a694-167">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="7a694-167">P2S External Radius server address.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a694-168">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a694-168">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7a694-169">A virtuális hálózati átjáró objektum a módosítások kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="7a694-169">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="7a694-170">Ezt az Get-AzVirtualNetworkGateway használatával lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="7a694-170">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a694-171">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="7a694-171">-VpnClientAddressPool</span></span>
<span data-ttu-id="7a694-172">A virtuális magánhálózati ügyfél IP-címeinek kiosztására szolgáló címterület.</span><span class="sxs-lookup"><span data-stu-id="7a694-172">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="7a694-173">Ennek a virtuális hálózatnak vagy a helyszíni tartományoknak nem szabad átfedésben lennie.</span><span class="sxs-lookup"><span data-stu-id="7a694-173">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="7a694-174">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7a694-174">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="7a694-175">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="7a694-175">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="7a694-176">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7a694-176">-VpnClientProtocol</span></span>
<span data-ttu-id="7a694-177">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="7a694-177">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="7a694-178">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="7a694-178">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="7a694-179">A visszavont VPN-ügyfél tanúsítványainak listája.</span><span class="sxs-lookup"><span data-stu-id="7a694-179">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="7a694-180">A VPN-ügyfél egy olyan tanúsítványt jelenít meg, amely megfelel a fentieknek.</span><span class="sxs-lookup"><span data-stu-id="7a694-180">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="7a694-181">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="7a694-181">-VpnClientRootCertificates</span></span>
<span data-ttu-id="7a694-182">A VPN-ügyfél-hitelesítéshez használni kívánt virtuális magánhálózati tanúsítványok listája.</span><span class="sxs-lookup"><span data-stu-id="7a694-182">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="7a694-183">A VPN-ügyfeleknek való csatlakozáskor az ilyen főtanúsítványokból származó tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="7a694-183">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="7a694-184">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a694-184">-Confirm</span></span>
<span data-ttu-id="7a694-185">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a694-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a694-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a694-186">-WhatIf</span></span>
<span data-ttu-id="7a694-187">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a694-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a694-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a694-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a694-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a694-189">CommonParameters</span></span>
<span data-ttu-id="7a694-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a694-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a694-191">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7a694-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a694-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a694-192">INPUTS</span></span>

### <span data-ttu-id="7a694-193">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a694-193">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7a694-194">System. String</span><span class="sxs-lookup"><span data-stu-id="7a694-194">System.String</span></span>

### <span data-ttu-id="7a694-195">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a694-195">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="7a694-196">System. string []</span><span class="sxs-lookup"><span data-stu-id="7a694-196">System.String[]</span></span>

### <span data-ttu-id="7a694-197">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="7a694-197">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="7a694-198">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="7a694-198">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="7a694-199">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="7a694-199">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7a694-200">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="7a694-200">System.UInt32</span></span>

### <span data-ttu-id="7a694-201">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7a694-201">System.Int32</span></span>

### <span data-ttu-id="7a694-202">Microsoft. Azure. commands. Network. models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="7a694-202">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="7a694-203">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7a694-203">System.Security.SecureString</span></span>

## <span data-ttu-id="7a694-204">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a694-204">OUTPUTS</span></span>

### <span data-ttu-id="7a694-205">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a694-205">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a694-206">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a694-206">NOTES</span></span>

## <span data-ttu-id="7a694-207">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a694-207">RELATED LINKS</span></span>
