---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357446"
---
# <span data-ttu-id="30c66-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="30c66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30c66-102">SYNOPSIS</span></span>
<span data-ttu-id="30c66-103">Virtuális hálózat frissítése.</span><span class="sxs-lookup"><span data-stu-id="30c66-103">Updates a virtual network.</span></span>

## <span data-ttu-id="30c66-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30c66-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30c66-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30c66-105">DESCRIPTION</span></span>
<span data-ttu-id="30c66-106">A **Set-AzVirtualNetwork** parancsmag frissíti a virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="30c66-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="30c66-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30c66-107">EXAMPLES</span></span>

### <span data-ttu-id="30c66-108">1: Virtuális hálózat létrehozása és az alhálózatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="30c66-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="30c66-109">Ez a példa létrehoz egy TestResourceGroup nevű virtuális hálózatot két alhálózattal: frontendSubnet és backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="30c66-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="30c66-110">Ezután eltávolítja a backendSubnet alhálózatot a virtuális hálózat memóriában való megjelenítéséből.</span><span class="sxs-lookup"><span data-stu-id="30c66-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="30c66-111">A Set-AzVirtualNetwork ezt követően a módosított virtuális hálózati állapotot a szolgáltatásoldalra írja.</span><span class="sxs-lookup"><span data-stu-id="30c66-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="30c66-112">Amikor végrehajtja Set-AzVirtualNetwork parancsmagot, a backendSubnet törlődik.</span><span class="sxs-lookup"><span data-stu-id="30c66-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="30c66-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30c66-113">PARAMETERS</span></span>

### <span data-ttu-id="30c66-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30c66-114">-AsJob</span></span>
<span data-ttu-id="30c66-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="30c66-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30c66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c66-116">-DefaultProfile</span></span>
<span data-ttu-id="30c66-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30c66-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c66-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-118">-VirtualNetwork</span></span>
<span data-ttu-id="30c66-119">Egy virtuális hálózati objektumot ad meg, amely azt az állapotot képviseli, amelyben a virtuális hálózatot be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="30c66-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="30c66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c66-120">CommonParameters</span></span>
<span data-ttu-id="30c66-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c66-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c66-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c66-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30c66-123">INPUTS</span></span>

### <span data-ttu-id="30c66-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="30c66-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30c66-125">OUTPUTS</span></span>

### <span data-ttu-id="30c66-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="30c66-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30c66-127">NOTES</span></span>

## <span data-ttu-id="30c66-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30c66-128">RELATED LINKS</span></span>

[<span data-ttu-id="30c66-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="30c66-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="30c66-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="30c66-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30c66-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


