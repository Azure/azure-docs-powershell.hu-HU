---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsectrafficselectorpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecTrafficSelectorPolicy.md
ms.openlocfilehash: 6980ccc3e3ad9c69755253183da1d83f522973da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010325"
---
# <span data-ttu-id="fffde-101">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="fffde-101">New-AzIpsecTrafficSelectorPolicy</span></span>

## <span data-ttu-id="fffde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fffde-102">SYNOPSIS</span></span>
<span data-ttu-id="fffde-103">Forgalomválasztó házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fffde-103">Creates a traffic selector policy.</span></span>

## <span data-ttu-id="fffde-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fffde-104">SYNTAX</span></span>

```
New-AzIpsecTrafficSelectorPolicy -LocalAddressRange <String[]> -RemoteAddressRange <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fffde-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fffde-105">DESCRIPTION</span></span>
<span data-ttu-id="fffde-106">A New-AzTrafficSelectorPolicy parancsmag létrehoz egy forgalomválasztó házirendjavaslatot, amely egy virtuális hálózati átjáró kapcsolatán használható.</span><span class="sxs-lookup"><span data-stu-id="fffde-106">The New-AzTrafficSelectorPolicy cmdlet creates a traffic selector policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="fffde-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fffde-107">EXAMPLES</span></span>

### <span data-ttu-id="fffde-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fffde-108">Example 1</span></span>
```powershell
$trafficSelectorPolicy = New-AzIpsecTrafficSelectorPolicy -LocalAddressRange ("10.10.10.0/24", "20.20.20.0/24") -RemoteAddressRange ("30.30.30.0/24", "40.40.40.0/24")
New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -TrafficSelectorPolicies ($trafficSelectorPolicy)
```

<span data-ttu-id="fffde-109">Létrehozza a forgalomkiválasztó házirend egy példányát, és hozzáadja paraméterként, amikor IKEv2 protokollt használ virtuális hálózati átjárókapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fffde-109">Creates an instance of a traffic selector policy and adds it as a parameter when creating a virtual network gateway connection with an IKEv2 protocol.</span></span>

## <span data-ttu-id="fffde-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fffde-110">PARAMETERS</span></span>

### <span data-ttu-id="fffde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffde-111">-DefaultProfile</span></span>
<span data-ttu-id="fffde-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fffde-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fffde-113">-LocalAddressRange</span><span class="sxs-lookup"><span data-stu-id="fffde-113">-LocalAddressRange</span></span>
<span data-ttu-id="fffde-114">CIDR-címtartományok gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="fffde-114">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="fffde-115">-RemoteAddressRange</span><span class="sxs-lookup"><span data-stu-id="fffde-115">-RemoteAddressRange</span></span>
<span data-ttu-id="fffde-116">CIDR-címtartományok gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="fffde-116">A collection of CIDR address ranges</span></span>

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

### <span data-ttu-id="fffde-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffde-117">CommonParameters</span></span>
<span data-ttu-id="fffde-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fffde-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffde-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fffde-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffde-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fffde-120">INPUTS</span></span>

### <span data-ttu-id="fffde-121">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fffde-121">System.String[]</span></span>

## <span data-ttu-id="fffde-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fffde-122">OUTPUTS</span></span>

### <span data-ttu-id="fffde-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelepolicy</span><span class="sxs-lookup"><span data-stu-id="fffde-123">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy</span></span>

## <span data-ttu-id="fffde-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fffde-124">NOTES</span></span>

## <span data-ttu-id="fffde-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fffde-125">RELATED LINKS</span></span>
