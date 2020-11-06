---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 66eaecd94c2275ff86af319a219c29f021100112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497559"
---
# <span data-ttu-id="7adc8-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="7adc8-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="7adc8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7adc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7adc8-103">Az Azure virtuális hálózati átjáró BGP-társainak listája</span><span class="sxs-lookup"><span data-stu-id="7adc8-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7adc8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7adc8-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7adc8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7adc8-105">DESCRIPTION</span></span>
<span data-ttu-id="7adc8-106">Ez a parancs a BGP-partnereket enumerálja egy Azure virtuális hálózati átjáró úgy van konfigurálva, hogy egyenrangú legyen.</span><span class="sxs-lookup"><span data-stu-id="7adc8-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="7adc8-107">Az egyes partnerek állapota szintén meg van adva.</span><span class="sxs-lookup"><span data-stu-id="7adc8-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="7adc8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7adc8-108">EXAMPLES</span></span>

### <span data-ttu-id="7adc8-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7adc8-109">Example 1</span></span>
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

<span data-ttu-id="7adc8-110">Visszanyeri a BGP-partnereket a gatewayName nevű Azure virtuális hálózati átjáróhoz az erőforráscsoport resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7adc8-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="7adc8-111">Ebben a példában a kimenet egy, a 10.0.0.254 IP-címével összekapcsolt BGP-partnert jelenít meg.</span><span class="sxs-lookup"><span data-stu-id="7adc8-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="7adc8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7adc8-112">PARAMETERS</span></span>

### <span data-ttu-id="7adc8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7adc8-113">-AsJob</span></span>
<span data-ttu-id="7adc8-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7adc8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7adc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adc8-115">-DefaultProfile</span></span>
<span data-ttu-id="7adc8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7adc8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7adc8-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="7adc8-117">-Peer</span></span>
<span data-ttu-id="7adc8-118">Az állapot beolvasására szolgáló társközi IP-címe</span><span class="sxs-lookup"><span data-stu-id="7adc8-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="7adc8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7adc8-119">-ResourceGroupName</span></span>
<span data-ttu-id="7adc8-120">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7adc8-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="7adc8-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="7adc8-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="7adc8-122">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="7adc8-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="7adc8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adc8-123">CommonParameters</span></span>
<span data-ttu-id="7adc8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7adc8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adc8-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adc8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adc8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7adc8-126">INPUTS</span></span>

### <span data-ttu-id="7adc8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7adc8-127">System.String</span></span>

## <span data-ttu-id="7adc8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7adc8-128">OUTPUTS</span></span>

### <span data-ttu-id="7adc8-129">Microsoft. Azure. commands. Network. models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="7adc8-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="7adc8-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7adc8-130">NOTES</span></span>

## <span data-ttu-id="7adc8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7adc8-131">RELATED LINKS</span></span>

