---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 22ea0a6a28a24503413fa9b8958002616c03b884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493723"
---
# <span data-ttu-id="0cc59-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="0cc59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cc59-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc59-103">A virtuális hálózat cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="0cc59-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cc59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cc59-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cc59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cc59-105">DESCRIPTION</span></span>
<span data-ttu-id="0cc59-106">A **set-AzureRmVirtualNetwork** parancsmag egy Azure virtuális hálózat céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="0cc59-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="0cc59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0cc59-107">EXAMPLES</span></span>

### <span data-ttu-id="0cc59-108">1: virtuális hálózat létrehozása és az egyik alhálózat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0cc59-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="0cc59-109">Ebben a példában két alhálózatot tartalmazó virtuális hálózat jön létre.</span><span class="sxs-lookup"><span data-stu-id="0cc59-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="0cc59-110">Ezután eltávolítja a virtuális hálózat memóriában való megjelenítésével egy alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="0cc59-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="0cc59-111">A rendszer a Set-AzureRmVirtualNetwork parancsmagot használva írja be a módosított virtuális hálózati állapotát a szolgáltatás oldalán.</span><span class="sxs-lookup"><span data-stu-id="0cc59-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="0cc59-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cc59-112">PARAMETERS</span></span>

### <span data-ttu-id="0cc59-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cc59-113">-AsJob</span></span>
<span data-ttu-id="0cc59-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0cc59-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc59-115">-DefaultProfile</span></span>
<span data-ttu-id="0cc59-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cc59-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cc59-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-117">-VirtualNetwork</span></span>
<span data-ttu-id="0cc59-118">Egy **VirtualNetwork** objektumot ad meg, amely a cél állapotát jelöli.</span><span class="sxs-lookup"><span data-stu-id="0cc59-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="0cc59-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc59-119">CommonParameters</span></span>
<span data-ttu-id="0cc59-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cc59-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc59-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc59-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc59-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cc59-122">INPUTS</span></span>

### <span data-ttu-id="0cc59-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-123">PSVirtualNetwork</span></span>
<span data-ttu-id="0cc59-124">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0cc59-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="0cc59-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cc59-125">OUTPUTS</span></span>

### <span data-ttu-id="0cc59-126">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0cc59-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cc59-127">NOTES</span></span>

## <span data-ttu-id="0cc59-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cc59-128">RELATED LINKS</span></span>

[<span data-ttu-id="0cc59-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0cc59-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0cc59-131">Új – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0cc59-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0cc59-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


