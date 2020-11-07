---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ceb009dba1984f69e7da3e04a9ae57a9da14c067
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850681"
---
# <span data-ttu-id="66f7e-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="66f7e-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="66f7e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="66f7e-103">Alhálózatot kap egy virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="66f7e-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f7e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66f7e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f7e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="66f7e-106">A **Get-AzureRmVirtualNetworkSubnetConfig** parancsmag egy vagy több alhálózat-konfigurációt kap egy Azure virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="66f7e-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="66f7e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="66f7e-108">1: alhálózat beszerzése virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="66f7e-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="66f7e-109">Ebben a példában egy erőforráscsoport és egy virtuális hálózat jön létre, amely egyetlen alhálózattal rendelkezik az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="66f7e-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="66f7e-110">Ezután beolvassa az alhálózat adatait.</span><span class="sxs-lookup"><span data-stu-id="66f7e-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="66f7e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66f7e-111">PARAMETERS</span></span>

### <span data-ttu-id="66f7e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f7e-112">-DefaultProfile</span></span>
<span data-ttu-id="66f7e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66f7e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f7e-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66f7e-114">-Name</span></span>
<span data-ttu-id="66f7e-115">Annak az alhálózati konfigurációnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="66f7e-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="66f7e-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="66f7e-116">-VirtualNetwork</span></span>
<span data-ttu-id="66f7e-117">Azt a **VirtualNetwork** objektumot adja meg, amely a parancsmag által beolvasott alhálózati konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="66f7e-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="66f7e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f7e-118">CommonParameters</span></span>
<span data-ttu-id="66f7e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66f7e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f7e-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f7e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f7e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66f7e-121">INPUTS</span></span>

### <span data-ttu-id="66f7e-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="66f7e-122">PSVirtualNetwork</span></span>
<span data-ttu-id="66f7e-123">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="66f7e-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="66f7e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66f7e-124">OUTPUTS</span></span>

### <span data-ttu-id="66f7e-125">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="66f7e-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="66f7e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66f7e-126">NOTES</span></span>

## <span data-ttu-id="66f7e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66f7e-127">RELATED LINKS</span></span>

[<span data-ttu-id="66f7e-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="66f7e-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="66f7e-129">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="66f7e-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="66f7e-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="66f7e-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="66f7e-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="66f7e-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


