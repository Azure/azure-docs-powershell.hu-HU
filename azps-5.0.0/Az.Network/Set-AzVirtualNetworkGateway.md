---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303116"
---
# <span data-ttu-id="7c2ab-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7c2ab-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7c2ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c2ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2ab-103">Virtuális hálózati átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="7c2ab-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="7c2ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c2ab-104">SYNTAX</span></span>

### <span data-ttu-id="7c2ab-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c2ab-105">Default (Default)</span></span>
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

### <span data-ttu-id="7c2ab-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c2ab-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="7c2ab-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="7c2ab-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
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

### <span data-ttu-id="7c2ab-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c2ab-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2ab-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c2ab-109">AadAuthenticationConfiguration</span></span>
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

### <span data-ttu-id="7c2ab-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="7c2ab-110">UpdateResourceWithTags</span></span>
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

## <span data-ttu-id="7c2ab-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c2ab-111">DESCRIPTION</span></span>
<span data-ttu-id="7c2ab-112">A **set-AzVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="7c2ab-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7c2ab-113">EXAMPLES</span></span>

### <span data-ttu-id="7c2ab-114">Példa 1: virtuális hálózati átjáró ASN-es frissítése</span><span class="sxs-lookup"><span data-stu-id="7c2ab-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="7c2ab-115">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancs $Gateway a második parancsban frissíti a $Gateway változóban tárolt virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="7c2ab-116">A parancs az ASN-1337 is beállítja.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="7c2ab-117">2. példa: IPsec-házirend hozzáadása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7c2ab-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="7c2ab-118">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és $Gateway a második parancsban tárolja a VPN IPSec-házirend-objektumot meghatározott IPSec-paraméterekként.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="7c2ab-119">A harmadik parancs az $Gateway változóban tárolt virtuális hálózati átjárót frissíti.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="7c2ab-120">A parancs a virtuális hálózati átjárón a $vpnclientipsecpolicy objektumban megadott egyéni virtuális magánhálózati IPSec-házirendet is beállítja.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="7c2ab-121">3. példa: Címkék hozzáadása vagy frissítése meglévő virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7c2ab-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="7c2ab-122">Az első parancs egy Gateway01 nevű virtuális hálózati átjárót kap, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban $Gateway tárolja a virtuális hálózati átjáró Gateway01 a @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="7c2ab-123">4. példa: a AAD hitelesítési konfigurációjának hozzáadása/frissítése egy meglévő virtuális hálózati átjáró VpnClient</span><span class="sxs-lookup"><span data-stu-id="7c2ab-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="7c2ab-124">Az első parancs be$Gateway olvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban tárolja a virtuális hálózati átjáró Gateway01 a AAD hitelesítési konfigurációk params: aadTenantUri, aadAudienceId, aadIssuerUri, VpnClient, és.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="7c2ab-125">A harmadik parancs eltávolítja a AAD-hitelesítés konfigurációját a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="7c2ab-126">Példa 5: IpConfigurationBgpPeeringAddresses hozzáadása és frissítése meglévő virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7c2ab-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
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

<span data-ttu-id="7c2ab-127">Az első parancs be$Gateway olvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban tárolja a virtuális hálózati átjáró Gateway01 IpConfiguration-azonosító értékét a változó ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="7c2ab-128">A harmadik parancs a címlistát a addresslist1-ba osztja.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="7c2ab-129">A negyedik parancs létrehozta a PSIpConfigurationBgpPeeringAddress objektumot.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="7c2ab-130">Az ötödik parancs beállítja ezt az új létrehozott PSIpConfigurationBgpPeeringAddress, hogy IpConfigurationBgpPeeringAddresses és frissítse az átjárót.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="7c2ab-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c2ab-131">PARAMETERS</span></span>

