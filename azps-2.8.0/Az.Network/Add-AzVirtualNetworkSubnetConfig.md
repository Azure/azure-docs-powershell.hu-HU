---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fea7f3f3d24595cdddd9635e73e3073efe5cb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837651"
---
# <span data-ttu-id="c6e4f-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6e4f-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c6e4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e4f-103">Alhálózat-konfiguráció felvétele virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="c6e4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6e4f-104">SYNTAX</span></span>

### <span data-ttu-id="c6e4f-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6e4f-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6e4f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6e4f-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6e4f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6e4f-107">DESCRIPTION</span></span>
<span data-ttu-id="c6e4f-108">Az **Add-AzVirtualNetworkSubnetConfig** parancsmag alhálózat-konfigurációt ad egy meglévő Azure virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="c6e4f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c6e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="c6e4f-110">1: alhálózat felvétele meglévő virtuális hálózatba</span><span class="sxs-lookup"><span data-stu-id="c6e4f-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="c6e4f-111">Ez a példa először létrehoz egy erőforráscsoportot a létrehozandó erőforrások tárolójából.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="c6e4f-112">Ekkor létrehoz egy alhálózat-konfigurációt, és a virtuális hálózat létrehozásához használja azt.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="c6e4f-113">A rendszer ezután felveszi az Add-AzVirtualNetworkSubnetConfig a virtuális hálózat memóriában való megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="c6e4f-114">A Set-AzVirtualNetwork parancs frissíti a meglévő virtuális hálózatot az új alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="c6e4f-115">2: a meglévő virtuális hálózathoz hozzáadott alhálózat delegálásának felvétele</span><span class="sxs-lookup"><span data-stu-id="c6e4f-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="c6e4f-116">Ez a példa először kap egy meglévő vnet.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="c6e4f-117">Ezután létrehoz egy meghatalmazási objektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="c6e4f-118">Végül létrehoz egy új alhálózatot, amely az adott delegálással hozzáadódik a vnet.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="c6e4f-119">A rendszer ekkor elküldi a módosított konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="c6e4f-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6e4f-120">PARAMETERS</span></span>

### <span data-ttu-id="c6e4f-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c6e4f-121">-AddressPrefix</span></span>
<span data-ttu-id="c6e4f-122">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="c6e4f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e4f-123">-DefaultProfile</span></span>
<span data-ttu-id="c6e4f-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6e4f-125">– Meghatalmazás</span><span class="sxs-lookup"><span data-stu-id="c6e4f-125">-Delegation</span></span>
<span data-ttu-id="c6e4f-126">Azon szolgáltatások listája, amelyeken műveleteket végezhet el az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="c6e4f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6e4f-127">-InputObject</span></span>
<span data-ttu-id="c6e4f-128">Az alhálózati konfigurációhoz társított NAT-átjárót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="c6e4f-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6e4f-129">-Name</span></span>
<span data-ttu-id="c6e4f-130">A hozzáadni kívánt alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-130">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="c6e4f-131">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6e4f-131">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c6e4f-132">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-132">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="c6e4f-133">Ez a parancsmag a virtuális hálózati alhálózat-konfigurációt hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-133">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6e4f-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c6e4f-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="c6e4f-135">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="c6e4f-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="c6e4f-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="c6e4f-137">Configure: a hálózati házirendek alkalmazása a privát végpontra az alhálózatban be-és kikapcsolható.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="c6e4f-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="c6e4f-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="c6e4f-139">Configure: a hálózati házirendek alkalmazása a privát hivatkozás szolgáltatásra az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="c6e4f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6e4f-140">-ResourceId</span></span>
<span data-ttu-id="c6e4f-141">Az alhálózati konfigurációhoz társított NAT-átjáró erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="c6e4f-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c6e4f-142">-RouteTable</span></span>
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

### <span data-ttu-id="c6e4f-143">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="c6e4f-143">-RouteTableId</span></span>
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

### <span data-ttu-id="c6e4f-144">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c6e4f-144">-ServiceEndpoint</span></span>
<span data-ttu-id="c6e4f-145">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="c6e4f-145">Service Endpoint Value</span></span>

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

### <span data-ttu-id="c6e4f-146">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c6e4f-146">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c6e4f-147">Szolgáltatási végpontokra vonatkozó házirendek</span><span class="sxs-lookup"><span data-stu-id="c6e4f-147">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="c6e4f-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c6e4f-148">-VirtualNetwork</span></span>
<span data-ttu-id="c6e4f-149">Azt a **VirtualNetwork** -objektumot adja meg, amelybe alhálózat-konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-149">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="c6e4f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e4f-150">CommonParameters</span></span>
<span data-ttu-id="c6e4f-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6e4f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e4f-152">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6e4f-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e4f-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6e4f-153">INPUTS</span></span>

### <span data-ttu-id="c6e4f-154">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c6e4f-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="c6e4f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e4f-155">System.String</span></span>

### <span data-ttu-id="c6e4f-156">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6e4f-156">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="c6e4f-157">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c6e4f-157">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="c6e4f-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="c6e4f-158">System.String[]</span></span>

### <span data-ttu-id="c6e4f-159">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="c6e4f-159">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="c6e4f-160">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="c6e4f-160">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="c6e4f-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6e4f-161">OUTPUTS</span></span>

### <span data-ttu-id="c6e4f-162">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c6e4f-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c6e4f-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6e4f-163">NOTES</span></span>

## <span data-ttu-id="c6e4f-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6e4f-164">RELATED LINKS</span></span>

[<span data-ttu-id="c6e4f-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6e4f-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c6e4f-166">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6e4f-166">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c6e4f-167">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6e4f-167">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c6e4f-168">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6e4f-168">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
