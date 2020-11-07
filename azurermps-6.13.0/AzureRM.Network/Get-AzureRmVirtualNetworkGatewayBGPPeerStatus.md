---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 4693b930714e70ad63dab25a4c8872feb5b92c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680795"
---
# <span data-ttu-id="8044f-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="8044f-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="8044f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8044f-102">SYNOPSIS</span></span>
<span data-ttu-id="8044f-103">Az Azure virtuális hálózati átjáró BGP-társainak listája</span><span class="sxs-lookup"><span data-stu-id="8044f-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8044f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8044f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8044f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8044f-105">DESCRIPTION</span></span>
<span data-ttu-id="8044f-106">Ez a parancs a BGP-partnereket enumerálja egy Azure virtuális hálózati átjáró úgy van konfigurálva, hogy egyenrangú legyen.</span><span class="sxs-lookup"><span data-stu-id="8044f-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="8044f-107">Az egyes partnerek állapota szintén meg van adva.</span><span class="sxs-lookup"><span data-stu-id="8044f-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="8044f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8044f-108">EXAMPLES</span></span>

### <span data-ttu-id="8044f-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8044f-109">Example 1</span></span>
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

<span data-ttu-id="8044f-110">Visszanyeri a BGP-partnereket a gatewayName nevű Azure virtuális hálózati átjáróhoz az erőforráscsoport resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8044f-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="8044f-111">Ebben a példában a kimenet egy, a 10.0.0.254 IP-címével összekapcsolt BGP-partnert jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="8044f-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="8044f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8044f-112">PARAMETERS</span></span>

### <span data-ttu-id="8044f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8044f-113">-AsJob</span></span>
<span data-ttu-id="8044f-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8044f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8044f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8044f-115">-DefaultProfile</span></span>
<span data-ttu-id="8044f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8044f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8044f-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="8044f-117">-Peer</span></span>
<span data-ttu-id="8044f-118">Az állapot beolvasására szolgáló társközi IP-címe</span><span class="sxs-lookup"><span data-stu-id="8044f-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="8044f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8044f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8044f-120">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8044f-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="8044f-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8044f-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8044f-122">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="8044f-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="8044f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8044f-123">CommonParameters</span></span>
<span data-ttu-id="8044f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8044f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8044f-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8044f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8044f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8044f-126">INPUTS</span></span>

### <span data-ttu-id="8044f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8044f-127">System.String</span></span>

## <span data-ttu-id="8044f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8044f-128">OUTPUTS</span></span>

### <span data-ttu-id="8044f-129">Microsoft. Azure. commands. Network. models. PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="8044f-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="8044f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8044f-130">NOTES</span></span>

## <span data-ttu-id="8044f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8044f-131">RELATED LINKS</span></span>
