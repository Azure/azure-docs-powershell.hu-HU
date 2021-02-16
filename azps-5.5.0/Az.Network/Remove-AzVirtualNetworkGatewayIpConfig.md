---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 3287644b3f953c001490c7be207865a88b000e10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146699"
---
# <span data-ttu-id="eea39-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="eea39-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="eea39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea39-102">SYNOPSIS</span></span>
<span data-ttu-id="eea39-103">Ip-konfiguráció eltávolítása virtuális hálózati átjáróból</span><span class="sxs-lookup"><span data-stu-id="eea39-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="eea39-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eea39-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea39-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eea39-105">DESCRIPTION</span></span>
<span data-ttu-id="eea39-106">Ip-konfiguráció eltávolítása virtuális hálózati átjáróból</span><span class="sxs-lookup"><span data-stu-id="eea39-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="eea39-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eea39-107">EXAMPLES</span></span>

### <span data-ttu-id="eea39-108">1. példa:</span><span class="sxs-lookup"><span data-stu-id="eea39-108">Example 1:</span></span>
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

## <span data-ttu-id="eea39-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eea39-109">PARAMETERS</span></span>

### <span data-ttu-id="eea39-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea39-110">-DefaultProfile</span></span>
<span data-ttu-id="eea39-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eea39-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea39-112">-Name</span><span class="sxs-lookup"><span data-stu-id="eea39-112">-Name</span></span>
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

### <span data-ttu-id="eea39-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eea39-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="eea39-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eea39-114">-Confirm</span></span>
<span data-ttu-id="eea39-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eea39-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea39-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea39-116">-WhatIf</span></span>
<span data-ttu-id="eea39-117">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eea39-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea39-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eea39-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea39-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea39-119">CommonParameters</span></span>
<span data-ttu-id="eea39-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea39-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea39-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea39-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea39-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eea39-122">INPUTS</span></span>

### <span data-ttu-id="eea39-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eea39-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="eea39-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eea39-124">OUTPUTS</span></span>

### <span data-ttu-id="eea39-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eea39-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="eea39-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eea39-126">NOTES</span></span>

## <span data-ttu-id="eea39-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eea39-127">RELATED LINKS</span></span>

[<span data-ttu-id="eea39-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="eea39-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="eea39-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="eea39-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
