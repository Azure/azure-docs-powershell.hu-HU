---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 3287644b3f953c001490c7be207865a88b000e10
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184082"
---
# <span data-ttu-id="ffdc9-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffdc9-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="ffdc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffdc9-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdc9-103">IP-konfiguráció eltávolítása virtuális hálózati átjáróról</span><span class="sxs-lookup"><span data-stu-id="ffdc9-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="ffdc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffdc9-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffdc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffdc9-105">DESCRIPTION</span></span>
<span data-ttu-id="ffdc9-106">IP-konfiguráció eltávolítása virtuális hálózati átjáróról</span><span class="sxs-lookup"><span data-stu-id="ffdc9-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="ffdc9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ffdc9-107">EXAMPLES</span></span>

### <span data-ttu-id="ffdc9-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="ffdc9-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="ffdc9-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffdc9-109">PARAMETERS</span></span>

### <span data-ttu-id="ffdc9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffdc9-110">-DefaultProfile</span></span>
<span data-ttu-id="ffdc9-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffdc9-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ffdc9-112">-Name</span></span>
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

### <span data-ttu-id="ffdc9-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ffdc9-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="ffdc9-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ffdc9-114">-Confirm</span></span>
<span data-ttu-id="ffdc9-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffdc9-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffdc9-116">-WhatIf</span></span>
<span data-ttu-id="ffdc9-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffdc9-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffdc9-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffdc9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdc9-119">CommonParameters</span></span>
<span data-ttu-id="ffdc9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffdc9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdc9-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffdc9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdc9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffdc9-122">INPUTS</span></span>

### <span data-ttu-id="ffdc9-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ffdc9-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ffdc9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffdc9-124">OUTPUTS</span></span>

### <span data-ttu-id="ffdc9-125">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ffdc9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ffdc9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffdc9-126">NOTES</span></span>

## <span data-ttu-id="ffdc9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffdc9-127">RELATED LINKS</span></span>

[<span data-ttu-id="ffdc9-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffdc9-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="ffdc9-129">Új – AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ffdc9-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
