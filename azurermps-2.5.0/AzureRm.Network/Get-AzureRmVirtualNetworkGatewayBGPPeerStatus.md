---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
ms.openlocfilehash: a6a199fcac918bcdee76f5dfdecafa3e82fe7f6d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848158"
---
# <span data-ttu-id="b5a38-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="b5a38-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="b5a38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5a38-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a38-103">Az Azure virtuális hálózati átjáró BGP-társainak listája</span><span class="sxs-lookup"><span data-stu-id="b5a38-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5a38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5a38-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5a38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5a38-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a38-106">Ez a parancs a BGP-partnereket enumerálja egy Azure virtuális hálózati átjáró úgy van konfigurálva, hogy egyenrangú legyen.</span><span class="sxs-lookup"><span data-stu-id="b5a38-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="b5a38-107">Az egyes partnerek állapota szintén meg van adva.</span><span class="sxs-lookup"><span data-stu-id="b5a38-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="b5a38-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b5a38-108">EXAMPLES</span></span>

### <span data-ttu-id="b5a38-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b5a38-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="b5a38-110">Visszanyeri a BGP-partnereket a gatewayName nevű Azure virtuális hálózati átjáróhoz az erőforráscsoport resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5a38-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="b5a38-111">Ebben a példában a kimenet egy, a 10.0.0.254 IP-címével összekapcsolt BGP-partnert jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="b5a38-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="b5a38-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5a38-112">PARAMETERS</span></span>

### <span data-ttu-id="b5a38-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5a38-113">-AsJob</span></span>
<span data-ttu-id="b5a38-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b5a38-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a38-115">-DefaultProfile</span></span>
<span data-ttu-id="b5a38-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5a38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a38-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="b5a38-117">-Peer</span></span>
<span data-ttu-id="b5a38-118">Az állapot beolvasására szolgáló társközi IP-címe</span><span class="sxs-lookup"><span data-stu-id="b5a38-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a38-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a38-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5a38-120">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b5a38-120">Virtual network gateway resource group's name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a38-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b5a38-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b5a38-122">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="b5a38-122">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a38-123">CommonParameters</span></span>
<span data-ttu-id="b5a38-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5a38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a38-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a38-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a38-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5a38-126">INPUTS</span></span>

### <span data-ttu-id="b5a38-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b5a38-127">System.String</span></span>

## <span data-ttu-id="b5a38-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5a38-128">OUTPUTS</span></span>

### <span data-ttu-id="b5a38-129">Microsoft. Azure. commands. Network. models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="b5a38-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="b5a38-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5a38-130">NOTES</span></span>

## <span data-ttu-id="b5a38-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5a38-131">RELATED LINKS</span></span>

