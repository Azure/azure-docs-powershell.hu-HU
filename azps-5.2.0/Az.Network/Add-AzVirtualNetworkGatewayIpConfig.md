---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359685"
---
# <span data-ttu-id="bbd30-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd30-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="bbd30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd30-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd30-103">IP-konfigurációt ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bbd30-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="bbd30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bbd30-104">SYNTAX</span></span>

### <span data-ttu-id="bbd30-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbd30-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbd30-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bbd30-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd30-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bbd30-107">DESCRIPTION</span></span>
<span data-ttu-id="bbd30-108">Az **Add-AzVirtualNetworkGatewayIpConfig** parancsmag IP-konfigurációt ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bbd30-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="bbd30-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bbd30-109">EXAMPLES</span></span>

### <span data-ttu-id="bbd30-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bbd30-110">Example 1</span></span>
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

## <span data-ttu-id="bbd30-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd30-111">PARAMETERS</span></span>

### <span data-ttu-id="bbd30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd30-112">-DefaultProfile</span></span>
<span data-ttu-id="bbd30-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbd30-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbd30-114">-Name</span><span class="sxs-lookup"><span data-stu-id="bbd30-114">-Name</span></span>
<span data-ttu-id="bbd30-115">A hozzáadni szükséges átjáró IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbd30-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="bbd30-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbd30-116">-PrivateIpAddress</span></span>
<span data-ttu-id="bbd30-117">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbd30-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="bbd30-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bbd30-118">-PublicIpAddress</span></span>
<span data-ttu-id="bbd30-119">A nyilvános IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbd30-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="bbd30-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bbd30-120">-PublicIpAddressId</span></span>
<span data-ttu-id="bbd30-121">A nyilvános IP-cím azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bbd30-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="bbd30-122">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="bbd30-122">-Subnet</span></span>
<span data-ttu-id="bbd30-123">EGY **PSSubnet-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="bbd30-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="bbd30-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bbd30-124">-SubnetId</span></span>
<span data-ttu-id="bbd30-125">Az alhálózat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbd30-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="bbd30-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bbd30-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bbd30-127">Egy **PSVirtualNetworkGateway-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="bbd30-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="bbd30-128">Ez a parancsmag módosítja a **megadott PSVirtualNetworkGateway** objektumot.</span><span class="sxs-lookup"><span data-stu-id="bbd30-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="bbd30-129">A Get-AzVirtualNetworkGateway használatával lekérhet egy **PSVirtualNetworkGateway-objektumot.**</span><span class="sxs-lookup"><span data-stu-id="bbd30-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="bbd30-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbd30-130">-Confirm</span></span>
<span data-ttu-id="bbd30-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bbd30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd30-132">-WhatIf</span></span>
<span data-ttu-id="bbd30-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bbd30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd30-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbd30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd30-135">CommonParameters</span></span>
<span data-ttu-id="bbd30-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd30-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd30-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd30-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbd30-138">INPUTS</span></span>

### <span data-ttu-id="bbd30-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bbd30-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bbd30-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbd30-140">OUTPUTS</span></span>

### <span data-ttu-id="bbd30-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bbd30-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bbd30-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bbd30-142">NOTES</span></span>

## <span data-ttu-id="bbd30-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbd30-143">RELATED LINKS</span></span>

[<span data-ttu-id="bbd30-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bbd30-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="bbd30-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd30-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="bbd30-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd30-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
