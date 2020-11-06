---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 7a26e563c8416f31178855acb2d97f318001f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501747"
---
# <span data-ttu-id="aa008-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aa008-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="aa008-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa008-102">SYNOPSIS</span></span>
<span data-ttu-id="aa008-103">Két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aa008-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa008-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa008-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa008-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa008-105">DESCRIPTION</span></span>
<span data-ttu-id="aa008-106">Az **Add-AzureRmVirtualNetworkPeering** parancsmag két virtuális hálózat közötti kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aa008-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="aa008-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa008-107">EXAMPLES</span></span>

### <span data-ttu-id="aa008-108">Példa 1: két virtuális hálózat közötti kapcsolat létrehozása ugyanazon a területen</span><span class="sxs-lookup"><span data-stu-id="aa008-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="aa008-109">Felhívjuk a figyelmét arra, hogy a vnet1-ről a vnet2-ra kell létrehozni a kapcsolatot, és fordítva kell ahhoz, hogy a felhasználók dolgozhassanak.</span><span class="sxs-lookup"><span data-stu-id="aa008-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="aa008-110">2. példa: kapcsolatok létrehozása két virtuális hálózat között különböző régiókban</span><span class="sxs-lookup"><span data-stu-id="aa008-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="aa008-111">Itt "myVnet1" in US West Central "myVnet2" a kanadai középen.</span><span class="sxs-lookup"><span data-stu-id="aa008-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="aa008-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa008-112">PARAMETERS</span></span>

### <span data-ttu-id="aa008-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="aa008-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="aa008-114">Jelzi, hogy ez a parancsmag lehetővé teszi a virtuális gépektől érkező forgalom továbbítását a távoli virtuális hálózatról.</span><span class="sxs-lookup"><span data-stu-id="aa008-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="aa008-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="aa008-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="aa008-116">Jelző, amely lehetővé teszi a gatewayLinks használatát a távoli virtuális hálózat hivatkozása erre a virtuális hálózatra</span><span class="sxs-lookup"><span data-stu-id="aa008-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa008-117">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="aa008-117">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="aa008-118">Jelzi, hogy ez a parancsmag blokkolja a virtuális gépeket a kapcsolódó virtuális hálózatban, hogy a helyi virtuális hálózat minden virtuális számítógépéhez hozzáférhessen.</span><span class="sxs-lookup"><span data-stu-id="aa008-118">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="aa008-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa008-119">-Name</span></span>
<span data-ttu-id="aa008-120">A virtuális hálózat társközi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa008-120">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="aa008-121">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="aa008-121">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="aa008-122">A távoli virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa008-122">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="aa008-123">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="aa008-123">-UseRemoteGateways</span></span>
<span data-ttu-id="aa008-124">Azt jelzi, hogy ez a parancsmag lehetővé teszi a virtuális hálózat távoli átjáróinak használatát.</span><span class="sxs-lookup"><span data-stu-id="aa008-124">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="aa008-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa008-125">-VirtualNetwork</span></span>
<span data-ttu-id="aa008-126">A fölérendelt virtuális hálózat meghatározása.</span><span class="sxs-lookup"><span data-stu-id="aa008-126">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="aa008-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa008-127">-DefaultProfile</span></span>
<span data-ttu-id="aa008-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa008-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa008-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa008-129">CommonParameters</span></span>
<span data-ttu-id="aa008-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa008-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa008-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa008-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa008-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa008-132">INPUTS</span></span>

### <span data-ttu-id="aa008-133">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="aa008-133">String</span></span>
<span data-ttu-id="aa008-134">A ' RemoteVirtualNetworkId ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="aa008-134">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="aa008-135">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa008-135">PSVirtualNetwork</span></span>
<span data-ttu-id="aa008-136">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="aa008-136">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="aa008-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa008-137">OUTPUTS</span></span>

### <span data-ttu-id="aa008-138">Microsoft. Azure. commands. Network. models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aa008-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="aa008-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa008-139">NOTES</span></span>

## <span data-ttu-id="aa008-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa008-140">RELATED LINKS</span></span>

[<span data-ttu-id="aa008-141">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa008-141">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="aa008-142">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aa008-142">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="aa008-143">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aa008-143">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="aa008-144">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="aa008-144">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


