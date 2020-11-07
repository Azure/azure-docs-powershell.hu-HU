---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838313"
---
# <span data-ttu-id="36374-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="36374-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36374-102">SYNOPSIS</span></span>
<span data-ttu-id="36374-103">Virtuális hálózati átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="36374-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="36374-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36374-104">SYNTAX</span></span>

### <span data-ttu-id="36374-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36374-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36374-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="36374-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36374-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="36374-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36374-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="36374-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36374-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="36374-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36374-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="36374-110">DESCRIPTION</span></span>
<span data-ttu-id="36374-111">A **set-AzVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="36374-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="36374-112">Példák</span><span class="sxs-lookup"><span data-stu-id="36374-112">EXAMPLES</span></span>

### <span data-ttu-id="36374-113">Példa 1: virtuális hálózati átjáró ASN-es frissítése</span><span class="sxs-lookup"><span data-stu-id="36374-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="36374-114">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancs $Gateway a második parancsban frissíti a $Gateway változóban tárolt virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="36374-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="36374-115">A parancs az ASN-1337 is beállítja.</span><span class="sxs-lookup"><span data-stu-id="36374-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="36374-116">2. példa: IPsec-házirend hozzáadása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="36374-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="36374-117">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és $Gateway a második parancsban tárolja a VPN IPSec-házirend-objektumot meghatározott IPSec-paraméterekként.</span><span class="sxs-lookup"><span data-stu-id="36374-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="36374-118">A harmadik parancs az $Gateway változóban tárolt virtuális hálózati átjárót frissíti.</span><span class="sxs-lookup"><span data-stu-id="36374-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="36374-119">A parancs a virtuális hálózati átjárón a $vpnclientipsecpolicy objektumban megadott egyéni virtuális magánhálózati IPSec-házirendet is beállítja.</span><span class="sxs-lookup"><span data-stu-id="36374-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="36374-120">3. példa: Címkék hozzáadása vagy frissítése meglévő virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="36374-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="36374-121">Az első parancs egy Gateway01 nevű virtuális hálózati átjárót kap, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban $Gateway tárolja a virtuális hálózati átjáró Gateway01 a @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="36374-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="36374-122">4. példa: a AAD hitelesítési konfigurációjának hozzáadása/frissítése egy meglévő virtuális hálózati átjáró VpnClient</span><span class="sxs-lookup"><span data-stu-id="36374-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="36374-123">Az első parancs be$Gateway olvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancsban tárolja a virtuális hálózati átjáró Gateway01 a AAD hitelesítési konfigurációk params: aadTenantUri, aadAudienceId, aadIssuerUri, VpnClient, és.</span><span class="sxs-lookup"><span data-stu-id="36374-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="36374-124">A harmadik parancs eltávolítja a AAD-hitelesítés konfigurációját a virtuális hálózati átjáró VpnClient.</span><span class="sxs-lookup"><span data-stu-id="36374-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="36374-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36374-125">PARAMETERS</span></span>

### <span data-ttu-id="36374-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="36374-126">-AadAudienceId</span></span>
<span data-ttu-id="36374-127">P2S AAD hitelesítési beállítás: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="36374-127">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="36374-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="36374-128">-AadIssuerUri</span></span>
<span data-ttu-id="36374-129">P2S AAD hitelesítési beállítás: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="36374-129">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="36374-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="36374-130">-AadTenantUri</span></span>
<span data-ttu-id="36374-131">P2S AAD hitelesítési beállítás: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="36374-131">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="36374-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36374-132">-AsJob</span></span>
<span data-ttu-id="36374-133">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="36374-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36374-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="36374-134">-Asn</span></span>
<span data-ttu-id="36374-135">Annak a virtuális hálózati átjárónak az autonóm rendszerszámát adja meg, amely az IPsec-alagutakban a Border Gateway Protocol (BGP) munkamenetek beállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="36374-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="36374-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="36374-136">-CustomRoute</span></span>
<span data-ttu-id="36374-137">Az egyéni útvonalak az ügyfél által megadott AddressPool</span><span class="sxs-lookup"><span data-stu-id="36374-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="36374-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36374-138">-DefaultProfile</span></span>
<span data-ttu-id="36374-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36374-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36374-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="36374-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="36374-141">Letiltja az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="36374-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="36374-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="36374-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="36374-143">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="36374-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="36374-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="36374-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="36374-145">Itt adhatja meg, hogy milyen alapértelmezett webhely legyen használható a kényszerítő bújtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="36374-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="36374-146">Ha meg van adva egy alapértelmezett webhely, az átjáró virtuális magánhálózat (VPN) minden internetes forgalmát átirányítja az adott webhelyre.</span><span class="sxs-lookup"><span data-stu-id="36374-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="36374-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="36374-147">-GatewaySku</span></span>
<span data-ttu-id="36374-148">A virtuális hálózati átjáró készlet-megőrzési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36374-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="36374-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="36374-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36374-150">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="36374-150">Basic</span></span>
- <span data-ttu-id="36374-151">Standard</span><span class="sxs-lookup"><span data-stu-id="36374-151">Standard</span></span>
- <span data-ttu-id="36374-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="36374-152">HighPerformance</span></span>
- <span data-ttu-id="36374-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="36374-153">VpnGw1</span></span>
- <span data-ttu-id="36374-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="36374-154">VpnGw2</span></span>
- <span data-ttu-id="36374-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="36374-155">VpnGw3</span></span>
- <span data-ttu-id="36374-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="36374-156">VpnGw1AZ</span></span>
- <span data-ttu-id="36374-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="36374-157">VpnGw2AZ</span></span>
- <span data-ttu-id="36374-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="36374-158">VpnGw3AZ</span></span>
- <span data-ttu-id="36374-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="36374-159">ErGw1AZ</span></span>
- <span data-ttu-id="36374-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="36374-160">ErGw2AZ</span></span>
- <span data-ttu-id="36374-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="36374-161">ErGw3AZ</span></span>

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

