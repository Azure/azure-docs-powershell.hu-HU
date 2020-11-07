---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: e5b881547f84714e238f541948602569c773c9c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670466"
---
# <span data-ttu-id="c38e7-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c38e7-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c38e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c38e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c38e7-103">Alhálózatot kap egy virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="c38e7-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="c38e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c38e7-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c38e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c38e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c38e7-106">A **Get-AzVirtualNetworkSubnetConfig** parancsmag egy vagy több alhálózat-konfigurációt kap egy Azure virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="c38e7-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="c38e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c38e7-107">EXAMPLES</span></span>

### <span data-ttu-id="c38e7-108">1: alhálózat beszerzése virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="c38e7-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="c38e7-109">Ebben a példában egy erőforráscsoport és egy virtuális hálózat jön létre, amely egyetlen alhálózattal rendelkezik az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="c38e7-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="c38e7-110">Ezután beolvassa az alhálózat adatait.</span><span class="sxs-lookup"><span data-stu-id="c38e7-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="c38e7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c38e7-111">PARAMETERS</span></span>

### <span data-ttu-id="c38e7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38e7-112">-DefaultProfile</span></span>
<span data-ttu-id="c38e7-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c38e7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c38e7-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c38e7-114">-Name</span></span>
<span data-ttu-id="c38e7-115">Annak az alhálózati konfigurációnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c38e7-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c38e7-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c38e7-116">-VirtualNetwork</span></span>
<span data-ttu-id="c38e7-117">Azt a **VirtualNetwork** objektumot adja meg, amely a parancsmag által beolvasott alhálózati konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c38e7-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c38e7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38e7-118">CommonParameters</span></span>
<span data-ttu-id="c38e7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c38e7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38e7-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c38e7-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38e7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c38e7-121">INPUTS</span></span>

### <span data-ttu-id="c38e7-122">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c38e7-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c38e7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c38e7-123">OUTPUTS</span></span>

### <span data-ttu-id="c38e7-124">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c38e7-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c38e7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c38e7-125">NOTES</span></span>

## <span data-ttu-id="c38e7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c38e7-126">RELATED LINKS</span></span>

[<span data-ttu-id="c38e7-127">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c38e7-127">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c38e7-128">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c38e7-128">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c38e7-129">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c38e7-129">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c38e7-130">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c38e7-130">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


