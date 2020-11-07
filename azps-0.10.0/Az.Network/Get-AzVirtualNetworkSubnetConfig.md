---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841478"
---
# <span data-ttu-id="8c7c5-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8c7c5-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="8c7c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7c5-103">Alhálózatot kap egy virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="8c7c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c7c5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c7c5-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7c5-106">A **Get-AzVirtualNetworkSubnetConfig** parancsmag egy vagy több alhálózat-konfigurációt kap egy Azure virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="8c7c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8c7c5-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7c5-108">1: alhálózat beszerzése virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="8c7c5-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="8c7c5-109">Ebben a példában egy erőforráscsoport és egy virtuális hálózat jön létre, amely egyetlen alhálózattal rendelkezik az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="8c7c5-110">Ezután beolvassa az alhálózat adatait.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="8c7c5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c7c5-111">PARAMETERS</span></span>

### <span data-ttu-id="8c7c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7c5-112">-DefaultProfile</span></span>
<span data-ttu-id="8c7c5-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c7c5-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c7c5-114">-Name</span></span>
<span data-ttu-id="8c7c5-115">Annak az alhálózati konfigurációnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8c7c5-116">-VirtualNetwork</span></span>
<span data-ttu-id="8c7c5-117">Azt a **VirtualNetwork** objektumot adja meg, amely a parancsmag által beolvasott alhálózati konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7c5-118">CommonParameters</span></span>
<span data-ttu-id="8c7c5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c7c5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7c5-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7c5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7c5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c7c5-121">INPUTS</span></span>

### <span data-ttu-id="8c7c5-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8c7c5-122">PSVirtualNetwork</span></span>
<span data-ttu-id="8c7c5-123">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8c7c5-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="8c7c5-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c7c5-124">OUTPUTS</span></span>

### <span data-ttu-id="8c7c5-125">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8c7c5-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="8c7c5-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c7c5-126">NOTES</span></span>

## <span data-ttu-id="8c7c5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c7c5-127">RELATED LINKS</span></span>

[<span data-ttu-id="8c7c5-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8c7c5-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8c7c5-129">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8c7c5-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8c7c5-130">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8c7c5-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8c7c5-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8c7c5-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


