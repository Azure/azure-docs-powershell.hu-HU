---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467414"
---
# <span data-ttu-id="7f41a-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7f41a-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="7f41a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f41a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f41a-103">Alhálózati konfigurációt ad hozzá egy virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="7f41a-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="7f41a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f41a-104">SYNTAX</span></span>

### <span data-ttu-id="7f41a-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f41a-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f41a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f41a-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f41a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f41a-107">DESCRIPTION</span></span>
<span data-ttu-id="7f41a-108">Az **Add-AzVirtualNetworkSubnetConfig** parancsmag hozzáad egy alhálózati konfigurációt egy meglévő Azure virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="7f41a-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="7f41a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f41a-109">EXAMPLES</span></span>

### <span data-ttu-id="7f41a-110">1. példa: Alhálózat hozzáadása meglévő virtuális hálózathoz</span><span class="sxs-lookup"><span data-stu-id="7f41a-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="7f41a-111">Ez a példa először létrehoz egy erőforráscsoportot a létrehozni szükséges erőforrások tárolójaként.</span><span class="sxs-lookup"><span data-stu-id="7f41a-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="7f41a-112">Ezután létrehoz egy alhálózati konfigurációt, és virtuális hálózatot hoz létre vele.</span><span class="sxs-lookup"><span data-stu-id="7f41a-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="7f41a-113">A Add-AzVirtualNetworkSubnetConfig a virtuális hálózat memóriában való megjelenítéséhez egy alhálózatot ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="7f41a-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="7f41a-114">A Set-AzVirtualNetwork parancs frissíti a meglévő virtuális hálózatot az új alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="7f41a-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="7f41a-115">2. példa: Delegálás hozzáadása meglévő virtuális hálózathoz hozzáadott alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="7f41a-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="7f41a-116">Ez a példa először egy meglévő vnetet kap.</span><span class="sxs-lookup"><span data-stu-id="7f41a-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="7f41a-117">Ezután delegálás objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="7f41a-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="7f41a-118">Végül létrehoz egy új alhálózatot a delegálással, amely hozzá van adva a vnethez.</span><span class="sxs-lookup"><span data-stu-id="7f41a-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="7f41a-119">A rendszer ekkor elküldi a módosított konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="7f41a-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="7f41a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f41a-120">PARAMETERS</span></span>

### <span data-ttu-id="7f41a-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7f41a-121">-AddressPrefix</span></span>
<span data-ttu-id="7f41a-122">Ip-címek tartományát adja meg az alhálózati konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="7f41a-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="7f41a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f41a-123">-DefaultProfile</span></span>
<span data-ttu-id="7f41a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f41a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f41a-125">-Delegálás</span><span class="sxs-lookup"><span data-stu-id="7f41a-125">-Delegation</span></span>
<span data-ttu-id="7f41a-126">Az alhálózaton műveletek elvégzésére engedéllyel rendelkező szolgáltatások listája.</span><span class="sxs-lookup"><span data-stu-id="7f41a-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="7f41a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f41a-127">-InputObject</span></span>
<span data-ttu-id="7f41a-128">Az alhálózati konfigurációhoz társított nat-átjáró.</span><span class="sxs-lookup"><span data-stu-id="7f41a-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="7f41a-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="7f41a-129">-IpAllocation</span></span>
<span data-ttu-id="7f41a-130">IpAllocations megadása alhálózathoz.</span><span class="sxs-lookup"><span data-stu-id="7f41a-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="7f41a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7f41a-131">-Name</span></span>
<span data-ttu-id="7f41a-132">A hozzáadni szükséges alhálózati konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f41a-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="7f41a-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f41a-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7f41a-134">**NetworkSecurityGroup-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="7f41a-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="7f41a-135">Ez a parancsmag hozzáad egy virtuális hálózati alhálózati konfigurációt a paraméter által megadott objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="7f41a-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f41a-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7f41a-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="7f41a-137">Egy hálózati biztonsági csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f41a-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="7f41a-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="7f41a-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="7f41a-139">Konfigurálja a hálózati házirendek alhálózati magánjellegű végponton való alkalmazásának engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="7f41a-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="7f41a-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="7f41a-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="7f41a-141">Konfigurálja, hogy engedélyezze vagy tiltsa le a hálózati házirendek alkalmazását az alhálózat privát hivatkozásszolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7f41a-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="7f41a-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f41a-142">-ResourceId</span></span>
<span data-ttu-id="7f41a-143">Az alhálózat konfigurációjával társított NAT-átjáró erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7f41a-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="7f41a-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7f41a-144">-RouteTable</span></span>
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

### <span data-ttu-id="7f41a-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="7f41a-145">-RouteTableId</span></span>
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

### <span data-ttu-id="7f41a-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f41a-146">-ServiceEndpoint</span></span>
<span data-ttu-id="7f41a-147">Szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="7f41a-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="7f41a-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7f41a-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="7f41a-149">Szolgáltatás végponti házirendek</span><span class="sxs-lookup"><span data-stu-id="7f41a-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="7f41a-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7f41a-150">-VirtualNetwork</span></span>
<span data-ttu-id="7f41a-151">Megadja azt **a VirtualNetwork** objektumot, amelyben alhálózati konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="7f41a-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="7f41a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f41a-152">CommonParameters</span></span>
<span data-ttu-id="7f41a-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f41a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f41a-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f41a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f41a-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f41a-155">INPUTS</span></span>

### <span data-ttu-id="7f41a-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7f41a-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="7f41a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7f41a-157">System.String</span></span>

### <span data-ttu-id="7f41a-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f41a-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="7f41a-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7f41a-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="7f41a-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7f41a-160">System.String[]</span></span>

### <span data-ttu-id="7f41a-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="7f41a-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="7f41a-162">Microsoft.Azure.Commands.Network.Models.PSD[]</span><span class="sxs-lookup"><span data-stu-id="7f41a-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="7f41a-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f41a-163">OUTPUTS</span></span>

### <span data-ttu-id="7f41a-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7f41a-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7f41a-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f41a-165">NOTES</span></span>

## <span data-ttu-id="7f41a-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f41a-166">RELATED LINKS</span></span>

[<span data-ttu-id="7f41a-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7f41a-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7f41a-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7f41a-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7f41a-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7f41a-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7f41a-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7f41a-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
