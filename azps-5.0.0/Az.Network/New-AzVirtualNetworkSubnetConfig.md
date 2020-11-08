---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186401"
---
# <span data-ttu-id="750f1-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="750f1-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="750f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="750f1-102">SYNOPSIS</span></span>
<span data-ttu-id="750f1-103">Virtuális hálózati alhálózat-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="750f1-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="750f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="750f1-104">SYNTAX</span></span>

### <span data-ttu-id="750f1-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="750f1-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="750f1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="750f1-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="750f1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="750f1-107">DESCRIPTION</span></span>
<span data-ttu-id="750f1-108">**A New-AzVirtualNetworkSubnetConfig** parancsmag virtuális hálózati alhálózat-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="750f1-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="750f1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="750f1-109">EXAMPLES</span></span>

### <span data-ttu-id="750f1-110">Példa 1: virtuális hálózat létrehozása két alhálózattal és egy hálózati biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="750f1-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
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

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="750f1-111">Ez a példa két új alhálózat-konfigurációt hoz létre az New-AzVirtualSubnetConfig parancsmag segítségével, majd virtuális hálózat létrehozására használja őket.</span><span class="sxs-lookup"><span data-stu-id="750f1-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="750f1-112">A New-AzVirtualSubnetConfig sablon csak az alhálózat memória szerinti ábrázolását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="750f1-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="750f1-113">Ebben a példában a frontendSubnet CIDR 10.0.1.0/24 verzióval rendelkezik, és egy hálózati biztonsági csoportra hivatkozik, amely lehetővé teszi az RDP-hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="750f1-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="750f1-114">A backendSubnet CIDR 10.0.2.0/24 verzióval rendelkezik, és ugyanarra a hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="750f1-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="750f1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="750f1-115">PARAMETERS</span></span>

### <span data-ttu-id="750f1-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="750f1-116">-AddressPrefix</span></span>
<span data-ttu-id="750f1-117">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="750f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750f1-118">-DefaultProfile</span></span>
<span data-ttu-id="750f1-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="750f1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="750f1-120">– Meghatalmazás</span><span class="sxs-lookup"><span data-stu-id="750f1-120">-Delegation</span></span>
<span data-ttu-id="750f1-121">Azon szolgáltatások listája, amelyeken műveleteket végezhet el az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="750f1-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="750f1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="750f1-122">-InputObject</span></span>
<span data-ttu-id="750f1-123">Az alhálózati konfigurációhoz társított NAT-átjárót adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-123">Specifies the nat gateway associated with the subnet configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750f1-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="750f1-124">-IpAllocation</span></span>
<span data-ttu-id="750f1-125">Az alhálózat IpAllocations adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-125">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750f1-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="750f1-126">-Name</span></span>
<span data-ttu-id="750f1-127">A létrehozandó alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="750f1-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="750f1-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="750f1-129">Egy NetworkSecurityGroup-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="750f1-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="750f1-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="750f1-131">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="750f1-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="750f1-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="750f1-133">Configure: a hálózati házirendek alkalmazása a privát végpontra az alhálózatban be-és kikapcsolható.</span><span class="sxs-lookup"><span data-stu-id="750f1-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750f1-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="750f1-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="750f1-135">Configure: a hálózati házirendek alkalmazása a privát hivatkozás szolgáltatásra az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="750f1-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750f1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="750f1-136">-ResourceId</span></span>
<span data-ttu-id="750f1-137">Az alhálózati konfigurációhoz társított NAT-átjáró erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="750f1-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="750f1-138">-RouteTable</span></span>
<span data-ttu-id="750f1-139">Az alhálózati konfigurációhoz társított útvonal táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="750f1-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="750f1-140">-RouteTableId</span></span>
<span data-ttu-id="750f1-141">Az alhálózati konfigurációhoz társított útvonali táblázat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="750f1-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="750f1-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="750f1-142">-ServiceEndpoint</span></span>
<span data-ttu-id="750f1-143">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="750f1-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="750f1-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="750f1-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="750f1-145">Szolgáltatási végpontokra vonatkozó házirendek</span><span class="sxs-lookup"><span data-stu-id="750f1-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="750f1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750f1-146">CommonParameters</span></span>
<span data-ttu-id="750f1-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="750f1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750f1-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="750f1-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750f1-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="750f1-149">INPUTS</span></span>

### <span data-ttu-id="750f1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="750f1-150">System.String</span></span>

### <span data-ttu-id="750f1-151">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="750f1-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="750f1-152">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="750f1-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="750f1-153">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="750f1-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="750f1-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="750f1-154">System.String[]</span></span>

### <span data-ttu-id="750f1-155">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="750f1-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="750f1-156">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="750f1-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="750f1-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="750f1-157">OUTPUTS</span></span>

### <span data-ttu-id="750f1-158">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="750f1-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="750f1-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="750f1-159">NOTES</span></span>

## <span data-ttu-id="750f1-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="750f1-160">RELATED LINKS</span></span>

[<span data-ttu-id="750f1-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="750f1-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="750f1-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="750f1-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="750f1-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="750f1-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="750f1-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="750f1-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
