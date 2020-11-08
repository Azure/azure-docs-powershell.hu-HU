---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183047"
---
# <span data-ttu-id="b449b-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b449b-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="b449b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b449b-102">SYNOPSIS</span></span>
<span data-ttu-id="b449b-103">Két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b449b-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="b449b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b449b-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b449b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b449b-105">DESCRIPTION</span></span>
<span data-ttu-id="b449b-106">Az **Add-AzVirtualNetworkPeering** parancsmag két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b449b-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="b449b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b449b-107">EXAMPLES</span></span>

### <span data-ttu-id="b449b-108">Példa 1: két virtuális hálózat közötti kapcsolat létrehozása ugyanazon a területen</span><span class="sxs-lookup"><span data-stu-id="b449b-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="b449b-109">Felhívjuk a figyelmét arra, hogy a vnet1-ről a vnet2-ra kell létrehozni a kapcsolatot, és fordítva kell ahhoz, hogy a felhasználók dolgozhassanak.</span><span class="sxs-lookup"><span data-stu-id="b449b-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="b449b-110">2. példa: kapcsolatok létrehozása két virtuális hálózat között különböző régiókban</span><span class="sxs-lookup"><span data-stu-id="b449b-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="b449b-111">Itt "myVnet1" in US West Central "myVnet2" a kanadai középen.</span><span class="sxs-lookup"><span data-stu-id="b449b-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="b449b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b449b-112">PARAMETERS</span></span>

### <span data-ttu-id="b449b-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="b449b-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="b449b-114">Jelzi, hogy ez a parancsmag lehetővé teszi a virtuális gépektől érkező forgalom továbbítását a távoli virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="b449b-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="b449b-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="b449b-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="b449b-116">Jelző, amely lehetővé teszi a gatewayLinks használatát a távoli virtuális hálózat hivatkozása erre a virtuális hálózatra</span><span class="sxs-lookup"><span data-stu-id="b449b-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="b449b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b449b-117">-AsJob</span></span>
<span data-ttu-id="b449b-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b449b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b449b-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b449b-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="b449b-120">Jelzi, hogy ez a parancsmag blokkolja a virtuális gépeket a kapcsolódó virtuális hálózatban, hogy a helyi virtuális hálózat minden virtuális számítógépéhez hozzáférhessen.</span><span class="sxs-lookup"><span data-stu-id="b449b-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="b449b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b449b-121">-DefaultProfile</span></span>
<span data-ttu-id="b449b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b449b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b449b-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b449b-123">-Name</span></span>
<span data-ttu-id="b449b-124">A virtuális hálózat társközi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b449b-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="b449b-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b449b-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="b449b-126">A távoli virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b449b-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="b449b-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="b449b-127">-UseRemoteGateways</span></span>
<span data-ttu-id="b449b-128">Azt jelzi, hogy ez a parancsmag lehetővé teszi a virtuális hálózat távoli átjáróinak használatát.</span><span class="sxs-lookup"><span data-stu-id="b449b-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="b449b-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b449b-129">-VirtualNetwork</span></span>
<span data-ttu-id="b449b-130">A fölérendelt virtuális hálózat meghatározása.</span><span class="sxs-lookup"><span data-stu-id="b449b-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="b449b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b449b-131">CommonParameters</span></span>
<span data-ttu-id="b449b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b449b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b449b-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b449b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b449b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b449b-134">INPUTS</span></span>

### <span data-ttu-id="b449b-135">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b449b-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="b449b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b449b-136">System.String</span></span>

## <span data-ttu-id="b449b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b449b-137">OUTPUTS</span></span>

### <span data-ttu-id="b449b-138">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b449b-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="b449b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b449b-139">NOTES</span></span>

## <span data-ttu-id="b449b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b449b-140">RELATED LINKS</span></span>

[<span data-ttu-id="b449b-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b449b-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b449b-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b449b-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b449b-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b449b-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="b449b-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b449b-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
