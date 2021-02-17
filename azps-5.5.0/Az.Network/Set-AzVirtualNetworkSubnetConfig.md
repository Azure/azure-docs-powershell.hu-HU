---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fe6c67c39ef3d14ec1b1e4200b4fad09aa7d2a24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158818"
---
# <span data-ttu-id="c7009-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c7009-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c7009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7009-102">SYNOPSIS</span></span>
<span data-ttu-id="c7009-103">Frissíti egy virtuális hálózat alhálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c7009-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="c7009-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7009-104">SYNTAX</span></span>

### <span data-ttu-id="c7009-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7009-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7009-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7009-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7009-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7009-107">DESCRIPTION</span></span>
<span data-ttu-id="c7009-108">A **Set-AzVirtualNetworkSubnetConfig** parancsmag frissíti egy virtuális hálózat alhálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c7009-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="c7009-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7009-109">EXAMPLES</span></span>

### <span data-ttu-id="c7009-110">1: Alhálózat címelőtagának módosítása</span><span class="sxs-lookup"><span data-stu-id="c7009-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="c7009-111">Ez a példa egy virtuális hálózatot hoz létre egy alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="c7009-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="c7009-112">Ezután a hívások Set-AzVirtualNetworkSubnetConfig az alhálózat AddressPrefix-ének módosításához.</span><span class="sxs-lookup"><span data-stu-id="c7009-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="c7009-113">Ez csak a virtuális hálózat memóriában való megjelenítését befolyásolja.</span><span class="sxs-lookup"><span data-stu-id="c7009-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="c7009-114">Set-AzVirtualNetwork a virtuális hálózat módosítására az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c7009-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="c7009-115">2: Hálózati biztonsági csoport hozzáadása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="c7009-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="c7009-116">Ebben a példában egy olyan erőforráscsoportot hoz létre, amely egyetlen alhálózatot tartalmazó virtuális hálózatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c7009-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="c7009-117">Ezután létrehoz egy hálózatbiztonsági csoportot, amely engedélyezi az RDP-adatforgalmat.</span><span class="sxs-lookup"><span data-stu-id="c7009-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="c7009-118">A Set-AzVirtualNetworkSubnetConfig parancsmag az előtér-alhálózat memóriában való megjelenítésének módosítására használható, hogy az az újonnan létrehozott hálózati biztonsági csoportra mutat.</span><span class="sxs-lookup"><span data-stu-id="c7009-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="c7009-119">A Set-AzVirtualNetwork parancsmagot a rendszer a módosított állapot visszaírására hívja a szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="c7009-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="c7009-120">3: Nat átjáró csatolása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="c7009-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="c7009-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7009-121">PARAMETERS</span></span>

### <span data-ttu-id="c7009-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c7009-122">-AddressPrefix</span></span>
<span data-ttu-id="c7009-123">Ip-címek tartományát adja meg az alhálózati konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="c7009-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="c7009-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7009-124">-DefaultProfile</span></span>
<span data-ttu-id="c7009-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7009-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7009-126">-Delegálás</span><span class="sxs-lookup"><span data-stu-id="c7009-126">-Delegation</span></span>
<span data-ttu-id="c7009-127">Az alhálózaton műveletek elvégzésére engedéllyel rendelkező szolgáltatások listája.</span><span class="sxs-lookup"><span data-stu-id="c7009-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="c7009-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7009-128">-InputObject</span></span>
<span data-ttu-id="c7009-129">Az alhálózati konfigurációhoz társított nat-átjáró.</span><span class="sxs-lookup"><span data-stu-id="c7009-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="c7009-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c7009-130">-IpAllocation</span></span>
<span data-ttu-id="c7009-131">IpAllocations megadása alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="c7009-131">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="c7009-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c7009-132">-Name</span></span>
<span data-ttu-id="c7009-133">A parancsmag által konfigurált alhálózati konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7009-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="c7009-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c7009-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c7009-135">**NetworkSecurityGroup-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="c7009-135">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="c7009-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c7009-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="c7009-137">Egy hálózati biztonsági csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7009-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="c7009-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="c7009-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="c7009-139">Konfigurálás hálózati házirendek alhálózati végponton való alkalmazásának engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="c7009-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="c7009-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="c7009-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="c7009-141">Konfigurálja, hogy engedélyezze vagy tiltsa le a hálózati házirendek alkalmazását az alhálózat privát hivatkozásszolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="c7009-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="c7009-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7009-142">-ResourceId</span></span>
<span data-ttu-id="c7009-143">Az alhálózat konfigurációjával társított NAT-átjáró erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7009-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="c7009-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c7009-144">-RouteTable</span></span>
<span data-ttu-id="c7009-145">A hálózati biztonsági csoporthoz társított útvonaltábla-objektum.</span><span class="sxs-lookup"><span data-stu-id="c7009-145">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="c7009-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="c7009-146">-RouteTableId</span></span>
<span data-ttu-id="c7009-147">A hálózati biztonsági csoporthoz társított útvonaltábla-objektum azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7009-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="c7009-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7009-148">-ServiceEndpoint</span></span>
<span data-ttu-id="c7009-149">Szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="c7009-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="c7009-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c7009-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c7009-151">Szolgáltatás végponti házirendek</span><span class="sxs-lookup"><span data-stu-id="c7009-151">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="c7009-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7009-152">-VirtualNetwork</span></span>
<span data-ttu-id="c7009-153">Megadja az alhálózati konfigurációt tartalmazó **VirtualNetwork** objektumot.</span><span class="sxs-lookup"><span data-stu-id="c7009-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="c7009-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7009-154">CommonParameters</span></span>
<span data-ttu-id="c7009-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7009-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7009-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7009-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7009-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7009-157">INPUTS</span></span>

### <span data-ttu-id="c7009-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7009-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="c7009-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c7009-159">System.String</span></span>

### <span data-ttu-id="c7009-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c7009-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="c7009-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7009-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="c7009-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c7009-162">System.String[]</span></span>

### <span data-ttu-id="c7009-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="c7009-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="c7009-164">Microsoft.Azure.Commands.Network.Models.PSD[]</span><span class="sxs-lookup"><span data-stu-id="c7009-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="c7009-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7009-165">OUTPUTS</span></span>

### <span data-ttu-id="c7009-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7009-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c7009-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7009-167">NOTES</span></span>

## <span data-ttu-id="c7009-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7009-168">RELATED LINKS</span></span>

[<span data-ttu-id="c7009-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c7009-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c7009-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c7009-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c7009-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c7009-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c7009-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c7009-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