### <span data-ttu-id="36374-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="36374-162">-PeerWeight</span></span>
<span data-ttu-id="36374-163">Itt adhatja meg, hogy a virtuális hálózati átjárótól kapott, a BGP-ról származó összes útvonalhoz hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="36374-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="36374-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="36374-164">-RadiusServerAddress</span></span>
<span data-ttu-id="36374-165">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="36374-165">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="36374-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="36374-166">-RadiusServerSecret</span></span>
<span data-ttu-id="36374-167">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="36374-167">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="36374-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="36374-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="36374-169">Megjelölés a P2S-ügyfél AAD-hitelesítésének eltávolításához a virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="36374-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="36374-170">-Címke</span><span class="sxs-lookup"><span data-stu-id="36374-170">-Tag</span></span>
<span data-ttu-id="36374-171">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="36374-171">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="36374-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="36374-173">Annak a virtuális hálózati átjáró objektumnak a meghatározása, amelynek alapján a módosítások le vannak kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="36374-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="36374-174">A virtuális hálózati átjáró objektum beszerzéséhez használhatja az Get-AzVirtualNetworkGateway parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="36374-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="36374-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="36374-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="36374-176">Azt a Címterület-címet adja meg, amelyre a parancsmag a VPN-ügyfél IP-címeinek hozzárendelését használja.</span><span class="sxs-lookup"><span data-stu-id="36374-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="36374-177">Ennek a virtuális hálózatnak vagy a helyszíni tartományoknak nem szabad átfedésben lennie.</span><span class="sxs-lookup"><span data-stu-id="36374-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="36374-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="36374-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="36374-179">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="36374-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="36374-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="36374-180">-VpnClientProtocol</span></span>
<span data-ttu-id="36374-181">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="36374-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="36374-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="36374-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="36374-183">A visszavont VPN-ügyfél tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="36374-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="36374-184">A VPN-ügyfél egy olyan tanúsítványt ad, amely megfelel az egyik ilyen elemnek.</span><span class="sxs-lookup"><span data-stu-id="36374-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="36374-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="36374-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="36374-186">A virtuális magánhálózati ügyfél-hitelesítéshez használni kívánt virtuális magánhálózati tanúsítványok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="36374-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="36374-187">A VPN-ügyfeleknek való csatlakozáskor az ilyen főtanúsítványokból származó tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="36374-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="36374-188">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36374-188">-Confirm</span></span>
<span data-ttu-id="36374-189">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36374-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36374-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36374-190">-WhatIf</span></span>
<span data-ttu-id="36374-191">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36374-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36374-192">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36374-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36374-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36374-193">CommonParameters</span></span>
<span data-ttu-id="36374-194">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36374-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36374-195">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36374-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36374-196">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36374-196">INPUTS</span></span>

### <span data-ttu-id="36374-197">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="36374-198">System. String</span><span class="sxs-lookup"><span data-stu-id="36374-198">System.String</span></span>

### <span data-ttu-id="36374-199">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="36374-200">System. string []</span><span class="sxs-lookup"><span data-stu-id="36374-200">System.String[]</span></span>

### <span data-ttu-id="36374-201">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="36374-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="36374-202">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="36374-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="36374-203">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="36374-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="36374-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="36374-204">System.UInt32</span></span>

### <span data-ttu-id="36374-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="36374-205">System.Int32</span></span>

### <span data-ttu-id="36374-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="36374-206">System.Security.SecureString</span></span>

## <span data-ttu-id="36374-207">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36374-207">OUTPUTS</span></span>

### <span data-ttu-id="36374-208">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="36374-209">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36374-209">NOTES</span></span>
* <span data-ttu-id="36374-210">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="36374-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="36374-211">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36374-211">RELATED LINKS</span></span>

[<span data-ttu-id="36374-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="36374-213">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="36374-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="36374-215">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="36374-216">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36374-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
