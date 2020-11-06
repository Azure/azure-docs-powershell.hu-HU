---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 742f1341401a5dab75f9cbf2f15f3698009589a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494987"
---
# <span data-ttu-id="6e1d9-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e1d9-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="6e1d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1d9-103">Virtuális hálózat egyszemélyes nézetének beállítása.</span><span class="sxs-lookup"><span data-stu-id="6e1d9-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e1d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e1d9-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e1d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e1d9-105">DESCRIPTION</span></span>
<span data-ttu-id="6e1d9-106">A **set-AzureRmVirtualNetworkPeering** parancsmag virtuális hálózat-összehívást konfigurál.</span><span class="sxs-lookup"><span data-stu-id="6e1d9-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="6e1d9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e1d9-107">EXAMPLES</span></span>

### <span data-ttu-id="6e1d9-108">1. példa: a virtuális hálózati kapcsolat továbbított forgalmi konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="6e1d9-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="6e1d9-109">2. példa: virtuális hálózati kapcsolat virtuális hálózati hozzáférésének módosítása</span><span class="sxs-lookup"><span data-stu-id="6e1d9-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="6e1d9-110">3. példa: a virtuális hálózat társközi átviteli tulajdonságának módosítása</span><span class="sxs-lookup"><span data-stu-id="6e1d9-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="6e1d9-111">Példa 4: távoli átjárók használata a virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="6e1d9-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="6e1d9-112">Ha ezt a tulajdonságot $Truere módosítja, akkor a VNet átjárója használható.</span><span class="sxs-lookup"><span data-stu-id="6e1d9-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="6e1d9-113">A társközi VNet azonban konfigurálnia kell az átjárót, és a **AllowGatewayTransit** értéke $true kell, hogy legyen.</span><span class="sxs-lookup"><span data-stu-id="6e1d9-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="6e1d9-114">Ez a tulajdonság nem használható, ha egy átjáró már konfigurálva van.</span><span class="sxs-lookup"><span data-stu-id="6e1d9-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="6e1d9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e1d9-115">PARAMETERS</span></span>

### <span data-ttu-id="6e1d9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e1d9-116">-AsJob</span></span>
<span data-ttu-id="6e1d9-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6e1d9-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1d9-118">-DefaultProfile</span></span>
<span data-ttu-id="6e1d9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e1d9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e1d9-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e1d9-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="6e1d9-121">A virtuális hálózat társközi beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e1d9-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="6e1d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1d9-122">CommonParameters</span></span>
<span data-ttu-id="6e1d9-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e1d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1d9-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e1d9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1d9-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e1d9-125">INPUTS</span></span>

### <span data-ttu-id="6e1d9-126">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e1d9-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>
<span data-ttu-id="6e1d9-127">Paraméterek: VirtualNetworkPeering (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e1d9-127">Parameters: VirtualNetworkPeering (ByValue)</span></span>

## <span data-ttu-id="6e1d9-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e1d9-128">OUTPUTS</span></span>

### <span data-ttu-id="6e1d9-129">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e1d9-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="6e1d9-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e1d9-130">NOTES</span></span>

## <span data-ttu-id="6e1d9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e1d9-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e1d9-132">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e1d9-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="6e1d9-133">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e1d9-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="6e1d9-134">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e1d9-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


