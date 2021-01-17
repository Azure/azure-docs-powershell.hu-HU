---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 421358a9241fe41549898547c62404f6ba1162e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331734"
---
# <span data-ttu-id="f7018-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7018-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="f7018-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7018-102">SYNOPSIS</span></span>
<span data-ttu-id="f7018-103">Virtuális hálózat társviszonyt konfigurál.</span><span class="sxs-lookup"><span data-stu-id="f7018-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="f7018-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7018-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7018-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7018-105">DESCRIPTION</span></span>
<span data-ttu-id="f7018-106">A **Set-AzVirtualNetworkPeering** parancsmag konfigurálja a virtuális hálózat társviszonyát.</span><span class="sxs-lookup"><span data-stu-id="f7018-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="f7018-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7018-107">EXAMPLES</span></span>

### <span data-ttu-id="f7018-108">1. példa: Virtuális hálózat társviszony-létesítésének továbbított forgalom konfigurációjának módosítása</span><span class="sxs-lookup"><span data-stu-id="f7018-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="f7018-109">2. példa: Virtuális hálózat társviszony-létesítés virtuális hálózati hozzáférésének módosítása</span><span class="sxs-lookup"><span data-stu-id="f7018-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="f7018-110">3. példa: Virtuális hálózat társviszony átjárótovábbítási tulajdonságának módosítása</span><span class="sxs-lookup"><span data-stu-id="f7018-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="f7018-111">4. példa: Távoli átjárók használata virtuális hálózati társviszonyban</span><span class="sxs-lookup"><span data-stu-id="f7018-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="f7018-112">Ha ezt a tulajdonságot $True, a társ VNet-átjáróját használhatja.</span><span class="sxs-lookup"><span data-stu-id="f7018-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="f7018-113">A társ virtuális hálózatnak azonban konfigurálva kell lennie egy átjárónak, és az **AllowGatewayTransit-nek** $True.</span><span class="sxs-lookup"><span data-stu-id="f7018-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="f7018-114">Ez a tulajdonság nem használható, ha egy átjáró már be van állítva.</span><span class="sxs-lookup"><span data-stu-id="f7018-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="f7018-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7018-115">PARAMETERS</span></span>

### <span data-ttu-id="f7018-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7018-116">-AsJob</span></span>
<span data-ttu-id="f7018-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f7018-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7018-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7018-118">-DefaultProfile</span></span>
<span data-ttu-id="f7018-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7018-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7018-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7018-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="f7018-121">A virtuális hálózat társviszonyát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f7018-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="f7018-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7018-122">CommonParameters</span></span>
<span data-ttu-id="f7018-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7018-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7018-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7018-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7018-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7018-125">INPUTS</span></span>

### <span data-ttu-id="f7018-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7018-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="f7018-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7018-127">OUTPUTS</span></span>

### <span data-ttu-id="f7018-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7018-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="f7018-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7018-129">NOTES</span></span>

## <span data-ttu-id="f7018-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7018-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7018-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7018-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f7018-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7018-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f7018-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f7018-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
