---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194049"
---
# <span data-ttu-id="f1fdd-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="f1fdd-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="f1fdd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fdd-103">Egy Azure virtuális hálózati átjáró által hirdetett útvonalak listázása</span><span class="sxs-lookup"><span data-stu-id="f1fdd-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="f1fdd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1fdd-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1fdd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="f1fdd-106">A BGP-peer IP-címének meghatározásakor a megadott Azure virtuális hálózati átjáró által az adott partnernek hirdetett útvonalakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="f1fdd-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="f1fdd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="f1fdd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f1fdd-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="f1fdd-109">Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, az IP-10.0.0.254 megkeresi az útvonalak listáját, amelyeket a BGP-partnernek hirdetett el</span><span class="sxs-lookup"><span data-stu-id="f1fdd-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="f1fdd-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="f1fdd-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="f1fdd-111">Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, lekérdezi az útvonalakat, hogy az első BGP-társa Hirdessen az átjáró listáját a BGP-partnerek listájáról.</span><span class="sxs-lookup"><span data-stu-id="f1fdd-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="f1fdd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1fdd-112">PARAMETERS</span></span>

### <span data-ttu-id="f1fdd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1fdd-113">-AsJob</span></span>
<span data-ttu-id="f1fdd-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f1fdd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1fdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fdd-115">-DefaultProfile</span></span>
<span data-ttu-id="f1fdd-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1fdd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1fdd-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="f1fdd-117">-Peer</span></span>
<span data-ttu-id="f1fdd-118">BGP társközi IP-címe.</span><span class="sxs-lookup"><span data-stu-id="f1fdd-118">BGP peer's IP address.</span></span> <span data-ttu-id="f1fdd-119">Ennek a helynek az IP-címének kell lennie az Azure virtuális hálózatról, amelyen az átjáró telepítve van.</span><span class="sxs-lookup"><span data-stu-id="f1fdd-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="f1fdd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1fdd-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1fdd-121">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f1fdd-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="f1fdd-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f1fdd-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f1fdd-123">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="f1fdd-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="f1fdd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fdd-124">CommonParameters</span></span>
<span data-ttu-id="f1fdd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1fdd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fdd-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1fdd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fdd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1fdd-127">INPUTS</span></span>

### <span data-ttu-id="f1fdd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f1fdd-128">System.String</span></span>

## <span data-ttu-id="f1fdd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1fdd-129">OUTPUTS</span></span>

### <span data-ttu-id="f1fdd-130">Microsoft. Azure. commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="f1fdd-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="f1fdd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1fdd-131">NOTES</span></span>
<span data-ttu-id="f1fdd-132">Ez a parancs csak az Azure virtuális hálózati átjárók esetében érvényes, amelyek BGP-kompatibilis kapcsolatokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="f1fdd-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="f1fdd-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1fdd-133">RELATED LINKS</span></span>
