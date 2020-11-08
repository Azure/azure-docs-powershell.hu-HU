---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7d90ffff788239996f7b79f7e56493611db86e04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181530"
---
# <span data-ttu-id="68f79-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="68f79-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="68f79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68f79-102">SYNOPSIS</span></span>
<span data-ttu-id="68f79-103">Alhálózat-konfiguráció eltávolítása virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="68f79-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="68f79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68f79-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68f79-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68f79-105">DESCRIPTION</span></span>
<span data-ttu-id="68f79-106">A **Remove-AzVirtualNetworkSubnetConfig** parancsmag eltávolítja az alhálózatokat egy Azure virtuális hálózatból.</span><span class="sxs-lookup"><span data-stu-id="68f79-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="68f79-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68f79-107">EXAMPLES</span></span>

### <span data-ttu-id="68f79-108">1: alhálózat eltávolítása virtuális hálózatról és a virtuális hálózat frissítése</span><span class="sxs-lookup"><span data-stu-id="68f79-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="68f79-109">Ebben a példában egy erőforráscsoport és egy virtuális hálózat jön létre két alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="68f79-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="68f79-110">Ezután a Remove-AzVirtualNetworkSubnetConfig parancs segítségével eltávolítja a backend-alhálózatot a virtuális hálózat memóriában való megjelenítéséről.</span><span class="sxs-lookup"><span data-stu-id="68f79-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="68f79-111">Ezt követően az Set-AzVirtualNetwork a virtuális hálózatnak a kiszolgáló oldalán való módosítását kéri.</span><span class="sxs-lookup"><span data-stu-id="68f79-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="68f79-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68f79-112">PARAMETERS</span></span>

### <span data-ttu-id="68f79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f79-113">-DefaultProfile</span></span>
<span data-ttu-id="68f79-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68f79-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68f79-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68f79-115">-Name</span></span>
<span data-ttu-id="68f79-116">Az eltávolítandó alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f79-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f79-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68f79-117">-VirtualNetwork</span></span>
<span data-ttu-id="68f79-118">Az eltávolítani kívánt alhálózat-konfigurációt tartalmazó **VirtualNetwork** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f79-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="68f79-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f79-119">CommonParameters</span></span>
<span data-ttu-id="68f79-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68f79-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f79-121">További információ: [about_CommonParameters] ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68f79-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f79-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68f79-122">INPUTS</span></span>

### <span data-ttu-id="68f79-123">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68f79-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="68f79-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68f79-124">OUTPUTS</span></span>

### <span data-ttu-id="68f79-125">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="68f79-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="68f79-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68f79-126">NOTES</span></span>

## <span data-ttu-id="68f79-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68f79-127">RELATED LINKS</span></span>

[<span data-ttu-id="68f79-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="68f79-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="68f79-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="68f79-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="68f79-130">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="68f79-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="68f79-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="68f79-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


