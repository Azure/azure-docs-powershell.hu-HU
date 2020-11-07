---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 416bc8910e651ca86ef064fda7bd934d67ed8056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670482"
---
# <span data-ttu-id="1e018-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="1e018-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="1e018-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e018-102">SYNOPSIS</span></span>
<span data-ttu-id="1e018-103">Az Azure virtuális hálózati átjáró BGP-társainak listája</span><span class="sxs-lookup"><span data-stu-id="1e018-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="1e018-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e018-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e018-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e018-105">DESCRIPTION</span></span>
<span data-ttu-id="1e018-106">Ez a parancs a BGP-partnereket enumerálja egy Azure virtuális hálózati átjáró úgy van konfigurálva, hogy egyenrangú legyen.</span><span class="sxs-lookup"><span data-stu-id="1e018-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="1e018-107">Az egyes partnerek állapota szintén meg van adva.</span><span class="sxs-lookup"><span data-stu-id="1e018-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="1e018-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1e018-108">EXAMPLES</span></span>

### <span data-ttu-id="1e018-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e018-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="1e018-110">Visszanyeri a BGP-partnereket a gatewayName nevű Azure virtuális hálózati átjáróhoz az erőforráscsoport resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1e018-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="1e018-111">Ebben a példában a kimenet egy, a 10.0.0.254 IP-címével összekapcsolt BGP-partnert jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="1e018-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="1e018-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e018-112">PARAMETERS</span></span>

### <span data-ttu-id="1e018-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e018-113">-AsJob</span></span>
<span data-ttu-id="1e018-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1e018-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e018-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e018-115">-DefaultProfile</span></span>
<span data-ttu-id="1e018-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e018-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e018-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="1e018-117">-Peer</span></span>
<span data-ttu-id="1e018-118">Az állapot beolvasására szolgáló társközi IP-címe</span><span class="sxs-lookup"><span data-stu-id="1e018-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e018-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e018-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e018-120">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1e018-120">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e018-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1e018-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1e018-122">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="1e018-122">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e018-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e018-123">CommonParameters</span></span>
<span data-ttu-id="1e018-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e018-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e018-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e018-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e018-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e018-126">INPUTS</span></span>

### <span data-ttu-id="1e018-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1e018-127">System.String</span></span>

## <span data-ttu-id="1e018-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e018-128">OUTPUTS</span></span>

### <span data-ttu-id="1e018-129">Microsoft. Azure. commands. Network. models. PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="1e018-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="1e018-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e018-130">NOTES</span></span>

## <span data-ttu-id="1e018-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e018-131">RELATED LINKS</span></span>
