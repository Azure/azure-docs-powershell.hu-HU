---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 3287644b3f953c001490c7be207865a88b000e10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013973"
---
# <span data-ttu-id="cafdb-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="cafdb-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="cafdb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cafdb-102">SYNOPSIS</span></span>
<span data-ttu-id="cafdb-103">IP-konfiguráció eltávolítása virtuális hálózati átjáróról</span><span class="sxs-lookup"><span data-stu-id="cafdb-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="cafdb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cafdb-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cafdb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cafdb-105">DESCRIPTION</span></span>
<span data-ttu-id="cafdb-106">IP-konfiguráció eltávolítása virtuális hálózati átjáróról</span><span class="sxs-lookup"><span data-stu-id="cafdb-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="cafdb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cafdb-107">EXAMPLES</span></span>

### <span data-ttu-id="cafdb-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="cafdb-108">Example 1:</span></span>
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

## <span data-ttu-id="cafdb-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cafdb-109">PARAMETERS</span></span>

### <span data-ttu-id="cafdb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafdb-110">-DefaultProfile</span></span>
<span data-ttu-id="cafdb-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cafdb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cafdb-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cafdb-112">-Name</span></span>
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

### <span data-ttu-id="cafdb-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cafdb-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="cafdb-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cafdb-114">-Confirm</span></span>
<span data-ttu-id="cafdb-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cafdb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafdb-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafdb-116">-WhatIf</span></span>
<span data-ttu-id="cafdb-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cafdb-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cafdb-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cafdb-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafdb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafdb-119">CommonParameters</span></span>
<span data-ttu-id="cafdb-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cafdb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafdb-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cafdb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafdb-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cafdb-122">INPUTS</span></span>

### <span data-ttu-id="cafdb-123">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cafdb-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="cafdb-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cafdb-124">OUTPUTS</span></span>

### <span data-ttu-id="cafdb-125">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cafdb-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="cafdb-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cafdb-126">NOTES</span></span>

## <span data-ttu-id="cafdb-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cafdb-127">RELATED LINKS</span></span>

[<span data-ttu-id="cafdb-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="cafdb-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="cafdb-129">Új – AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="cafdb-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
