---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: bee7857751b9553314085ab3fee4f5edbadce1b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931753"
---
# <span data-ttu-id="7fce3-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7fce3-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="7fce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fce3-102">SYNOPSIS</span></span>
<span data-ttu-id="7fce3-103">Egy virtuális hálózaton található alhálózatot kap.</span><span class="sxs-lookup"><span data-stu-id="7fce3-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="7fce3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fce3-104">SYNTAX</span></span>

### <span data-ttu-id="7fce3-105">GetByVirtualNetwork (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fce3-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fce3-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7fce3-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fce3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fce3-107">DESCRIPTION</span></span>
<span data-ttu-id="7fce3-108">A **Get-AzVirtualNetworkSubnetConfig** parancsmag egy vagy több alhálózati konfigurációt kap egy Azure virtuális hálózatban.</span><span class="sxs-lookup"><span data-stu-id="7fce3-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="7fce3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fce3-109">EXAMPLES</span></span>

### <span data-ttu-id="7fce3-110">1: Alhálózat lekérte virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="7fce3-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="7fce3-111">Ez a példa létrehoz egy erőforráscsoportot és egy virtuális hálózatot egyetlen alhálózattal az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7fce3-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="7fce3-112">Ezután beolvassa az alhálózat adatait.</span><span class="sxs-lookup"><span data-stu-id="7fce3-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="7fce3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fce3-113">PARAMETERS</span></span>

### <span data-ttu-id="7fce3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fce3-114">-DefaultProfile</span></span>
<span data-ttu-id="7fce3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fce3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fce3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7fce3-116">-Name</span></span>
<span data-ttu-id="7fce3-117">Annak az alhálózati konfigurációnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="7fce3-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fce3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fce3-118">-ResourceId</span></span>
<span data-ttu-id="7fce3-119">Annak az alhálózatnak az erőforrás-azonosítója, amelybe ez a parancsmag be fog jut.</span><span class="sxs-lookup"><span data-stu-id="7fce3-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fce3-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fce3-120">-VirtualNetwork</span></span>
<span data-ttu-id="7fce3-121">Megadja azt a **VirtualNetwork** objektumot, amely a parancsmag alhálózati konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7fce3-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fce3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fce3-122">CommonParameters</span></span>
<span data-ttu-id="7fce3-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fce3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fce3-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fce3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fce3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fce3-125">INPUTS</span></span>

### <span data-ttu-id="7fce3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fce3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="7fce3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7fce3-127">System.String</span></span>

## <span data-ttu-id="7fce3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fce3-128">OUTPUTS</span></span>

### <span data-ttu-id="7fce3-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7fce3-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7fce3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fce3-130">NOTES</span></span>

## <span data-ttu-id="7fce3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fce3-131">RELATED LINKS</span></span>

[<span data-ttu-id="7fce3-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7fce3-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7fce3-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7fce3-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7fce3-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7fce3-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7fce3-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7fce3-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
