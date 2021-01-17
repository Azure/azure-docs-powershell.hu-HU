---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480325"
---
# <span data-ttu-id="fdddb-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="fdddb-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="fdddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdddb-102">SYNOPSIS</span></span>
<span data-ttu-id="fdddb-103">Egy Azure virtuális hálózati átjáró BGP-társlistáit sorolja fel</span><span class="sxs-lookup"><span data-stu-id="fdddb-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="fdddb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fdddb-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdddb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fdddb-105">DESCRIPTION</span></span>
<span data-ttu-id="fdddb-106">Ez a parancs felsorolja a BGP-társokat, amelyekhez az Azure virtuális hálózati átjáró be van állítva társviszonyként.</span><span class="sxs-lookup"><span data-stu-id="fdddb-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="fdddb-107">Az egyes partnerek állapota is meg van adva.</span><span class="sxs-lookup"><span data-stu-id="fdddb-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="fdddb-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fdddb-108">EXAMPLES</span></span>

### <span data-ttu-id="fdddb-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="fdddb-109">Example 1</span></span>
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

<span data-ttu-id="fdddb-110">Beolvassa a BGP-társokat az ÁtjáróNév nevű Azure virtuális hálózati átjáróhoz az erőforráscsoport erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="fdddb-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="fdddb-111">Ebben a példában egy csatlakoztatott BGP-társ látható 10.0.0.254-es IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="fdddb-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="fdddb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdddb-112">PARAMETERS</span></span>

### <span data-ttu-id="fdddb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdddb-113">-AsJob</span></span>
<span data-ttu-id="fdddb-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fdddb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdddb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdddb-115">-DefaultProfile</span></span>
<span data-ttu-id="fdddb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdddb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdddb-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="fdddb-117">-Peer</span></span>
<span data-ttu-id="fdddb-118">ANNAK a társnak az IP-címe, amelyről beolvassa a következő állapotát:</span><span class="sxs-lookup"><span data-stu-id="fdddb-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="fdddb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdddb-119">-ResourceGroupName</span></span>
<span data-ttu-id="fdddb-120">Virtuális hálózati átjáró erőforráscsoportja neve</span><span class="sxs-lookup"><span data-stu-id="fdddb-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="fdddb-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fdddb-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fdddb-122">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="fdddb-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="fdddb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdddb-123">CommonParameters</span></span>
<span data-ttu-id="fdddb-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdddb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdddb-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdddb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdddb-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fdddb-126">INPUTS</span></span>

### <span data-ttu-id="fdddb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fdddb-127">System.String</span></span>

## <span data-ttu-id="fdddb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdddb-128">OUTPUTS</span></span>

### <span data-ttu-id="fdddb-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="fdddb-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="fdddb-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fdddb-130">NOTES</span></span>

## <span data-ttu-id="fdddb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdddb-131">RELATED LINKS</span></span>
