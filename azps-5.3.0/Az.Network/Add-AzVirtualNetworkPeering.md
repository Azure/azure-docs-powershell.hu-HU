---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467417"
---
# <span data-ttu-id="20870-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20870-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="20870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20870-102">SYNOPSIS</span></span>
<span data-ttu-id="20870-103">Társviszonyt hoz létre két virtuális hálózat között.</span><span class="sxs-lookup"><span data-stu-id="20870-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="20870-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20870-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20870-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20870-105">DESCRIPTION</span></span>
<span data-ttu-id="20870-106">Az **Add-AzVirtualNetworkPeering** parancsmag két virtuális hálózat közötti társviszonyt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="20870-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="20870-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20870-107">EXAMPLES</span></span>

### <span data-ttu-id="20870-108">1. példa: Társviszony létrehozása két virtuális hálózat között ugyanabban a régióban</span><span class="sxs-lookup"><span data-stu-id="20870-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="20870-109">Ne feledje, hogy a társviszony-létesítés munkához vnet1-ről vnet2-re kell hivatkozni, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="20870-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="20870-110">2. példa: Társviszony létrehozása két virtuális hálózat között különböző régiókban</span><span class="sxs-lookup"><span data-stu-id="20870-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="20870-111">A "myVnet1" az Amerikai Egyesült Államok Nyugati részén a Canada Central "myVnet2" (sajátVnet2) társviszonyban van.</span><span class="sxs-lookup"><span data-stu-id="20870-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="20870-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20870-112">PARAMETERS</span></span>

### <span data-ttu-id="20870-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="20870-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="20870-114">Azt jelzi, hogy ez a parancsmag lehetővé teszi a távoli virtuális hálózat virtuális gépei által továbbított forgalmat.</span><span class="sxs-lookup"><span data-stu-id="20870-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="20870-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="20870-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="20870-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span><span class="sxs-lookup"><span data-stu-id="20870-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="20870-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20870-117">-AsJob</span></span>
<span data-ttu-id="20870-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="20870-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20870-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="20870-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="20870-120">Azt jelzi, hogy ez a parancsmag blokkolja a virtuális gépeket a hivatkozott virtuális hálózati térben, hogy a helyi virtuális hálózati térben lévő összes virtuális géphez hozzáférjen.</span><span class="sxs-lookup"><span data-stu-id="20870-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="20870-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20870-121">-DefaultProfile</span></span>
<span data-ttu-id="20870-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20870-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20870-123">-Name</span><span class="sxs-lookup"><span data-stu-id="20870-123">-Name</span></span>
<span data-ttu-id="20870-124">A virtuális hálózat társviszony-létesítésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20870-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20870-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="20870-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="20870-126">A távoli virtuális hálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="20870-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20870-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="20870-127">-UseRemoteGateways</span></span>
<span data-ttu-id="20870-128">Azt jelzi, hogy ez a parancsmag távoli átjárókat tesz lehetővé ezen a virtuális hálózaton.</span><span class="sxs-lookup"><span data-stu-id="20870-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="20870-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20870-129">-VirtualNetwork</span></span>
<span data-ttu-id="20870-130">A szülő virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="20870-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="20870-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20870-131">CommonParameters</span></span>
<span data-ttu-id="20870-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20870-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20870-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20870-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20870-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20870-134">INPUTS</span></span>

### <span data-ttu-id="20870-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20870-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="20870-136">System.String</span><span class="sxs-lookup"><span data-stu-id="20870-136">System.String</span></span>

## <span data-ttu-id="20870-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20870-137">OUTPUTS</span></span>

### <span data-ttu-id="20870-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20870-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="20870-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20870-139">NOTES</span></span>

## <span data-ttu-id="20870-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20870-140">RELATED LINKS</span></span>

[<span data-ttu-id="20870-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20870-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="20870-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20870-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="20870-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20870-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="20870-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20870-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
