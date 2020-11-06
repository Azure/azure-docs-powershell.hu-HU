---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493408"
---
# <span data-ttu-id="081be-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="081be-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="081be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="081be-102">SYNOPSIS</span></span>
<span data-ttu-id="081be-103">Virtuális hálózat egyszemélyes nézetének beállítása.</span><span class="sxs-lookup"><span data-stu-id="081be-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="081be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="081be-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="081be-105">DESCRIPTION</span></span>
<span data-ttu-id="081be-106">A **set-AzureRmVirtualNetworkPeering** parancsmag virtuális hálózat-összehívást konfigurál.</span><span class="sxs-lookup"><span data-stu-id="081be-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="081be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="081be-107">EXAMPLES</span></span>

### <span data-ttu-id="081be-108">1. példa: a virtuális hálózati kapcsolat továbbított forgalmi konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="081be-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="081be-109">2. példa: virtuális hálózati kapcsolat virtuális hálózati hozzáférésének módosítása</span><span class="sxs-lookup"><span data-stu-id="081be-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="081be-110">3. példa: a virtuális hálózat társközi átviteli tulajdonságának módosítása</span><span class="sxs-lookup"><span data-stu-id="081be-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="081be-111">Példa 4: távoli átjárók használata a virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="081be-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="081be-112">Ha ezt a tulajdonságot $Truere módosítja, akkor a VNet átjárója használható.</span><span class="sxs-lookup"><span data-stu-id="081be-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="081be-113">A társközi VNet azonban konfigurálnia kell az átjárót, és a **AllowGatewayTransit** értéke $true kell, hogy legyen.</span><span class="sxs-lookup"><span data-stu-id="081be-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="081be-114">Ez a tulajdonság nem használható, ha egy átjáró már konfigurálva van.</span><span class="sxs-lookup"><span data-stu-id="081be-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="081be-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="081be-115">PARAMETERS</span></span>

### <span data-ttu-id="081be-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="081be-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="081be-117">A virtuális hálózat társközi beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="081be-117">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="081be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081be-118">-DefaultProfile</span></span>
<span data-ttu-id="081be-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="081be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="081be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081be-120">CommonParameters</span></span>
<span data-ttu-id="081be-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="081be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081be-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081be-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081be-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="081be-123">INPUTS</span></span>

### <span data-ttu-id="081be-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="081be-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="081be-125">A ' VirtualNetworkPeering ' paraméter az "PSVirtualNetworkPeering" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="081be-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="081be-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="081be-126">OUTPUTS</span></span>

### <span data-ttu-id="081be-127">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="081be-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="081be-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="081be-128">NOTES</span></span>

## <span data-ttu-id="081be-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="081be-129">RELATED LINKS</span></span>

[<span data-ttu-id="081be-130">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="081be-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="081be-131">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="081be-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="081be-132">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="081be-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


