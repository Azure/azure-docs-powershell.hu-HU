---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 60331e70ac29d81cc8ba2ea6cd1e8688a5484349
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680058"
---
# <span data-ttu-id="114ae-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="114ae-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="114ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="114ae-102">SYNOPSIS</span></span>
<span data-ttu-id="114ae-103">Két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="114ae-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="114ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="114ae-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="114ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="114ae-105">DESCRIPTION</span></span>
<span data-ttu-id="114ae-106">Az **Add-AzureRmVirtualNetworkPeering** parancsmag két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="114ae-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="114ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="114ae-107">EXAMPLES</span></span>

### <span data-ttu-id="114ae-108">Példa 1: két virtuális hálózat közötti kapcsolat létrehozása ugyanazon a területen</span><span class="sxs-lookup"><span data-stu-id="114ae-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="114ae-109">Felhívjuk a figyelmét arra, hogy a vnet1-ről a vnet2-ra kell létrehozni a kapcsolatot, és fordítva kell ahhoz, hogy a felhasználók dolgozhassanak.</span><span class="sxs-lookup"><span data-stu-id="114ae-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="114ae-110">2. példa: kapcsolatok létrehozása két virtuális hálózat között különböző régiókban</span><span class="sxs-lookup"><span data-stu-id="114ae-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="114ae-111">Itt "myVnet1" in US West Central "myVnet2" a kanadai középen.</span><span class="sxs-lookup"><span data-stu-id="114ae-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="114ae-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="114ae-112">PARAMETERS</span></span>

### <span data-ttu-id="114ae-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="114ae-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="114ae-114">Jelzi, hogy ez a parancsmag lehetővé teszi a virtuális gépektől érkező forgalom továbbítását a távoli virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="114ae-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="114ae-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="114ae-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="114ae-116">Jelző, amely lehetővé teszi a gatewayLinks használatát a távoli virtuális hálózat hivatkozása erre a virtuális hálózatra</span><span class="sxs-lookup"><span data-stu-id="114ae-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="114ae-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="114ae-117">-AsJob</span></span>
<span data-ttu-id="114ae-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="114ae-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="114ae-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="114ae-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="114ae-120">Jelzi, hogy ez a parancsmag blokkolja a virtuális gépeket a kapcsolódó virtuális hálózatban, hogy a helyi virtuális hálózat minden virtuális számítógépéhez hozzáférhessen.</span><span class="sxs-lookup"><span data-stu-id="114ae-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="114ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114ae-121">-DefaultProfile</span></span>
<span data-ttu-id="114ae-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="114ae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="114ae-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="114ae-123">-Name</span></span>
<span data-ttu-id="114ae-124">A virtuális hálózat társközi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="114ae-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="114ae-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="114ae-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="114ae-126">A távoli virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="114ae-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="114ae-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="114ae-127">-UseRemoteGateways</span></span>
<span data-ttu-id="114ae-128">Azt jelzi, hogy ez a parancsmag lehetővé teszi a virtuális hálózat távoli átjáróinak használatát.</span><span class="sxs-lookup"><span data-stu-id="114ae-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="114ae-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="114ae-129">-VirtualNetwork</span></span>
<span data-ttu-id="114ae-130">A fölérendelt virtuális hálózat meghatározása.</span><span class="sxs-lookup"><span data-stu-id="114ae-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="114ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114ae-131">CommonParameters</span></span>
<span data-ttu-id="114ae-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="114ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114ae-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114ae-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114ae-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="114ae-134">INPUTS</span></span>

### <span data-ttu-id="114ae-135">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="114ae-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="114ae-136">Paraméterek: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="114ae-136">Parameters: VirtualNetwork (ByValue)</span></span>

### <span data-ttu-id="114ae-137">System. String</span><span class="sxs-lookup"><span data-stu-id="114ae-137">System.String</span></span>
<span data-ttu-id="114ae-138">Paraméterek: RemoteVirtualNetworkId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="114ae-138">Parameters: RemoteVirtualNetworkId (ByValue)</span></span>

## <span data-ttu-id="114ae-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="114ae-139">OUTPUTS</span></span>

### <span data-ttu-id="114ae-140">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="114ae-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="114ae-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="114ae-141">NOTES</span></span>

## <span data-ttu-id="114ae-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="114ae-142">RELATED LINKS</span></span>

[<span data-ttu-id="114ae-143">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="114ae-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="114ae-144">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="114ae-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="114ae-145">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="114ae-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="114ae-146">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="114ae-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


