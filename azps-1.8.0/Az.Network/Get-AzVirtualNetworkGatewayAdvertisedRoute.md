---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: f7ac40d088cca1b88a5a4a5413fe048faac99d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670483"
---
# <span data-ttu-id="d4913-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="d4913-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="d4913-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4913-102">SYNOPSIS</span></span>
<span data-ttu-id="d4913-103">Egy Azure virtuális hálózati átjáró által hirdetett útvonalak listázása</span><span class="sxs-lookup"><span data-stu-id="d4913-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="d4913-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4913-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4913-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4913-105">DESCRIPTION</span></span>
<span data-ttu-id="d4913-106">A BGP-peer IP-címének meghatározásakor a megadott Azure virtuális hálózati átjáró által az adott partnernek hirdetett útvonalakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d4913-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="d4913-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d4913-107">EXAMPLES</span></span>

### <span data-ttu-id="d4913-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4913-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="d4913-109">Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, az IP-10.0.0.254 megkeresi a BGP-partnernek küldött útvonalak listáját.</span><span class="sxs-lookup"><span data-stu-id="d4913-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="d4913-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4913-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="d4913-111">Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, lekérdezi az útvonalakat, hogy az első BGP-társa Hirdessen az átjáró listáját a BGP-partnerek listájáról.</span><span class="sxs-lookup"><span data-stu-id="d4913-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="d4913-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4913-112">PARAMETERS</span></span>

### <span data-ttu-id="d4913-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4913-113">-AsJob</span></span>
<span data-ttu-id="d4913-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d4913-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4913-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4913-115">-DefaultProfile</span></span>
<span data-ttu-id="d4913-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4913-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4913-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="d4913-117">-Peer</span></span>
<span data-ttu-id="d4913-118">BGP társközi IP-címe.</span><span class="sxs-lookup"><span data-stu-id="d4913-118">BGP peer's IP address.</span></span> <span data-ttu-id="d4913-119">Ennek a helynek az IP-címének kell lennie az Azure virtuális hálózatról, amelyen az átjáró telepítve van.</span><span class="sxs-lookup"><span data-stu-id="d4913-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="d4913-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4913-120">-ResourceGroupName</span></span>
<span data-ttu-id="d4913-121">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d4913-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d4913-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d4913-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d4913-123">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="d4913-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="d4913-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4913-124">CommonParameters</span></span>
<span data-ttu-id="d4913-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4913-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4913-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4913-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4913-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4913-127">INPUTS</span></span>

### <span data-ttu-id="d4913-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d4913-128">System.String</span></span>

## <span data-ttu-id="d4913-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4913-129">OUTPUTS</span></span>

### <span data-ttu-id="d4913-130">Microsoft. Azure. commands. Network. models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="d4913-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="d4913-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4913-131">NOTES</span></span>
<span data-ttu-id="d4913-132">Ez a parancs csak az Azure virtuális hálózati átjárók esetében érvényes, amelyek BGP-kompatibilis kapcsolatokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="d4913-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="d4913-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4913-133">RELATED LINKS</span></span>
