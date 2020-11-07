---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847458"
---
# <span data-ttu-id="db6e2-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="db6e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="db6e2-103">Virtuális hálózat frissítése</span><span class="sxs-lookup"><span data-stu-id="db6e2-103">Updates a virtual network.</span></span>

## <span data-ttu-id="db6e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db6e2-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db6e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="db6e2-106">A **set-AzVirtualNetwork** parancsmag frissíti a virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="db6e2-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="db6e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db6e2-107">EXAMPLES</span></span>

### <span data-ttu-id="db6e2-108">1: virtuális hálózat létrehozása és az egyik alhálózat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="db6e2-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="db6e2-109">Ez a példa létrehoz egy TestResourceGroup nevű virtuális hálózatot két alhálózattal: frontendSubnet és backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="db6e2-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="db6e2-110">Ezután eltávolítja a backendSubnet alhálózatot a virtuális hálózat memóriában való megjelenítéséről.</span><span class="sxs-lookup"><span data-stu-id="db6e2-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="db6e2-111">A rendszer a Set-AzVirtualNetwork parancsmagot használva írja be a módosított virtuális hálózati állapotát a szolgáltatás oldalán.</span><span class="sxs-lookup"><span data-stu-id="db6e2-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="db6e2-112">A Set-AzVirtualNetwork-parancsmag végrehajtásakor a program eltávolítja a backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="db6e2-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="db6e2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db6e2-113">PARAMETERS</span></span>

### <span data-ttu-id="db6e2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db6e2-114">-AsJob</span></span>
<span data-ttu-id="db6e2-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="db6e2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db6e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6e2-116">-DefaultProfile</span></span>
<span data-ttu-id="db6e2-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db6e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6e2-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-118">-VirtualNetwork</span></span>
<span data-ttu-id="db6e2-119">Azt a virtuális hálózati objektumot adja meg, amely az a virtuális hálózatnak megfelelő állapotot jelenti.</span><span class="sxs-lookup"><span data-stu-id="db6e2-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db6e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6e2-120">CommonParameters</span></span>
<span data-ttu-id="db6e2-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db6e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6e2-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6e2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6e2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db6e2-123">INPUTS</span></span>

### <span data-ttu-id="db6e2-124">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="db6e2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db6e2-125">OUTPUTS</span></span>

### <span data-ttu-id="db6e2-126">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="db6e2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db6e2-127">NOTES</span></span>

## <span data-ttu-id="db6e2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db6e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="db6e2-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="db6e2-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="db6e2-131">Új – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="db6e2-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db6e2-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

