---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 421358a9241fe41549898547c62404f6ba1162e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300347"
---
# <span data-ttu-id="f30de-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f30de-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="f30de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f30de-102">SYNOPSIS</span></span>
<span data-ttu-id="f30de-103">Virtuális hálózat egyszemélyes nézetének beállítása.</span><span class="sxs-lookup"><span data-stu-id="f30de-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="f30de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f30de-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f30de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f30de-105">DESCRIPTION</span></span>
<span data-ttu-id="f30de-106">A **set-AzVirtualNetworkPeering** parancsmag virtuális hálózat-összehívást konfigurál.</span><span class="sxs-lookup"><span data-stu-id="f30de-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="f30de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f30de-107">EXAMPLES</span></span>

### <span data-ttu-id="f30de-108">1. példa: a virtuális hálózati kapcsolat továbbított forgalmi konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="f30de-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="f30de-109">2. példa: virtuális hálózati kapcsolat virtuális hálózati hozzáférésének módosítása</span><span class="sxs-lookup"><span data-stu-id="f30de-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="f30de-110">3. példa: a virtuális hálózat társközi átviteli tulajdonságának módosítása</span><span class="sxs-lookup"><span data-stu-id="f30de-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="f30de-111">Példa 4: távoli átjárók használata a virtuális hálózatban</span><span class="sxs-lookup"><span data-stu-id="f30de-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="f30de-112">Ha ezt a tulajdonságot $Truere módosítja, akkor a VNet átjárója használható.</span><span class="sxs-lookup"><span data-stu-id="f30de-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="f30de-113">A társközi VNet azonban konfigurálnia kell az átjárót, és a **AllowGatewayTransit** értéke $true kell, hogy legyen.</span><span class="sxs-lookup"><span data-stu-id="f30de-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="f30de-114">Ez a tulajdonság nem használható, ha egy átjáró már konfigurálva van.</span><span class="sxs-lookup"><span data-stu-id="f30de-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="f30de-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f30de-115">PARAMETERS</span></span>

### <span data-ttu-id="f30de-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f30de-116">-AsJob</span></span>
<span data-ttu-id="f30de-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f30de-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f30de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30de-118">-DefaultProfile</span></span>
<span data-ttu-id="f30de-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f30de-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30de-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f30de-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="f30de-121">A virtuális hálózat társközi beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f30de-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="f30de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30de-122">CommonParameters</span></span>
<span data-ttu-id="f30de-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f30de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30de-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30de-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30de-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30de-125">INPUTS</span></span>

### <span data-ttu-id="f30de-126">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f30de-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="f30de-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30de-127">OUTPUTS</span></span>

### <span data-ttu-id="f30de-128">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f30de-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="f30de-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f30de-129">NOTES</span></span>

## <span data-ttu-id="f30de-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f30de-130">RELATED LINKS</span></span>

[<span data-ttu-id="f30de-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f30de-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f30de-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f30de-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f30de-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f30de-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
