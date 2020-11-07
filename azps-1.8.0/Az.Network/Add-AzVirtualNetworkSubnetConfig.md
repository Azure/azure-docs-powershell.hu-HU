---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670682"
---
# <span data-ttu-id="ddb6b-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddb6b-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="ddb6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb6b-103">Alhálózat-konfiguráció felvétele virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="ddb6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddb6b-104">SYNTAX</span></span>

### <span data-ttu-id="ddb6b-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ddb6b-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddb6b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddb6b-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb6b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddb6b-107">DESCRIPTION</span></span>
<span data-ttu-id="ddb6b-108">Az **Add-AzVirtualNetworkSubnetConfig** parancsmag alhálózat-konfigurációt ad egy meglévő Azure virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="ddb6b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ddb6b-109">EXAMPLES</span></span>

### <span data-ttu-id="ddb6b-110">1: alhálózat felvétele meglévő virtuális hálózatba</span><span class="sxs-lookup"><span data-stu-id="ddb6b-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="ddb6b-111">Ez a példa először létrehoz egy erőforráscsoportot a létrehozandó erőforrások tárolójából.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="ddb6b-112">Ekkor létrehoz egy alhálózat-konfigurációt, és a virtuális hálózat létrehozásához használja azt.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="ddb6b-113">A rendszer ezután felveszi az Add-AzVirtualNetworkSubnetConfig a virtuális hálózat memóriában való megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="ddb6b-114">A Set-AzVirtualNetwork parancs frissíti a meglévő virtuális hálózatot az új alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="ddb6b-115">2: a meglévő virtuális hálózathoz hozzáadott alhálózat delegálásának felvétele</span><span class="sxs-lookup"><span data-stu-id="ddb6b-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="ddb6b-116">Ez a példa először kap egy meglévő vnet.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="ddb6b-117">Ezután létrehoz egy meghatalmazási objektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="ddb6b-118">Végül létrehoz egy új alhálózatot, amely az adott delegálással hozzáadódik a vnet.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="ddb6b-119">A rendszer ekkor elküldi a módosított konfigurációt a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="ddb6b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddb6b-120">PARAMETERS</span></span>

### <span data-ttu-id="ddb6b-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ddb6b-121">-AddressPrefix</span></span>
<span data-ttu-id="ddb6b-122">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="ddb6b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb6b-123">-DefaultProfile</span></span>
<span data-ttu-id="ddb6b-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb6b-125">– Meghatalmazás</span><span class="sxs-lookup"><span data-stu-id="ddb6b-125">-Delegation</span></span>
<span data-ttu-id="ddb6b-126">Azon szolgáltatások listája, amelyeken műveleteket végezhet el az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="ddb6b-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddb6b-127">-Name</span></span>
<span data-ttu-id="ddb6b-128">A hozzáadni kívánt alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="ddb6b-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ddb6b-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ddb6b-130">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="ddb6b-131">Ez a parancsmag a virtuális hálózati alhálózat-konfigurációt hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddb6b-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ddb6b-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="ddb6b-133">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="ddb6b-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ddb6b-134">-RouteTable</span></span>
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

### <span data-ttu-id="ddb6b-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="ddb6b-135">-RouteTableId</span></span>
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

### <span data-ttu-id="ddb6b-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ddb6b-136">-ServiceEndpoint</span></span>
<span data-ttu-id="ddb6b-137">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="ddb6b-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="ddb6b-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ddb6b-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ddb6b-139">Szolgáltatási végpontokra vonatkozó házirendek</span><span class="sxs-lookup"><span data-stu-id="ddb6b-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="ddb6b-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ddb6b-140">-VirtualNetwork</span></span>
<span data-ttu-id="ddb6b-141">Azt a **VirtualNetwork** -objektumot adja meg, amelybe alhálózat-konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="ddb6b-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="ddb6b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb6b-142">CommonParameters</span></span>
<span data-ttu-id="ddb6b-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddb6b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb6b-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb6b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb6b-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddb6b-145">INPUTS</span></span>

### <span data-ttu-id="ddb6b-146">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ddb6b-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="ddb6b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb6b-147">System.String</span></span>

### <span data-ttu-id="ddb6b-148">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ddb6b-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="ddb6b-149">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ddb6b-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="ddb6b-150">System. string []</span><span class="sxs-lookup"><span data-stu-id="ddb6b-150">System.String[]</span></span>

### <span data-ttu-id="ddb6b-151">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="ddb6b-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="ddb6b-152">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="ddb6b-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="ddb6b-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddb6b-153">OUTPUTS</span></span>

### <span data-ttu-id="ddb6b-154">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ddb6b-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ddb6b-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddb6b-155">NOTES</span></span>

## <span data-ttu-id="ddb6b-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddb6b-156">RELATED LINKS</span></span>

[<span data-ttu-id="ddb6b-157">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddb6b-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ddb6b-158">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddb6b-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ddb6b-159">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddb6b-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ddb6b-160">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ddb6b-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
