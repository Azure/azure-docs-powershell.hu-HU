---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494991"
---
# <span data-ttu-id="fb855-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="fb855-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb855-102">SYNOPSIS</span></span>
<span data-ttu-id="fb855-103">A virtuális hálózat cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="fb855-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb855-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb855-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb855-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb855-105">DESCRIPTION</span></span>
<span data-ttu-id="fb855-106">A **set-AzureRmVirtualNetwork** parancsmag egy Azure virtuális hálózat céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="fb855-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="fb855-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb855-107">EXAMPLES</span></span>

### <span data-ttu-id="fb855-108">1: virtuális hálózat létrehozása és az egyik alhálózat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fb855-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="fb855-109">Ez a példa létrehoz egy TestResourceGroup nevű virtuális hálózatot két alhálózattal: frontendSubnet és backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="fb855-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="fb855-110">Ezután eltávolítja a backendSubnet alhálózatot a virtuális hálózat memóriában való megjelenítéséről.</span><span class="sxs-lookup"><span data-stu-id="fb855-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="fb855-111">A rendszer a Set-AzureRmVirtualNetwork parancsmagot használva írja be a módosított virtuális hálózati állapotát a szolgáltatás oldalán.</span><span class="sxs-lookup"><span data-stu-id="fb855-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="fb855-112">A Set-AzureRmVirtualNetwork-parancsmag végrehajtásakor a program eltávolítja a backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="fb855-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="fb855-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb855-113">PARAMETERS</span></span>

### <span data-ttu-id="fb855-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb855-114">-AsJob</span></span>
<span data-ttu-id="fb855-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fb855-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb855-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb855-116">-DefaultProfile</span></span>
<span data-ttu-id="fb855-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb855-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb855-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-118">-VirtualNetwork</span></span>
<span data-ttu-id="fb855-119">Egy **VirtualNetwork** objektumot ad meg, amely a cél állapotát jelöli.</span><span class="sxs-lookup"><span data-stu-id="fb855-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="fb855-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb855-120">CommonParameters</span></span>
<span data-ttu-id="fb855-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb855-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb855-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb855-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb855-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb855-123">INPUTS</span></span>

### <span data-ttu-id="fb855-124">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="fb855-125">Paraméterek: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb855-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="fb855-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb855-126">OUTPUTS</span></span>

### <span data-ttu-id="fb855-127">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="fb855-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb855-128">NOTES</span></span>

## <span data-ttu-id="fb855-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb855-129">RELATED LINKS</span></span>

[<span data-ttu-id="fb855-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fb855-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fb855-132">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fb855-133">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb855-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


