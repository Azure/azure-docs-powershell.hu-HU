---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fe6c67c39ef3d14ec1b1e4200b4fad09aa7d2a24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024530"
---
# <span data-ttu-id="357cb-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="357cb-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="357cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="357cb-102">SYNOPSIS</span></span>
<span data-ttu-id="357cb-103">Egy virtuális hálózat alhálózat-konfigurációjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="357cb-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="357cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="357cb-104">SYNTAX</span></span>

### <span data-ttu-id="357cb-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="357cb-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="357cb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="357cb-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="357cb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="357cb-107">DESCRIPTION</span></span>
<span data-ttu-id="357cb-108">A **set-AzVirtualNetworkSubnetConfig** parancsmag frissíti a virtuális hálózat alhálózati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="357cb-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="357cb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="357cb-109">EXAMPLES</span></span>

### <span data-ttu-id="357cb-110">1: az alhálózat cím előtagjának módosítása</span><span class="sxs-lookup"><span data-stu-id="357cb-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="357cb-111">Ez a példa egy virtuális hálózatot hoz létre egy alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="357cb-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="357cb-112">Ezután a hívások Set-AzVirtualNetworkSubnetConfig az alhálózat AddressPrefix módosítására.</span><span class="sxs-lookup"><span data-stu-id="357cb-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="357cb-113">Ez a funkció csak a virtuális hálózat memóriában való megjelenítését befolyásolja.</span><span class="sxs-lookup"><span data-stu-id="357cb-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="357cb-114">Ezt követően a rendszer az Azure virtuális hálózatának módosítását kéri Set-AzVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="357cb-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="357cb-115">2: hálózati biztonsági csoport hozzáadása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="357cb-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="357cb-116">Ez a példa olyan erőforráscsoportot hoz létre, amelynek egyetlen virtuális hálózata csak egy alhálózatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="357cb-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="357cb-117">Ekkor létrehoz egy hálózati biztonsági csoportot az RDP-forgalom engedélyezési szabályával.</span><span class="sxs-lookup"><span data-stu-id="357cb-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="357cb-118">A Set-AzVirtualNetworkSubnetConfig parancsmag a felületi alhálózat memóriában való megjelenítésének módosítására szolgál, hogy az az újonnan létrehozott hálózati biztonsági csoportra mutasson.</span><span class="sxs-lookup"><span data-stu-id="357cb-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="357cb-119">Ezt követően az Set-AzVirtualNetwork parancsmag a módosított állapotnak a szolgáltatásba való visszaírását kéri.</span><span class="sxs-lookup"><span data-stu-id="357cb-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="357cb-120">3: NAT-átjáró csatolása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="357cb-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="357cb-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="357cb-121">PARAMETERS</span></span>

### <span data-ttu-id="357cb-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="357cb-122">-AddressPrefix</span></span>
<span data-ttu-id="357cb-123">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="357cb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357cb-124">-DefaultProfile</span></span>
<span data-ttu-id="357cb-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="357cb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="357cb-126">– Meghatalmazás</span><span class="sxs-lookup"><span data-stu-id="357cb-126">-Delegation</span></span>
<span data-ttu-id="357cb-127">Azon szolgáltatások listája, amelyeken műveleteket végezhet el az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="357cb-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="357cb-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="357cb-128">-InputObject</span></span>
<span data-ttu-id="357cb-129">Az alhálózati konfigurációhoz társított NAT-átjárót adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="357cb-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="357cb-130">-IpAllocation</span></span>
<span data-ttu-id="357cb-131">Az alhálózat IpAllocations adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-131">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="357cb-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="357cb-132">-Name</span></span>
<span data-ttu-id="357cb-133">A parancsmag által konfigurált alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="357cb-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="357cb-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="357cb-135">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-135">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="357cb-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="357cb-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="357cb-137">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="357cb-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="357cb-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="357cb-139">Configure: a hálózati házirendek alkalmazása a privát végpontra az alhálózatban be-és kikapcsolható.</span><span class="sxs-lookup"><span data-stu-id="357cb-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="357cb-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="357cb-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="357cb-141">Configure: a hálózati házirendek alkalmazása a privát hivatkozás szolgáltatásra az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="357cb-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="357cb-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="357cb-142">-ResourceId</span></span>
<span data-ttu-id="357cb-143">Az alhálózati konfigurációhoz társított NAT-átjáró erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="357cb-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="357cb-144">-RouteTable</span></span>
<span data-ttu-id="357cb-145">A hálózati biztonsági csoporthoz tartozó Route Table objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-145">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="357cb-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="357cb-146">-RouteTableId</span></span>
<span data-ttu-id="357cb-147">Annak az útválasztási objektumnak az AZONOSÍTÓját adja meg, amely a hálózat biztonsági csoportjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="357cb-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="357cb-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="357cb-148">-ServiceEndpoint</span></span>
<span data-ttu-id="357cb-149">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="357cb-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="357cb-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="357cb-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="357cb-151">Szolgáltatási végpontokra vonatkozó házirendek</span><span class="sxs-lookup"><span data-stu-id="357cb-151">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="357cb-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="357cb-152">-VirtualNetwork</span></span>
<span data-ttu-id="357cb-153">Az alhálózati konfigurációt tartalmazó **VirtualNetwork** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="357cb-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="357cb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357cb-154">CommonParameters</span></span>
<span data-ttu-id="357cb-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="357cb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357cb-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="357cb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357cb-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="357cb-157">INPUTS</span></span>

### <span data-ttu-id="357cb-158">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="357cb-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="357cb-159">System. String</span><span class="sxs-lookup"><span data-stu-id="357cb-159">System.String</span></span>

### <span data-ttu-id="357cb-160">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="357cb-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="357cb-161">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="357cb-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="357cb-162">System. string []</span><span class="sxs-lookup"><span data-stu-id="357cb-162">System.String[]</span></span>

### <span data-ttu-id="357cb-163">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="357cb-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="357cb-164">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="357cb-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="357cb-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="357cb-165">OUTPUTS</span></span>

### <span data-ttu-id="357cb-166">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="357cb-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="357cb-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="357cb-167">NOTES</span></span>

## <span data-ttu-id="357cb-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="357cb-168">RELATED LINKS</span></span>

[<span data-ttu-id="357cb-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="357cb-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="357cb-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="357cb-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="357cb-171">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="357cb-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="357cb-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="357cb-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
