---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4fa6fe0ca041d89b6429323fb262e68f39a8aede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495004"
---
# <span data-ttu-id="a798f-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a798f-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a798f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a798f-102">SYNOPSIS</span></span>
<span data-ttu-id="a798f-103">Alhálózat-konfiguráció eltávolítása virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="a798f-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a798f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a798f-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a798f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a798f-105">DESCRIPTION</span></span>
<span data-ttu-id="a798f-106">A **Remove-AzureRmVirtualNetworkSubnetConfig** parancsmag eltávolítja az alhálózatokat egy Azure virtuális hálózatból.</span><span class="sxs-lookup"><span data-stu-id="a798f-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="a798f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a798f-107">EXAMPLES</span></span>

### <span data-ttu-id="a798f-108">1: alhálózat eltávolítása virtuális hálózatról és a virtuális hálózat frissítése</span><span class="sxs-lookup"><span data-stu-id="a798f-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="a798f-109">Ebben a példában egy erőforráscsoport és egy virtuális hálózat jön létre két alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="a798f-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="a798f-110">Ezután a Remove-AzureRmVirtualNetworkSubnetConfig parancs segítségével eltávolítja a backend-alhálózatot a virtuális hálózat memóriában való megjelenítéséről.</span><span class="sxs-lookup"><span data-stu-id="a798f-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a798f-111">Ezt követően az Set-AzureRmVirtualNetwork a virtuális hálózatnak a kiszolgáló oldalán való módosítását kéri.</span><span class="sxs-lookup"><span data-stu-id="a798f-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="a798f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a798f-112">PARAMETERS</span></span>

### <span data-ttu-id="a798f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a798f-113">-DefaultProfile</span></span>
<span data-ttu-id="a798f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a798f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a798f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a798f-115">-Name</span></span>
<span data-ttu-id="a798f-116">Az eltávolítandó alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a798f-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="a798f-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a798f-117">-VirtualNetwork</span></span>
<span data-ttu-id="a798f-118">Az eltávolítani kívánt alhálózat-konfigurációt tartalmazó **VirtualNetwork** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a798f-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="a798f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a798f-119">CommonParameters</span></span>
<span data-ttu-id="a798f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a798f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a798f-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a798f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a798f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a798f-122">INPUTS</span></span>

### <span data-ttu-id="a798f-123">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a798f-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="a798f-124">Paraméterek: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a798f-124">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="a798f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a798f-125">OUTPUTS</span></span>

### <span data-ttu-id="a798f-126">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a798f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a798f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a798f-127">NOTES</span></span>

## <span data-ttu-id="a798f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a798f-128">RELATED LINKS</span></span>

[<span data-ttu-id="a798f-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a798f-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a798f-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a798f-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a798f-131">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a798f-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a798f-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a798f-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