### <span data-ttu-id="7c2ab-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="7c2ab-132">-AadAudienceId</span></span>
<span data-ttu-id="7c2ab-133">P2S AAD hitelesítési beállítás: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="7c2ab-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="7c2ab-134">-AadIssuerUri</span></span>
<span data-ttu-id="7c2ab-135">P2S AAD hitelesítési beállítás: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="7c2ab-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="7c2ab-136">-AadTenantUri</span></span>
<span data-ttu-id="7c2ab-137">P2S AAD hitelesítési beállítás: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="7c2ab-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c2ab-138">-AsJob</span></span>
<span data-ttu-id="7c2ab-139">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7c2ab-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c2ab-140">-ASN</span><span class="sxs-lookup"><span data-stu-id="7c2ab-140">-Asn</span></span>
<span data-ttu-id="7c2ab-141">A virtuális hálózat átjárójának ASN-je, amelyet az IPsec-alagutakon belül a BGP-munkamenetek beállításához használt.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="7c2ab-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="7c2ab-142">-CustomRoute</span></span>
<span data-ttu-id="7c2ab-143">Az egyéni útvonalak az ügyfél által megadott AddressPool</span><span class="sxs-lookup"><span data-stu-id="7c2ab-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="7c2ab-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2ab-144">-DefaultProfile</span></span>
<span data-ttu-id="7c2ab-145">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c2ab-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7c2ab-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="7c2ab-147">Megjelölés az aktív aktív funkció letiltására a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="7c2ab-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7c2ab-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7c2ab-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="7c2ab-149">Megjelölés az aktív aktív funkció engedélyezéséhez a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="7c2ab-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7c2ab-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7c2ab-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="7c2ab-151">Megjelölés az aktív aktív funkció engedélyezéséhez a virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="7c2ab-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7c2ab-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7c2ab-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="7c2ab-153">Az alapértelmezett webhely, amellyel kényszerítheti a bújtatási alagút használatát.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="7c2ab-154">Ha meg van adva egy alapértelmezett webhely, az átjáró vnet az összes internetes forgalom az adott webhelyre továbbítódik.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="7c2ab-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7c2ab-155">-GatewaySku</span></span>
<span data-ttu-id="7c2ab-156">A virtuális hálózati átjáró SKU-je</span><span class="sxs-lookup"><span data-stu-id="7c2ab-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="7c2ab-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7c2ab-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="7c2ab-158">A virtuális hálózati átjáró bgpsettings BgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7c2ab-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="7c2ab-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="7c2ab-159">-PeerWeight</span></span>
<span data-ttu-id="7c2ab-160">A virtuális hálózati átjárótól a BGP-től kapott értékekhez hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="7c2ab-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="7c2ab-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="7c2ab-161">-RadiusServerAddress</span></span>
<span data-ttu-id="7c2ab-162">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="7c2ab-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="7c2ab-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="7c2ab-163">-RadiusServerList</span></span>
<span data-ttu-id="7c2ab-164">P2S több külső RADIUS-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="7c2ab-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="7c2ab-165">-RadiusServerSecret</span></span>
<span data-ttu-id="7c2ab-166">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="7c2ab-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="7c2ab-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="7c2ab-168">Megjelölés a P2S-ügyfél AAD-hitelesítésének eltávolításához a virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="7c2ab-169">-Címke</span><span class="sxs-lookup"><span data-stu-id="7c2ab-169">-Tag</span></span>
<span data-ttu-id="7c2ab-170">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="7c2ab-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="7c2ab-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7c2ab-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7c2ab-172">A virtuális hálózati átjáró objektum a módosítások kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="7c2ab-173">Ezt az Get-AzVirtualNetworkGateway használatával lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="7c2ab-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c2ab-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="7c2ab-175">A virtuális magánhálózati ügyfél IP-címeinek kiosztására szolgáló címterület.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="7c2ab-176">Ennek a virtuális hálózatnak vagy a helyszíni tartományoknak nem szabad átfedésben lennie.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="7c2ab-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7c2ab-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="7c2ab-178">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="7c2ab-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7c2ab-179">-VpnClientProtocol</span></span>
<span data-ttu-id="7c2ab-180">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="7c2ab-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="7c2ab-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="7c2ab-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="7c2ab-182">A visszavont VPN-ügyfél tanúsítványainak listája.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="7c2ab-183">A VPN-ügyfél egy olyan tanúsítványt jelenít meg, amely megfelel a fentieknek.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="7c2ab-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="7c2ab-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="7c2ab-185">A VPN-ügyfél-hitelesítéshez használni kívánt virtuális magánhálózati tanúsítványok listája.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="7c2ab-186">A VPN-ügyfeleknek való csatlakozáskor az ilyen főtanúsítványokból származó tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="7c2ab-187">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c2ab-187">-Confirm</span></span>
<span data-ttu-id="7c2ab-188">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2ab-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2ab-189">-WhatIf</span></span>
<span data-ttu-id="7c2ab-190">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c2ab-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2ab-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2ab-192">CommonParameters</span></span>
<span data-ttu-id="7c2ab-193">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c2ab-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2ab-194">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c2ab-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2ab-195">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c2ab-195">INPUTS</span></span>

### <span data-ttu-id="7c2ab-196">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7c2ab-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7c2ab-197">System. String</span><span class="sxs-lookup"><span data-stu-id="7c2ab-197">System.String</span></span>

### <span data-ttu-id="7c2ab-198">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7c2ab-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="7c2ab-199">System. string []</span><span class="sxs-lookup"><span data-stu-id="7c2ab-199">System.String[]</span></span>

### <span data-ttu-id="7c2ab-200">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="7c2ab-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="7c2ab-201">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="7c2ab-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="7c2ab-202">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="7c2ab-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7c2ab-203">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="7c2ab-203">System.UInt32</span></span>

### <span data-ttu-id="7c2ab-204">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7c2ab-204">System.Int32</span></span>

### <span data-ttu-id="7c2ab-205">Microsoft. Azure. commands. Network. models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="7c2ab-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="7c2ab-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7c2ab-206">System.Security.SecureString</span></span>

## <span data-ttu-id="7c2ab-207">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c2ab-207">OUTPUTS</span></span>

### <span data-ttu-id="7c2ab-208">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7c2ab-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7c2ab-209">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c2ab-209">NOTES</span></span>

## <span data-ttu-id="7c2ab-210">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c2ab-210">RELATED LINKS</span></span>
