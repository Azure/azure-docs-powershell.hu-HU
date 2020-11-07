---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: a0369a598cd7a3a0fa4044a267568260fbfda86c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837653"
---
# <span data-ttu-id="b1fb3-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1fb3-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="b1fb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fb3-103">IP-konfigurációt ad hozzá egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="b1fb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1fb3-104">SYNTAX</span></span>

### <span data-ttu-id="b1fb3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1fb3-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1fb3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b1fb3-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1fb3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1fb3-107">DESCRIPTION</span></span>
<span data-ttu-id="b1fb3-108">Az **Add-AzVirtualNetworkGatewayIpConfig** parancsmag IP-konfigurációt ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="b1fb3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b1fb3-109">EXAMPLES</span></span>

### <span data-ttu-id="b1fb3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b1fb3-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="b1fb3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1fb3-111">PARAMETERS</span></span>

### <span data-ttu-id="b1fb3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fb3-112">-DefaultProfile</span></span>
<span data-ttu-id="b1fb3-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1fb3-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1fb3-114">-Name</span></span>
<span data-ttu-id="b1fb3-115">A hozzáadni kívánt átjáró IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fb3-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b1fb3-116">-PrivateIpAddress</span></span>
<span data-ttu-id="b1fb3-117">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="b1fb3-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b1fb3-118">-PublicIpAddress</span></span>
<span data-ttu-id="b1fb3-119">Adja meg a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fb3-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b1fb3-120">-PublicIpAddressId</span></span>
<span data-ttu-id="b1fb3-121">A nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fb3-122">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="b1fb3-122">-Subnet</span></span>
<span data-ttu-id="b1fb3-123">Egy **PSSubnet** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fb3-124">– NetI</span><span class="sxs-lookup"><span data-stu-id="b1fb3-124">-SubnetId</span></span>
<span data-ttu-id="b1fb3-125">Az alhálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fb3-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1fb3-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b1fb3-127">Egy **PSVirtualNetworkGateway** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="b1fb3-128">Ez a parancsmag módosítja a megadott **PSVirtualNetworkGateway** objektumot.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="b1fb3-129">A **PSVirtualNetworkGateway** -objektumok a Get-AzVirtualNetworkGateway parancsmag használatával is beolvashatók.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="b1fb3-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b1fb3-130">-Confirm</span></span>
<span data-ttu-id="b1fb3-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fb3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fb3-132">-WhatIf</span></span>
<span data-ttu-id="b1fb3-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1fb3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1fb3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fb3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fb3-135">CommonParameters</span></span>
<span data-ttu-id="b1fb3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1fb3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fb3-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fb3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fb3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1fb3-138">INPUTS</span></span>

### <span data-ttu-id="b1fb3-139">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1fb3-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b1fb3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1fb3-140">OUTPUTS</span></span>

### <span data-ttu-id="b1fb3-141">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1fb3-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b1fb3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1fb3-142">NOTES</span></span>

## <span data-ttu-id="b1fb3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1fb3-143">RELATED LINKS</span></span>

[<span data-ttu-id="b1fb3-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1fb3-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b1fb3-145">Új – AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1fb3-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="b1fb3-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1fb3-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
