---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 440c1395c30f396ff1ae2430828cac7aae675734
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841798"
---
# <span data-ttu-id="ebc52-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ebc52-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="ebc52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebc52-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc52-103">Két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ebc52-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="ebc52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebc52-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebc52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebc52-105">DESCRIPTION</span></span>
<span data-ttu-id="ebc52-106">Az **Add-AzVirtualNetworkPeering** parancsmag két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ebc52-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="ebc52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ebc52-107">EXAMPLES</span></span>

### <span data-ttu-id="ebc52-108">Példa 1: két virtuális hálózat közötti kapcsolat létrehozása ugyanazon a területen</span><span class="sxs-lookup"><span data-stu-id="ebc52-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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
Add-AzVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="ebc52-109">Felhívjuk a figyelmét arra, hogy a vnet1-ről a vnet2-ra kell létrehozni a kapcsolatot, és fordítva kell ahhoz, hogy a felhasználók dolgozhassanak.</span><span class="sxs-lookup"><span data-stu-id="ebc52-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="ebc52-110">2. példa: kapcsolatok létrehozása két virtuális hálózat között különböző régiókban</span><span class="sxs-lookup"><span data-stu-id="ebc52-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="ebc52-111">Itt "myVnet1" in US West Central "myVnet2" a kanadai középen.</span><span class="sxs-lookup"><span data-stu-id="ebc52-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="ebc52-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebc52-112">PARAMETERS</span></span>

### <span data-ttu-id="ebc52-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="ebc52-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="ebc52-114">Jelzi, hogy ez a parancsmag lehetővé teszi a virtuális gépektől érkező forgalom továbbítását a távoli virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="ebc52-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="ebc52-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="ebc52-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="ebc52-116">Jelző, amely lehetővé teszi a gatewayLinks használatát a távoli virtuális hálózat hivatkozása erre a virtuális hálózatra</span><span class="sxs-lookup"><span data-stu-id="ebc52-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc52-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebc52-117">-AsJob</span></span>
<span data-ttu-id="ebc52-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ebc52-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebc52-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ebc52-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="ebc52-120">Jelzi, hogy ez a parancsmag blokkolja a virtuális gépeket a kapcsolódó virtuális hálózatban, hogy a helyi virtuális hálózat minden virtuális számítógépéhez hozzáférhessen.</span><span class="sxs-lookup"><span data-stu-id="ebc52-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="ebc52-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc52-121">-DefaultProfile</span></span>
<span data-ttu-id="ebc52-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebc52-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebc52-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ebc52-123">-Name</span></span>
<span data-ttu-id="ebc52-124">A virtuális hálózat társközi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebc52-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc52-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ebc52-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="ebc52-126">A távoli virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebc52-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc52-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="ebc52-127">-UseRemoteGateways</span></span>
<span data-ttu-id="ebc52-128">Azt jelzi, hogy ez a parancsmag lehetővé teszi a virtuális hálózat távoli átjáróinak használatát.</span><span class="sxs-lookup"><span data-stu-id="ebc52-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="ebc52-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ebc52-129">-VirtualNetwork</span></span>
<span data-ttu-id="ebc52-130">A fölérendelt virtuális hálózat meghatározása.</span><span class="sxs-lookup"><span data-stu-id="ebc52-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="ebc52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc52-131">CommonParameters</span></span>
<span data-ttu-id="ebc52-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebc52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc52-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebc52-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc52-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc52-134">INPUTS</span></span>

### <span data-ttu-id="ebc52-135">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="ebc52-135">String</span></span>
<span data-ttu-id="ebc52-136">A ' RemoteVirtualNetworkId ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ebc52-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ebc52-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ebc52-137">PSVirtualNetwork</span></span>
<span data-ttu-id="ebc52-138">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ebc52-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="ebc52-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc52-139">OUTPUTS</span></span>

### <span data-ttu-id="ebc52-140">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ebc52-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="ebc52-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebc52-141">NOTES</span></span>

## <span data-ttu-id="ebc52-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebc52-142">RELATED LINKS</span></span>

[<span data-ttu-id="ebc52-143">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ebc52-143">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ebc52-144">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ebc52-144">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ebc52-145">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ebc52-145">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ebc52-146">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ebc52-146">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


