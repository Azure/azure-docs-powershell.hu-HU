---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 836973c4b1d95445d905bb41f489c48136e12f6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670257"
---
# <span data-ttu-id="2b7b8-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b7b8-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="2b7b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7b8-103">Virtuális hálózati alhálózat-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="2b7b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b7b8-104">SYNTAX</span></span>

### <span data-ttu-id="2b7b8-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b7b8-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b7b8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7b8-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b7b8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b7b8-107">DESCRIPTION</span></span>
<span data-ttu-id="2b7b8-108">**A New-AzVirtualNetworkSubnetConfig** parancsmag virtuális hálózati alhálózat-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="2b7b8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2b7b8-109">EXAMPLES</span></span>

### <span data-ttu-id="2b7b8-110">1: virtuális hálózat létrehozása két alhálózattal és egy hálózati biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="2b7b8-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="2b7b8-111">Ez a példa két új alhálózat-konfigurációt hoz létre az New-AzVirtualSubnetConfig parancsmag segítségével, majd virtuális hálózat létrehozására használja őket.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="2b7b8-112">A New-AzVirtualSubnetConfig sablon csak az alhálózat memória szerinti ábrázolását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="2b7b8-113">Ebben a példában a frontendSubnet CIDR 10.0.1.0/24 verzióval rendelkezik, és egy hálózati biztonsági csoportra hivatkozik, amely lehetővé teszi az RDP-hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="2b7b8-114">A backendSubnet CIDR 10.0.2.0/24 verzióval rendelkezik, és ugyanarra a hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="2b7b8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b7b8-115">PARAMETERS</span></span>

### <span data-ttu-id="2b7b8-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2b7b8-116">-AddressPrefix</span></span>
<span data-ttu-id="2b7b8-117">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7b8-118">-DefaultProfile</span></span>
<span data-ttu-id="2b7b8-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b7b8-120">– Meghatalmazás</span><span class="sxs-lookup"><span data-stu-id="2b7b8-120">-Delegation</span></span>
<span data-ttu-id="2b7b8-121">Azon szolgáltatások listája, amelyeken műveleteket végezhet el az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-121">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b7b8-122">-Name</span></span>
<span data-ttu-id="2b7b8-123">A létrehozandó alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="2b7b8-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b7b8-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2b7b8-125">Egy NetworkSecurityGroup-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-125">Specifies a NetworkSecurityGroup object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2b7b8-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2b7b8-127">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-127">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2b7b8-128">-RouteTable</span></span>
<span data-ttu-id="2b7b8-129">Az alhálózati konfigurációhoz társított útvonal táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-129">Specifies the route table associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="2b7b8-130">-RouteTableId</span></span>
<span data-ttu-id="2b7b8-131">Az alhálózati konfigurációhoz társított útvonali táblázat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b7b8-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b7b8-132">-ServiceEndpoint</span></span>
<span data-ttu-id="2b7b8-133">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="2b7b8-133">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2b7b8-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2b7b8-135">Szolgáltatási végpontokra vonatkozó házirendek</span><span class="sxs-lookup"><span data-stu-id="2b7b8-135">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7b8-136">CommonParameters</span></span>
<span data-ttu-id="2b7b8-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b7b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7b8-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7b8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7b8-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b7b8-139">INPUTS</span></span>

### <span data-ttu-id="2b7b8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2b7b8-140">System.String</span></span>

### <span data-ttu-id="2b7b8-141">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b7b8-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="2b7b8-142">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b7b8-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="2b7b8-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="2b7b8-143">System.String[]</span></span>

### <span data-ttu-id="2b7b8-144">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="2b7b8-144">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="2b7b8-145">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="2b7b8-145">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="2b7b8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b7b8-146">OUTPUTS</span></span>

### <span data-ttu-id="2b7b8-147">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="2b7b8-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="2b7b8-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b7b8-148">NOTES</span></span>

## <span data-ttu-id="2b7b8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b7b8-149">RELATED LINKS</span></span>

[<span data-ttu-id="2b7b8-150">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b7b8-150">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2b7b8-151">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b7b8-151">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2b7b8-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b7b8-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2b7b8-153">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2b7b8-153">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
