---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 658403add3bffb0395678ba5709ce19baf993d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499483"
---
# <span data-ttu-id="85263-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="85263-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="85263-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85263-102">SYNOPSIS</span></span>
<span data-ttu-id="85263-103">Alhálózatot kap egy virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="85263-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85263-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85263-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85263-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85263-105">DESCRIPTION</span></span>
<span data-ttu-id="85263-106">A **Get-AzureRmVirtualNetworkSubnetConfig** parancsmag egy vagy több alhálózat-konfigurációt kap egy Azure virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="85263-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="85263-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85263-107">EXAMPLES</span></span>

### <span data-ttu-id="85263-108">1: alhálózat beszerzése virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="85263-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="85263-109">Ebben a példában egy erőforráscsoport és egy virtuális hálózat jön létre, amely egyetlen alhálózattal rendelkezik az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="85263-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="85263-110">Ezután beolvassa az alhálózat adatait.</span><span class="sxs-lookup"><span data-stu-id="85263-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="85263-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85263-111">PARAMETERS</span></span>

### <span data-ttu-id="85263-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85263-112">-DefaultProfile</span></span>
<span data-ttu-id="85263-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85263-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85263-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="85263-114">-Name</span></span>
<span data-ttu-id="85263-115">Annak az alhálózati konfigurációnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="85263-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="85263-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="85263-116">-VirtualNetwork</span></span>
<span data-ttu-id="85263-117">Azt a **VirtualNetwork** objektumot adja meg, amely a parancsmag által beolvasott alhálózati konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="85263-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="85263-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85263-118">CommonParameters</span></span>
<span data-ttu-id="85263-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85263-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85263-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85263-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85263-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85263-121">INPUTS</span></span>

### <span data-ttu-id="85263-122">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="85263-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="85263-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85263-123">OUTPUTS</span></span>

### <span data-ttu-id="85263-124">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="85263-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="85263-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85263-125">NOTES</span></span>

## <span data-ttu-id="85263-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85263-126">RELATED LINKS</span></span>

[<span data-ttu-id="85263-127">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="85263-127">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="85263-128">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="85263-128">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="85263-129">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="85263-129">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="85263-130">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="85263-130">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


