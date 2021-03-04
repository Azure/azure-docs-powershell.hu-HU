---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 17d9e024d13db1871bfab3b5b7230391fe22d192
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938009"
---
# <span data-ttu-id="ed1c6-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed1c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1c6-103">Frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="ed1c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed1c6-104">SYNTAX</span></span>

### <span data-ttu-id="ed1c6-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed1c6-105">Default (Default)</span></span>
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

### <span data-ttu-id="ed1c6-106">ServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed1c6-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="ed1c6-107">ServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="ed1c6-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
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

### <span data-ttu-id="ed1c6-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed1c6-108">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="ed1c6-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed1c6-109">AadAuthenticationConfiguration</span></span>
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

### <span data-ttu-id="ed1c6-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="ed1c6-110">UpdateResourceWithTags</span></span>
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

## <span data-ttu-id="ed1c6-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed1c6-111">DESCRIPTION</span></span>
<span data-ttu-id="ed1c6-112">A **Set-AzVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="ed1c6-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed1c6-113">EXAMPLES</span></span>

### <span data-ttu-id="ed1c6-114">1. példa: Virtuális hálózati átjáró ASN-ének frissítése</span><span class="sxs-lookup"><span data-stu-id="ed1c6-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="ed1c6-115">Az első parancs egy Átjáró01 nevű virtuális hálózati átjárót kap, amely az ResourceGroup001 erőforráscsoporthoz tartozik, és az $Gateway A második parancs frissíti a változóban tárolt virtuális hálózati átjárót $Gateway.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="ed1c6-116">A parancs az ASN-t is 1337-re állítja.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="ed1c6-117">2. példa: IPsec-házirend hozzáadása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="ed1c6-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="ed1c6-118">Az első parancs egy Átjáró01 nevű virtuális hálózati átjárót kap, amely az ResourceGroup001 erőforráscsoporthoz tartozik, és az $Gateway A második parancs a Megadott ipsec-paramétereknek megfelelő Vpn ipsec házirendobjektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="ed1c6-119">A harmadik parancs frissíti a változó típusú $Gateway.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="ed1c6-120">A parancs a virtuális hálózat átjáró $vpnclientipsecpolicy objektumában megadott egyéni vpn ipsec házirendet is beállítja.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="ed1c6-121">3. példa: Címkék hozzáadása/frissítése meglévő virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="ed1c6-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="ed1c6-122">Az első parancs egy Átjáró01 nevű virtuális hálózati átjárót kap, amely az ResourceGroup001 erőforráscsoporthoz tartozik, és az $Gateway A második parancs frissíti az Átjáró01 virtuális hálózati átjárót a @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" } címkével.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="ed1c6-123">4. példa: AAD-hitelesítési konfiguráció hozzáadása/frissítése meglévő virtuális hálózati átjáró VpnClient-éhez</span><span class="sxs-lookup"><span data-stu-id="ed1c6-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="ed1c6-124">Az első parancs egy Átjáró01 nevű virtuális hálózati átjárót kap, amely az ResourceGroup001 erőforráscsoporthoz tartozik, és a $Gateway A második parancs frissíti az Átjáró01 virtuális hálózati átjárót az AAD-hitelesítési konfigurációval: paraméter:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="ed1c6-125">A harmadik parancs eltávolítja az AAD-hitelesítési konfigurációt a virtuális hálózati átjáró VpnClient szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="ed1c6-126">5. példa: IpConfigurationBgpPeeringAddresses hozzáadása/frissítése meglévő virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="ed1c6-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
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

<span data-ttu-id="ed1c6-127">Az első parancs egy Átjáró01 nevű virtuális hálózati átjárót kap, amely az ResourceGroup001 erőforráscsoporthoz tartozik, és az $Gateway A második parancs a virtuális hálózati átjáró átjárójának értékét (Gateway01 IpConfiguration Id) változó ipconfigurationId1 változóhoz rendeli hozzá.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="ed1c6-128">A harmadik parancs hozzárendeli a címlistát a címlistához1.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="ed1c6-129">A negyedik parancs létrehozott egy PSIpConfigurationBgpPeeringAddress objektumot.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="ed1c6-130">Az ötödik parancs ezt az új PSIpConfigurationBgpPeeringAddress címet IpConfigurationBgpPeeringAddresses-re állítsa be, és frissítse az átjárót.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="ed1c6-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed1c6-131">PARAMETERS</span></span>

