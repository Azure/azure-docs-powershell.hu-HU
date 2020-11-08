---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: f335272bce6591c617d8111dd1d0d81af50ec255
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181568"
---
# <span data-ttu-id="1e8c3-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="1e8c3-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="1e8c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8c3-103">Forgalmi kiválasztó házirend létrehozása.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="1e8c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e8c3-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e8c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="1e8c3-106">Az New-AzTrafficSelectorPolicy parancsmag létrehoz egy forgalmi választó házirend-javaslatot, amelyet a virtuális hálózati átjáró kapcsolata esetén kell használni.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="1e8c3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1e8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="1e8c3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e8c3-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="1e8c3-109">A forgalmi kiválasztó házirend példányát hozza létre, és paraméterként hozzáadja a virtuális hálózati átjáró-kapcsolat IKEv2-protokollal való létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="1e8c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e8c3-110">PARAMETERS</span></span>

### <span data-ttu-id="1e8c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8c3-111">-DefaultProfile</span></span>
<span data-ttu-id="1e8c3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e8c3-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="1e8c3-113">-LocalAddressRange</span></span>
<span data-ttu-id="1e8c3-114">CIDR-címtartományok gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="1e8c3-114">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e8c3-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="1e8c3-115">-RemoteAddressRange</span></span>
<span data-ttu-id="1e8c3-116">CIDR-címtartományok gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="1e8c3-116">A collection of CIDR address ranges</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e8c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8c3-117">CommonParameters</span></span>
<span data-ttu-id="1e8c3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e8c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8c3-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8c3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e8c3-120">INPUTS</span></span>

### <span data-ttu-id="1e8c3-121">System. string []</span><span class="sxs-lookup"><span data-stu-id="1e8c3-121">System.String[]</span></span>

## <span data-ttu-id="1e8c3-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e8c3-122">OUTPUTS</span></span>

### <span data-ttu-id="1e8c3-123">Microsoft. Azure. commands. Network. models. PSTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="1e8c3-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="1e8c3-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e8c3-124">NOTES</span></span>

## <span data-ttu-id="1e8c3-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e8c3-125">RELATED LINKS</span></span>
