---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
ms.openlocfilehash: 0097cd022387b3ac2ee8ceb1fa2a831b60c4256d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848161"
---
# <span data-ttu-id="4ecc6-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="4ecc6-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="4ecc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ecc6-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecc6-103">Egy Azure virtuális hálózati átjáró által hirdetett útvonalak listázása</span><span class="sxs-lookup"><span data-stu-id="4ecc6-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ecc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ecc6-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ecc6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ecc6-105">DESCRIPTION</span></span>
<span data-ttu-id="4ecc6-106">A BGP-peer IP-címének meghatározásakor a megadott Azure virtuális hálózati átjáró által az adott partnernek hirdetett útvonalakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="4ecc6-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="4ecc6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ecc6-107">EXAMPLES</span></span>

### <span data-ttu-id="4ecc6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ecc6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="4ecc6-109">Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, az IP-10.0.0.254 megkeresi a BGP-partnernek küldött útvonalak listáját.</span><span class="sxs-lookup"><span data-stu-id="4ecc6-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="4ecc6-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="4ecc6-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="4ecc6-111">Ha az Azure Gateway nevű gatewayName az erőforráscsoport resourceGroupName, lekérdezi az útvonalakat, hogy az első BGP-társa Hirdessen az átjáró listáját a BGP-partnerek listájáról.</span><span class="sxs-lookup"><span data-stu-id="4ecc6-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="4ecc6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ecc6-112">PARAMETERS</span></span>

### <span data-ttu-id="4ecc6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ecc6-113">-AsJob</span></span>
<span data-ttu-id="4ecc6-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4ecc6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ecc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecc6-115">-DefaultProfile</span></span>
<span data-ttu-id="4ecc6-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ecc6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ecc6-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="4ecc6-117">-Peer</span></span>
<span data-ttu-id="4ecc6-118">BGP társközi IP-címe.</span><span class="sxs-lookup"><span data-stu-id="4ecc6-118">BGP peer's IP address.</span></span> <span data-ttu-id="4ecc6-119">Ennek a helynek az IP-címének kell lennie az Azure virtuális hálózatról, amelyen az átjáró telepítve van.</span><span class="sxs-lookup"><span data-stu-id="4ecc6-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="4ecc6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecc6-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ecc6-121">A virtuális hálózati átjáró erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4ecc6-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="4ecc6-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4ecc6-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4ecc6-123">Virtuális hálózati átjáró neve</span><span class="sxs-lookup"><span data-stu-id="4ecc6-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="4ecc6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecc6-124">CommonParameters</span></span>
<span data-ttu-id="4ecc6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ecc6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecc6-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecc6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecc6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ecc6-127">INPUTS</span></span>

### <span data-ttu-id="4ecc6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ecc6-128">System.String</span></span>

## <span data-ttu-id="4ecc6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ecc6-129">OUTPUTS</span></span>

### <span data-ttu-id="4ecc6-130">Microsoft. Azure. commands. Network. models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="4ecc6-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="4ecc6-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ecc6-131">NOTES</span></span>
<span data-ttu-id="4ecc6-132">Ez a parancs csak az Azure virtuális hálózati átjárók esetében érvényes, amelyek BGP-kompatibilis kapcsolatokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="4ecc6-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="4ecc6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ecc6-133">RELATED LINKS</span></span>