### <span data-ttu-id="ed1c6-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="ed1c6-132">-AadAudienceId</span></span>
<span data-ttu-id="ed1c6-133">P2S AAD authentication option:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="ed1c6-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="ed1c6-134">-AadIssuerUri</span></span>
<span data-ttu-id="ed1c6-135">P2S AAD authentication option:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="ed1c6-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="ed1c6-136">-AadTenantUri</span></span>
<span data-ttu-id="ed1c6-137">P2S AAD authentication option:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="ed1c6-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed1c6-138">-AsJob</span></span>
<span data-ttu-id="ed1c6-139">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ed1c6-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed1c6-140">-Asn</span><span class="sxs-lookup"><span data-stu-id="ed1c6-140">-Asn</span></span>
<span data-ttu-id="ed1c6-141">A virtuális hálózati átjáró ASN-je, amely az IPsec-alagutakon belüli BGP-munkamenetek beállításához használatos</span><span class="sxs-lookup"><span data-stu-id="ed1c6-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="ed1c6-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="ed1c6-142">-CustomRoute</span></span>
<span data-ttu-id="ed1c6-143">Custom routes AddressPool specified by customer</span><span class="sxs-lookup"><span data-stu-id="ed1c6-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="ed1c6-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1c6-144">-DefaultProfile</span></span>
<span data-ttu-id="ed1c6-145">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed1c6-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="ed1c6-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="ed1c6-147">Flag to disable Active Active feature on virtual network gateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="ed1c6-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="ed1c6-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="ed1c6-149">Flag to enable Active Active feature on virtual network gateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="ed1c6-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ed1c6-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="ed1c6-151">Flag to enable Active Active feature on virtual network gateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="ed1c6-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="ed1c6-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="ed1c6-153">A kényszerítés kényszerítésére használt alapértelmezett webhely.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="ed1c6-154">Ha meg van adva egy alapértelmezett webhely, az átjáró virtuális hálózatának összes internetes adata arra a webhelyre lesz irányítva.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="ed1c6-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="ed1c6-155">-GatewaySku</span></span>
<span data-ttu-id="ed1c6-156">A virtuális hálózati átjáró termékváltozata</span><span class="sxs-lookup"><span data-stu-id="ed1c6-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="ed1c6-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="ed1c6-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="ed1c6-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="ed1c6-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ed1c6-159">-PeerWeight</span></span>
<span data-ttu-id="ed1c6-160">A BGP-hálózaton keresztül ebből a virtuális hálózati átjáróból megtanult útvonalak súlyozása</span><span class="sxs-lookup"><span data-stu-id="ed1c6-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="ed1c6-161">-ServerAddress</span><span class="sxs-lookup"><span data-stu-id="ed1c6-161">-RadiusServerAddress</span></span>
<span data-ttu-id="ed1c6-162">A P2S külső sugarú kiszolgálójának címe.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="ed1c6-163">-Sugárkiszolgáló-lista</span><span class="sxs-lookup"><span data-stu-id="ed1c6-163">-RadiusServerList</span></span>
<span data-ttu-id="ed1c6-164">P2S több külső Sugárkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="ed1c6-165">-ServerSecret</span><span class="sxs-lookup"><span data-stu-id="ed1c6-165">-RadiusServerSecret</span></span>
<span data-ttu-id="ed1c6-166">P2S Külső sugár kiszolgálói titkos.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="ed1c6-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="ed1c6-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="ed1c6-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="ed1c6-169">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed1c6-169">-Tag</span></span>
<span data-ttu-id="ed1c6-170">A P2S külső sugarú kiszolgálójának címe.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="ed1c6-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ed1c6-172">A virtuális hálózati átjáró objektum, amelyből ki kell alapozni a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="ed1c6-173">Ezt a lekérdezést a Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="ed1c6-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="ed1c6-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="ed1c6-175">A VPN-ügyfél IP-címeinek kiosztható címterülete.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="ed1c6-176">Ez nem lehet átfedésben a virtuális hálózattal vagy a helyi tartományokkal.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="ed1c6-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="ed1c6-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="ed1c6-178">IPSec-házirendek listája a P2S VPN-ügyféloldali protokollokhoz.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="ed1c6-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="ed1c6-179">-VpnClientProtocol</span></span>
<span data-ttu-id="ed1c6-180">A P2S VPN-ügyféloldali alagutassági protokollok listája</span><span class="sxs-lookup"><span data-stu-id="ed1c6-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="ed1c6-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="ed1c6-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="ed1c6-182">A visszavont VPN-ügyféltanúsítványok listája.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="ed1c6-183">Egy ilyen tanúsítványt bemutató VPN-ügyfél azt fogja mondani, hogy el kell mennie.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="ed1c6-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="ed1c6-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="ed1c6-185">A VPN-ügyfélalkalmazások főtanúsítványai, amelyek a VPN-ügyfélhitelesítéshez használhatók.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="ed1c6-186">A virtuális magánhálózati ügyfélnek az ilyen főtanúsítványok egyikében létrehozott tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="ed1c6-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed1c6-187">-Confirm</span></span>
<span data-ttu-id="ed1c6-188">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed1c6-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed1c6-189">-WhatIf</span></span>
<span data-ttu-id="ed1c6-190">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed1c6-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed1c6-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1c6-192">CommonParameters</span></span>
<span data-ttu-id="ed1c6-193">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed1c6-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1c6-194">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed1c6-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1c6-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed1c6-195">INPUTS</span></span>

### <span data-ttu-id="ed1c6-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ed1c6-197">System.String</span><span class="sxs-lookup"><span data-stu-id="ed1c6-197">System.String</span></span>

### <span data-ttu-id="ed1c6-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="ed1c6-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ed1c6-199">System.String[]</span></span>

### <span data-ttu-id="ed1c6-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="ed1c6-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="ed1c6-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="ed1c6-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="ed1c6-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="ed1c6-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="ed1c6-203">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="ed1c6-203">System.UInt32</span></span>

### <span data-ttu-id="ed1c6-204">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ed1c6-204">System.Int32</span></span>

### <span data-ttu-id="ed1c6-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="ed1c6-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="ed1c6-206">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="ed1c6-206">System.Security.SecureString</span></span>

## <span data-ttu-id="ed1c6-207">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed1c6-207">OUTPUTS</span></span>

### <span data-ttu-id="ed1c6-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed1c6-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed1c6-209">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed1c6-209">NOTES</span></span>

## <span data-ttu-id="ed1c6-210">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed1c6-210">RELATED LINKS</span></span>
