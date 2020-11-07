---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843565"
---
# <span data-ttu-id="ecc5a-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="ecc5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ecc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc5a-103">A virtuális hálózat cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="ecc5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ecc5a-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc5a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ecc5a-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc5a-106">A **set-AzVirtualNetwork** parancsmag egy Azure virtuális hálózat céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="ecc5a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ecc5a-107">EXAMPLES</span></span>

### <span data-ttu-id="ecc5a-108">1: virtuális hálózat létrehozása és az egyik alhálózat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ecc5a-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="ecc5a-109">Ebben a példában két alhálózatot tartalmazó virtuális hálózat jön létre.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="ecc5a-110">Ezután eltávolítja a virtuális hálózat memóriában való megjelenítésével egy alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="ecc5a-111">A rendszer a Set-AzVirtualNetwork parancsmagot használva írja be a módosított virtuális hálózati állapotát a szolgáltatás oldalán.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="ecc5a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ecc5a-112">PARAMETERS</span></span>

### <span data-ttu-id="ecc5a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecc5a-113">-AsJob</span></span>
<span data-ttu-id="ecc5a-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ecc5a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecc5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc5a-115">-DefaultProfile</span></span>
<span data-ttu-id="ecc5a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc5a-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-117">-VirtualNetwork</span></span>
<span data-ttu-id="ecc5a-118">Egy **VirtualNetwork** objektumot ad meg, amely a cél állapotát jelöli.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="ecc5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc5a-119">CommonParameters</span></span>
<span data-ttu-id="ecc5a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ecc5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc5a-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecc5a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc5a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecc5a-122">INPUTS</span></span>

### <span data-ttu-id="ecc5a-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-123">PSVirtualNetwork</span></span>
<span data-ttu-id="ecc5a-124">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ecc5a-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="ecc5a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecc5a-125">OUTPUTS</span></span>

### <span data-ttu-id="ecc5a-126">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ecc5a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ecc5a-127">NOTES</span></span>

## <span data-ttu-id="ecc5a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecc5a-128">RELATED LINKS</span></span>

[<span data-ttu-id="ecc5a-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ecc5a-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ecc5a-131">Új – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="ecc5a-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecc5a-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


