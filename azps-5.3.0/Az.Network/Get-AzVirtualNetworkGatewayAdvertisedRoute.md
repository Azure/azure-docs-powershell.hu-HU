---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480327"
---
# <span data-ttu-id="13157-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="13157-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="13157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13157-102">SYNOPSIS</span></span>
<span data-ttu-id="13157-103">Az Azure virtuális hálózati átjáró által meghirdetett útvonalak felsorolása</span><span class="sxs-lookup"><span data-stu-id="13157-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="13157-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13157-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13157-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13157-105">DESCRIPTION</span></span>
<span data-ttu-id="13157-106">A BGP-társ IP-címe alapján felsorolja az adott társnak a megadott virtuális Azure-hálózati átjáró által meghirdetett útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="13157-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="13157-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13157-107">EXAMPLES</span></span>

### <span data-ttu-id="13157-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="13157-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="13157-109">Az erőforráscsoport erőforrásCsoportNeve nevű Azure-átjáróhoz beolvassa a BGP-társnak 10.0.0.254-es IP-címmel meghirdetett útvonalak listáját.</span><span class="sxs-lookup"><span data-stu-id="13157-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="13157-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="13157-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="13157-111">Az erőforráscsoport resourceGroupName erőforráscsoportban az átjáróNév nevű Azure-átjáró esetében beolvassa a meghirdetett útvonalakat az első BGP-társhoz az átjáró BGP-társlistán.</span><span class="sxs-lookup"><span data-stu-id="13157-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="13157-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13157-112">PARAMETERS</span></span>

### <span data-ttu-id="13157-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13157-113">-AsJob</span></span>
<span data-ttu-id="13157-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="13157-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13157-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13157-115">-DefaultProfile</span></span>
<span data-ttu-id="13157-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13157-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13157-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="13157-117">-Peer</span></span>
<span data-ttu-id="13157-118">BGP-társ IP-címe.</span><span class="sxs-lookup"><span data-stu-id="13157-118">BGP peer's IP address.</span></span> <span data-ttu-id="13157-119">Ennek ip-címnek kell lennie a címterületen belül, amely az átjáró által üzembe helyezett Azure virtuális hálózatból érhető el.</span><span class="sxs-lookup"><span data-stu-id="13157-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="13157-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13157-120">-ResourceGroupName</span></span>
<span data-ttu-id="13157-121">Virtuális hálózati átjáró erőforráscsoportja neve</span><span class="sxs-lookup"><span data-stu-id="13157-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="13157-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="13157-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="13157-123">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="13157-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="13157-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13157-124">CommonParameters</span></span>
<span data-ttu-id="13157-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13157-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13157-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13157-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13157-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13157-127">INPUTS</span></span>

### <span data-ttu-id="13157-128">System.String</span><span class="sxs-lookup"><span data-stu-id="13157-128">System.String</span></span>

## <span data-ttu-id="13157-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13157-129">OUTPUTS</span></span>

### <span data-ttu-id="13157-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="13157-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="13157-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13157-131">NOTES</span></span>
<span data-ttu-id="13157-132">Ez a parancs csak a BGP-kompatibilis kapcsolatokkal rendelkező virtuális Azure-átjárókra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="13157-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="13157-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13157-133">RELATED LINKS</span></span>
