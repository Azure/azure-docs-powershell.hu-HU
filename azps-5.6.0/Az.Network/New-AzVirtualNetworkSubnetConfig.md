---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 5a874bac2a546a07b2946ec8315065035cabba72
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931746"
---
# <span data-ttu-id="4f6bc-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f6bc-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4f6bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="4f6bc-103">Virtuális hálózati alhálózati konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="4f6bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4f6bc-104">SYNTAX</span></span>

### <span data-ttu-id="4f6bc-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f6bc-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f6bc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f6bc-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f6bc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4f6bc-107">DESCRIPTION</span></span>
<span data-ttu-id="4f6bc-108">**A New-AzVirtualNetworkSubnetConfig** parancsmag létrehoz egy virtuális hálózati alhálózati konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="4f6bc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4f6bc-109">EXAMPLES</span></span>

### <span data-ttu-id="4f6bc-110">1. példa: Virtuális hálózat létrehozása két alhálózattal és egy hálózati biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="4f6bc-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="4f6bc-111">Ebben a példában két új alhálózati konfigurációt hoz létre a New-AzVirtualSubnetConfig parancsmag használatával, majd egy virtuális hálózat létrehozásához használja őket.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="4f6bc-112">A New-AzVirtualSubnetConfig sablon csak az alhálózat memóriában való megjelenítését hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="4f6bc-113">Ebben a példában a frontendSubnet CIDR 10.0.1.0/24-es, és egy RDP-hozzáférést lehetővé tő hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="4f6bc-114">A BackendSubnet CIDR 10.0.2.0/24-es, és ugyanazon hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="4f6bc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f6bc-115">PARAMETERS</span></span>

### <span data-ttu-id="4f6bc-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4f6bc-116">-AddressPrefix</span></span>
<span data-ttu-id="4f6bc-117">Ip-címek tartományát adja meg az alhálózati konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="4f6bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f6bc-118">-DefaultProfile</span></span>
<span data-ttu-id="4f6bc-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f6bc-120">-Delegálás</span><span class="sxs-lookup"><span data-stu-id="4f6bc-120">-Delegation</span></span>
<span data-ttu-id="4f6bc-121">Az alhálózaton műveletek elvégzésére engedéllyel rendelkező szolgáltatások listája.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="4f6bc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f6bc-122">-InputObject</span></span>
<span data-ttu-id="4f6bc-123">Az alhálózati konfigurációhoz társított nat-átjárót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="4f6bc-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="4f6bc-124">-IpAllocation</span></span>
<span data-ttu-id="4f6bc-125">IpAllocations megadása alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="4f6bc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4f6bc-126">-Name</span></span>
<span data-ttu-id="4f6bc-127">A létrehozni szükséges alhálózati konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="4f6bc-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4f6bc-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4f6bc-129">NetworkSecurityGroup-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="4f6bc-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4f6bc-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="4f6bc-131">Egy hálózati biztonsági csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="4f6bc-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="4f6bc-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="4f6bc-133">Konfigurálja a hálózati házirendek alhálózati magánjellegű végponton való alkalmazásának engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="4f6bc-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="4f6bc-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="4f6bc-135">Konfigurálja, hogy engedélyezze vagy tiltsa le a hálózati házirendek alkalmazását az alhálózat privát hivatkozásszolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="4f6bc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f6bc-136">-ResourceId</span></span>
<span data-ttu-id="4f6bc-137">Az alhálózat konfigurációjával társított NAT-átjáró erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="4f6bc-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4f6bc-138">-RouteTable</span></span>
<span data-ttu-id="4f6bc-139">Az alhálózati konfigurációhoz társított útvonaltábla.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="4f6bc-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="4f6bc-140">-RouteTableId</span></span>
<span data-ttu-id="4f6bc-141">Az alhálózat konfigurációjával társított útválasztási tábla azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="4f6bc-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f6bc-142">-ServiceEndpoint</span></span>
<span data-ttu-id="4f6bc-143">Szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="4f6bc-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="4f6bc-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4f6bc-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4f6bc-145">Szolgáltatás végponti házirendek</span><span class="sxs-lookup"><span data-stu-id="4f6bc-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="4f6bc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f6bc-146">CommonParameters</span></span>
<span data-ttu-id="4f6bc-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f6bc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f6bc-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f6bc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f6bc-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f6bc-149">INPUTS</span></span>

### <span data-ttu-id="4f6bc-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4f6bc-150">System.String</span></span>

### <span data-ttu-id="4f6bc-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4f6bc-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="4f6bc-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f6bc-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="4f6bc-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="4f6bc-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="4f6bc-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4f6bc-154">System.String[]</span></span>

### <span data-ttu-id="4f6bc-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="4f6bc-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="4f6bc-156">Microsoft.Azure.Commands.Network.Models.PSD[]</span><span class="sxs-lookup"><span data-stu-id="4f6bc-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="4f6bc-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f6bc-157">OUTPUTS</span></span>

### <span data-ttu-id="4f6bc-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4f6bc-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="4f6bc-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4f6bc-159">NOTES</span></span>

## <span data-ttu-id="4f6bc-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f6bc-160">RELATED LINKS</span></span>

[<span data-ttu-id="4f6bc-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f6bc-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4f6bc-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f6bc-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4f6bc-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f6bc-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4f6bc-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4f6bc-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
